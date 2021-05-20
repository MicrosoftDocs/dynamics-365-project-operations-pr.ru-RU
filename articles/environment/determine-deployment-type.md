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
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948130"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="f868b-103">Определение типа развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-103">Determine your deployment type</span></span>

<span data-ttu-id="f868b-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="f868b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f868b-105">После покупки лицензии начните здесь, чтобы определить лучшую модель развертывания Dynamics 365 Project Operations с использованием [Управляемого процесса установки](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f868b-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="f868b-106">После завершения процесса управляемой установки вы будете перенаправлены на нужный портал управления для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="f868b-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="f868b-107">См. сведения о развертывании, чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="f868b-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="f868b-108">Существующие клиенты Dynamics, использующие Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f868b-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="f868b-109">Project Operations включает возможности, которые поставляются с Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f868b-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="f868b-110">Путь обновления будет выпущен для этих клиентов в волне 1 выпуска 2021 года.</span><span class="sxs-lookup"><span data-stu-id="f868b-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="f868b-111">Существующие клиенты Dynamics 365 Finance, использующие управление проектами и учет</span><span class="sxs-lookup"><span data-stu-id="f868b-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="f868b-112">Существующие клиенты Finance, которые используют функцию управления и учета по проектам, могут продолжать использовать ее как есть.</span><span class="sxs-lookup"><span data-stu-id="f868b-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="f868b-113">См. [Project Operations для сценариев на основе запасов/производственных заказов](#pma).</span><span class="sxs-lookup"><span data-stu-id="f868b-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="f868b-114">Регионы развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-114">Deployment regions</span></span>
<span data-ttu-id="f868b-115">Чтобы определить, какие регионы поддерживают развертывание Project Operations, см. [Отчет о географической доступности Dynamics 365 и Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="f868b-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="f868b-116">Выберите **Посмотреть отчет** и разверните **Dynamics 365 > Приложения Operations > Dynamics 365 Project Operations** для просмотра поддерживаемых регионов.</span><span class="sxs-lookup"><span data-stu-id="f868b-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="f868b-117">Типы развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-117">Deployment types</span></span>
<span data-ttu-id="f868b-118">Project Operations поддерживает несколько вариантов развертывания в соответствии с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="f868b-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="f868b-119">Независимо от того, являетесь ли вы новым или существующим клиентом Dynamics 365, Project Operations может удовлетворить ваши потребности.</span><span class="sxs-lookup"><span data-stu-id="f868b-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="f868b-120">Наша [анкета развертывания](https://aka.ms/provisionprojectoperations) поможет вам определить правильное развертывание.</span><span class="sxs-lookup"><span data-stu-id="f868b-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="f868b-121">Результаты помогут вам выбрать один из следующих типов развертывания:</span><span class="sxs-lookup"><span data-stu-id="f868b-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="f868b-122">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="f868b-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="f868b-123">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="f868b-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="f868b-124">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="f868b-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="f868b-125">Project Operations поддерживает сценарии складирования/производственного заказа и сценарии отсутствия запасов/ресурсов в одной и той же среде посредством конфигураций на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="f868b-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="f868b-126">Например, Contoso может использовать возможности запасов/производственного заказа на своем производственном предприятии в США (юридическое лицо = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="f868b-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="f868b-127">Contoso может использовать возможности, не связанные с запасами/ресурсами, в своем сервисном предприятии Contoso Robotics Arms в Великобритании (юридическое лицо = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="f868b-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="f868b-128">Облегченное развертывание — от сделки до счетов-проформ</span><span class="sxs-lookup"><span data-stu-id="f868b-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="f868b-129">Облегченное развертывание включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="f868b-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="f868b-130">Процесс продаж для проектов, расширяющих возможности приложения Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f868b-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="f868b-131">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="f868b-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f868b-132">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="f868b-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f868b-133">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="f868b-133">Unified resource management</span></span>
- <span data-ttu-id="f868b-134">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="f868b-134">Time tracking</span></span>
- <span data-ttu-id="f868b-135">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="f868b-135">Basic expense</span></span>
- <span data-ttu-id="f868b-136">Выставление счета-проформы для проверки и редактирования руководителем проекта</span><span class="sxs-lookup"><span data-stu-id="f868b-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="f868b-137">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-137">Deployment steps</span></span>
<span data-ttu-id="f868b-138">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f868b-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f868b-139">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](lite-preview-subscription-sign-up.md) и [Подготовка новой среды](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f868b-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="f868b-140">Project Operations для сценариев на основе ресурсов / без запасов</span><span class="sxs-lookup"><span data-stu-id="f868b-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="f868b-141">Project Operations для сценариев ресурсов/отсутствия запасов включают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="f868b-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="f868b-142">Процесс продаж для проектов, расширяющих приложение Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f868b-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="f868b-143">Планирование проекта с помощью Microsoft Project для Интернета</span><span class="sxs-lookup"><span data-stu-id="f868b-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f868b-144">Многомерное ценообразование</span><span class="sxs-lookup"><span data-stu-id="f868b-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f868b-145">Единое управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="f868b-145">Unified resource management</span></span>
- <span data-ttu-id="f868b-146">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="f868b-146">Time tracking</span></span>
- <span data-ttu-id="f868b-147">Базовые расходы</span><span class="sxs-lookup"><span data-stu-id="f868b-147">Basic expense</span></span>
- <span data-ttu-id="f868b-148">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="f868b-148">Full expense</span></span>
- <span data-ttu-id="f868b-149">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="f868b-149">Receipt OCR</span></span>
- <span data-ttu-id="f868b-150">Проформа и выставление счетов для клиентов</span><span class="sxs-lookup"><span data-stu-id="f868b-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="f868b-151">Признание выручки для проектов</span><span class="sxs-lookup"><span data-stu-id="f868b-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f868b-152">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-152">Deployment steps</span></span>
<span data-ttu-id="f868b-153">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f868b-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f868b-154">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](resource-sign-up-preview-subscription.md) и [Подготовка новой среды](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f868b-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="f868b-155">Project Operations для сценариев на основе запасов/производственных заказов</span><span class="sxs-lookup"><span data-stu-id="f868b-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="f868b-156">Планирование проектов с использованием WBS</span><span class="sxs-lookup"><span data-stu-id="f868b-156">Project planning using WBS</span></span>
- <span data-ttu-id="f868b-157">Управление ресурсами</span><span class="sxs-lookup"><span data-stu-id="f868b-157">Resource management</span></span>
- <span data-ttu-id="f868b-158">Отслеживание времени</span><span class="sxs-lookup"><span data-stu-id="f868b-158">Time tracking</span></span>
- <span data-ttu-id="f868b-159">Полные расходы</span><span class="sxs-lookup"><span data-stu-id="f868b-159">Full expense</span></span>
- <span data-ttu-id="f868b-160">OCR чеков</span><span class="sxs-lookup"><span data-stu-id="f868b-160">Receipt OCR</span></span>
- <span data-ttu-id="f868b-161">Полное выставление счетов</span><span class="sxs-lookup"><span data-stu-id="f868b-161">Full invoicing</span></span>
- <span data-ttu-id="f868b-162">Признание выручки</span><span class="sxs-lookup"><span data-stu-id="f868b-162">Revenue recognition</span></span>
- <span data-ttu-id="f868b-163">Производственные заказы</span><span class="sxs-lookup"><span data-stu-id="f868b-163">Production orders</span></span>
- <span data-ttu-id="f868b-164">Сопровождение складских материалов с инвентаризацией</span><span class="sxs-lookup"><span data-stu-id="f868b-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f868b-165">Шаги развертывания</span><span class="sxs-lookup"><span data-stu-id="f868b-165">Deployment steps</span></span>
<span data-ttu-id="f868b-166">Определите лучшую модель развертывания Project Operations, используя [анкету развертывания](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f868b-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f868b-167">Для этого развертывания см. разделы [Регистрация на подписки на предварительную версию](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) и [Подготовка новой среды](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="f868b-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]