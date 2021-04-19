---
title: Создание и применение условий удержания платежей поставщикам
description: Эта тема предоставляет информацию о том, как настроить и поддерживать условия удержания платежей поставщикам.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270964"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="54e4c-103">Создание и применение условий удержания платежей поставщикам</span><span class="sxs-lookup"><span data-stu-id="54e4c-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="54e4c-104">Настройка условий удержания платежей поставщикам для проекта полезна, когда ваша организация хочет задержать часть платежей, производимых поставщику.</span><span class="sxs-lookup"><span data-stu-id="54e4c-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="54e4c-105">Например, если вы хотите отложить платеж поставщику до тех пор, пока не убедитесь, что поставленные продукты соответствуют вашим ожиданиям.</span><span class="sxs-lookup"><span data-stu-id="54e4c-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="54e4c-106">Условия удержания платежей поставщикам могут быть указаны при заключении контракта с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="54e4c-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="54e4c-107">Создание условий удержания платежей поставщикам</span><span class="sxs-lookup"><span data-stu-id="54e4c-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="54e4c-108">Вы можете ввести процент платежа поставщику для удержания и процент ранее удерживаемых сумм, подлежащих деблокированию.</span><span class="sxs-lookup"><span data-stu-id="54e4c-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="54e4c-109">Суммы автоматически сохраняются в счетах поставщиков до тех пор, пока контракт не достигнет указанного состояния завершения.</span><span class="sxs-lookup"><span data-stu-id="54e4c-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="54e4c-110">После настройки условий удержания вы можете применить их к любому проекту для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="54e4c-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="54e4c-111">Выполните следующие действия, чтобы настроить и поддерживать условия удержания платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="54e4c-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="54e4c-112">Перейдите в раздел **Управление и учет по проектам** > **Удержание** > **Условия удержания оплаты поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="54e4c-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="54e4c-113">Выберите **Создать**, чтобы добавить новое условие удержание оплаты поставщикам.</span><span class="sxs-lookup"><span data-stu-id="54e4c-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="54e4c-114">Значение **Код правила** для новых условий вводится автоматически.</span><span class="sxs-lookup"><span data-stu-id="54e4c-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="54e4c-115">Введите краткое описание в поле **Описание** и на экспресс-вкладке **Условия** выберите **Добавить строку** для ввода значений условий для следующего:</span><span class="sxs-lookup"><span data-stu-id="54e4c-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="54e4c-116">**Процент поставленных единиц**: введите процент выполнения для условия.</span><span class="sxs-lookup"><span data-stu-id="54e4c-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="54e4c-117">Суммы автоматически сохраняются в счетах поставщиков до тех пор, пока стадия завершения проекта не достигнет указанного значения в процентах.</span><span class="sxs-lookup"><span data-stu-id="54e4c-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="54e4c-118">Например, если вы введете 50,00, суммы будут удерживаться до тех пор, пока проект не будет завершен на 50 процентов.</span><span class="sxs-lookup"><span data-stu-id="54e4c-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="54e4c-119">**Удерживаемый процент**: введите процент удерживаемой суммы счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="54e4c-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="54e4c-120">Например, если вы введете 10,00, то 10 процентов суммы из счета поставщика будет удерживаться до тех пор, пока проект не достигнет процента завершения, установленного в поле **Процент поставленных единиц**.</span><span class="sxs-lookup"><span data-stu-id="54e4c-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="54e4c-121">**Освобождаемый процент**: выберите **Добавить строку** для ввода процентной доли любых ранее удерживаемых сумм, подлежащих деблокированию для выбранного уровня завершения проекта.</span><span class="sxs-lookup"><span data-stu-id="54e4c-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="54e4c-122">Если у вас есть более одной вехи для разных уровней завершения проекта, введите отдельную строку условий удержания выплат поставщику для каждого правила удержания.</span><span class="sxs-lookup"><span data-stu-id="54e4c-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="54e4c-123">В каждой строке можно указать разный процент удержания и разный процент выпуска для каждого назначенного уровня завершения проекта.</span><span class="sxs-lookup"><span data-stu-id="54e4c-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="54e4c-124">После создания условий удержания для поставщика вы можете применить эти условия к проекту.</span><span class="sxs-lookup"><span data-stu-id="54e4c-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="54e4c-125">Применение условий удержания поставщика к проекту</span><span class="sxs-lookup"><span data-stu-id="54e4c-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="54e4c-126">Перейдите в раздел **Управление и учет по проектам** > **Проекты** > **Все проекты** и откройте проект со страницы списка проектов.</span><span class="sxs-lookup"><span data-stu-id="54e4c-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="54e4c-127">На экспресс-вкладке **Договора с поставщиками**, выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="54e4c-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="54e4c-128">В поле **Код счета** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="54e4c-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="54e4c-129">**Таблица**: условия удержания платежей поставщику распространяются на одного поставщика.</span><span class="sxs-lookup"><span data-stu-id="54e4c-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="54e4c-130">**Группа**: условия удержания платежей поставщику распространяются на всех поставщиков в группе поставщиков.</span><span class="sxs-lookup"><span data-stu-id="54e4c-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="54e4c-131">**Все**: условия удержания платежей поставщику распространяются на всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="54e4c-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="54e4c-132">В поле **Поставщик/группа поставщиков** выберите поставщика или группу поставщиков, к которым применяются условия удержания платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="54e4c-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="54e4c-133">Если вы выбрали **Все** на предыдущем шаге, это поле недоступно.</span><span class="sxs-lookup"><span data-stu-id="54e4c-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="54e4c-134">В поле **Условия удержания поставщика** выберите условия удержания, которые вы создали в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="54e4c-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="54e4c-135">Если в проекте также установлены условия оплаты после оплаты клиентом (PWP) для поставщика, введите пороговый процент для проекта в поле **Процент порогового уровня КПП**.</span><span class="sxs-lookup"><span data-stu-id="54e4c-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="54e4c-136">Условия удержания платежей поставщикам также отображаются в заказах на покупку, которые вы создаете для поставщика.</span><span class="sxs-lookup"><span data-stu-id="54e4c-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]