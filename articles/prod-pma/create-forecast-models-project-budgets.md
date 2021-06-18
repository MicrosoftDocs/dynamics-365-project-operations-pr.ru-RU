---
title: Создание моделей прогнозов для бюджетов проектов
description: В этой теме описывается, как создать модель прогноза для оставшихся бюджетов.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006311"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="8eb61-103">Создание моделей прогнозов для бюджетов проектов</span><span class="sxs-lookup"><span data-stu-id="8eb61-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eb61-104">В этой теме описывается, как создать модель прогноза для оставшихся бюджетов.</span><span class="sxs-lookup"><span data-stu-id="8eb61-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="8eb61-105">В проекте, подлежащем бюджетному контролю, используются два типа бюджетов: исходный и оставшийся.</span><span class="sxs-lookup"><span data-stu-id="8eb61-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="8eb61-106">При создании бюджета проекта необходимо указать модели прогноза исходного и оставшегося бюджета, которые были созданы на странице **Модели прогнозов**.</span><span class="sxs-lookup"><span data-stu-id="8eb61-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="8eb61-107">Бюджеты проекта на основе указанных моделей создаются, когда вы фиксируете бюджет проекта.</span><span class="sxs-lookup"><span data-stu-id="8eb61-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="8eb61-108">Модель прогноза, которая используется для контроля бюджета, не может иметь подмодель или использоваться как подмодель.</span><span class="sxs-lookup"><span data-stu-id="8eb61-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="8eb61-109">Выберите **Управление и учет по проектам** > **Настройка** > **Прогнозы**  > **Модели прогнозов**.</span><span class="sxs-lookup"><span data-stu-id="8eb61-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="8eb61-110">Выберите **Создать**, чтобы создать новую модель прогноза, затем введите идентификационный номер модели и имя для новой модели.</span><span class="sxs-lookup"><span data-stu-id="8eb61-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="8eb61-111">Установите для параметра **Остановлено** значение **Да**, чтобы предотвратить любые изменения строк прогноза для модели прогноза.</span><span class="sxs-lookup"><span data-stu-id="8eb61-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="8eb61-112">Если строки прогноза, с которыми связана модель, должны генерировать прогнозы денежных потоков в главной книге, установите для параметра **Включить в прогнозы движения денежных средств** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="8eb61-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="8eb61-113">Чтобы использовать дату проекта в качестве даты выставления счета, установите для параметра **Дата накладной прогноза** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="8eb61-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="8eb61-114">В поле **Тип бюджета** выберите один из следующих типов модели:</span><span class="sxs-lookup"><span data-stu-id="8eb61-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="8eb61-115">**Исходный бюджет**: используйте исходные суммы бюджета, которые фиксируются при создании и утверждении первоначального бюджета.</span><span class="sxs-lookup"><span data-stu-id="8eb61-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="8eb61-116">**Остаток бюджета**: используйте оставшиеся суммы бюджета в течение срока действия проекта.</span><span class="sxs-lookup"><span data-stu-id="8eb61-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="8eb61-117">Сальдо в этой модели прогноза сокращаются фактическими транзакциями и увеличиваются или уменьшаются при пересмотре бюджета.</span><span class="sxs-lookup"><span data-stu-id="8eb61-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="8eb61-118">**Перенос**: используйте перенесенные суммы бюджета для проекта.</span><span class="sxs-lookup"><span data-stu-id="8eb61-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="8eb61-119">Перенос — это необязательный процесс, который можно запустить для переноса неиспользованных сумм бюджета с одного финансовый год на другой.</span><span class="sxs-lookup"><span data-stu-id="8eb61-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="8eb61-120">Задайте требуемые значения для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="8eb61-120">Set the following options as required:</span></span>

   - <span data-ttu-id="8eb61-121">Включите параметр **Дата накладной прогноза**, чтобы использовать дату проекта в качестве даты выставления счета.</span><span class="sxs-lookup"><span data-stu-id="8eb61-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="8eb61-122">Включите **Прогноз с НЗП** для прогнозирования на основе незавершенной работы (НЗП), затем выберите тип НЗП.</span><span class="sxs-lookup"><span data-stu-id="8eb61-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="8eb61-123">Вы можете оставить значение по умолчанию **Тип бюджета** как **Нет** или ввести новый тип.</span><span class="sxs-lookup"><span data-stu-id="8eb61-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="8eb61-124">Тип бюджета нельзя изменить после изменения записи.</span><span class="sxs-lookup"><span data-stu-id="8eb61-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="8eb61-125">Если вы измените тип бюджета по умолчанию, все остальные параметры станут недоступны для обновлений, и вы не сможете повторно использовать эту модель прогноза.</span><span class="sxs-lookup"><span data-stu-id="8eb61-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]