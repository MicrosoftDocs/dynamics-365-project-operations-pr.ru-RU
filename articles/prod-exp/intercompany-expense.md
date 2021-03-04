---
title: Внутрихолдинговые расходы
description: Этот тема предоставляет информацию о том, как использовать внутрихолдинговые расходы, чтобы отнести расходы работника к юридическому лицу, для которого выполнялась работа.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960848"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="f9301-103">Внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="f9301-103">Intercompany expenses</span></span>

<span data-ttu-id="f9301-104">Работник, нанятый одним юридическим лицом в организации, может выполнять работу на другое юридическое лицо в той же организации.</span><span class="sxs-lookup"><span data-stu-id="f9301-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="f9301-105">Можно использовать внутрихолдинговые расходы, чтобы отнести расходы работника к юридическому лицу, для которого выполнялась работа.</span><span class="sxs-lookup"><span data-stu-id="f9301-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="f9301-106">Юридическое лицо, которое нанимает работника, называется юридическим лицом-арендодателем.</span><span class="sxs-lookup"><span data-stu-id="f9301-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="f9301-107">Юридическое лицо, для которого работник несет расходы, называется юридическим лицом-заемщиком.</span><span class="sxs-lookup"><span data-stu-id="f9301-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="f9301-108">Прежде чем работник сможет создавать и отправлять внутрихолдинговые расходы, вы должны включить строки внутрихолдинговых расходов.</span><span class="sxs-lookup"><span data-stu-id="f9301-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="f9301-109">В юридическом лице-кредиторе на страница **Параметры управления расходами** выберите **Разрешить строки внутрихолдинговых расходов**.</span><span class="sxs-lookup"><span data-stu-id="f9301-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="f9301-110">Проводка налога на внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="f9301-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9301-111">Прежде чем вы сможете использовать налоговые группы, связанные с юридическим лицом-кредитором (источник), вместо юридического лица-заемщика (целевого) в своем отчете о расходах, вы должны включить функциональность в настройке налога с продаж Главной книги.</span><span class="sxs-lookup"><span data-stu-id="f9301-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="f9301-112">Когда параметр **Юридическое лицо для разноски внутрихолдинговых налогов** установлен на **Источник** и **Применить правила налогообложения налога с продаж** установлен на **Нет**, используется комбинация налогов для юридическом лица-кредитора.</span><span class="sxs-lookup"><span data-stu-id="f9301-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="f9301-113">Когда этот же параметр установлен на значение **Место назначения**, будет использоваться комбинация налогов для юридического лица-заемщика.</span><span class="sxs-lookup"><span data-stu-id="f9301-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="f9301-114">Для юридических лиц в США, если для параметра установлено значение **Источник**, поле **Входящий налог** поле также должно быть настроено на новой странице **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="f9301-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="f9301-115">Система бухгалтерского учета будет использовать информацию из этого поля для операции учета налогов.</span><span class="sxs-lookup"><span data-stu-id="f9301-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="f9301-116">Такое поведение одинаково для строк расходов, разнесенных с проектом или без него.</span><span class="sxs-lookup"><span data-stu-id="f9301-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
