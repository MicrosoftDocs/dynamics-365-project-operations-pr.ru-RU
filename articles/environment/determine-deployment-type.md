---
title: Типы развертывания
description: В этой теме дана информация, помогающая определить правильный тип развертывания Project Operations для вашей компании.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949038"
---
# <a name="deployment-types"></a><span data-ttu-id="ef496-103">Типы развертывания</span><span class="sxs-lookup"><span data-stu-id="ef496-103">Deployment types</span></span>

<span data-ttu-id="ef496-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="ef496-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef496-105">После покупки лицензии начните здесь, чтобы определить лучшую модель развертывания Dynamics 365 Project Operations с помощью [управляемого потока установки](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ef496-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="ef496-106">После завершения процесса управляемой установки вы будете перенаправлены на нужный портал управления для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="ef496-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="ef496-107">См. сведения о развертывании ниже, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="ef496-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="ef496-108">Существующие клиенты Dynamics, использующие Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ef496-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="ef496-109">Project Operations включает возможности, которые поставляются с Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ef496-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="ef496-110">В будущем для этих клиентов будет выпущен путь обновления.</span><span class="sxs-lookup"><span data-stu-id="ef496-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="ef496-111">Существующие клиенты Dynamics 365 Finance, использующие управление проектами и учет</span><span class="sxs-lookup"><span data-stu-id="ef496-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="ef496-112">Существующие клиенты Finance, которые используют функцию управления проектами и учета, могут продолжать использовать ее как есть.</span><span class="sxs-lookup"><span data-stu-id="ef496-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="ef496-113">См. [Project Operations для сценариев на основе запасов/производственных заказов](#pma).</span><span class="sxs-lookup"><span data-stu-id="ef496-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="ef496-114">Project Operations поддерживает несколько вариантов развертывания в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="ef496-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="ef496-115">Независимо от того, являетесь ли вы новым или существующим клиентом Dynamics 365, Project Operations может удовлетворить ваши потребности.</span><span class="sxs-lookup"><span data-stu-id="ef496-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="ef496-116">Наша [анкета развертывания](https://aka.ms/provisionprojectoperations) поможет вам определить правильное развертывание.</span><span class="sxs-lookup"><span data-stu-id="ef496-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="ef496-117">Результаты помогут вам выбрать один из следующих типов развертывания:</span><span class="sxs-lookup"><span data-stu-id="ef496-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="ef496-118">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="ef496-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="ef496-119">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="ef496-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="ef496-120">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="ef496-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="ef496-121">Project Operations поддерживает сценарии складирования/производственного заказа и сценарии отсутствия запасов/ресурсов в одной и той же среде посредством конфигураций на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="ef496-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="ef496-122">Например, Contoso может использовать возможности складирования/производственного заказа на своем производственном предприятии в США (юридическое лицо = Contoso Manufacturing United States) и возможности отсутствия запасов/ресурсов на своем предприятии по обслуживанию Contoso Robotics Arms в Соединенном Королевстве (юридическое лицо = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="ef496-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="ef496-123"><a name="lite"><a/>Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="ef496-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="ef496-124">Облегченное развертывание включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="ef496-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="ef496-125">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="ef496-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ef496-126">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="ef496-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ef496-127">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="ef496-127">Unified Resource Management</span></span>
- <span data-ttu-id="ef496-128">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="ef496-128">Time Tracking</span></span>
- <span data-ttu-id="ef496-129">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="ef496-129">Basic Expense</span></span>
- <span data-ttu-id="ef496-130">Предложение по счету</span><span class="sxs-lookup"><span data-stu-id="ef496-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="ef496-131">Шаги развертывания:</span><span class="sxs-lookup"><span data-stu-id="ef496-131">Deployment steps:</span></span>
<span data-ttu-id="ef496-132">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ef496-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ef496-133">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](lite-preview-subscription-sign-up.md) и [Подготовка новой среды](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="ef496-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="ef496-134"><a name="integrated"><a/>Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="ef496-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="ef496-135">Project Operations для сценариев ресурсов/отсутствия запасов включают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="ef496-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="ef496-136">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="ef496-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ef496-137">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="ef496-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ef496-138">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="ef496-138">Unified Resource Management</span></span>
- <span data-ttu-id="ef496-139">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="ef496-139">Time Tracking</span></span>
- <span data-ttu-id="ef496-140">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="ef496-140">Basic Expense</span></span>
- <span data-ttu-id="ef496-141">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="ef496-141">Full Expense</span></span>
- <span data-ttu-id="ef496-142">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="ef496-142">Receipt OCR</span></span>
- <span data-ttu-id="ef496-143">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="ef496-143">Full Invoicing</span></span>
- <span data-ttu-id="ef496-144">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="ef496-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="ef496-145">Шаги развертывания:</span><span class="sxs-lookup"><span data-stu-id="ef496-145">Deployment steps:</span></span>
<span data-ttu-id="ef496-146">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ef496-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ef496-147">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](resource-sign-up-preview-subscription.md) и [Подготовка новой среды](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ef496-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="ef496-148">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="ef496-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="ef496-149">Планирование проектов с использованием WBS</span><span class="sxs-lookup"><span data-stu-id="ef496-149">Project planning using WBS</span></span>
- <span data-ttu-id="ef496-150">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="ef496-150">Resource Management</span></span>
- <span data-ttu-id="ef496-151">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="ef496-151">Time Tracking</span></span>
- <span data-ttu-id="ef496-152">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="ef496-152">Full Expense</span></span>
- <span data-ttu-id="ef496-153">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="ef496-153">Receipt OCR</span></span>
- <span data-ttu-id="ef496-154">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="ef496-154">Full Invoicing</span></span>
- <span data-ttu-id="ef496-155">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="ef496-155">Revenue Recognition</span></span>
- <span data-ttu-id="ef496-156">Производственные заказы</span><span class="sxs-lookup"><span data-stu-id="ef496-156">Production Orders</span></span>
- <span data-ttu-id="ef496-157">Поддержка материалов</span><span class="sxs-lookup"><span data-stu-id="ef496-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="ef496-158">Шаги развертывания:</span><span class="sxs-lookup"><span data-stu-id="ef496-158">Deployment steps:</span></span>
<span data-ttu-id="ef496-159">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ef496-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ef496-160">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) и [Подготовка новой среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ef496-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



