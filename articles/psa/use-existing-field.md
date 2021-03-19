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
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281584"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="e02b1-103">измерение цен существующего поля в Project Service как измерение цен</span><span class="sxs-lookup"><span data-stu-id="e02b1-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e02b1-104">Project Service Automation (PSA) имеет много полей в сущности **Фактические значения**, которые можно использовать в качестве измерений цен для ценообразования на основе ресурсов в проектных организациях.</span><span class="sxs-lookup"><span data-stu-id="e02b1-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="e02b1-105">Например, общее поле **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="e02b1-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="e02b1-106">Небольшие компании, которые имеют менее 20-30 оплачиваемых ресурсов, могут обнаружить, что иметь тарифы выставления счетов и нормы затрат, специфичные для каждого ресурса — более простой подход.</span><span class="sxs-lookup"><span data-stu-id="e02b1-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="e02b1-107">Однако по мере роста оплачиваемой рабочей силы, особые ставки могут стать проблематичными для поддержания, так как стоимость ресурсов и тарифы выставления счетов начинают меняться по мере продвижения ресурсов, получения большего опыта или приобретения других наборов навыков.</span><span class="sxs-lookup"><span data-stu-id="e02b1-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="e02b1-108">Поскольку этот подход по-прежнему работает для компаний определенного размера, см. [Использование резервируемого ресурса как измерения цен](bookable-resource-pricing-dimension.md) чтобы понять, как можно использовать существующее поле Project Service в качестве измерения цен.</span><span class="sxs-lookup"><span data-stu-id="e02b1-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="e02b1-109">Другим примером является категория проводки.</span><span class="sxs-lookup"><span data-stu-id="e02b1-109">Another example is that of transaction category.</span></span> <span data-ttu-id="e02b1-110">Клиенты и исполнители использовали категорию проводки в PSA для классификации работы и использования поля для расчета цены и расхода в зависимости от категории работы.</span><span class="sxs-lookup"><span data-stu-id="e02b1-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="e02b1-111">Дополнительные сведения см. в разделе [Использование категории проводки как измерение цен](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="e02b1-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]