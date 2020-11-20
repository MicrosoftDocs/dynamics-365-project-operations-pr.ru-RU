---
title: Создание счета-проформы вручную — облегченное развертывание
description: В этой теме предоставлена информация о создании счета-проформы вручную в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176402"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="a5ddf-103">Создание счета-проформы вручную — облегченное развертывание</span><span class="sxs-lookup"><span data-stu-id="a5ddf-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="a5ddf-104">_**Относится к:** развертывание Lite — от сделки до счетов-проформ_</span><span class="sxs-lookup"><span data-stu-id="a5ddf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5ddf-105">В Dynamics 365 Project Operations счета-проформы можно создавать вручную по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="a5ddf-106">Вы можете вручную создать счет-проформу со страницы списка **Контракты по проектам** или со страницы сведений **Контракт по проекту**.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="a5ddf-107">Страница списка контрактов по проектам</span><span class="sxs-lookup"><span data-stu-id="a5ddf-107">Project Contracts list page</span></span>

<span data-ttu-id="a5ddf-108">Со страницы списка **Контракты по проектам** выберите один или несколько контрактов по проекту и создайте счета для всех выбранных записей.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="a5ddf-109">Система проверяет, какой из выбранных контрактов по проекту имеет невыполненную работу **Готово к выставлению счета** с датами до сегодняшней даты.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="a5ddf-110">Из этих контрактов система создает черновики счетов-проформ.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="a5ddf-111">Если контракт по проекту имеет несколько клиентов, может быть создан один счет для каждого клиента и несколько счетов для каждого контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="a5ddf-112">Все созданные счета по проекту доступны на странице **Счет** в разделе **Выставление счетов** области **Продажи**.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="a5ddf-113">Страница сведения контракта по проекту</span><span class="sxs-lookup"><span data-stu-id="a5ddf-113">Project Contract details page</span></span>

<span data-ttu-id="a5ddf-114">Счет-проформа также может быть создан со страницы сведений **Контракт по проекту**, при этом создается счет для конкретного контракта по проекту.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="a5ddf-115">Система проверяет, что контракт по проекту имеет невыполненную работу **Готово к выставлению счета** с датами до сегодняшней даты.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="a5ddf-116">На основе этих контрактов система создает черновики счетов-проформ на основе количества клиентов по каждой строке контракта.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="a5ddf-117">Когда создается единый счет-проформа, открывается страница **Счет**.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="a5ddf-118">Если для этого контракта по проекту создано несколько счетов, то открывается страница списка **Счета**, на которой будут показаны все созданные счета.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
