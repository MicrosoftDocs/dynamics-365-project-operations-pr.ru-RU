---
title: Домашняя страница отчетности
description: В этом разделе представлена информация об отчетности в Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147714"
---
# <a name="reporting-home-page"></a>Домашняя страница отчетности

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation позволяет организациям, работающим на основе проектов, эффективно управлять операциями своего бизнеса. В любом проекте участники рабочей группы должны управлять возможной сделкой, составлять предложение с расценками и планировать работу, подбирать ресурсы для проектов, управлять работой в соответствии с планом, выставлять счета за работу, затем выполнять работу для завершения проекта. Возможность сообщать об операциях является ключевой для определения состояния организации и принятия каких-либо корректирующих мер в случае необходимости. PSA использует методы и технологии отчетности из Microsoft Dynamics 365 для всех своих отчетов. Для получения дополнительной информации о существующих вариантах отчетности см. [Руководство по отчетам для Dynamics 365 Customer Engagement (on-premises), версия 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Мастер отчетов

Мастер отчетов позволяет пользователям, не являющимся разработчиками, создавать простые отчеты. Поскольку приложение построено на существующей платформе, взаимодействие такое же, как описанное в разделе [Создание или изменение отчетов с помощью мастера отчетов](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Однако вы будете использовать сущности, специфические для Project Service Automation.

## <a name="custom-sql-server-reporting-services-reports"></a>Настраиваемые отчеты службы отчетов SQL Server

Если в организации требуется специальный отчет, который не может быть создан с помощью мастера отчетов, можно создать настраиваемый отчет. Необходимо, чтобы был установлен пакет Microsoft Visual Studio, а также соответствующие средства Microsoft SQL Server Data Tools и расширения создания отчетов. Для получения дополнительных сведений о средствах и версиях см. в разделе [Среда создания отчетов с помощью средств SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Дополнительные сведения о том, как создать настраиваемый отчет, см. в разделе [Создайте новый отчет, используя SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Приложения аналитики Power BI

Совместно Microsoft Power BI и Dynamics 365 обеспечивают мощный способ работы с данными в виде приложений аналитики. Дополнительные сведения о доступности приложений аналитики см. на странице [приложений аналитики Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Дополнительные ресурсы
Дополнительные сведения об отчетности в PSA см. в следующих разделах:

- [Работа с моделью данных Project Service](reports-working-project-service-data-model.md)
- [Панели мониторинга](reports-dashboards.md)

