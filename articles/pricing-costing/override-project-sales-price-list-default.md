---
title: Переопределение прайс-листов продаж по проекту
description: Эта тема предоставляет информацию о создании пользовательских прайс-листов продажи.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275554"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="7be87-103">Переопределение прайс-листов продаж по проекту</span><span class="sxs-lookup"><span data-stu-id="7be87-103">Override project sales price lists</span></span>

<span data-ttu-id="7be87-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="7be87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="7be87-105">Прайс-листы проекта для конкретного клиента</span><span class="sxs-lookup"><span data-stu-id="7be87-105">Customer-specific project price lists</span></span>

<span data-ttu-id="7be87-106">Ценовые соглашения для конкретного клиента могут быть настроены как прайс-листы проекта в записи учетной записи в Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7be87-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="7be87-107">Чтобы настроить прайс-лист проекта для конкретного клиента, в области **Продажи** перейдите к записи учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7be87-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="7be87-108">Откройте страницу списка **Учетные записи**.</span><span class="sxs-lookup"><span data-stu-id="7be87-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="7be87-109">Найдите и дважды щелкните запись клиента, чтобы открыть страницу сведений **Учетная запись**.</span><span class="sxs-lookup"><span data-stu-id="7be87-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="7be87-110">На вкладке **Прайс-листы проекта** выберите **+ Создать прайс-лист проекта**.</span><span class="sxs-lookup"><span data-stu-id="7be87-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="7be87-111">На странице **Создать прайс-лист проекта** выберите прайс-лист из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="7be87-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="7be87-112">Включены только прайс-листы, для которых задан контекст **Продажи** и валюта которых совпадает с валютой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7be87-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="7be87-113">Назовите связь, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7be87-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="7be87-114">Прайс-лист проекта для конкретного клиента создан.</span><span class="sxs-lookup"><span data-stu-id="7be87-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="7be87-115">Этот прайс-лист будет использоваться для цен проекта по умолчанию в предложениях с расценками по проекту или для контрактов, созданных для этого клиента, если дата создания предложения с расценками или контракта по проекту попадает в дату действия прайс-листа.</span><span class="sxs-lookup"><span data-stu-id="7be87-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="7be87-116">Пользовательские цены в предложениях с расценками по проектам</span><span class="sxs-lookup"><span data-stu-id="7be87-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="7be87-117">В предложениях с расценками по проекту вы можете указать цену проекта, которая начинается со стандартного прайс-листа по умолчанию, который по умолчанию устанавливается по клиенту или из параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="7be87-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="7be87-118">Если вам нужна индивидуальная цена для работы, связанной с проектом, по определенному предложению с расценками, вы можете получить это из связанной сущности прайс-листов проекта.</span><span class="sxs-lookup"><span data-stu-id="7be87-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="7be87-119">Выполните следующие шаги, чтобы установить цены по проекту для конкретного предложения с расценками.</span><span class="sxs-lookup"><span data-stu-id="7be87-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="7be87-120">Откройте предложение с расценками по проекту и выберите вкладку **Прайс-листы проекта**.</span><span class="sxs-lookup"><span data-stu-id="7be87-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="7be87-121">Во вложенной сетке выберите **Создать пользовательские цены**.</span><span class="sxs-lookup"><span data-stu-id="7be87-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="7be87-122">Все прайс-листы проекта, прилагаемые к предложению с расценками, копируются в новые прайс-листы.</span><span class="sxs-lookup"><span data-stu-id="7be87-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="7be87-123">Имена новых прайс-листов отражают название предложения с расценками с отметкой даты и времени, когда эти прайс-листы были созданы.</span><span class="sxs-lookup"><span data-stu-id="7be87-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="7be87-124">Вы можете использовать каждый из этих прайс-листов и обновлять цены на рабочую силу (цены ролей) или цены расходов (цена категории).</span><span class="sxs-lookup"><span data-stu-id="7be87-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="7be87-125">Эти цены будут применяться только к данному предложению с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="7be87-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="7be87-126">Прайс-листы в контракте по проекту</span><span class="sxs-lookup"><span data-stu-id="7be87-126">Price lists on a project contract</span></span>

<span data-ttu-id="7be87-127">В контракте по проекту цена для проекта всегда устанавливается по умолчанию в виде настраиваемого прайс-листа с названием контракта и отметкой даты и времени создания, добавленной к имени.</span><span class="sxs-lookup"><span data-stu-id="7be87-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="7be87-128">Это верно независимо от того, был ли контракт создан при выигрыше предложения с расценками или контракт был создан с нуля.</span><span class="sxs-lookup"><span data-stu-id="7be87-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="7be87-129">При необходимости вы можете удалить эту связь с настраиваемым прайс-листом и вместо этого связать стандартный прайс-лист с контрактом по проекту.</span><span class="sxs-lookup"><span data-stu-id="7be87-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="7be87-130">Когда вы связываете стандартный прайс-лист с прайс-листами проекта в предложении с расценками или контракте, любые изменения, внесенные в цены в прайс-листе, повлияют на все предложения с расценками и контракты, в которых используется этот прайс-лист.</span><span class="sxs-lookup"><span data-stu-id="7be87-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]