---
title: Разработка шаблонов проектов с помощью копирования проектов
description: Эта тема предоставляет информацию о том, как создавать шаблоны проектов с помощью настраиваемого действия копирования проекта.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045025"
---
# <a name="develop-project-templates-with-copy-project"></a>Разработка шаблонов проектов с помощью копирования проектов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations поддерживает возможность копирования проекта и отзыва любых назначений обратно к универсальным ресурсам, представляющим роль. Клиенты могут использовать эту функцию для создания базовых шаблонов проектов.

Когда вы выбираете действие **Копировать проект**, статус целевого проекта обновляется. Используйте поле **Причина состояния**, чтобы определить, когда действие копирования завершено. Выбор действия **Копировать проект** также обновляет дату начала проекта до текущей даты начала, если в целевой сущности проекта не обнаружена целевая дата.

## <a name="copy-project-custom-action"></a>Настраиваемое действие копирования проекта 

### <a name="name"></a>Название 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Входные параметры
Имеются три входных параметра:

| Параметр          | Тип   | Значения                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** или **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Ссылка на сущность | Исходный проект |
| Целевой объект             | Ссылка на сущность | Целевой проект |


- **{"clearTeamsAndAssignments":true}**: поведение по умолчанию для Project для Интернета, и удаляет все назначения и участников рабочей группы.
- **{"removeNamedResources":true}** поведение по умолчанию для Project Operations, и возвратит назначения на универсальные ресурсы.

Дополнительные сведения о значениях по умолчанию для действий см. в разделе [Использование действий веб-API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Указание полей для копирования 
Когда действие **Копировать проект** вызывается, оно смотрит на представление проекта **Копировать столбцы проекта**, чтобы определить, какие поля копировать при копировании проекта.


### <a name="example"></a>Пример
В следующем примере показано, как вызвать настраиваемое действие **CopyProject** с помощью набора параметров **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
