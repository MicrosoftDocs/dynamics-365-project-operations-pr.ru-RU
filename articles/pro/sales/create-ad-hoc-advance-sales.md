---
title: Создание специального аванса по контракту
description: Эта тема предоставляет информацию о создании аванса по контракту при необходимости.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273613"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="35d9c-103">Создание специального аванса по контракту</span><span class="sxs-lookup"><span data-stu-id="35d9c-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="35d9c-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="35d9c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35d9c-105">Microsoft Dynamics 365 Project Operations поддерживает сценарии выставления счетов, которые включают предоплату и авансы.</span><span class="sxs-lookup"><span data-stu-id="35d9c-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="35d9c-106">Процесс использования **Авансов** в **Project Operations** похож на контракты с **Гонораром**.</span><span class="sxs-lookup"><span data-stu-id="35d9c-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="35d9c-107">Выполните следующие шаги, чтобы выставить клиенту счет на аванс.</span><span class="sxs-lookup"><span data-stu-id="35d9c-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="35d9c-108">Перейдите в раздел **Контракт по проекту**, затем выберите вкладку **Авансы и гонорары**.</span><span class="sxs-lookup"><span data-stu-id="35d9c-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="35d9c-109">Во вложенной сетке, в которой перечислены все ранее записанные авансы и предоплаты, выберите **+ Создать гонорар по контракту по проекту**.</span><span class="sxs-lookup"><span data-stu-id="35d9c-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="35d9c-110">Открывается форма **Быстрое создание** для записи предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="35d9c-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="35d9c-111">В таблице ниже перечислены поля для записи аванса и рекомендации, которые следует учитывать при создании новых:</span><span class="sxs-lookup"><span data-stu-id="35d9c-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="35d9c-112">Поле</span><span class="sxs-lookup"><span data-stu-id="35d9c-112">Field</span></span> | <span data-ttu-id="35d9c-113">Описание:</span><span class="sxs-lookup"><span data-stu-id="35d9c-113">Description</span></span> | <span data-ttu-id="35d9c-114">Воздействие на последующие элементы</span><span class="sxs-lookup"><span data-stu-id="35d9c-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="35d9c-115">**Клиент контракта по проекту**</span><span class="sxs-lookup"><span data-stu-id="35d9c-115">**Project Contract Customer**</span></span> | <span data-ttu-id="35d9c-116">В этом поле указано, какому клиенту по контракту будет выставлен счет на этот аванс.</span><span class="sxs-lookup"><span data-stu-id="35d9c-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="35d9c-117">Если у вас есть несколько клиентов по контракту и вы хотите выставить счет каждому из них на определенную сумму предоплаты или аванса, создайте аванс для каждого клиента индивидуально.</span><span class="sxs-lookup"><span data-stu-id="35d9c-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="35d9c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35d9c-118">**Description**</span></span> | <span data-ttu-id="35d9c-119">Описание цели или времени аванса, чтобы помочь идентифицировать этот аванс.</span><span class="sxs-lookup"><span data-stu-id="35d9c-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="35d9c-120">Это описание отображается в строке счета для данного аванса.</span><span class="sxs-lookup"><span data-stu-id="35d9c-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="35d9c-121">**Сумма**</span><span class="sxs-lookup"><span data-stu-id="35d9c-121">**Amount**</span></span> | <span data-ttu-id="35d9c-122">Сумма предоплаты или аванса.</span><span class="sxs-lookup"><span data-stu-id="35d9c-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="35d9c-123">Эта сумма отображается в строке счета для данного аванса.</span><span class="sxs-lookup"><span data-stu-id="35d9c-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="35d9c-124">**Дата счета**</span><span class="sxs-lookup"><span data-stu-id="35d9c-124">**Invoice Date**</span></span> | <span data-ttu-id="35d9c-125">Дата выставления клиенту счета на этот аванс.</span><span class="sxs-lookup"><span data-stu-id="35d9c-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="35d9c-126">Эта дата процесса автоматического создания счета для создания строки счета для этого аванса.</span><span class="sxs-lookup"><span data-stu-id="35d9c-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="35d9c-127">**Состояние счета**</span><span class="sxs-lookup"><span data-stu-id="35d9c-127">**Invoice Status**</span></span> | <span data-ttu-id="35d9c-128">Это параметр, указывающий, добавлен ли этот аванс в черновик счета для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="35d9c-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="35d9c-129">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="35d9c-129">The possible values are:</span></span></br><span data-ttu-id="35d9c-130">- **Не готово к выставлению счета**</span><span class="sxs-lookup"><span data-stu-id="35d9c-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="35d9c-131">- **Готово к выставлению счета**</span><span class="sxs-lookup"><span data-stu-id="35d9c-131">- **Ready to invoice**</span></span> | <span data-ttu-id="35d9c-132">Когда аванс или предоплата отмечены как **Готово к выставлению счета**, он добавляется как время строки в черновик счета.</span><span class="sxs-lookup"><span data-stu-id="35d9c-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="35d9c-133">Только полностью выставленный аванс может использоваться для сверки с затратами по проекту на следующий период выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="35d9c-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="35d9c-134">Выберите **Сохранить и закрыть** в диалоге быстрого создания для записи аванса или предоплаты.</span><span class="sxs-lookup"><span data-stu-id="35d9c-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]