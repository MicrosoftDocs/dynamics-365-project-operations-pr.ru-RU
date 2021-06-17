---
title: Интеграция с двойной записью Project Operations
description: В этом разделе представлен обзор интеграции с двойной записью Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998697"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="05569-103">Обзор интеграции с двойной записью Project Operations</span><span class="sxs-lookup"><span data-stu-id="05569-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="05569-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="05569-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="05569-105">Project Operations использует [возможности двойной записи](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), чтобы синхронизировать данные между Microsoft Dataverse и Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="05569-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="05569-106">На следующем рисунке показано, как данные синхронизируются в рамках этой интеграции между Dataverse и Финансы.</span><span class="sxs-lookup"><span data-stu-id="05569-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Обзор потоков данных Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="05569-108">Project Operations на Dataverse предоставляет современный пользовательский интерфейс и простую расширяемость без кода/с минимумом кода, используя возможности Power Platform.</span><span class="sxs-lookup"><span data-stu-id="05569-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="05569-109">Руководители проектов, менеджеры ресурсов, участники проектных групп и другие сотрудники, непосредственно взаимодействующие с клиентами, выполняют свои действия в Project Operations на Dataverse.</span><span class="sxs-lookup"><span data-stu-id="05569-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="05569-110">Project Operations в Финансы обеспечивает учет проектов и поддержку признания выручки.</span><span class="sxs-lookup"><span data-stu-id="05569-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="05569-111">Project Operations подключается к финансовой платформе в Финансы для расчета налога, курсов обмена валют, отчетности по финансовым аналитикам и многого другого.</span><span class="sxs-lookup"><span data-stu-id="05569-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="05569-112">Опыт бухгалтеров по проектам в основном основан на Финансах.</span><span class="sxs-lookup"><span data-stu-id="05569-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="05569-113">Интеграция Project Operations состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="05569-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="05569-114">Настройка Project Operations и интеграция данных конфигурации</span><span class="sxs-lookup"><span data-stu-id="05569-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="05569-115">Оценки проекта и фактические данные</span><span class="sxs-lookup"><span data-stu-id="05569-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="05569-116">Счета проекта</span><span class="sxs-lookup"><span data-stu-id="05569-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="05569-117">Управление расходами</span><span class="sxs-lookup"><span data-stu-id="05569-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="05569-118">Накладная поставщика</span><span class="sxs-lookup"><span data-stu-id="05569-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
