---
title: Обзор расходов
description: В этой теме предоставлена информация о функциях расходов в Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2a26b321e15080cc6a4a6a3ed410be175e790a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995412"
---
# <a name="expense-home-page"></a><span data-ttu-id="59cf0-103">Домашняя страница расходов</span><span class="sxs-lookup"><span data-stu-id="59cf0-103">Expense home page</span></span>

<span data-ttu-id="59cf0-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="59cf0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="59cf0-105">Dynamics 365 Project Operations поддерживает возможность обрабатывать расходы.</span><span class="sxs-lookup"><span data-stu-id="59cf0-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="59cf0-106">Обработка расходов происходит с проектами или без них с использованием настраиваемого рабочего процесса политик, категорий транзакций и утверждений.</span><span class="sxs-lookup"><span data-stu-id="59cf0-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="59cf0-107">В Project Operations поддерживаются две модели развертывания для расходов:</span><span class="sxs-lookup"><span data-stu-id="59cf0-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="59cf0-108">**Полный**: полное развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** или **Project Operations для сценариев на основе производственного заказа**.</span><span class="sxs-lookup"><span data-stu-id="59cf0-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="59cf0-109">**Базовый**: базовое развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** и **Облегченного развертывания — от сделки до выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="59cf0-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="59cf0-110">Полный</span><span class="sxs-lookup"><span data-stu-id="59cf0-110">Full</span></span> 
<span data-ttu-id="59cf0-111">Развертывание Full Expense обеспечивает полное соблюдения политик, включая возможность создавать политики, такие как:</span><span class="sxs-lookup"><span data-stu-id="59cf0-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="59cf0-112">Лимиты категорий расходов</span><span class="sxs-lookup"><span data-stu-id="59cf0-112">Expense category limits</span></span>
  - <span data-ttu-id="59cf0-113">Поездка</span><span class="sxs-lookup"><span data-stu-id="59cf0-113">Travel</span></span>
  - <span data-ttu-id="59cf0-114">В день</span><span class="sxs-lookup"><span data-stu-id="59cf0-114">Per diem</span></span>
  - <span data-ttu-id="59cf0-115">Импорты кредитных карточек</span><span class="sxs-lookup"><span data-stu-id="59cf0-115">Credit card imports</span></span>
  - <span data-ttu-id="59cf0-116">Оптическое распознавание символов чека</span><span class="sxs-lookup"><span data-stu-id="59cf0-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="59cf0-117">Обычная</span><span class="sxs-lookup"><span data-stu-id="59cf0-117">Basic</span></span> 
<span data-ttu-id="59cf0-118">Сценарий развертывания базовых расходов позволяет записывать только базовые расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="59cf0-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="59cf0-119">Для получения дополнительной информации см. раздел [Запись о расходах (облегченная)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="59cf0-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="59cf0-120">Определение развертывания расходов</span><span class="sxs-lookup"><span data-stu-id="59cf0-120">Determine your Expense deployment</span></span>
<span data-ttu-id="59cf0-121">Чтобы определить, используете ли вы базовое развертывание управления расходами, убедитесь, что URL-адрес заканчивается на **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="59cf0-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]