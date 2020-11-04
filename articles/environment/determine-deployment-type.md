---
title: Определение типа развертывания
description: В этой теме дана информация, помогающая определить правильный тип развертывания Project Operations для вашей компании.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083192"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="059c5-103">Определение типа развертывания</span><span class="sxs-lookup"><span data-stu-id="059c5-103">Determine your deployment type</span></span>

<span data-ttu-id="059c5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="059c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="059c5-105">После покупки лицензии начните здесь, чтобы определить лучшую модель развертывания Dynamics 365 Project Operations с помощью [управляемого потока установки](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="059c5-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="059c5-106">После завершения процесса управляемой установки вы будете перенаправлены на нужный портал управления для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="059c5-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="059c5-107">См. сведения о развертывании, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="059c5-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="059c5-108">Существующие клиенты Dynamics, использующие Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="059c5-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="059c5-109">Project Operations включает возможности, которые поставляются с Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="059c5-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="059c5-110">В будущем для этих клиентов будет выпущен путь обновления.</span><span class="sxs-lookup"><span data-stu-id="059c5-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="059c5-111">Существующие клиенты Dynamics 365 Finance, использующие управление проектами и учет</span><span class="sxs-lookup"><span data-stu-id="059c5-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="059c5-112">Существующие клиенты Finance, которые используют функцию управления проектами и учета, могут продолжать использовать ее как есть.</span><span class="sxs-lookup"><span data-stu-id="059c5-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="059c5-113">См. [Project Operations для сценариев на основе запасов/производственных заказов](#pma).</span><span class="sxs-lookup"><span data-stu-id="059c5-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="059c5-114">Типы развертывания</span><span class="sxs-lookup"><span data-stu-id="059c5-114">Deployment types</span></span>
<span data-ttu-id="059c5-115">Project Operations поддерживает несколько вариантов развертывания в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="059c5-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="059c5-116">Независимо от того, являетесь ли вы новым или существующим клиентом Dynamics 365, Project Operations может удовлетворить ваши потребности.</span><span class="sxs-lookup"><span data-stu-id="059c5-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="059c5-117">Наша [анкета развертывания](https://aka.ms/provisionprojectoperations) поможет вам определить правильное развертывание.</span><span class="sxs-lookup"><span data-stu-id="059c5-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="059c5-118">Результаты помогут вам выбрать один из следующих типов развертывания:</span><span class="sxs-lookup"><span data-stu-id="059c5-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="059c5-119">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="059c5-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="059c5-120">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="059c5-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="059c5-121">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="059c5-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="059c5-122">Project Operations поддерживает сценарии складирования/производственного заказа и сценарии отсутствия запасов/ресурсов в одной и той же среде посредством конфигураций на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="059c5-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="059c5-123">Например, Contoso может использовать возможности складирования/производственного заказа на своем производственном предприятии в США (юридическое лицо = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="059c5-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="059c5-124">Contoso может использовать возможности на основе ресурсов/без запасов в своем сервисном центре Contoso Robotics Arms в Соединенном Королевстве (юридическое лицо = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="059c5-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="059c5-125">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="059c5-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="059c5-126">Облегченное развертывание включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="059c5-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="059c5-127">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="059c5-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="059c5-128">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="059c5-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="059c5-129">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="059c5-129">Unified Resource Management</span></span>
- <span data-ttu-id="059c5-130">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="059c5-130">Time Tracking</span></span>
- <span data-ttu-id="059c5-131">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="059c5-131">Basic Expense</span></span>
- <span data-ttu-id="059c5-132">Предложение по счету</span><span class="sxs-lookup"><span data-stu-id="059c5-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="059c5-133">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="059c5-133">Deployment steps</span></span>
<span data-ttu-id="059c5-134">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="059c5-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="059c5-135">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](lite-preview-subscription-sign-up.md) и [Подготовка новой среды](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="059c5-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="059c5-136">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="059c5-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="059c5-137">Project Operations для сценариев ресурсов/отсутствия запасов включают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="059c5-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="059c5-138">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="059c5-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="059c5-139">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="059c5-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="059c5-140">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="059c5-140">Unified Resource Management</span></span>
- <span data-ttu-id="059c5-141">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="059c5-141">Time Tracking</span></span>
- <span data-ttu-id="059c5-142">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="059c5-142">Basic Expense</span></span>
- <span data-ttu-id="059c5-143">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="059c5-143">Full Expense</span></span>
- <span data-ttu-id="059c5-144">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="059c5-144">Receipt OCR</span></span>
- <span data-ttu-id="059c5-145">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="059c5-145">Full Invoicing</span></span>
- <span data-ttu-id="059c5-146">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="059c5-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="059c5-147">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="059c5-147">Deployment steps</span></span>
<span data-ttu-id="059c5-148">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="059c5-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="059c5-149">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](resource-sign-up-preview-subscription.md) и [Подготовка новой среды](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="059c5-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="059c5-150">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="059c5-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="059c5-151">Планирование проектов с использованием WBS</span><span class="sxs-lookup"><span data-stu-id="059c5-151">Project planning using WBS</span></span>
- <span data-ttu-id="059c5-152">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="059c5-152">Resource Management</span></span>
- <span data-ttu-id="059c5-153">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="059c5-153">Time Tracking</span></span>
- <span data-ttu-id="059c5-154">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="059c5-154">Full Expense</span></span>
- <span data-ttu-id="059c5-155">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="059c5-155">Receipt OCR</span></span>
- <span data-ttu-id="059c5-156">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="059c5-156">Full Invoicing</span></span>
- <span data-ttu-id="059c5-157">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="059c5-157">Revenue Recognition</span></span>
- <span data-ttu-id="059c5-158">Производственные заказы</span><span class="sxs-lookup"><span data-stu-id="059c5-158">Production Orders</span></span>
- <span data-ttu-id="059c5-159">Поддержка материалов</span><span class="sxs-lookup"><span data-stu-id="059c5-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="059c5-160">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="059c5-160">Deployment steps</span></span>
<span data-ttu-id="059c5-161">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="059c5-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="059c5-162">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) и [Подготовка новой среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="059c5-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

