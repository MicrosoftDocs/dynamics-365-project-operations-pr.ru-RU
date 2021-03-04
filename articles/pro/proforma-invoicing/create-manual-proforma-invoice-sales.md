---
title: Создание счета-проформы вручную — облегченное развертывание
description: В этой теме предоставлена информация о создании счета-проформы вручную в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764519"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="e5ba0-103">Создание счета-проформы вручную — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="e5ba0-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="e5ba0-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="e5ba0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5ba0-105">В Dynamics 365 Project Operations, при необходимости счета-проформы можно создавать вручную.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="e5ba0-106">Вы можете вручную создать счет-проформу со страницы списка **Контракты по проектам** или со страницы сведений **Контракт по проекту**.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="e5ba0-107">Страница списка контрактов по проектам</span><span class="sxs-lookup"><span data-stu-id="e5ba0-107">Project Contracts list page</span></span>

<span data-ttu-id="e5ba0-108">Со страницы списка **Контракты по проектам** выберите один или несколько контрактов по проекту и создайте счета для всех выбранных записей.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="e5ba0-109">Система проверяет, какой из выбранных контрактов по проекту имеет невыполненную работу **Готово к выставлению счета** с датами до сегодняшней даты.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e5ba0-110">Из этих контрактов система создает черновики счетов-проформ.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="e5ba0-111">Если контракт по проекту имеет несколько клиентов, может быть создан один счет для каждого клиента и несколько счетов для каждого контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="e5ba0-112">Все созданные счета по проекту доступны на странице **Счет** в разделе **Выставление счетов** области **Продажи**.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="e5ba0-113">Страница сведения контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="e5ba0-113">Project Contract details page</span></span>

<span data-ttu-id="e5ba0-114">Счет-проформа также может быть создан на странице сведений **Контракт по проекту**.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="e5ba0-115">Система проверяет, какой из контрактов по проекту имеет невыполненную работу **Готово к выставлению счета** с датами до сегодняшней даты.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e5ba0-116">На основе этих контрактов система создает черновики счетов-проформ на основе количества клиентов по каждой строке контракта.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="e5ba0-117">Когда создается единый счет-проформа, открывается страница **Счет**.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="e5ba0-118">Если для этого контракта по проекту создано несколько счетов, откроется страница списка **Счета**, на которой будут показаны все созданные счета.</span><span class="sxs-lookup"><span data-stu-id="e5ba0-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
