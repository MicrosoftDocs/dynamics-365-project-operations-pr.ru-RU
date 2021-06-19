---
title: Работа с личными расходами в отчете о расходах
description: В этой теме содержится информация о том, как работать с личными расходами, которые несут сотрудники во время деловых поездок.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025700"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="dc227-103">Работа с личными расходами в отчете о расходах</span><span class="sxs-lookup"><span data-stu-id="dc227-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="dc227-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="dc227-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc227-105">Во время деловой поездки сотрудник может списать личные расходы со своей корпоративной кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="dc227-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="dc227-106">Если не определен процесс обработки личных расходов, процесс утверждения отчета о расходах может быть прерван, когда сотрудник отправит свой подробный отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="dc227-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="dc227-107">Есть два метода, которые вы можете использовать для работы с личными расходами сотрудника:</span><span class="sxs-lookup"><span data-stu-id="dc227-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="dc227-108">**Оплачивается сотрудником**: ваша организация не оплачивает личные расходы, указанные в счете по корпоративной кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="dc227-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="dc227-109">Вместо этого сотрудник оплачивает расходы поставщику кредитной карты напрямую.</span><span class="sxs-lookup"><span data-stu-id="dc227-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="dc227-110">**Оплачивает компания**: ваша организация полностью оплачивает счет по корпоративной кредитной карте, а затем дебетует счет сотрудника для покрытия личных расходов.</span><span class="sxs-lookup"><span data-stu-id="dc227-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="dc227-111">Вы можете выбрать метод, который использует ваша организация, на странице **Параметры управления расходами**.</span><span class="sxs-lookup"><span data-stu-id="dc227-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="dc227-112">Включите функцию разделения расходов, если в поле личной суммы задано значение</span><span class="sxs-lookup"><span data-stu-id="dc227-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="dc227-113">Функция **Включите функцию разделения расходов, если в поле личной суммы задано значение** применяется только к отчетам о расходах, утвержденным с использованием рабочего процесса на уровне строк.</span><span class="sxs-lookup"><span data-stu-id="dc227-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="dc227-114">Отчеты утверждаются путем перехода в **Обработать отчеты о расходах** > **Назначенные мне отчеты о расходах** > **Открыть отчет о расходах**.</span><span class="sxs-lookup"><span data-stu-id="dc227-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="dc227-115">Чтобы включить эту функцию, перейдите у **Рабочие области** > **Управление функциями**, выберите **Включите функцию разделения расходов, если в поле личной суммы задано значение**, а затем выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="dc227-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="dc227-116">Когда эта функция включена, строки расходов, использующие эту функцию, при отправке отчета генерируют две строки.</span><span class="sxs-lookup"><span data-stu-id="dc227-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="dc227-117">Создаются две строки, чтобы утверждающий мог утвердить каждую строку отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc227-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
