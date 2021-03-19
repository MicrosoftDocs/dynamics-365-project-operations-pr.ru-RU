---
title: Настройка учета для внутренних проектов
description: В этой теме представлена информация о том, как настроить практику учета для внутренних проектов в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287614"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="4e27a-103">Настройка учета для внутренних проектов</span><span class="sxs-lookup"><span data-stu-id="4e27a-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="4e27a-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="4e27a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4e27a-105">Внутренние проекты позволяют компаниям отслеживать затраты, связанные с действиями, счета за которые не выставляется клиенту.</span><span class="sxs-lookup"><span data-stu-id="4e27a-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="4e27a-106">Примеры внутренних проектов:</span><span class="sxs-lookup"><span data-stu-id="4e27a-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="4e27a-107">Разработка продукта, например мобильного приложения, и отслеживание затрат, связанных с разработкой.</span><span class="sxs-lookup"><span data-stu-id="4e27a-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="4e27a-108">Управление предпродажным временем и расходами.</span><span class="sxs-lookup"><span data-stu-id="4e27a-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="4e27a-109">Этот предпродажный внутренний проект может быть преобразован позже в оплачиваемый проект, если предложение с расценками будет выиграно.</span><span class="sxs-lookup"><span data-stu-id="4e27a-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="4e27a-110">Любой проект, не связанный с контрактом в Dynamics 365 Project Operations, считается внутренним.</span><span class="sxs-lookup"><span data-stu-id="4e27a-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="4e27a-111">Профили затрат и доходов проекта не используются для определения правил учета для проекта.</span><span class="sxs-lookup"><span data-stu-id="4e27a-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="4e27a-112">Себестоимость внутреннего проекта всегда разносится с использованием принципов прибылей и убытков.</span><span class="sxs-lookup"><span data-stu-id="4e27a-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="4e27a-113">Счета книги учета для проводок определяются на странице **Настройка разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="4e27a-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="4e27a-114">Проводки по времени разносятся путем дебетования счета **Затраты** и кредитуются на счет **Распределение зарплаты**.</span><span class="sxs-lookup"><span data-stu-id="4e27a-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="4e27a-115">Проводки по расходам разносятся путем дебетования счета **Затраты** и кредитуются на **Корреспондирующий счет для расходов**.</span><span class="sxs-lookup"><span data-stu-id="4e27a-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="4e27a-116">После разноски проводок в проект, если проект связан с контрактом по проекту, система сторнирует все накопленные проводки и создает новые оплачиваемые проводки.</span><span class="sxs-lookup"><span data-stu-id="4e27a-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="4e27a-117">Оплачиваемые транзакции подчиняются правилам учета, определенным в соответствующем профиле затрат и доходов проекта.</span><span class="sxs-lookup"><span data-stu-id="4e27a-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]