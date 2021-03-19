---
title: Обновление атрибутов подключаемых модулей новыми измерений цен
description: В этом разделе представлена информация об обновлении атрибутов подключаемого модуля для измерений цены.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274699"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="183b9-103">Обновление атрибутов подключаемых модулей новыми измерений цен</span><span class="sxs-lookup"><span data-stu-id="183b9-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="183b9-104">В этом разделе представлена информация об обновлении атрибутов подключаемого модуля для измерений цены.</span><span class="sxs-lookup"><span data-stu-id="183b9-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="183b9-105">Этот раздел применим только к функциям предложения с расценками и контракта в Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="183b9-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="183b9-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="183b9-106">Prerequisites</span></span>
<span data-ttu-id="183b9-107">Прежде чем выполнять действия из этого раздела, вы должны выполнить процедуры из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="183b9-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="183b9-108">Создание настраиваемых полей и сущностей</span><span class="sxs-lookup"><span data-stu-id="183b9-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="183b9-109">Добавление настраиваемых полей в сущности транзакций и настройки цен</span><span class="sxs-lookup"><span data-stu-id="183b9-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="183b9-110">[Создание настраиваемых полей в качестве измерений цен](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="183b9-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="183b9-111">Если вы еще не завершили эти процедуры, выполните их, а затем вернитесь к этому разделу.</span><span class="sxs-lookup"><span data-stu-id="183b9-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="183b9-112">Регистрация подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="183b9-112">Register a plug-in</span></span>
<span data-ttu-id="183b9-113">Когда сведения строки предложения создаются на страницы **Строка предложения с расценками** для строки предложения с расценками по проекту, система создает две строки оценки.</span><span class="sxs-lookup"><span data-stu-id="183b9-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="183b9-114">Одна строка предназначена для стороны стоимости оценки, а другая — для стороны продаж.</span><span class="sxs-lookup"><span data-stu-id="183b9-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="183b9-115">То же самое для строк контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="183b9-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="183b9-116">Когда вы вносите изменение в количество или поле на стороне стоимости, это изменение также сделано на стороне продаж.</span><span class="sxs-lookup"><span data-stu-id="183b9-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="183b9-117">Это возможно, потому что подключаемые модули PreOperation в сущностях Quotelinedetail и contractline detail соединяют определенные атрибуты на стороне затрат со стороной продажи транзакции.</span><span class="sxs-lookup"><span data-stu-id="183b9-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="183b9-118">Если вам нужно, чтобы изменения, внесенные в значения измерения цен на стороне продаж, также были внесены на стороне стоимости, следующие подключаемые модули должны быть повторно зарегистрированы после внесения изменений в измерение цен.</span><span class="sxs-lookup"><span data-stu-id="183b9-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="183b9-119">Это подключаемые модули для обновления и повторной регистрации:</span><span class="sxs-lookup"><span data-stu-id="183b9-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="183b9-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="183b9-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="183b9-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="183b9-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="183b9-122">Выполните следующие шаги, чтобы обновить и повторно зарегистрировать плагины.</span><span class="sxs-lookup"><span data-stu-id="183b9-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="183b9-123">Откройте **PluginRegistrationTool** и подключитесь к вашей среде Dataverse Project Operations.</span><span class="sxs-lookup"><span data-stu-id="183b9-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="183b9-124">Выбрать **Поиск**, и введите первые несколько букв подключаемого модуля, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="183b9-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="183b9-125">После того как найден подключаемый модуль, выберите его и затем нажмите **Выбрать в основной форме**.</span><span class="sxs-lookup"><span data-stu-id="183b9-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="183b9-126">Выберите шаг **Update msdyn_orderlinetransaction**, щелкните правой кнопкой мыши, затем выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="183b9-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="183b9-127">В диалоговом окне **Обновить** выберите многоточие (**...**) в атрибутах фильтрации.</span><span class="sxs-lookup"><span data-stu-id="183b9-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="183b9-128">Откроется окно атрибутов фильтрации со списком всех атрибутов в сущности и измерений цен.</span><span class="sxs-lookup"><span data-stu-id="183b9-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="183b9-129">Установите флажки для атрибутов измерения цен.</span><span class="sxs-lookup"><span data-stu-id="183b9-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="183b9-130">Нажмите **ОК**, чтобы закрыть страницу, затем выберите **Обновить шаг**.</span><span class="sxs-lookup"><span data-stu-id="183b9-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="183b9-131">Повторите шаги 2-7 для второго подключаемого модуля, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="183b9-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="183b9-132">Для этого подключаемого модуля необходимо обновить шаг **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="183b9-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="183b9-133">Закройте **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="183b9-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]