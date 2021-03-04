---
title: Обновление атрибутов подключаемых модулей для включения новых измерений ценообразования
description: В этом разделе представлена информация об обновлении атрибутов подключаемого модуля для измерений цены.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147084"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="58f61-103">Обновление атрибутов подключаемых модулей для включения новых измерений ценообразования</span><span class="sxs-lookup"><span data-stu-id="58f61-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="58f61-104">Если вы не используете функции предложений с расценками и заключения контрактов Project Service Automation (PSA), можно пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="58f61-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="58f61-105">Данный раздел предполагает, что пользователь завершил процедуры из разделов [Создание настраиваемых полей и сущностей](create-custom-fields-entities.md), [Добавление настраиваемых полей к настройке цены и транзакционным сущностям](field-references.md), и [Настройка настраиваемых полей в качестве измерений цен](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="58f61-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="58f61-106">Если вы еще не завершили эти процедуры, вернитесь и выполните их, а затем вернитесь к этому разделу.</span><span class="sxs-lookup"><span data-stu-id="58f61-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="58f61-107">Когда сведения о строке предложения с расценками создаются на странице **Строка предложения с расценками** для строки предложения с расценками проекта, система создает две строки оценки в фоновом режиме — одна строка для части стороны стоимости и одна для стороны продаж.</span><span class="sxs-lookup"><span data-stu-id="58f61-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="58f61-108">То же самое для строк контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="58f61-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="58f61-109">Когда вы вносите изменение в количество или поле на стороне стоимости, это изменение распространяется на сторону продаж.</span><span class="sxs-lookup"><span data-stu-id="58f61-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="58f61-110">Это возможно из-за следующих подключаемых модулей, которые должны быть перерегистрированы после изменения измерений цен.</span><span class="sxs-lookup"><span data-stu-id="58f61-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="58f61-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="58f61-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="58f61-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="58f61-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="58f61-113">Следующие шаги проведут вас через процесс регистрации подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="58f61-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="58f61-114">Откройте **PluginRegistrationTool** и подключитесь к вашему экземпляру в сети.</span><span class="sxs-lookup"><span data-stu-id="58f61-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="58f61-115">Нажмите **Поиск** и выполните поиск подключаемого модуля для обновления.</span><span class="sxs-lookup"><span data-stu-id="58f61-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Снимок экрана дерева поиска](media/PRT-1.png)

3. <span data-ttu-id="58f61-117">После того как найден подключаемый модуль, выберите его и затем нажмите **Выбрать в основной форме**.</span><span class="sxs-lookup"><span data-stu-id="58f61-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="58f61-118">Выберите шаг подключаемого модуля для обновления, щелкните правой кнопкой мыши, затем выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="58f61-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Снимок экрана подключаемого модуля, подлежащего обновлению](media/PRT-2.png)
 
5. <span data-ttu-id="58f61-120">В окне обновления щелкните многоточие (**...**) в атрибутах фильтрации.</span><span class="sxs-lookup"><span data-stu-id="58f61-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Снимок экрана сведений о конфигурации обновления существующего шага](media/PRT-3.png)
 
6. <span data-ttu-id="58f61-122">Установите флажки атрибута цены.</span><span class="sxs-lookup"><span data-stu-id="58f61-122">Select the pricing attribute check boxes.</span></span>

 ![Снимок экрана, показывающий выбор флажков для атрибутов цены](media/PRT-4.png)

7. <span data-ttu-id="58f61-124">Нажмите **ОК**, чтобы закрыть страницу, затем выберите **Обновить шаг**.</span><span class="sxs-lookup"><span data-stu-id="58f61-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Снимок экрана с кнопкой «Обновить шаг»](media/PRT-5.png)
 
8. <span data-ttu-id="58f61-126">Повторяйте эти действия для второго подключаемого модуля, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="58f61-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="58f61-127">Закройте инструмент регистрации подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="58f61-127">Close the plug-in registration tool.</span></span>

