---
title: Что нового и что изменилось в Project Service Automation версии 3.x, волна 1, 2020 г.
description: В этом разделе приведены сведения о новых возможностях и изменениях в Project Service Automation версии 3, волна 1, 2020 г.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2308f83e09c25059b6a36599b04b5b00f66c704f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126499"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="622c1-103">Что нового и что изменилось в Project Service Automation версии 3, волна 1, 2020 г.</span><span class="sxs-lookup"><span data-stu-id="622c1-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="622c1-104">В этом разделе перечислены основные моменты, которые следует учитывать при переходе на последний выпуск Project Service Automation (PSA) версии 3.x, волна 1, 2020 г.</span><span class="sxs-lookup"><span data-stu-id="622c1-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="622c1-105">Запись времени</span><span class="sxs-lookup"><span data-stu-id="622c1-105">Time entry</span></span>
<span data-ttu-id="622c1-106">Интерфейс записи времени расширен и теперь предусматривает возможности для записи времени в дополнительных сценариях, возможных на предприятиях клиентов.</span><span class="sxs-lookup"><span data-stu-id="622c1-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="622c1-107">В частности, это возможность добавления типов записи, которые теперь обуславливают определенное поведение в зависимости от имени схемы **Параметры записи времени** (в интерфейсе отображается как **Источник времени**).</span><span class="sxs-lookup"><span data-stu-id="622c1-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="622c1-108">Для поддержки этой функции было добавлено новое решение под названием "Time, Expense, Statusing, and Approvals (TESA)".</span><span class="sxs-lookup"><span data-stu-id="622c1-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="622c1-109">Моменты, которые следует учитывать при обновлении</span><span class="sxs-lookup"><span data-stu-id="622c1-109">Upgrade consideration</span></span>
<span data-ttu-id="622c1-110">Для поддержки этой функциональности роли в PSA обновлены и теперь включают в себя новые привилегии.</span><span class="sxs-lookup"><span data-stu-id="622c1-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="622c1-111">Эти привилегии предоставляют доступ на чтение к новой сущности **Параметры записи времени**.</span><span class="sxs-lookup"><span data-stu-id="622c1-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="622c1-112">Пользователям, которым требуется возможность регистрировать время, должна в дополнение к существующим ролям быть предоставлена роль пользователя **Пользователь записи времени**.</span><span class="sxs-lookup"><span data-stu-id="622c1-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="622c1-113">Эта роль включает в себя новую функциональность и гарантирует, что запись времени продолжит работать.</span><span class="sxs-lookup"><span data-stu-id="622c1-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="622c1-114">Кроме того, если у вас есть какие-либо пользовательские модули приложения, которые включают все формы для сущности ввода времени, вам потребуется удалить из модуля **Форму быстрого создания записи времени TESA**.</span><span class="sxs-lookup"><span data-stu-id="622c1-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="622c1-115">Изменения, связанные с существующими расширениями записи времени</span><span class="sxs-lookup"><span data-stu-id="622c1-115">Currently extended time entry changes</span></span>
<span data-ttu-id="622c1-116">Чтобы свести к минимуму влияние на пользователей записи времени, это изменение в ролях — единственное базовое требование, которое необходимо выполнить для продолжения использования записи времени.</span><span class="sxs-lookup"><span data-stu-id="622c1-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="622c1-117">Если вы создали пользовательские представления или отдельные интерфейсы для записи времени, необходимо задать в полях **Параметр записи времени** соответствующее значение PSA.</span><span class="sxs-lookup"><span data-stu-id="622c1-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
