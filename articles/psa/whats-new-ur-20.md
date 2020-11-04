---
title: Что нового и что изменилось в выпуске-обновлении 20 для Project Service Automation версии 3
description: В этом разделе перечислены функции и исправления, доступные в выпуске-обновлении 20 для Project Service Automation версии 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083137"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="1743c-103">Выпуск-обновление 20 Project Service Automation, версия 3</span><span class="sxs-lookup"><span data-stu-id="1743c-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="1743c-104">Мы рады объявить о последнем обновлении приложения Project Service Automation для Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1743c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1743c-105">Этот выпуск содержит некоторые важные усовершенствования, направленные на качество, производительность и удобство использования.</span><span class="sxs-lookup"><span data-stu-id="1743c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1743c-106">Этот выпуск совместим с Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1743c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1743c-107">Чтобы обновить приложение до этого выпуска, посетите страницу решений Центра администрирования Dynamics 365 Online и установите обновление.</span><span class="sxs-lookup"><span data-stu-id="1743c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1743c-108">Дополнительные сведения см. в разделе [Установка, обновление или удаление предпочтительного решения](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1743c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1743c-109">В этом разделе перечислены функции и исправления, появившиеся или изменившиеся в выпуске-обновлении 20 для Project Service Automation версии 3.</span><span class="sxs-lookup"><span data-stu-id="1743c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="1743c-110">Эта версия имеет номер сборки V3.10.31.37 и стала доступна для широкой публики после автоматического обновления в июне 2020 г.</span><span class="sxs-lookup"><span data-stu-id="1743c-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="1743c-111">Выпуск-обновление 20</span><span class="sxs-lookup"><span data-stu-id="1743c-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1743c-112">Исправленные ошибки</span><span class="sxs-lookup"><span data-stu-id="1743c-112">Bug fixes</span></span>

<span data-ttu-id="1743c-113">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="1743c-113">**Project Management**</span></span>

<span data-ttu-id="1743c-114">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="1743c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1743c-115">Импорт членов команды проекта с методом распределения, который требует часов, вызывает непонятное сообщение об ошибке, когда указанные часы равны нулю.</span><span class="sxs-lookup"><span data-stu-id="1743c-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="1743c-116">Пользователи получают неверную ошибку, когда в поле **Описание** для задачи проекта введено максимальное количество символов.</span><span class="sxs-lookup"><span data-stu-id="1743c-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="1743c-117">Страница **Загрузка надстройки Microsoft Dynamics 365 Project Service Automation** перенаправляет на страницу загрузки на английском языке, когда языковые настройки пользователя установлены на японский.</span><span class="sxs-lookup"><span data-stu-id="1743c-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="1743c-118">При возникновении ошибки сервера метка синхронизации на вкладке **Расписание** формы **Проекты** иногда остается.</span><span class="sxs-lookup"><span data-stu-id="1743c-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="1743c-119">Избыточные обновления задач отправляются на сервер при изменении задачи.</span><span class="sxs-lookup"><span data-stu-id="1743c-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="1743c-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1743c-120">**Sales**</span></span>

<span data-ttu-id="1743c-121">Следующие проблемы были исправлены:</span><span class="sxs-lookup"><span data-stu-id="1743c-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="1743c-122">В форме **Контракт** двойной щелчок **Создать накладные** создает две накладные для одной фактической записи.</span><span class="sxs-lookup"><span data-stu-id="1743c-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="1743c-123">В Internet Explorer 11 пользователи не могут создавать записи расходов.</span><span class="sxs-lookup"><span data-stu-id="1743c-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="1743c-124">Отмена затрат и отмена фактических продаж без счета не связаны.</span><span class="sxs-lookup"><span data-stu-id="1743c-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="1743c-125">Кнопка **Обновить фактические показатели** в форме **Проект** не обновляет **Фактические часы по задаче**.</span><span class="sxs-lookup"><span data-stu-id="1743c-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="1743c-126">Подключаемый модуль **PreValidateProjectTeamMemberCreate** может создавать дубликаты общих резервируемых ресурсов, когда атрибут **msdyn_isgenericresourceprojectscoped** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="1743c-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="1743c-127">**Пересчитать** очищает подлежащие оплате затраты в сведениях строки предложения с расценками на основе продуктов и в сведениях по строке контракта.</span><span class="sxs-lookup"><span data-stu-id="1743c-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="1743c-128">В некоторых сценариях подключаемый модуль **PostEstimateLineUpdate** отображает ошибку пустой ссылки.</span><span class="sxs-lookup"><span data-stu-id="1743c-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="1743c-129">Продолжительность фазы времени на диаграмме **Анализ рентабельности** не соответствует длительности затрат в строке предложения с фиксированной ценой.</span><span class="sxs-lookup"><span data-stu-id="1743c-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="1743c-130">Значения единиц и групп единиц измерения по умолчанию неверны для категорий расходов в формах **Сведения строки контракта** и **Сведения строки предложения с расценками**.</span><span class="sxs-lookup"><span data-stu-id="1743c-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="1743c-131">Списки **Себестоимость подразделения** допускают частичное совпадение даты вступления в силу.</span><span class="sxs-lookup"><span data-stu-id="1743c-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="1743c-132">Пользователям не разрешено изменять **Подразделение** , если тип заказа не основан на работе, так как это приведет к ошибке пустой ссылки.</span><span class="sxs-lookup"><span data-stu-id="1743c-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="1743c-133">При попытке перейти из формы **Сведения строки предложения с расценками** на вкладку **Предложение с расценками** форма обновляется и открывается вкладка **Сводка**.</span><span class="sxs-lookup"><span data-stu-id="1743c-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
