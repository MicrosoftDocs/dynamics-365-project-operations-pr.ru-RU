---
title: Календарь записи времени
description: В этом разделе представлена информация о том, как использовать календарь записи времени.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cc78d9ae-9f1b-4bd4-8cdf-41406f859ff7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ea8c5113b9ba89e2255218e6a53f062c25badc98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754997"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="f689a-103">Календарь записи времени</span><span class="sxs-lookup"><span data-stu-id="f689a-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f689a-104">На странице **Записи времени** можно просмотреть записи времени в календаре, выбрав **Показать как** \> **Элемент управления календарем**.</span><span class="sxs-lookup"><span data-stu-id="f689a-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="f689a-105">Обновленный элемент управления календарем</span><span class="sxs-lookup"><span data-stu-id="f689a-105">Updated calendar control</span></span>

<span data-ttu-id="f689a-106">Dynamics 365 Project Service Automation предлагает новые и расширяемое взаимодействие записи времени.</span><span class="sxs-lookup"><span data-stu-id="f689a-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="f689a-107">Это новое взаимодействие заменяет настраиваемый элемент управления календаря, который использовался с более ранними версиями.</span><span class="sxs-lookup"><span data-stu-id="f689a-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="f689a-108">Однако можно и дальше просматривать записи времени с помощью доступного только для чтения элемента управления календаря, который платформа единого интерфейса предоставляет для ежедневного, еженедельного или ежемесячного представления.</span><span class="sxs-lookup"><span data-stu-id="f689a-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="f689a-109">Календарь не поддерживает действия с отдельными элементами календаря, и невозможно выбрать один или несколько элементов календаря для отправки или удаления.</span><span class="sxs-lookup"><span data-stu-id="f689a-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="f689a-110">Вместо этого выберите элемент календаря, чтобы открыть страницу сущности **Запись времени**, в которой можно выполнить необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="f689a-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="f689a-111">Расширяемость</span><span class="sxs-lookup"><span data-stu-id="f689a-111">Extensibility</span></span>

<span data-ttu-id="f689a-112">На странице **Записи времени**, которая имеет сетку записей времени, можно добавить настраиваемые поля, настроить поля подстановки, а также создать пользовательские представления.</span><span class="sxs-lookup"><span data-stu-id="f689a-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="f689a-113">Можно также настроить настраиваемую бизнес-логику, основанную на значениях, которые выбираются и вводятся в настраиваемых полях.</span><span class="sxs-lookup"><span data-stu-id="f689a-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>