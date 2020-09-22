---
title: Домашняя страница отчетности
description: В этом разделе представлена информация об отчетности в Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ee9bdfc6-123d-4146-8706-eab76fa37b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 42e24f42fd80b445718f81f4ff40e52c8cdaa7ba
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755008"
---
# <a name="reporting-home-page"></a><span data-ttu-id="93178-103">Домашняя страница отчетности</span><span class="sxs-lookup"><span data-stu-id="93178-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="93178-104">Microsoft Dynamics 365 Project Service Automation позволяет организациям, работающим на основе проектов, эффективно управлять операциями своего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="93178-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="93178-105">В любом проекте участники рабочей группы должны управлять возможной сделкой, составлять предложение с расценками и планировать работу, подбирать ресурсы для проектов, управлять работой в соответствии с планом, выставлять счета за работу, затем выполнять работу для завершения проекта.</span><span class="sxs-lookup"><span data-stu-id="93178-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="93178-106">Возможность сообщать об операциях является ключевой для определения состояния организации и принятия каких-либо корректирующих мер в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="93178-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="93178-107">PSA использует методы и технологии отчетности из Microsoft Dynamics 365 для всех своих отчетов.</span><span class="sxs-lookup"><span data-stu-id="93178-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="93178-108">Для получения дополнительной информации о существующих вариантах отчетности см. [Руководство по отчетам для Dynamics 365 Customer Engagement (on-premises), версия 9](../analytics/reporting-analytics-with-dynamics-365.md).</span><span class="sxs-lookup"><span data-stu-id="93178-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](../analytics/reporting-analytics-with-dynamics-365.md).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="93178-109">Мастер отчетов</span><span class="sxs-lookup"><span data-stu-id="93178-109">Report Wizard</span></span>

<span data-ttu-id="93178-110">Мастер отчетов позволяет пользователям, не являющимся разработчиками, создавать простые отчеты.</span><span class="sxs-lookup"><span data-stu-id="93178-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="93178-111">Поскольку приложение построено на существующей платформе, взаимодействие такое же, как описанное в разделе [Создание или изменение отчетов с помощью мастера отчетов](../basics/create-edit-copy-report-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="93178-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](../basics/create-edit-copy-report-wizard.md).</span></span> <span data-ttu-id="93178-112">Однако вы будете использовать сущности, специфические для Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="93178-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="93178-113">Настраиваемые отчеты службы отчетов SQL Server</span><span class="sxs-lookup"><span data-stu-id="93178-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="93178-114">Если в организации требуется специальный отчет, который не может быть создан с помощью мастера отчетов, можно создать настраиваемый отчет.</span><span class="sxs-lookup"><span data-stu-id="93178-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="93178-115">Необходимо, чтобы был установлен пакет Microsoft Visual Studio, а также соответствующие средства Microsoft SQL Server Data Tools и расширения создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="93178-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="93178-116">Для получения дополнительных сведений о средствах и версиях см. в разделе [Среда создания отчетов с помощью средств SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="93178-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span></span> <span data-ttu-id="93178-117">Дополнительные сведения о том, как создать настраиваемый отчет, см. в разделе [Создайте новый отчет, используя SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="93178-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="93178-118">Приложения аналитики Power BI</span><span class="sxs-lookup"><span data-stu-id="93178-118">Power BI insights apps</span></span>

<span data-ttu-id="93178-119">Совместно Microsoft Power BI и Dynamics 365 обеспечивают мощный способ работы с данными в виде приложений аналитики.</span><span class="sxs-lookup"><span data-stu-id="93178-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="93178-120">Дополнительные сведения о доступности приложений аналитики см. на странице [приложений аналитики Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="93178-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="93178-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93178-121">Additional resources</span></span>
<span data-ttu-id="93178-122">Дополнительные сведения об отчетности в PSA см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="93178-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="93178-123">Работа с моделью данных Project Service</span><span class="sxs-lookup"><span data-stu-id="93178-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="93178-124">Панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="93178-124">Dashboards</span></span>](reports-dashboards.md)

