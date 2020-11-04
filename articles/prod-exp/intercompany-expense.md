---
title: Внутрихолдинговые расходы
description: Работник, нанятый одним юридическим лицом в организации, может выполнять работу на другое юридическое лицо в той же организации. В этой ситуации вы можете использовать функцию внутрихолдинговых расходов, чтобы назначить расходы работника юридическому лицу, для которого выполнялась работа.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083339"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="e24fd-104">Внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="e24fd-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e24fd-105">Работник, нанятый одним юридическим лицом в организации, может выполнять работу на другое юридическое лицо в той же организации.</span><span class="sxs-lookup"><span data-stu-id="e24fd-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="e24fd-106">В этой ситуации вы можете использовать функцию внутрихолдинговых расходов, чтобы назначить расходы работника юридическому лицу, для которого выполнялась работа.</span><span class="sxs-lookup"><span data-stu-id="e24fd-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="e24fd-107">Юридическое лицо, которое нанимает работника, называется юридическим лицом-арендодателем.</span><span class="sxs-lookup"><span data-stu-id="e24fd-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="e24fd-108">Юридическое лицо, для которого работник несет расходы, называется юридическим лицом-заемщиком.</span><span class="sxs-lookup"><span data-stu-id="e24fd-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="e24fd-109">Прежде чем работник сможет создавать и представлять расходы за работу, которая выполняется для другого юридического лица, в юридическом лице-арендодателе, на странице **Параметры управления расходами** выберите параметр **Разрешить строки внутрихолдинговых расходов**.</span><span class="sxs-lookup"><span data-stu-id="e24fd-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="e24fd-110">Проводка налога на внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="e24fd-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e24fd-111">Если вы хотите использовать налоговые группы, связанные с юридическим лицом-арендодателем (исходным), вместо юридического лица-заемщика (целевого) в своем отчете о расходах, вам нужно будет настроить это в настройке налога с продаж в главной книге.</span><span class="sxs-lookup"><span data-stu-id="e24fd-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="e24fd-112">Когда параметру главной книги **Информация о компании для разноски налога при внутрихолдинговом платеже** задано значение **Источник** , а параметру **Применить правила налогообложения** задано значение **Нет** , будет использоваться комбинация налогов для юридического лица-арендодателя.</span><span class="sxs-lookup"><span data-stu-id="e24fd-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="e24fd-113">Когда этот же параметр установлен на значение **Место назначения** , будет использоваться комбинация налогов для юридического лица-заемщика.</span><span class="sxs-lookup"><span data-stu-id="e24fd-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="e24fd-114">Для юридических лиц в США, если для параметра установлено значение **Источник** , поле **Входящий налог** поле также должно быть настроено на новой странице **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="e24fd-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="e24fd-115">Система бухгалтерского учета будет использовать информацию из этого поля для операции учета налогов.</span><span class="sxs-lookup"><span data-stu-id="e24fd-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="e24fd-116">Такое поведение одинаково для строк расходов, разнесенных с проектом или без него.</span><span class="sxs-lookup"><span data-stu-id="e24fd-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
