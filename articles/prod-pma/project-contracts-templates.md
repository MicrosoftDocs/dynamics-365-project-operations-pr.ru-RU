---
title: Синхронизация контрактов по проекту и проектов напрямую из Project Service Automation в Finance
description: В этой теме описаны шаблон и базовые задачи, которые используются для синхронизации контрактов по проекту и проектов непосредственно из Microsoft Dynamics 365 Project Service Automation с Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 319000e6a826580049e8575def5790ab595a3165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289610"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Синхронизация контрактов по проекту и проектов напрямую из Project Service Automation в Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описаны шаблон и базовые задачи, которые используются для синхронизации контрактов по проекту и проектов непосредственно из Dynamics 365 Project Service Automation с Dynamics 365 Finance.

> [!NOTE] 
> Если вы используете выпуск Enterprise Edition 7.3.0, вам необходимо установить KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Поток данных для Project Service Automation в Finance

> [!NOTE]
> Прежде чем вы сможете использовать решение интеграции Project Service Automation с Finance, вы должны быть знакомы с функцией интеграции данных Dynamics 365.

Решение для интеграции Project Service Automation в Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance. Шаблон интеграции, доступный с функцией интеграции данных, позволяет передавать данные о контрактах, проектах, строках контрактов по проектам и вехах строк контрактов проекта из Project Service Automation в Finance.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.

[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Чтобы получить доступ к доступным шаблонам, в центре администрирования Microsoft Power Apps выберите **Проекты**, а затем в правом верхнем углу выберите **Создать проект** для выбора общедоступных шаблонов.

Следующие шаблоны и базовые задачи используются для синхронизации контрактов по проекту и проектов из Project Service Automation в Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Интеграция с Dynamics 365 Project Service Automation v2.x
- **Название шаблона в Интеграции данных:** Проекты и контракты (Project Service Automation в Finance)
- **Название задач в проекте:**

    - Контракты по проектам Project Service Automation в Finance
    - Проекты Project Service Automation в Finance
    - Строки контракта по проекту Project Service Automation в Finance
    - Вехи строки контракта по проекту Project Service Automation в Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Интеграция с Dynamics 365 Project Service Automation v3.x
В Project Service Automation произошло изменение схемы, которое влияет на шаблон вехи строк контракта по проекту, и для интеграции Project Service Automation v3.x с Dynamics 365 требуется использование версии шаблона v2.

- **Название шаблона в Интеграции данных:** Проекты и контракты (Project Service Automation 3.x в Finance) — v2
- **Название задач в проекте:**

    - Контракты по проектам Project Service Automation в Finance
    - Проекты Project Service Automation в Finance
    - Строки контракта по проекту Project Service Automation в Finance
    - Вехи строки контракта по проекту Project Service Automation в Finance

Перед синхронизацией контрактов по проектам и проектов вы должны синхронизировать организации.

## <a name="entity-set"></a>Набор сущностей

| Project Service Automation       | Финансы                                                |
|----------------------------------|--------------------------------------------------------|
| Заказы                           | Сущность интеграции для контрактов по проекту                |
| Проекты                         | Сущность интеграции для проекта                         |
| Строки заказа                      | Сущность интеграции для строки контракта по проекту           |
| Вехи строки контракта по проекту | Сущность интеграции для вехи строк контракта по проекту |

## <a name="entity-flow"></a>Поток сущностей

Контракты по проекту управляются в Project Service Automation и синхронизируются с Finance как контракты по проекту. В рамках шаблона интеграции вы можете задать источник интеграции в Finance для контракта по проекту.

Временные и материальные проекты, а также проекты с фиксированной ценой управляются в Project Service Automation и синхронизируются с Finance как проекты. В рамках шаблона интеграции вы можете установить источник интеграции для проекта в Finance. В настоящее время поддерживаются только временные и материальные проекты, а также проекты с фиксированной ценой.


Строки контрактов по проекту управляются в Project Service Automation и синхронизируются с Finance как правила выставления счетов по проекту. Если метод выставления счетов отличается от типа проекта по умолчанию, синхронизация обновляет тип проекта для проекта строки контракта и группы проектов.

Вехи строк контрактов по проекту управляются в Project Service Automation и синхронизируются с Finance как вехи правил выставления счетов по проекту.

## <a name="project-service-automation-to-finance-integration-solution"></a>Решение для интеграции Project Service Automation с Finance

Поле **Код контракта по проекту** доступно на странице **Контракты по проектам**. Это поле стало естественным и уникальным ключом для поддержки интеграции.

При создании нового контракта по проекту, если значение **Код контракта по проекту** еще не существует, оно автоматически создается с использованием числовой последовательности. Значение состоит из **ORD**, за которым следует возрастающая числовая последовательность, а затем суффикс из шести символов. Например: **ORD-01022-Z4M9Q0**.

Поле **Номер проекта** доступно на странице **Проекты**. Это поле стало естественным и уникальным ключом для поддержки интеграции.

При создании нового проекта, если значение **Номер проекта** еще не существует, оно автоматически создается с использованием числовой последовательности. Значение состоит из **PRJ**, за которым следует возрастающая числовая последовательность, а затем суффикс из шести символов. Например: **PRJ-01049-CCNID0**.

Когда применяется решение интеграции Project Service Automation с Finance, сценарий обновления задает поле **Код контракта по проекту** для существующих контрактов по проекту и поле **Номер проекта** для существующих проектов в Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

- Перед синхронизацией контрактов по проектам и проектов вы должны синхронизировать организации.
- В вашем наборе подключения добавьте сопоставление поля ключа интеграции для **msdyn\_organizationalunits** в **msdyn\_name \[Name\]**. Сначала вам может потребоваться добавить проект в набор подключений. Для получения дополнительной информации см. [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- В вашем наборе подключения добавьте сопоставление поля ключа интеграции для **msdyn\_projects** в **msdynce\_projectnumber \[Project Number\]**. Сначала вам может потребоваться добавить проект в набор подключений. Для получения дополнительной информации см. [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** для контрактов по проекту и проектов может быть обновлено на другое значение или удалено из сопоставления. Значение шаблона по умолчанию — **Project Service Automation**.
- Сопоставление **PaymentTerms** необходимо обновить, чтобы оно отражало действительные условия оплаты в Finance. Вы также можете удалить сопоставление из задачи проекта. У сопоставления значений по умолчанию — значения по умолчанию для демонстрационных данных. В следующей таблице показаны значения в Project Service Automation.

    | Value | Описание   |
    |-------|---------------|
    | 1     | Оплата через 30 дней        |
    | 2     | Оплата через 30 дней, при оплате через 10 дней скидка 2 % |
    | 3     | Оплата через 45 дней        |
    | 4     | Оплата через 60 дней        |

## <a name="power-query"></a>Power Query

Используйте Microsoft Power Query для Excel для фильтрации данных, если выполняются следующие условия:

- У вас есть заказы на продажу в Dynamics 365 Sales.
- У вас есть несколько подразделений в Project Service Automation, и эти они будут сопоставлены с несколькими юридическими лицами в Finance.

Если вам необходимо использовать Power Query, следуйте этим рекомендациям:

- В шаблоне проектов и контрактов (из PSA в Fin and Ops) есть фильтр по умолчанию, который включает только заказы на продажу типа **рабочий элемент (msdyn\_ordertype = 192350001)**. Этот фильтр помогает гарантировать, что контракты по проекту не создаются для заказов на продажу в Finance. Если вы создаете свой собственный шаблон, вы должны добавить этот фильтр.
- Создайте фильтр Power Query, который включает только контрактные организации, которые должны быть синхронизированы с юридическим лицом набора интеграционных подключений. Например, контракты по проекту, которые у вас есть с подразделением по контракту Contoso US, должны быть синхронизированы с юридическим лицом USSI, но контракты по проекту, которые у вас есть с подразделением по контракту Contoso Global, должны быть синхронизированы с юридическим лицом USMF. Если вы не добавите этот фильтр в сопоставление задач, все контракты по проекту будут синхронизированы с юридическим лицом, которое определено для набора подключений, независимо от подразделения по контракту.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблонов в интеграции данных

> [!NOTE] 
> Поля **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, и **AddressZipCode** не включены в сопоставление по умолчанию для контрактов по проекту. Вы можете добавить сопоставления, если вам нужно синхронизировать эти данные для контрактов по проекту.
>
> Поля **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** и **ProjectType** не включены в сопоставление по умолчанию для проектов. Вы можете добавить сопоставления, если вам нужно синхронизировать эти данные для проектов.

На следующих рисунках показаны примеры сопоставлений задач шаблона в интеграции данных. В сопоставлении отображается информация о полях, которые будут синхронизированы из Project Service Automation в Finance.

[![Сопоставление шаблона контракта по проекту](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Сопоставление шаблона проекта](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Сопоставление шаблона строк контракта по проекту](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Сопоставление шаблона вех строк контракта по проекту](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Сопоставление вех строк контракта по проекту в Projects and Contracts (PSA 3.x в Dynamics) — шаблон v2:

[![Сопоставление вех строк контракта по проекту с шаблоном второй версии](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]