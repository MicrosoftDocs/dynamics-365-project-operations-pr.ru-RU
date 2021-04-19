---
title: Финансовые измерения по умолчанию
description: Эта тема предоставляет информацию о том, как настроить значения по умолчанию для финансовых измерений.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287389"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="5f219-103">Финансовые измерения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5f219-103">Financial dimension defaults</span></span>

<span data-ttu-id="5f219-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="5f219-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5f219-105">Dynamics 365 Project Operations использует платформу [Финансовые аналитики](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) в Dynamics 365 Finance, чтобы предоставить дополнительную аналитику о транзакциях вспомогательной и главной книги проекта.</span><span class="sxs-lookup"><span data-stu-id="5f219-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="5f219-106">Финансовые измерения по умолчанию могут быть установлены для клиента, источника финансирования проекта, вехи, строки контракта по проекту или проекта.</span><span class="sxs-lookup"><span data-stu-id="5f219-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="5f219-107">Определение финансовых измерений по умолчанию для клиента</span><span class="sxs-lookup"><span data-stu-id="5f219-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="5f219-108">Значения по умолчанию для измерения клиента указаны в Finance.</span><span class="sxs-lookup"><span data-stu-id="5f219-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="5f219-109">Выполните следующие шаги, чтобы задать измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f219-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="5f219-110">Перейдите в раздел **Расчеты с клиентами** > **Клиенты** > **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="5f219-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="5f219-111">На странице **Клиенты** на вкладке **Финансовые измерения** установите значения финансовых измерений для конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="5f219-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="5f219-112">Определение финансовых измерений по умолчанию для контрактов по проекту</span><span class="sxs-lookup"><span data-stu-id="5f219-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="5f219-113">Контракты по проектам создаются и поддерживаются в Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="5f219-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="5f219-114">Атрибуты учета для контрактов по проектам устанавливаются в модуле **Управление и учет по проектам** в Finance.</span><span class="sxs-lookup"><span data-stu-id="5f219-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="5f219-115">Задание финансовых измерений для источника финансирования проекта</span><span class="sxs-lookup"><span data-stu-id="5f219-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="5f219-116">Перейдите в раздел **Управление и учет по проектам** > **Проекты** > **Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5f219-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="5f219-117">Выберите запись, которую хотите обновить, и на вкладке **Контракт по проекту** выберите **Показать учет по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="5f219-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="5f219-118">Разверните раздел **Связанная информация** и выберите вкладку **Источники финансирования**.</span><span class="sxs-lookup"><span data-stu-id="5f219-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="5f219-119">Задайте финансовые измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f219-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="5f219-120">Обратите внимание, что значения по умолчанию финансовых измерений относятся к учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="5f219-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="5f219-121">Задание финансовых измерений для строки контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="5f219-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="5f219-122">Перейдите в раздел **Управление и учет по проектам** > **Проекты** > **Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5f219-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="5f219-123">Выберите запись, которую хотите обновить, и на вкладке **Контракт по проекту** выберите **Показать учет по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="5f219-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="5f219-124">Разверните раздел **Связанная информация** и выберите вкладку **Строки контракта**.</span><span class="sxs-lookup"><span data-stu-id="5f219-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="5f219-125">Задайте финансовые измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f219-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="5f219-126">Значения по умолчанию для финансовых измерений применимы и могут использоваться только со строками контракта с фиксированной ценой (вехой).</span><span class="sxs-lookup"><span data-stu-id="5f219-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="5f219-127">Эти значения по умолчанию используются для связанных проводок по промежуточным накладным проекта и строк счета.</span><span class="sxs-lookup"><span data-stu-id="5f219-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="5f219-128">Определение финансовых измерений по умолчанию для проектов</span><span class="sxs-lookup"><span data-stu-id="5f219-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="5f219-129">Проекты создаются и поддерживаются в CDS.</span><span class="sxs-lookup"><span data-stu-id="5f219-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="5f219-130">Атрибуты учета для проектов устанавливаются в модуле **Управление и учет по проектам** в Finance.</span><span class="sxs-lookup"><span data-stu-id="5f219-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="5f219-131">Перейдите в раздел **Управление и учет по проектам** > **Проекты** > **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="5f219-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="5f219-132">Выберите запись, которую хотите обновить, и на вкладке **Проект** выберите **Показать учет по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="5f219-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="5f219-133">Разверните раздел **Связанная информация** и выберите вкладку **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="5f219-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="5f219-134">Задайте финансовые измерения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f219-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="5f219-135">Обратите внимание, что значения по умолчанию финансовых измерений относятся к учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="5f219-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="5f219-136">Если проект связан со строкой контракта с несколькими клиентами контракта по проекту, основной клиент используется для финансовых измерений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f219-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="5f219-137">Финансовые измерения проекта по умолчанию используются для установки значений по умолчанию для строк журнала для транзакций времени, расходов и сборов в **журнале интеграции Project Operations** и в связанных строках счетов по проекту.</span><span class="sxs-lookup"><span data-stu-id="5f219-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]