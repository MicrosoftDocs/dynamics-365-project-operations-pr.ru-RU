---
title: Обзор расходов
description: В этой теме предоставлена информация о функциях расходов в Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276589"
---
# <a name="expense-home-page"></a><span data-ttu-id="daf12-103">Домашняя страница расходов</span><span class="sxs-lookup"><span data-stu-id="daf12-103">Expense home page</span></span>

<span data-ttu-id="daf12-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="daf12-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="daf12-105">Dynamics 365 Project Operations поддерживает возможность обрабатывать расходы.</span><span class="sxs-lookup"><span data-stu-id="daf12-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="daf12-106">Обработка расходов происходит с проектами или без них с использованием настраиваемого рабочего процесса политик, категорий транзакций и утверждений.</span><span class="sxs-lookup"><span data-stu-id="daf12-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="daf12-107">В Project Operations поддерживаются две модели развертывания для расходов:</span><span class="sxs-lookup"><span data-stu-id="daf12-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="daf12-108">**Полный**: полное развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** или **Project Operations для сценариев на основе производственного заказа**.</span><span class="sxs-lookup"><span data-stu-id="daf12-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="daf12-109">**Базовый**: базовое развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** и **Облегченного развертывания — от сделки до выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="daf12-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="daf12-110">Полный</span><span class="sxs-lookup"><span data-stu-id="daf12-110">Full</span></span> 
<span data-ttu-id="daf12-111">Развертывание Full Expense обеспечивает полное соблюдения политик, включая возможность создавать политики, такие как:</span><span class="sxs-lookup"><span data-stu-id="daf12-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="daf12-112">Лимиты категорий расходов</span><span class="sxs-lookup"><span data-stu-id="daf12-112">Expense category limits</span></span>
  - <span data-ttu-id="daf12-113">Поездка</span><span class="sxs-lookup"><span data-stu-id="daf12-113">Travel</span></span>
  - <span data-ttu-id="daf12-114">В день</span><span class="sxs-lookup"><span data-stu-id="daf12-114">Per diem</span></span>
  - <span data-ttu-id="daf12-115">Импорты кредитных карточек</span><span class="sxs-lookup"><span data-stu-id="daf12-115">Credit card imports</span></span>
  - <span data-ttu-id="daf12-116">Оптическое распознавание символов чека</span><span class="sxs-lookup"><span data-stu-id="daf12-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="daf12-117">Обычная</span><span class="sxs-lookup"><span data-stu-id="daf12-117">Basic</span></span> 
<span data-ttu-id="daf12-118">Сценарий развертывания базовых расходов позволяет записывать только базовые расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="daf12-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="daf12-119">Для получения дополнительной информации см. раздел [Запись о расходах (облегченная)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="daf12-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="daf12-120">Определение развертывания расходов</span><span class="sxs-lookup"><span data-stu-id="daf12-120">Determine your Expense deployment</span></span>
<span data-ttu-id="daf12-121">Чтобы определить, используете ли вы базовое развертывание управления расходами, убедитесь, что URL-адрес заканчивается на **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="daf12-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]