---
title: Определение типа развертывания
description: В этой теме дана информация, помогающая определить правильный тип развертывания Project Operations для вашей компании.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401234"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="a3953-103">Определение типа развертывания</span><span class="sxs-lookup"><span data-stu-id="a3953-103">Determine your deployment type</span></span>

<span data-ttu-id="a3953-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="a3953-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3953-105">После покупки лицензии начните здесь, чтобы определить лучшую модель развертывания Dynamics 365 Project Operations с помощью [управляемого потока установки](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a3953-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="a3953-106">После завершения процесса управляемой установки вы будете перенаправлены на нужный портал управления для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="a3953-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="a3953-107">См. сведения о развертывании, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="a3953-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="a3953-108">Существующие клиенты Dynamics, использующие Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3953-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="a3953-109">Project Operations включает возможности, которые поставляются с Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3953-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="a3953-110">Путь обновления будет выпущен для этих клиентов в волне 1 выпуска 2021 года.</span><span class="sxs-lookup"><span data-stu-id="a3953-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="a3953-111">Существующие клиенты Dynamics 365 Finance, использующие управление проектами и учет</span><span class="sxs-lookup"><span data-stu-id="a3953-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="a3953-112">Существующие клиенты Finance, которые используют функцию управления и учета по проектам, могут продолжать использовать ее как есть.</span><span class="sxs-lookup"><span data-stu-id="a3953-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="a3953-113">См. [Project Operations для сценариев на основе запасов/производственных заказов](#pma).</span><span class="sxs-lookup"><span data-stu-id="a3953-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="a3953-114">Типы развертывания</span><span class="sxs-lookup"><span data-stu-id="a3953-114">Deployment types</span></span>
<span data-ttu-id="a3953-115">Project Operations поддерживает несколько вариантов развертывания в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="a3953-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="a3953-116">Независимо от того, являетесь ли вы новым или существующим клиентом Dynamics 365, Project Operations может удовлетворить ваши потребности.</span><span class="sxs-lookup"><span data-stu-id="a3953-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="a3953-117">Наша [анкета развертывания](https://aka.ms/provisionprojectoperations) поможет вам определить правильное развертывание.</span><span class="sxs-lookup"><span data-stu-id="a3953-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="a3953-118">Результаты помогут вам выбрать один из следующих типов развертывания:</span><span class="sxs-lookup"><span data-stu-id="a3953-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="a3953-119">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="a3953-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="a3953-120">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="a3953-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="a3953-121">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="a3953-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="a3953-122">Project Operations поддерживает сценарии складирования/производственного заказа и сценарии отсутствия запасов/ресурсов в одной и той же среде посредством конфигураций на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="a3953-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="a3953-123">Например, Contoso может использовать возможности складирования/производственного заказа на своем производственном предприятии в США (юридическое лицо = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="a3953-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="a3953-124">Contoso может использовать возможности на основе ресурсов/без запасов в своем сервисном центре Contoso Robotics Arms в Соединенном Королевстве (юридическое лицо = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="a3953-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="a3953-125">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="a3953-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="a3953-126">Облегченное развертывание включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="a3953-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="a3953-127">Процесс продаж для проектов, расширяющих возможности приложения Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a3953-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="a3953-128">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="a3953-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a3953-129">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="a3953-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a3953-130">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="a3953-130">Unified resource management</span></span>
- <span data-ttu-id="a3953-131">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="a3953-131">Time tracking</span></span>
- <span data-ttu-id="a3953-132">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="a3953-132">Basic expense</span></span>
- <span data-ttu-id="a3953-133">Проформа и выставление счетов для клиентов</span><span class="sxs-lookup"><span data-stu-id="a3953-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="a3953-134">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="a3953-134">Deployment steps</span></span>
<span data-ttu-id="a3953-135">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a3953-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a3953-136">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](lite-preview-subscription-sign-up.md) и [Подготовка новой среды](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a3953-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="a3953-137">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="a3953-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="a3953-138">Project Operations для сценариев ресурсов/отсутствия запасов включают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="a3953-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="a3953-139">Процесс продаж для проектов, расширяющих приложение Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a3953-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="a3953-140">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="a3953-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a3953-141">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="a3953-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a3953-142">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="a3953-142">Unified resource management</span></span>
- <span data-ttu-id="a3953-143">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="a3953-143">Time tracking</span></span>
- <span data-ttu-id="a3953-144">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="a3953-144">Basic expense</span></span>
- <span data-ttu-id="a3953-145">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="a3953-145">Full expense</span></span>
- <span data-ttu-id="a3953-146">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="a3953-146">Receipt OCR</span></span>
- <span data-ttu-id="a3953-147">Проформа и выставление счетов для клиентов</span><span class="sxs-lookup"><span data-stu-id="a3953-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="a3953-148">Признание выручки для проектов</span><span class="sxs-lookup"><span data-stu-id="a3953-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a3953-149">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="a3953-149">Deployment steps</span></span>
<span data-ttu-id="a3953-150">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a3953-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a3953-151">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](resource-sign-up-preview-subscription.md) и [Подготовка новой среды](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a3953-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="a3953-152">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="a3953-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="a3953-153">Планирование проектов с использованием WBS</span><span class="sxs-lookup"><span data-stu-id="a3953-153">Project planning using WBS</span></span>
- <span data-ttu-id="a3953-154">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="a3953-154">Resource Management</span></span>
- <span data-ttu-id="a3953-155">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="a3953-155">Time Tracking</span></span>
- <span data-ttu-id="a3953-156">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="a3953-156">Full Expense</span></span>
- <span data-ttu-id="a3953-157">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="a3953-157">Receipt OCR</span></span>
- <span data-ttu-id="a3953-158">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="a3953-158">Full Invoicing</span></span>
- <span data-ttu-id="a3953-159">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="a3953-159">Revenue Recognition</span></span>
- <span data-ttu-id="a3953-160">Производственные заказы</span><span class="sxs-lookup"><span data-stu-id="a3953-160">Production Orders</span></span>
- <span data-ttu-id="a3953-161">Поддержка материалов</span><span class="sxs-lookup"><span data-stu-id="a3953-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="a3953-162">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="a3953-162">Deployment steps</span></span>
<span data-ttu-id="a3953-163">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="a3953-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a3953-164">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) и [Подготовка новой среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a3953-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

