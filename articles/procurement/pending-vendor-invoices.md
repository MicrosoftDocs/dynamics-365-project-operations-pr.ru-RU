---
title: Покупка нескладируемые материалы с помощью незавершенной накладной поставщика
description: В этой теме объясняется, как записывать незавершенные накладные поставщика.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993825"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="05f2d-103">Покупка нескладируемые материалы с помощью незавершенной накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="05f2d-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="05f2d-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="05f2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="05f2d-105">Поскольку компания закупает нескладируемые материалы для проекта, затраты могут быть немедленно записаны в отношении проекта.</span><span class="sxs-lookup"><span data-stu-id="05f2d-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="05f2d-106">Например, Contoso Robotics US выполняет проект по обновлению оборудования и нуждается в лицензиях на программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="05f2d-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="05f2d-107">Эти лицензии приобретаются у стороннего поставщика.</span><span class="sxs-lookup"><span data-stu-id="05f2d-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="05f2d-108">С использованием Dynamics 365 Finance, специалист по расчетам с поставщиками записывает незавершенную накладную поставщика и относит затраты на лицензию непосредственно к проекту обновления оборудования.</span><span class="sxs-lookup"><span data-stu-id="05f2d-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="05f2d-109">Прежде чем использовать функции, описанные в этой теме, просмотрите и примените необходимые конфигурации.</span><span class="sxs-lookup"><span data-stu-id="05f2d-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="05f2d-110">Дополнительные сведения см. в [Включите нескладируемые материалы и незавершенные накладные поставщика](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="05f2d-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="05f2d-111">Разноска отложенной накладной поставщика, связанного с проектом</span><span class="sxs-lookup"><span data-stu-id="05f2d-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="05f2d-112">Незавершенные накладные поставщика могут быть записаны на страница **Незавершенные накладные поставщика** (**Расчеты с поставщиками** > **Счета** > **Незавершенные накладные поставщика**).</span><span class="sxs-lookup"><span data-stu-id="05f2d-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="05f2d-113">Выполните следующие шаги, чтобы разнести отложенной накладной поставщика, связанного с проектом:</span><span class="sxs-lookup"><span data-stu-id="05f2d-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="05f2d-114">Перейти к **Расчеты с поставщиками** > **Счета** и выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="05f2d-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="05f2d-115">В поле **учетная запись накладной** выберите поставщика и в поле **Число** введите идентификатор накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="05f2d-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="05f2d-116">Добавьте строку в накладную поставщика и в поле **Номер элемента** выберите нескладируемый элемент, приобретенный у поставщика.</span><span class="sxs-lookup"><span data-stu-id="05f2d-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05f2d-117">Строки накладной поставщика, основанные на категории закупаемой продукции, не могут быть записаны в проект.</span><span class="sxs-lookup"><span data-stu-id="05f2d-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="05f2d-118">Добавьте приобретенное количество.</span><span class="sxs-lookup"><span data-stu-id="05f2d-118">Add the quantity purchased.</span></span> <span data-ttu-id="05f2d-119">Система подставит цену за единицу на основе конфигурации цены нескладируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="05f2d-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="05f2d-120">Проверьте общую сумму и другие необходимые данные в строке.</span><span class="sxs-lookup"><span data-stu-id="05f2d-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="05f2d-121">В сведениях о строке , на вкладке **Проект** выберите ИД проекта, в который будет записан этот элемент.</span><span class="sxs-lookup"><span data-stu-id="05f2d-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="05f2d-122">При желании выберите номер операции и обновите категорию проекта и свойство строки.</span><span class="sxs-lookup"><span data-stu-id="05f2d-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="05f2d-123">Разноска незавершенной накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="05f2d-123">Post pending vendor invoice.</span></span> <span data-ttu-id="05f2d-124">При разноске накладной система записывает:</span><span class="sxs-lookup"><span data-stu-id="05f2d-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="05f2d-125">Сумма сальдо поставщика.</span><span class="sxs-lookup"><span data-stu-id="05f2d-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="05f2d-126">Сумма налога.</span><span class="sxs-lookup"><span data-stu-id="05f2d-126">The sales tax amount.</span></span>
    - <span data-ttu-id="05f2d-127">Стоимость проекта записывается на учетная запись интеграции закупок.</span><span class="sxs-lookup"><span data-stu-id="05f2d-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="05f2d-128">Фактическая транзакция по проекту в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="05f2d-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="05f2d-129">Эта транзакция далее обрабатывается с использованием [Журнал интеграции Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="05f2d-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="05f2d-130">При разноске этого журнала сумма перемещается со учетной записи интеграции закупок в учетная запись затрат по проекту.</span><span class="sxs-lookup"><span data-stu-id="05f2d-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
