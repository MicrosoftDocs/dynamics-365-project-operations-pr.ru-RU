---
title: Поля Project Operations в качестве измерений цен
description: В этом разделе представлена информация об использовании полей в качестве измерений цен в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274654"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="bf43f-103">Поля Project Operations в качестве измерений цен</span><span class="sxs-lookup"><span data-stu-id="bf43f-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="bf43f-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="bf43f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf43f-105">Сущность **Фактические значения** имеет много полей, которые можно использовать в качестве измерений ценообразования для ценообразования на основе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf43f-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="bf43f-106">Например, общее поле **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="bf43f-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="bf43f-107">Небольшие компании, которые имеют менее 20-30 оплачиваемых ресурсов, могут обнаружить, что иметь тарифы выставления счетов и нормы затрат, специфичные для каждого ресурса — более простой подход.</span><span class="sxs-lookup"><span data-stu-id="bf43f-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="bf43f-108">Однако по мере роста оплачиваемой рабочей силы количество тарифов на основе ресурсов может стать нереальным для поддержания.</span><span class="sxs-lookup"><span data-stu-id="bf43f-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="bf43f-109">Стоимость ресурсов и ставки счетов начинают меняться по мере продвижения ресурсов, накопления опыта или приобретения другого набора навыков.</span><span class="sxs-lookup"><span data-stu-id="bf43f-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="bf43f-110">Другим примером является категория проводки.</span><span class="sxs-lookup"><span data-stu-id="bf43f-110">Another example is that of transaction category.</span></span> <span data-ttu-id="bf43f-111">Клиенты и исполнители использовали категорию проводки для классификации работы и использования поля для расчета цены и расхода в зависимости от категории работы.</span><span class="sxs-lookup"><span data-stu-id="bf43f-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]