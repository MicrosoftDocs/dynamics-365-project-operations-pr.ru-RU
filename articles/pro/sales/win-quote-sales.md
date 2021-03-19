---
title: Закрытие предложения с расценками — облегченное развертывание
description: Эта тема предоставляет информацию о закрытии предложения с расценками в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272300"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="89847-103">Закрытие предложения с расценками — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="89847-103">Close a quote - lite</span></span>

<span data-ttu-id="89847-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="89847-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="89847-105">Предложение с расценками по проекту может быть закрыто как выигранное или потерянное.</span><span class="sxs-lookup"><span data-stu-id="89847-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="89847-106">Черновик предложения с расценками может быть закрыт, поскольку операции «Активировать» и «Пересмотреть» для предложений с расценками не поддерживаются Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="89847-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="89847-107">Закрытие предложения с расценками как реализованного</span><span class="sxs-lookup"><span data-stu-id="89847-107">Close a quote as Won</span></span>

<span data-ttu-id="89847-108">Когда вы закрываете предложение с расценками по проекту как "Заключенное", устанавливается состояние "Закрыто", а причина состояния - "Заключенное".</span><span class="sxs-lookup"><span data-stu-id="89847-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="89847-109">Закрытие предложения с расценками делает предложение с расценками по проекту доступным только для чтения и создает черновик контракта по проекту, который содержит информацию о предложении с расценками.</span><span class="sxs-lookup"><span data-stu-id="89847-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="89847-110">Поскольку закрытое предложение с расценками не может быть открыто повторно, диалоговое окно подтверждения подтвердит ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="89847-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="89847-111">Если предложение с расценками прикреплено к возможной сделке, любые другие предложения с расценками по проекту по возможной сделке автоматически закрываются как потерянные.</span><span class="sxs-lookup"><span data-stu-id="89847-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="89847-112">Финансовые последствия закрытия предложения с расценками как реализованного</span><span class="sxs-lookup"><span data-stu-id="89847-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="89847-113">Если есть какие-либо фактические данные о затраченном времени на проект, которые все еще прикреплены к черновику предложения с расценками, записывается только стоимость времени или затрат.</span><span class="sxs-lookup"><span data-stu-id="89847-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="89847-114">После того, как предложение с расценками будет закрыто как выигранное, приложение произведет рефакторинг затрат, обратив старые фактические затраты и воссоздав новые фактические затраты.</span><span class="sxs-lookup"><span data-stu-id="89847-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="89847-115">Приложение будет обрабатывать эти фактические затраты на основе метода выставления счетов для соответствующей строки контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="89847-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="89847-116">Если фактические затраты ссылаются на строку контракта по времени и материалам, соответствующие фактические данные продаж без выставленного счета, создаются на тот момент, когда предложение с расценками закрывается и создается контракт по проекту.</span><span class="sxs-lookup"><span data-stu-id="89847-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="89847-117">Если фактические затраты ссылаются на строку контракта с фиксированной ценой, приложение прекратит повторную обработку фактических затрат, основанных на правилах выставления счетов с разбиением для заказчиков контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="89847-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="89847-118">Закрытие предложения с расценками как потерянного:</span><span class="sxs-lookup"><span data-stu-id="89847-118">Closing a quote as lost:</span></span>

<span data-ttu-id="89847-119">Когда вы закрываете предложение с расценками по проекту как "Потеряно", устанавливается состояние "Закрыто", а причина состояния — "Потеряно".</span><span class="sxs-lookup"><span data-stu-id="89847-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="89847-120">Закрытие предложения с расценками делает предложение с расценками по проекту доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89847-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="89847-121">Поскольку закрытое предложение с расценками не может быть повторно открыто, перед закрытием предложения с расценками диалоговое окно подтверждения подтвердит ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="89847-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="89847-122">Если предложение с расценками по проекту, закрытое как "Потеряно", ссылается на проект в любой из его строк, этот проект также отмечается как "Закрытый".</span><span class="sxs-lookup"><span data-stu-id="89847-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="89847-123">Любые резервирования ресурсов с этого дня отменяются.</span><span class="sxs-lookup"><span data-stu-id="89847-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="89847-124">В Project Operations закрытие предложения с расценками как выигранного или потерянного не повлияет на статус возможной сделки, которая будет оставаться открытой до тех пор, пока не будет закрыта вручную.</span><span class="sxs-lookup"><span data-stu-id="89847-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]