---
title: измерение цен существующего поля в Project Service как измерение цен
description: В этом разделе представлена информация об использовании существующих полей Project Service в качестве измерений цен.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083266"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="cf5e4-103">измерение цен существующего поля в Project Service как измерение цен</span><span class="sxs-lookup"><span data-stu-id="cf5e4-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="cf5e4-104">Project Service Automation (PSA) имеет много полей в сущности **Фактические значения** , которые можно использовать в качестве измерений цен для ценообразования на основе ресурсов в проектных организациях.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="cf5e4-105">Например, общее поле **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="cf5e4-106">Небольшие компании, которые имеют менее 20-30 оплачиваемых ресурсов, могут обнаружить, что иметь тарифы выставления счетов и нормы затрат, специфичные для каждого ресурса — более простой подход.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="cf5e4-107">Однако по мере роста оплачиваемой рабочей силы, может стать проблематичным для поддержания, так как стоимость ресурсов и тарифы выставления счетов начинают меняться по мере продвижения ресурсов, получения большего опыта или приобретения других навыков.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="cf5e4-108">Поскольку этот подход по-прежнему работает для компаний определенного размера, см. раздел [Использование резервируемого ресурса как измерения цен](bookable-resource-pricing-dimension.md) чтобы понять, как можно использовать существующее поле Project Service в качестве измерения цен.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="cf5e4-109">Другим примером является категория проводки.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-109">Another example is that of transaction category.</span></span> <span data-ttu-id="cf5e4-110">Клиенты и исполнители использовали категорию проводки в PSA для классификации работы и использования поля для расчета цены и расхода в зависимости от категории работы.</span><span class="sxs-lookup"><span data-stu-id="cf5e4-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="cf5e4-111">Дополнительные сведения см. в разделе [Использование категории проводки как измерение цен](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="cf5e4-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
