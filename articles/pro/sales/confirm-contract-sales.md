---
title: Подтверждение контракта по проекту
description: В этой теме предоставлена информация о порядке подтверждения контракта в Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003692"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="bb509-103">Подтверждение контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="bb509-103">Confirm a project contract</span></span>

<span data-ttu-id="bb509-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="bb509-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb509-105">Контракт по проекту в Dynamics 365 Project Operations можно активировать с причиной **Подтверждено** или закрыть с причиной **Не реализовано**.</span><span class="sxs-lookup"><span data-stu-id="bb509-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="bb509-106">Когда вы подтверждаете контракт по проекту, статус обновляется с **Черновик** на **Активно**, а причина состояния — **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="bb509-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="bb509-107">Активный или закрытый контракт не может быть отредактирован или повторно открыт.</span><span class="sxs-lookup"><span data-stu-id="bb509-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="bb509-108">Финансовые последствия подтверждения контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="bb509-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="bb509-109">После того, как контракт по проекту подтвержден, приложение заново вычисляет затраты, обратив старые фактические затраты и создав новые фактические затраты.</span><span class="sxs-lookup"><span data-stu-id="bb509-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="bb509-110">Новые фактические затраты затем обрабатываются на основе метода выставления счетов для соответствующей строки контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="bb509-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="bb509-111">Если фактические затраты ссылаются на строку контракта "Время и материалы", приложение автоматически заново создает соответствующие фактические данные продаж, за которые не выставлены счета.</span><span class="sxs-lookup"><span data-stu-id="bb509-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="bb509-112">Если фактические затраты ссылаются на строку контракта с фиксированной ценой, приложение прекращает повторную обработку фактических затрат.</span><span class="sxs-lookup"><span data-stu-id="bb509-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="bb509-113">Пределы, которые запрещается превышать, настройка возможности выставления счетов, а также расценки и затраты по фактическим данным оцениваются и затем обновляются в рамках процесса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bb509-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="bb509-114">Закрытие контракта по проекту как упущенного</span><span class="sxs-lookup"><span data-stu-id="bb509-114">Close a project contract as lost</span></span>

<span data-ttu-id="bb509-115">Когда вы закрываете контракт по проекту как упущенный, статус контракта обновляется на **Закрыто**, а причина состояния — **Упущено**.</span><span class="sxs-lookup"><span data-stu-id="bb509-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="bb509-116">Контракт по проекту становится доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bb509-116">The project contract becomes read-only.</span></span> <span data-ttu-id="bb509-117">Перед тем, как изменения будут внесены, отображается диалоговое окно подтверждения, поскольку вы не можете повторно открыть закрытый контракт по проекту.</span><span class="sxs-lookup"><span data-stu-id="bb509-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="bb509-118">Если контракт по проекту, закрытый как упущенный, ссылается на проект в своих строках, этот проект также помечается как закрытый.</span><span class="sxs-lookup"><span data-stu-id="bb509-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="bb509-119">Любые резервирования ресурсов с этого дня отменяются.</span><span class="sxs-lookup"><span data-stu-id="bb509-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="bb509-120">Любые фактические продажи по контракту по проекту, за которые еще не выставлены счета, но которые уже включены в счет, будут сторнированы.</span><span class="sxs-lookup"><span data-stu-id="bb509-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="bb509-121">В Dynamics 365 Project Operations закрытие контракта по проекту как не реализованного не повлияет на статус связанной возможной сделки.</span><span class="sxs-lookup"><span data-stu-id="bb509-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="bb509-122">Возможная сделка останется открытой и должна быть закрыта вручную.</span><span class="sxs-lookup"><span data-stu-id="bb509-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]