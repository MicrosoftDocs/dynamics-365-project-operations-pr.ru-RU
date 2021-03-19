---
title: Обзор внутрихолдингового выставления счетов
description: В этом разделе представлена информация и примеры внутрихолдингового выставления счетов для проектов.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287344"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="685c0-103">Обзор внутрихолдингового выставления счетов</span><span class="sxs-lookup"><span data-stu-id="685c0-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="685c0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="685c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="685c0-105">В вашей организации может быть несколько подразделений, дочерних компаний и других юридических лиц, которые передают продукты и услуги друг другу для проектов.</span><span class="sxs-lookup"><span data-stu-id="685c0-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="685c0-106">Юридическое лицо, предоставляющее услугу или продукт, называется *юридическое лицо-кредитор*.</span><span class="sxs-lookup"><span data-stu-id="685c0-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="685c0-107">Юридическое лицо, получающее услугу или продукт, называется *юридическое лицо-заемщик*.</span><span class="sxs-lookup"><span data-stu-id="685c0-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="685c0-108">На следующем рисунке показан типичный сценарий, в котором два юридических лица, Contoso Robotics USA (юридическое лицо-заемщик) и Contoso Robotics UK (юридическое лицо-кредитор) совместно используют ресурсы для реализации проекта для клиента, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="685c0-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="685c0-109">В этом сценарии Contoso Robotics USA заключает контракт на поставку работы для Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="685c0-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Внутрихолдинговое выставление счетов](./media/IntercompanyScenario.png) 

<span data-ttu-id="685c0-111">Dynamics 365 Project Operations использует следующий поток для обработки внутрихолдинговых транзакций:</span><span class="sxs-lookup"><span data-stu-id="685c0-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="685c0-112">Ресурсы юридического лица-кредитора регистрируют внутрихолдинговые транзакции времени или расходов путем резервирования времени и расходов по проектам в юридическом лице-заемщике.</span><span class="sxs-lookup"><span data-stu-id="685c0-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="685c0-113">Затраты времени и расходов учитываются в кредитной компании с использованием прайс-листа стоимости единицы компании-заемщика.</span><span class="sxs-lookup"><span data-stu-id="685c0-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="685c0-114">Внутрихолдинговые транзакции продаж без выставления счета учитываются в кредитной компании с использованием прайс-листа стоимости единицы компании-заемщика.</span><span class="sxs-lookup"><span data-stu-id="685c0-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="685c0-115">Доход без выставления счета отражается в компании-заемщике с использованием прайс-листа продаж контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="685c0-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="685c0-116">Счет покупателю может быть выставлен при регистрации дохода без выставления счета.</span><span class="sxs-lookup"><span data-stu-id="685c0-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="685c0-117">Клиенту не нужно ждать завершения обработки внутрихолдинговых счетов.</span><span class="sxs-lookup"><span data-stu-id="685c0-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="685c0-118">Внутрихолдинговые счета клиентов создаются в кредитной компании на периодической основе.</span><span class="sxs-lookup"><span data-stu-id="685c0-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="685c0-119">Счета создаются вручную или с использованием периодического автоматизированного процесса.</span><span class="sxs-lookup"><span data-stu-id="685c0-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="685c0-120">Для каждого юридического лица-заемщика может быть создан единый счет или отдельные счета могут быть созданы по проекту.</span><span class="sxs-lookup"><span data-stu-id="685c0-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="685c0-121">Когда внутрихолдинговый счет клиента разносится в юридическое лицо-кредитора, в юридическом лице-заемщике создается соответствующий ожидающий обработки счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="685c0-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="685c0-122">Затраты в счете поставщика, ожидающем обработки, будут записаны во вспомогательную книгу проекта при разноске счета.</span><span class="sxs-lookup"><span data-stu-id="685c0-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="685c0-123">На следующей диаграмме показано внутрихолдинговое выставление счетов, поскольку оно связано с событиями учета и ожидаемыми разносками в главной книге.</span><span class="sxs-lookup"><span data-stu-id="685c0-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Внутрихолдинговый поток](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="685c0-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="685c0-125">Additional resources</span></span>

- [<span data-ttu-id="685c0-126">Настройка внутрихолдингового выставления счетов</span><span class="sxs-lookup"><span data-stu-id="685c0-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="685c0-127">Запись внутрихолдинговых транзакций</span><span class="sxs-lookup"><span data-stu-id="685c0-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="685c0-128">Создание внутрихолдинговых счетов для клиентов и поставщиков</span><span class="sxs-lookup"><span data-stu-id="685c0-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]