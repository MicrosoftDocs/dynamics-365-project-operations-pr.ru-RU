---
title: Обновление атрибутов подключаемых модулей для включения новых измерений ценообразования
description: В этом разделе представлена информация об обновлении атрибутов подключаемого модуля для измерений цены.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754993"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="27a01-103">Обновление атрибутов подключаемых модулей для включения новых измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="27a01-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="27a01-104">Если вы не используете функции предложений с расценками и заключения контрактов Project Service Automation (PSA), можно пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="27a01-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="27a01-105">Данный раздел предполагает, что пользователь завершил процедуры из разделов [Создание настраиваемых полей и сущностей](create-custom-fields-entities.md), [Добавление настраиваемых полей к настройке цены и транзакционным сущностям](field-references.md), и [Настройка настраиваемых полей в качестве измерений цен](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="27a01-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="27a01-106">Если вы еще не завершили эти процедуры, вернитесь и выполните их, а затем вернитесь к этому разделу.</span><span class="sxs-lookup"><span data-stu-id="27a01-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="27a01-107">Когда сведения о строке предложения с расценками создаются на странице **Строка предложения с расценками** для строки предложения с расценками проекта, система создает две строки оценки в фоновом режиме — одна строка для части стороны стоимости и одна для стороны продаж.</span><span class="sxs-lookup"><span data-stu-id="27a01-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="27a01-108">То же самое для строк контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="27a01-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="27a01-109">Когда вы вносите изменение в количество или поле на стороне стоимости, это изменение распространяется на сторону продаж.</span><span class="sxs-lookup"><span data-stu-id="27a01-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="27a01-110">Это возможно из-за следующих подключаемых модулей, которые должны быть перерегистрированы после изменения измерений цен.</span><span class="sxs-lookup"><span data-stu-id="27a01-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="27a01-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="27a01-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="27a01-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="27a01-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="27a01-113">Следующие шаги проведут вас через процесс регистрации подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="27a01-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="27a01-114">Откройте **PluginRegistrationTool** и подключитесь к вашему экземпляру в сети.</span><span class="sxs-lookup"><span data-stu-id="27a01-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="27a01-115">Нажмите **Поиск** и выполните поиск подключаемого модуля для обновления.</span><span class="sxs-lookup"><span data-stu-id="27a01-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Снимок экрана дерева поиска](media/PRT-1.png)

3. <span data-ttu-id="27a01-117">После того как найден подключаемый модуль, выберите его и затем нажмите **Выбрать в основной форме**.</span><span class="sxs-lookup"><span data-stu-id="27a01-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="27a01-118">Выберите шаг подключаемого модуля для обновления, щелкните правой кнопкой мыши, затем выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="27a01-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Снимок экрана подключаемого модуля, подлежащего обновлению](media/PRT-2.png)
 
5. <span data-ttu-id="27a01-120">В окне обновления щелкните многоточие (**...**) в атрибутах фильтрации.</span><span class="sxs-lookup"><span data-stu-id="27a01-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Снимок экрана сведений о конфигурации обновления существующего шага](media/PRT-3.png)
 
6. <span data-ttu-id="27a01-122">Установите флажки атрибута цены.</span><span class="sxs-lookup"><span data-stu-id="27a01-122">Select the pricing attribute check boxes.</span></span>

 ![Снимок экрана, показывающий выбор флажков для атрибутов цены](media/PRT-4.png)

7. <span data-ttu-id="27a01-124">Нажмите **ОК**, чтобы закрыть страницу, затем выберите **Обновить шаг**.</span><span class="sxs-lookup"><span data-stu-id="27a01-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Снимок экрана с кнопкой «Обновить шаг»](media/PRT-5.png)
 
8. <span data-ttu-id="27a01-126">Повторяйте эти действия для второго подключаемого модуля, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="27a01-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="27a01-127">Закройте инструмент регистрации подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="27a01-127">Close the plug-in registration tool.</span></span>
