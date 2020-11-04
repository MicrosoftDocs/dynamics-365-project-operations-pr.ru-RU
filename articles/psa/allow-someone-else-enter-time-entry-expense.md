---
title: Разрешение другим пользователям вводить данные о ваших затратах времени или расходах
description: Как разрешить другим пользователям вводить запись времени или расход в Project Service
author: revathiMuthiah
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 7/31/2018
ms.topic: article
ms.author: revathim
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f56fae115b383d66a59cbcb08fffe95c83c83e17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083161"
---
# <a name="allow-someone-else-to-enter-your-time-entry-or-expense-project-service"></a><span data-ttu-id="af685-103">Разрешение другим пользователям вводить запись времени или расход (Project Service)</span><span class="sxs-lookup"><span data-stu-id="af685-103">Allow someone else to enter your time entry or expense (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="af685-104">Настройте делегата, чтобы позволить другому пользователю вводить записи времени или расхода от вашего имени в [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="af685-104">Set up a delegate to let someone else make time or expense entries on your behalf in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  
  
## <a name="create-a-delegate"></a><span data-ttu-id="af685-105">Создание делегата</span><span class="sxs-lookup"><span data-stu-id="af685-105">Create a delegate</span></span>  
  
1.  <span data-ttu-id="af685-106">В основном меню щелкните **Project Service** > **Делегирования**.</span><span class="sxs-lookup"><span data-stu-id="af685-106">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="af685-107">На панели команд щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="af685-107">On the command bar, click **New**.</span></span>  
  
3. <span data-ttu-id="af685-108">**Имя** : введите имя записи.</span><span class="sxs-lookup"><span data-stu-id="af685-108">**Name** : Enter a name for the record.</span></span>  
  
4. <span data-ttu-id="af685-109">**Тип** : выберите, может ли делегат вводить записи времени или расхода от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="af685-109">**Type** : Select whether the delegate can enter time or expense entries on your behalf.</span></span>  
  
5. <span data-ttu-id="af685-110">**Делегат** : выберите имя пользователя, который будет вашим делегатом.</span><span class="sxs-lookup"><span data-stu-id="af685-110">**Delegate** : Select the name of the person you want to be the delegate.</span></span>  
  
6. <span data-ttu-id="af685-111">**Даты начала и окончания** : выберите даты начала и окончания делегирования.</span><span class="sxs-lookup"><span data-stu-id="af685-111">**Start and end dates** : Choose dates when delegation starts and ends.</span></span>  
  
7.  <span data-ttu-id="af685-112">Закончив, щелкните **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="af685-112">When you're done, click **Save & Close**.</span></span>  
  
## <a name="turn-off-delegation"></a><span data-ttu-id="af685-113">Отключение делегирования</span><span class="sxs-lookup"><span data-stu-id="af685-113">Turn off delegation</span></span>  
  
1.  <span data-ttu-id="af685-114">В основном меню щелкните **Project Service** > **Делегирования**.</span><span class="sxs-lookup"><span data-stu-id="af685-114">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="af685-115">Выберите запись делегирования, которую требуется отключить.</span><span class="sxs-lookup"><span data-stu-id="af685-115">Select the delegation record you want to turn off.</span></span>  
  
3.  <span data-ttu-id="af685-116">В командной строке щелкните **Деактивировать**.</span><span class="sxs-lookup"><span data-stu-id="af685-116">On the command bar, click **Deactivate**.</span></span>  
  
4.  <span data-ttu-id="af685-117">В диалоговом окне **Подтвердить деактивацию** щелкните **Деактивировать**.</span><span class="sxs-lookup"><span data-stu-id="af685-117">On the **Confirm Deactivation** dialog box, click **Deactivate**.</span></span>  
  
## <a name="enter-time-for-someone-else"></a><span data-ttu-id="af685-118">Ввод времени для другого пользователя</span><span class="sxs-lookup"><span data-stu-id="af685-118">Enter time for someone else</span></span>  
  
1.  <span data-ttu-id="af685-119">В основном меню щелкните **Project Service** > **Записи времени**.</span><span class="sxs-lookup"><span data-stu-id="af685-119">From the main menu, click **Project Service** > **Time Entries**.</span></span>  
  
2.  <span data-ttu-id="af685-120">В командной строке выберите раскрывающееся меню **ИМЯ РЕСУРСА** и выберите имя пользователя, для которого требуется ввести время.</span><span class="sxs-lookup"><span data-stu-id="af685-120">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering time for.</span></span>  
  
3.  <span data-ttu-id="af685-121">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="af685-121">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="af685-122">Откроется календарь.</span><span class="sxs-lookup"><span data-stu-id="af685-122">This brings up the calendar.</span></span> <span data-ttu-id="af685-123">Для просмотра предыдущей или следующей недели в календаре щелкните **Назад** или **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af685-123">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="af685-124">Щелкните **Сегодня** , чтобы вернуться к текущей неделе.</span><span class="sxs-lookup"><span data-stu-id="af685-124">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="af685-125">Чтобы ввести время, щелкните **Создать** или дважды щелкните в календаре под днем, для которого требуется ввести время.</span><span class="sxs-lookup"><span data-stu-id="af685-125">To enter your time, either click **New** or double-click in the calendar under the day you want to enter time for.</span></span>  
  
6.  <span data-ttu-id="af685-126">Заполните поля в форме **Запись времени** и щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="af685-126">Fill in the fields in the **Time Entry** form and click **Save**.</span></span>  
  
7.  <span data-ttu-id="af685-127">Продолжите ввод времени для недели.</span><span class="sxs-lookup"><span data-stu-id="af685-127">Continue entering time for the week.</span></span> <span data-ttu-id="af685-128">Завершив настройку и проверив правильность всего, щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="af685-128">When you’re done and everything looks correct, click **Submit**.</span></span>  
  
## <a name="enter-expenses-for-someone-else"></a><span data-ttu-id="af685-129">Ввод расходов для другого пользователя</span><span class="sxs-lookup"><span data-stu-id="af685-129">Enter expenses for someone else</span></span>  
  
1.  <span data-ttu-id="af685-130">В основном меню щелкните **Project Service** > **Расходы**.</span><span class="sxs-lookup"><span data-stu-id="af685-130">From the main menu, click **Project Service** > **Expenses**.</span></span>  
  
2.  <span data-ttu-id="af685-131">В командной строке выберите раскрывающееся меню **ИМЯ РЕСУРСА** выберите имя пользователя, для которого требуется ввести расходы.</span><span class="sxs-lookup"><span data-stu-id="af685-131">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering expenses for.</span></span>  
  
3.  <span data-ttu-id="af685-132">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="af685-132">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="af685-133">Для просмотра предыдущей или следующей недели в календаре щелкните **Назад** или **Далее**.</span><span class="sxs-lookup"><span data-stu-id="af685-133">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="af685-134">Щелкните **Сегодня** , чтобы вернуться к текущей неделе.</span><span class="sxs-lookup"><span data-stu-id="af685-134">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="af685-135">Чтобы ввести расход, щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="af685-135">To enter an expense, either click **New**</span></span>  
  
6.  <span data-ttu-id="af685-136">Заполните поля в форме **Новые расходы**.</span><span class="sxs-lookup"><span data-stu-id="af685-136">Fill in the fields in the **New Expense** form.</span></span> <span data-ttu-id="af685-137">Можно также добавлять чеки.</span><span class="sxs-lookup"><span data-stu-id="af685-137">You can also add receipts.</span></span>  
  
7.  <span data-ttu-id="af685-138">По завершении нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="af685-138">When you’re done, click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="af685-139">См. также</span><span class="sxs-lookup"><span data-stu-id="af685-139">See Also</span></span>  
 [<span data-ttu-id="af685-140">Руководство по совместной работе и вводу данных о времени и расходах</span><span class="sxs-lookup"><span data-stu-id="af685-140">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
