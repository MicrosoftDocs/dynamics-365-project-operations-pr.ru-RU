---
title: Обзор расходов
description: В этой теме предоставлена информация о функциях расходов в Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083068"
---
# <a name="expense-home-page"></a><span data-ttu-id="4440b-103">Домашняя страница расходов</span><span class="sxs-lookup"><span data-stu-id="4440b-103">Expense home page</span></span>

<span data-ttu-id="4440b-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="4440b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4440b-105">Dynamics 365 Project Operations поддерживает возможность обработки расходов.</span><span class="sxs-lookup"><span data-stu-id="4440b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="4440b-106">Обработка расходов происходит с проектами или без них с использованием настраиваемого рабочего процесса политик, категорий транзакций и утверждений.</span><span class="sxs-lookup"><span data-stu-id="4440b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="4440b-107">В Project Operations поддерживаются две модели развертывания для расходов:</span><span class="sxs-lookup"><span data-stu-id="4440b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="4440b-108">**Полный** : полное развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** или **Project Operations для сценариев на основе производственного заказа**.</span><span class="sxs-lookup"><span data-stu-id="4440b-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="4440b-109">**Базовый** : базовое развертывание доступно для **Project Operations для сценариев на основе ресурсов/отсутствия запасов** и **Облегченного развертывания — от сделки до выставления счетов**.</span><span class="sxs-lookup"><span data-stu-id="4440b-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="4440b-110">Полный</span><span class="sxs-lookup"><span data-stu-id="4440b-110">Full</span></span> 
<span data-ttu-id="4440b-111">Полное развертывание модуля расходов обеспечивает полное применение политик, которое включает в себя возможность создавать политики, такие как:</span><span class="sxs-lookup"><span data-stu-id="4440b-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="4440b-112">Лимиты категорий расходов</span><span class="sxs-lookup"><span data-stu-id="4440b-112">Expense category limits</span></span>
  - <span data-ttu-id="4440b-113">Поездка</span><span class="sxs-lookup"><span data-stu-id="4440b-113">Travel</span></span>
  - <span data-ttu-id="4440b-114">В день</span><span class="sxs-lookup"><span data-stu-id="4440b-114">Per diem</span></span>
  - <span data-ttu-id="4440b-115">Импорты кредитных карточек</span><span class="sxs-lookup"><span data-stu-id="4440b-115">Credit card imports</span></span>
  - <span data-ttu-id="4440b-116">Оптическое распознавание символов чека</span><span class="sxs-lookup"><span data-stu-id="4440b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="4440b-117">Обычная</span><span class="sxs-lookup"><span data-stu-id="4440b-117">Basic</span></span> 
<span data-ttu-id="4440b-118">Сценарий развертывания базовых расходов позволяет записывать только базовые расходы по проекту.</span><span class="sxs-lookup"><span data-stu-id="4440b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="4440b-119">Для получения дополнительной информации см. раздел [Запись о расходах (облегченная)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="4440b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="4440b-120">Определение развертывания расходов</span><span class="sxs-lookup"><span data-stu-id="4440b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="4440b-121">Чтобы определить, используете ли вы базовое развертывание управления расходами, убедитесь, что URL-адрес заканчивается на **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="4440b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
