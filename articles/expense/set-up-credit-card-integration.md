---
title: Настройка интеграции с кредитными картами
description: В этой теме объясняется, как импортировать и поддерживать связанные с расходами транзакции по кредитным картам.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896837"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="5b322-103">Настройка интеграции с кредитными картами</span><span class="sxs-lookup"><span data-stu-id="5b322-103">Set up credit card integration</span></span>

<span data-ttu-id="5b322-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="5b322-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b322-105">Связанные с расходами транзакции по кредитным картам можно настроить так, чтобы они автоматически импортировались по повторяющемуся графику.</span><span class="sxs-lookup"><span data-stu-id="5b322-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="5b322-106">Кроме того, транзакции можно импортировать вручную по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5b322-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="5b322-107">Операции по кредитной карте импортируются через сущность данных операций по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="5b322-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="5b322-108">Импорт транзакций по кредитной карте</span><span class="sxs-lookup"><span data-stu-id="5b322-108">Import credit card transactions</span></span>

1. <span data-ttu-id="5b322-109">На странице **Операции по кредитной карте** выберите **Импорт транзакций**.</span><span class="sxs-lookup"><span data-stu-id="5b322-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="5b322-110">Если вы открываете управление данными впервые, система должна обновить список сущностей данных, прежде чем вы сможете продолжить.</span><span class="sxs-lookup"><span data-stu-id="5b322-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="5b322-111">В поле **Имя** введите уникальное описание задания импорта.</span><span class="sxs-lookup"><span data-stu-id="5b322-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="5b322-112">В поле **Формат исходных данных** выберите формат файла, содержащего транзакции по кредитной карте для импорта.</span><span class="sxs-lookup"><span data-stu-id="5b322-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="5b322-113">Выберите **Отправить**, затем найдите и выберите файл для импорта.</span><span class="sxs-lookup"><span data-stu-id="5b322-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="5b322-114">После отправки файла проверьте сопоставление файла транзакции по кредитной карте и столбцов сущности данных транзакций кредитной карты, выбрав ссылку **Просмотр сопоставления** на плитке.</span><span class="sxs-lookup"><span data-stu-id="5b322-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="5b322-115">Если есть ошибки сопоставления или если вам необходимо изменить сопоставление, внесите изменения сопоставления на вкладке **Визуализация сопоставления** или на вкладке **Детали сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="5b322-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="5b322-116">Чтобы автоматизировать транзакции по кредитной карте, выберите **Создать повторяющееся задание данных**.</span><span class="sxs-lookup"><span data-stu-id="5b322-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="5b322-117">Затем вы можете установить периодичность, которая определяет, как часто следует импортировать транзакции по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="5b322-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="5b322-118">По завершении выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b322-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="5b322-119">Чтобы импортировать выбранный файл сейчас, выберите **Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="5b322-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="5b322-120">Если во время импорта возникают ошибки, вы можете просмотреть журнал выполнения или промежуточные данные, чтобы увидеть ошибки, которые необходимо исправить, чтобы гарантировать успешный импорт.</span><span class="sxs-lookup"><span data-stu-id="5b322-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="5b322-121">Если необходимо импортировать файлы нескольких форматов, необходимо создать отдельные задания импорта для каждого типа формата.</span><span class="sxs-lookup"><span data-stu-id="5b322-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="5b322-122">Переназначение транзакций по кредитной карте для уволенных сотрудников</span><span class="sxs-lookup"><span data-stu-id="5b322-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="5b322-123">После прекращения записи сотрудника его учетная запись служб Active Directory Domain Services (AD DS) отключается.</span><span class="sxs-lookup"><span data-stu-id="5b322-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="5b322-124">Однако могут существовать активные транзакции по кредитным картам, которые все равно должны быть учтены в расходах и возмещены.</span><span class="sxs-lookup"><span data-stu-id="5b322-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="5b322-125">На странице **Операции по кредитной карте** вы можете переназначить сотрудника для любой транзакции по кредитной карте, по которой связанный сотрудник был уволен.</span><span class="sxs-lookup"><span data-stu-id="5b322-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="5b322-126">Выберите одну или несколько транзакций по кредитной карте, затем выберите **Переназначить транзакции**.</span><span class="sxs-lookup"><span data-stu-id="5b322-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="5b322-127">Затем вы можете выбрать другого сотрудника, которому будут назначены операции по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="5b322-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="5b322-128">После переназначения транзакций по кредитной карте их можно выбрать для отчета о расходах и оплатить с помощью обычного процесса возмещения расходов по отчету о расходах.</span><span class="sxs-lookup"><span data-stu-id="5b322-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
