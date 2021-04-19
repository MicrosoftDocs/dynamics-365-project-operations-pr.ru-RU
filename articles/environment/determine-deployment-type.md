---
title: Определение типа развертывания
description: В этой теме дана информация, помогающая определить правильный тип развертывания Project Operations для вашей компании.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 715b117cae5418fc743ea870772278450fff5ae9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663610"
---
# <a name="determine-your-deployment-type"></a>Определение типа развертывания

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

> [!IMPORTANT]
> После покупки лицензии начните здесь, чтобы определить лучшую модель развертывания Dynamics 365 Project Operations с использованием [Управляемого процесса установки](https://aka.ms/provisionprojectoperations).
> После завершения процесса управляемой установки вы будете перенаправлены на нужный портал управления для завершения установки. См. сведения о развертывании, чтобы завершить установку.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Существующие клиенты Dynamics, использующие Dynamics 365 Project Service Automation
Project Operations включает возможности, которые поставляются с Project Service Automation. Путь обновления будет выпущен для этих клиентов в волне 1 выпуска 2021 года.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Существующие клиенты Dynamics 365 Finance, использующие управление проектами и учет 

Существующие клиенты Finance, которые используют функцию управления и учета по проектам, могут продолжать использовать ее как есть. См. [Project Operations для сценариев на основе запасов/производственных заказов](#pma).


## <a name="deployment-regions"></a>Регионы развертывания
Чтобы определить, какие регионы поддерживают развертывание Project Operations, см. [Отчет о географической доступности Dynamics 365 и Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Выберите **Посмотреть отчет** и разверните **Dynamics 365 > Приложения Operations > Dynamics 365 Project Operations** для просмотра поддерживаемых регионов.

## <a name="deployment-types"></a>Типы развертывания
Project Operations поддерживает несколько вариантов развертывания в соответствии с вашими требованиями. Независимо от того, являетесь ли вы новым или существующим клиентом Dynamics 365, Project Operations может удовлетворить ваши потребности.

Наша [анкета развертывания](https://aka.ms/provisionprojectoperations) поможет вам определить правильное развертывание. Результаты помогут вам выбрать один из следующих типов развертывания:

- [Облегченное развертывание — от сделки до счетов-проформ](#lite)
- [Project Operations для сценариев на основе ресурсов / без запасов](#integrated)
- [Project Operations для сценариев на основе запасов/производственных заказов](#pma)

Project Operations поддерживает сценарии складирования/производственного заказа и сценарии отсутствия запасов/ресурсов в одной и той же среде посредством конфигураций на уровне юридического лица. Например, Contoso может использовать возможности запасов/производственного заказа на своем производственном предприятии в США (юридическое лицо = Contoso Manufacturing United States). Contoso может использовать возможности, не связанные с запасами/ресурсами, в своем сервисном предприятии Contoso Robotics Arms в Великобритании (юридическое лицо = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Облегченное развертывание — от сделки до счетов-проформ

Облегченное развертывание включает следующие возможности:

- Процесс продаж для проектов, расширяющих возможности приложения Dynamics 365 Sales
- Планирование проекта с помощью Microsoft Project для Интернета
- Многомерное ценообразование
- Единое управление ресурсами
- Отслеживание времени
- Базовые расходы
- Выставление счета-проформы для проверки и редактирования руководителем проекта 

#### <a name="deployment-steps"></a>Шаги развертывания
Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).

Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](lite-preview-subscription-sign-up.md) и [Подготовка новой среды](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations для сценариев на основе ресурсов / без запасов
Project Operations для сценариев ресурсов/отсутствия запасов включают следующие возможности:
 
- Процесс продаж для проектов, расширяющих приложение Dynamics 365 Sales
- Планирование проекта с помощью Microsoft Project для Интернета
- Многомерное ценообразование
- Единое управление ресурсами
- Отслеживание времени
- Базовые расходы
- Полные расходы
- OCR чеков
- Проформа и выставление счетов для клиентов 
- Признание выручки для проектов

#### <a name="deployment-steps"></a>Шаги развертывания
Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).

Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](resource-sign-up-preview-subscription.md) и [Подготовка новой среды](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations для сценариев на основе запасов/производственных заказов

- Планирование проектов с использованием WBS
- Управление ресурсами
- Отслеживание времени
- Полные расходы
- OCR чеков
- Полное выставление счетов
- Признание выручки
- Производственные заказы
- Сопровождение складских материалов с инвентаризацией

#### <a name="deployment-steps"></a>Шаги развертывания
Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).

Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) и [Подготовка новой среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
