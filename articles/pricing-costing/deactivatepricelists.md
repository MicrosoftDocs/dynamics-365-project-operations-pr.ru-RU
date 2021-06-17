---
title: Деактивация прайс-листов
description: В этой теме объясняется, как деактивировать или удалить неиспользуемые или старые прайс-листы.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001352"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="f5621-103">Деактивация прайс-листов</span><span class="sxs-lookup"><span data-stu-id="f5621-103">Deactivate price lists</span></span> 

<span data-ttu-id="f5621-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="f5621-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f5621-105">Чтобы удалить старые или неиспользованные прайс-листы из Dynamics 365 Project Operations, необходимо выполнить два шага.</span><span class="sxs-lookup"><span data-stu-id="f5621-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="f5621-106">Удалите прайс-лист с конкретных страниц.</span><span class="sxs-lookup"><span data-stu-id="f5621-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="f5621-107">Деактивируйте или удалите прайс-лист из активных прайс-листов на странице **Прайс-листы**.</span><span class="sxs-lookup"><span data-stu-id="f5621-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="f5621-108">Следует выполнить оба шага, чтобы полностью удалить прайс-лист.</span><span class="sxs-lookup"><span data-stu-id="f5621-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="f5621-109">Одного выполнения шага 2, который заключается в непосредственном удалении или деактивации прайс-листа из представления "Активные прайс-листы", недостаточно.</span><span class="sxs-lookup"><span data-stu-id="f5621-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="f5621-110">Вы также должны удалить связь этого прайс-листа из всех мест, упомянутых в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="f5621-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="f5621-111">Удаление прайс-листа с конкретных страниц</span><span class="sxs-lookup"><span data-stu-id="f5621-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="f5621-112">Чтобы удалить прайс-лист из Project Operations, перейдите на следующие страницы:</span><span class="sxs-lookup"><span data-stu-id="f5621-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="f5621-113">Страница **Параметры проекта** > вкладка **Прайс-листы**</span><span class="sxs-lookup"><span data-stu-id="f5621-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="f5621-114">Страница **Подразделение** > сетка **Прайс-листы**</span><span class="sxs-lookup"><span data-stu-id="f5621-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="f5621-115">Страница **Организация** > сетка **Прайс-листы проекта**</span><span class="sxs-lookup"><span data-stu-id="f5621-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="f5621-116">Страница **Предложения с расценками по проекту** > сетка **Прайс-листы проекта**: это относится ко всем активным предложениям с расценками по проекту.</span><span class="sxs-lookup"><span data-stu-id="f5621-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="f5621-117">Страница **Контракты по проектам** > сетка **Прайс-листы проекта**: это относится ко всем активным контрактам по проекту.</span><span class="sxs-lookup"><span data-stu-id="f5621-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="f5621-118">На каждой странице вам нужно выбрать прайс-лист, который нужно удалить, а затем выбрать **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="f5621-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="f5621-119">Деактивация или удаление прайс-листа со страницы "Прайс-листы"</span><span class="sxs-lookup"><span data-stu-id="f5621-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="f5621-120">Чтобы удалить прайс-лист из активных прайс-листов, перейдите **Продажи** > **Клиенты** > **Прайс-листы**.</span><span class="sxs-lookup"><span data-stu-id="f5621-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="f5621-121">Выберите прайс-лист, который требуется удалить, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="f5621-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="f5621-122">Если прайс-лист ссылается на какие-либо существующие транзакции, вы не сможете его удалить.</span><span class="sxs-lookup"><span data-stu-id="f5621-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="f5621-123">В этом случае вы можете деактивировать прайс-лист, чтобы он не отображался ни в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="f5621-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="f5621-124">Чтобы деактивировать прайс-лист, выберите прайс-лист еще раз, а затем выберите **Деактивировать**.</span><span class="sxs-lookup"><span data-stu-id="f5621-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
