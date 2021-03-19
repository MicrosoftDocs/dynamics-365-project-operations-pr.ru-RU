---
title: Типы периодов
description: В этом разделе представлена информация о том, как настроить типы периодов для оценки дохода.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287299"
---
# <a name="period-types"></a><span data-ttu-id="748c5-103">Типы периодов</span><span class="sxs-lookup"><span data-stu-id="748c5-103">Period types</span></span>

<span data-ttu-id="748c5-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="748c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="748c5-105">Тип периода определяет, как часто оценивается доход по проекту.</span><span class="sxs-lookup"><span data-stu-id="748c5-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="748c5-106">В этом разделе представлена информация о том, как настроить типы периодов для оценки дохода.</span><span class="sxs-lookup"><span data-stu-id="748c5-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="748c5-107">Создание и работа с типами периодов</span><span class="sxs-lookup"><span data-stu-id="748c5-107">Create and work with period types</span></span>
<span data-ttu-id="748c5-108">Чтобы создать типы периодов и работать с ними, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="748c5-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="748c5-109">В вашей среде Dynamics 365 Finance перейдите в **Управление и учет по проектам** > **Настройка** > **Оценки** > **Типы периодов**.</span><span class="sxs-lookup"><span data-stu-id="748c5-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="748c5-110">Чтобы создать новый тип периода, выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="748c5-110">Select **New** to create new period type.</span></span> <span data-ttu-id="748c5-111">Введите имя и описание.</span><span class="sxs-lookup"><span data-stu-id="748c5-111">Enter a name and description.</span></span>
3. <span data-ttu-id="748c5-112">В поле **Частота** выберите значение:</span><span class="sxs-lookup"><span data-stu-id="748c5-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="748c5-113">Если вы выберете **Неделя**, **Раз в две недели**, **Раз в полмесяца**, **Месяц**, **День**, **Квартал** или **Год**, календарь будет использоваться для создания периодов.</span><span class="sxs-lookup"><span data-stu-id="748c5-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="748c5-114">Если вы выберете **Период книги учета**, периоды книги учета из конфигурации главной книги будут использоваться для создания периодов.</span><span class="sxs-lookup"><span data-stu-id="748c5-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="748c5-115">Если вы выберете **Безлимитный**, вы можете указать собственные периоды.</span><span class="sxs-lookup"><span data-stu-id="748c5-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="748c5-116">Выберите запись типа периода, а затем выберите **Создать периоды** для создания периодов для типа периода.</span><span class="sxs-lookup"><span data-stu-id="748c5-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="748c5-117">В зависимости от выбранной вами частоты периодов у вас может быть возможность указать дату начала или количество периодов для создания.</span><span class="sxs-lookup"><span data-stu-id="748c5-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="748c5-118">Выбрать **Периоды** для просмотра созданных периодов.</span><span class="sxs-lookup"><span data-stu-id="748c5-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]