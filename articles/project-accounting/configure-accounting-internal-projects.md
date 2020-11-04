---
title: Настройка учета для внутренних проектов
description: В этой теме представлена информация о том, как настроить практику учета для внутренних проектов в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083122"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="089c4-103">Настройка учета для внутренних проектов</span><span class="sxs-lookup"><span data-stu-id="089c4-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="089c4-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="089c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="089c4-105">Внутренние проекты позволяют компаниям отслеживать затраты, связанные с действиями, счета за которые не выставляется клиенту.</span><span class="sxs-lookup"><span data-stu-id="089c4-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="089c4-106">Примеры внутренних проектов:</span><span class="sxs-lookup"><span data-stu-id="089c4-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="089c4-107">Разработка продукта, например мобильного приложения, и отслеживание затрат, связанных с разработкой.</span><span class="sxs-lookup"><span data-stu-id="089c4-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="089c4-108">Управление предпродажным временем и расходами.</span><span class="sxs-lookup"><span data-stu-id="089c4-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="089c4-109">Этот предпродажный внутренний проект может быть преобразован позже в оплачиваемый проект, если предложение с расценками будет выиграно.</span><span class="sxs-lookup"><span data-stu-id="089c4-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="089c4-110">Любой проект, не связанный с контрактом в Dynamics 365 Project Operations, рассматривается как внутренний.</span><span class="sxs-lookup"><span data-stu-id="089c4-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="089c4-111">Профили затрат и доходов проекта не используются для определения правил учета для проекта.</span><span class="sxs-lookup"><span data-stu-id="089c4-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="089c4-112">Себестоимость внутреннего проекта всегда разносится с использованием принципов прибылей и убытков.</span><span class="sxs-lookup"><span data-stu-id="089c4-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="089c4-113">Счета книги учета для проводок определяются на странице **Настройка разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="089c4-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="089c4-114">Проводки по времени разносятся путем дебетования счета **Затраты** и кредитуются на счет **Распределение зарплаты**.</span><span class="sxs-lookup"><span data-stu-id="089c4-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="089c4-115">Проводки по расходам разносятся путем дебетования счета **Затраты** и кредитуются на **Корреспондирующий счет для расходов**.</span><span class="sxs-lookup"><span data-stu-id="089c4-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="089c4-116">После разноски проводок в проект, если проект связан с контрактом по проекту, система сторнирует все накопленные проводки и создает новые оплачиваемые проводки.</span><span class="sxs-lookup"><span data-stu-id="089c4-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="089c4-117">Оплачиваемые транзакции подчиняются правилам учета, определенным в соответствующем профиле затрат и доходов проекта.</span><span class="sxs-lookup"><span data-stu-id="089c4-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


