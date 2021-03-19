---
title: Исключение оценки по проекту
description: Эта тема предоставляет информацию об удалении оценки проекта после его завершения.
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270694"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="75b27-103">Исключение оценки по проекту</span><span class="sxs-lookup"><span data-stu-id="75b27-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75b27-104">Оценки проекта обеспечивают финансовое представление для работы, оцененной и запланированной для проекта.</span><span class="sxs-lookup"><span data-stu-id="75b27-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="75b27-105">Для работы с оценками для проекта необходимо прикрепить проект к проекту оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="75b27-106">Проект оценки всегда основан на существующем проекте, однако несколько проектов могут ссылаться на один проект оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="75b27-107">К проектам оценки можно присоединять только проекты с фиксированной ценой и инвестиционные проекты, и эти проекты должны принадлежать к той же группе проектов, что и проект оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="75b27-108">Чтобы исключить проект оценки, он должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="75b27-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="75b27-109">Следующие шаги объясняют, как удалить оценку.</span><span class="sxs-lookup"><span data-stu-id="75b27-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="75b27-110">Перейдите в раздел **Управление и учет по проектам** > **Все проекты** и откройте проект.</span><span class="sxs-lookup"><span data-stu-id="75b27-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="75b27-111">На вкладке **Управление** выберите **Оценки**, и на странице **Оценка** выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="75b27-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="75b27-112">На странице **Удаление оценки** на вкладке **Общие** установите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="75b27-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="75b27-113">**Код периода**: выберите код периода, чтобы выбрать подходящие проекты оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="75b27-114">**Дата оценки**: выберите подходящую дату оценки для исключения.</span><span class="sxs-lookup"><span data-stu-id="75b27-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="75b27-115">**Удалить с напоминаниями НЗП**: включите этот параметр, чтобы предоставлять уведомление, когда оценка, связанная с незавершенным производством (НЗП), будет удалена.</span><span class="sxs-lookup"><span data-stu-id="75b27-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="75b27-116">Если этот параметр не включен, удаление не может продолжаться, если существуют какие-либо неоцененные транзакции.</span><span class="sxs-lookup"><span data-stu-id="75b27-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="75b27-117">Этот параметр доступен только в том случае, если исключение применяется к проекту оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="75b27-118">Он недоступен, если вы используете периодические проводки.</span><span class="sxs-lookup"><span data-stu-id="75b27-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="75b27-119">Этот параметр работает с настройками на вкладке **Оценка** на странице **Параметры проекта** в группе полей **Разрешить исключение при существовании не входящих в оценку проводок**.</span><span class="sxs-lookup"><span data-stu-id="75b27-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="75b27-120">**Установить статус в "Завершено"**: включите этот параметр, чтобы установить стадию проекта оценки на **Завершено** после запуска исключения.</span><span class="sxs-lookup"><span data-stu-id="75b27-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="75b27-121">**Печать списка оценок**: выберите информацию, которая будет включена при распечатке списка оценок.</span><span class="sxs-lookup"><span data-stu-id="75b27-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="75b27-122">**Отобразить Infolog**: включите этот параметр, чтобы отображать Infolog.</span><span class="sxs-lookup"><span data-stu-id="75b27-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="75b27-123">**Дата разноски**: выберите дату разноски книги учета для оценки.</span><span class="sxs-lookup"><span data-stu-id="75b27-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="75b27-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="75b27-124">Select **OK**.</span></span>
5. <span data-ttu-id="75b27-125">После завершения процесса исключения исключенный проект оценки отображается с отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="75b27-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="75b27-126">Если вы не собирались исключать оценку, вы можете выбрать исключенную оценку и выбрать **Сторнировать исключение**.</span><span class="sxs-lookup"><span data-stu-id="75b27-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]