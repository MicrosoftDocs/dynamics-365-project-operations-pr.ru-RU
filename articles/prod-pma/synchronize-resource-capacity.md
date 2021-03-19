---
title: Синхронизация емкости ресурсов
description: Эта тема предоставляет информацию о том, как синхронизировать емкость ресурса в календарях и проектах.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288587"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="ae3e6-103">Синхронизация емкости ресурсов</span><span class="sxs-lookup"><span data-stu-id="ae3e6-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae3e6-104">Процессы синхронизации ресурсов помогают гарантировать, что информация для календаря и базового календаря попадет в планирование ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="ae3e6-105">Если календарь изменяется, процессы вносят необходимые обновления в планирование ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="ae3e6-106">Эти процессы также помогают повысить производительность, поскольку информация о ресурсах календаря заранее синхронизируется.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="ae3e6-107">Следовательно, обновления информации о планировании ресурсов происходят быстрее.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="ae3e6-108">Мы рекомендуем вам планировать процессы как пакет, а не по одному.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="ae3e6-109">В противном случае есть риск, что кто-то забудет инклюзивные даты при последней синхронизации информации.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="ae3e6-110">Если инклюзивные даты не используются, во время синхронизации дат могут возникать пропуски.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Синхронизация календаря](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="ae3e6-112">Синхронизация операций сведения загрузки ресурсов</span><span class="sxs-lookup"><span data-stu-id="ae3e6-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="ae3e6-113">Процесс синхронизации предназначен для синхронизации всей информации календаря ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="ae3e6-114">Эта информация включает базовую календарную информацию обо всех изменениях в таблице загрузки календаря ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="ae3e6-115">Если в проект добавляются новые ресурсы, синхронизация помогает гарантировать доступность обновленной информации календаря.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="ae3e6-116">Эту синхронизацию можно выполнить в любое время.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="ae3e6-117">Рекомендуется использовать пакеты.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-117">We recommend that you use a batch.</span></span> <span data-ttu-id="ae3e6-118">Параметры доступны во время синхронизации зарезервированных мощностей.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="ae3e6-119">Выберите **Управление проектами и учет** &gt; **Периодический** &gt; **Синхронизация загрузки** &gt; **Синхронизация операций сведения загрузки ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="ae3e6-120">Задайте параметры в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="ae3e6-121">Вариант</span><span class="sxs-lookup"><span data-stu-id="ae3e6-121">Option</span></span>      | <span data-ttu-id="ae3e6-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ae3e6-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="ae3e6-123">Код периода</span><span class="sxs-lookup"><span data-stu-id="ae3e6-123">Period code</span></span> | <span data-ttu-id="ae3e6-124">При желании выберите код интервала дат Главной книги, чтобы установить даты начала и окончания для процесса синхронизации для операций сведения загрузки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ae3e6-125">Дата начала</span><span class="sxs-lookup"><span data-stu-id="ae3e6-125">Start date</span></span>  | <span data-ttu-id="ae3e6-126">Введите дату начала процесса синхронизации для операций сведения загрузки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ae3e6-127">Дата окончания</span><span class="sxs-lookup"><span data-stu-id="ae3e6-127">End date</span></span>    | <span data-ttu-id="ae3e6-128">Введите дату окончания процесса синхронизации для операций сведения загрузки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="ae3e6-129">[![Процесс синхронизации](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="ae3e6-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]