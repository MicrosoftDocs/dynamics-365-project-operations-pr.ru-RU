---
title: Обзор развертывания Project Operations для сценариев на основе ресурсов/без запасов
description: Эта тема предоставляет информацию о типе развертывания Project Operations для сценариев на основе ресурсов/без запасов.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365594"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="69d75-103">Обзор развертывания Project Operations для сценариев на основе ресурсов/без запасов</span><span class="sxs-lookup"><span data-stu-id="69d75-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="69d75-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="69d75-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69d75-105">Тип развертывания Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов имеет следующие возможности для компаний, работающих на основе проектов:</span><span class="sxs-lookup"><span data-stu-id="69d75-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="69d75-106">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="69d75-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="69d75-107">Многомерное ценообразование и калькуляция трудовых ресурсов</span><span class="sxs-lookup"><span data-stu-id="69d75-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="69d75-108">Ценообразование на основе категорий для категорий расходов</span><span class="sxs-lookup"><span data-stu-id="69d75-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="69d75-109">Управление продажами на основе проектов с использованием возможностей Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="69d75-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="69d75-110">Universal Resource Scheduling, который интегрируется с другими приложениями, такими как Dynamics 365 Field Service и Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="69d75-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="69d75-111">Ход выполнения проекта и отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="69d75-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="69d75-112">Базовый и полный интерфейсы управления расходами для проектных и внепроектных расходов, включая фиксацию квитанций с использованием возможностей OCR</span><span class="sxs-lookup"><span data-stu-id="69d75-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="69d75-113">Выставление счетов, которое охватывает от проформы до интерфейса клиентов и поддерживается системой налога с продаж корпоративного класса и обменных курсов, действующих на требуемую дату.</span><span class="sxs-lookup"><span data-stu-id="69d75-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="69d75-114">Настраиваемая себестоимость проекта, профили доходов и правила учета и начисления незавершенного производства (НЗП)</span><span class="sxs-lookup"><span data-stu-id="69d75-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="69d75-115">Признание выручки по проекту</span><span class="sxs-lookup"><span data-stu-id="69d75-115">Project revenue recognition</span></span>
- <span data-ttu-id="69d75-116">Расширяемость через Power Platform</span><span class="sxs-lookup"><span data-stu-id="69d75-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="69d75-117">Этот тип развертывания обеспечивает расширение функциональных возможностей, предоставляемых приложениями Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="69d75-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="69d75-118">Это развертывание следует выбирать, если от Project Operations ожидается использование полного жизненного цикла проекта, который включает следующие требования:</span><span class="sxs-lookup"><span data-stu-id="69d75-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="69d75-119">Возможность управлять продажами на основе проектов с другими типами продаж, используя возможности приложения Sales.</span><span class="sxs-lookup"><span data-stu-id="69d75-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="69d75-120">Интегрированная система управления проектами, которая управляет внутренними и оплачиваемыми проектами для составления графиков и финансовых отчетов, от продаж по проектам до учета.</span><span class="sxs-lookup"><span data-stu-id="69d75-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="69d75-121">Система управления расходами, которая включает меры по обеспечению соблюдения политик и возмещения для отслеживания проектных и внепроектных расходов.</span><span class="sxs-lookup"><span data-stu-id="69d75-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="69d75-122">Требуется богатый механизм обработки налога с продаж и обменного курса корпоративного класса для создания счетов для клиентов по проектам.</span><span class="sxs-lookup"><span data-stu-id="69d75-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="69d75-123">Система бухгалтерского учета и признания выручки по проектам, соответствующая международным стандартам финансовой отчетности (МСФО).</span><span class="sxs-lookup"><span data-stu-id="69d75-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="69d75-124">Приложения Finance или Supply Chain Management и интеграция транзакций на основе проектов.</span><span class="sxs-lookup"><span data-stu-id="69d75-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
