---
title: Разработка шаблонов проектов с помощью копирования проектов
description: Эта тема предоставляет информацию о том, как создавать шаблоны проектов с помощью настраиваемого действия копирования проекта.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590915"
---
# <a name="develop-project-templates-with-copy-project"></a>Разработка шаблонов проектов с помощью копирования проектов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations поддерживает возможность копирования проекта и отзыва любых назначений обратно к универсальным ресурсам, представляющим роль. Клиенты могут использовать эту функцию для создания базовых шаблонов проектов.

Когда вы выбираете действие **Копировать проект**, статус целевого проекта обновляется. Используйте поле **Причина состояния**, чтобы определить, когда действие копирования завершено. Выбор действия **Копировать проект** также обновляет дату начала проекта до текущей даты начала, если в целевой сущности проекта не обнаружена целевая дата.

## <a name="copy-project-custom-action"></a>Настраиваемое действие копирования проекта

### <a name="name"></a>Имя. 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Входные параметры

Имеются три входных параметра:

- **ReplaceNamedResources** или **ClearTeamsAndAssignments** — задайте только один из параметров. Не задавайте их оба.

    - **\{"ReplaceNamedResources":true\}** — поведение по умолчанию для Project Operations. Все именованные ресурсы заменяются универсальными ресурсами.
    - **\{"ClearTeamsAndAssignments":true\}** — поведение по умолчанию для Project for the Web. Все назначения и участники рабочей группы удаляются.

- **SourceProject** — ссылка на сущность исходного проекта, из которого производится копирование. Этот параметр не может иметь значение NULL.
- **Target** — ссылка на сущность целевого проекта, в который производится копирование. Этот параметр не может иметь значение NULL.

В следующей таблице приведено краткое описание трех параметров.

| Параметр                | Type             | Стоимость                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Логический          | **True** или **False** |
| ClearTeamsAndAssignments | Логический          | **True** или **False** |
| SourceProject            | Ссылка на сущность | Исходный проект    |
| Target                   | Ссылка на сущность | Целевой проект    |

Дополнительные сведения о значениях по умолчанию для действий см. в разделе [Использование действий веб-API](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Проверки

Выполняются следующие проверки.

1. Проверка на значения NULL,, а также извлечение исходного и целевого проектов для подтверждения существования обоих проектов в организации.
2. Система проверяет пригодность целевого проекта для копирования, проверяя следующие условия:

    - В проекте нет предыдущей деятельности (в том числе выбора значений на вкладке **Задачи**), и проект только что создан.
    - Нет ранее сделанных копий, в этом проекте не запрашивался импорт, и проект не находится в состоянии **Сбой**.

3. Операция не вызывается с использованием HTTP.

## <a name="specify-fields-to-copy"></a>Указание полей для копирования

Когда действие **Копировать проект** вызывается, оно смотрит на представление проекта **Копировать столбцы проекта**, чтобы определить, какие поля копировать при копировании проекта.

### <a name="example"></a>Пример

В следующем примере показано, как вызвать пользовательское действие **CopyProjectV3** с заданным параметром **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
