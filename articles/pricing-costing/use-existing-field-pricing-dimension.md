---
title: Поля Project Operations в качестве измерений цен
description: В этой теме предоставлена информация об использовании полей в качестве измерений ценообразования в Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083251"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="d2666-103">Поля Project Operations в качестве измерений цен</span><span class="sxs-lookup"><span data-stu-id="d2666-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="d2666-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="d2666-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d2666-105">Сущность **Фактические значения** имеет много полей, которые можно использовать в качестве измерений ценообразования для ценообразования на основе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2666-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="d2666-106">Например, общее поле **Резервируемый ресурс**.</span><span class="sxs-lookup"><span data-stu-id="d2666-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d2666-107">Небольшие компании, которые имеют менее 20-30 оплачиваемых ресурсов, могут обнаружить, что иметь тарифы выставления счетов и нормы затрат, специфичные для каждого ресурса — более простой подход.</span><span class="sxs-lookup"><span data-stu-id="d2666-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d2666-108">Однако по мере роста оплачиваемой рабочей силы количество тарифов на основе ресурсов может стать нереальным для поддержания.</span><span class="sxs-lookup"><span data-stu-id="d2666-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="d2666-109">Стоимость ресурсов и ставки счетов начинают меняться по мере продвижения ресурсов, накопления опыта или приобретения другого набора навыков.</span><span class="sxs-lookup"><span data-stu-id="d2666-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="d2666-110">Другим примером является категория проводки.</span><span class="sxs-lookup"><span data-stu-id="d2666-110">Another example is that of transaction category.</span></span> <span data-ttu-id="d2666-111">Клиенты и исполнители использовали категорию проводки для классификации работы и использования поля для расчета цены и расхода в зависимости от категории работы.</span><span class="sxs-lookup"><span data-stu-id="d2666-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
