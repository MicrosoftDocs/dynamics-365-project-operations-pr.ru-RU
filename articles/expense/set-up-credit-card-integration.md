---
title: Настройка интеграции с кредитными картами
description: В этой теме объясняется, как работать с транзакциями по кредитным картам, связанным с расходами.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866699"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="fa3d1-103">Настройка интеграции с кредитными картами</span><span class="sxs-lookup"><span data-stu-id="fa3d1-103">Set up credit card integration</span></span>

<span data-ttu-id="fa3d1-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_</span><span class="sxs-lookup"><span data-stu-id="fa3d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa3d1-105">Связанные с расходами транзакции по кредитным картам можно настроить так, чтобы они автоматически импортировались по повторяющемуся графику.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="fa3d1-106">Кроме того, транзакции можно импортировать вручную по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="fa3d1-107">Транзакции по кредитной карте импортируются через сущность данных транзакций по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="fa3d1-108">Импорт транзакций по кредитной карте</span><span class="sxs-lookup"><span data-stu-id="fa3d1-108">Import credit card transactions</span></span>

<span data-ttu-id="fa3d1-109">Чтобы импортировать транзакции по кредитной карте, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fa3d1-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="fa3d1-110">На странице **Операции по кредитной карте** выберите **Импорт транзакций**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="fa3d1-111">Если вы открываете управление данными впервые, система должна обновить список сущностей данных, прежде чем вы сможете продолжить.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="fa3d1-112">В поле **Имя** введите уникальное описание для задания импорта.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="fa3d1-113">В поле **Формат исходных данных** выберите формат файла, содержащего транзакции по кредитной карте для импорта.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="fa3d1-114">Выберите **Отправить**, затем найдите и выберите файл для импорта.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="fa3d1-115">После отправки файла проверьте сопоставление файла транзакции по кредитной карте и столбцов сущности данных транзакций кредитной карты, выбрав ссылку **Просмотр сопоставления** на плитке.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="fa3d1-116">Если есть ошибки сопоставления или если вам необходимо изменить сопоставление, внесите изменения сопоставления на вкладке **Визуализация сопоставления** или на вкладке **Детали сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="fa3d1-117">Чтобы автоматизировать транзакции по кредитной карте, выберите **Создать повторяющееся задание данных**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="fa3d1-118">Затем вы можете установить периодичность, которая определяет, как часто следует импортировать транзакции по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="fa3d1-119">По завершении выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="fa3d1-120">Чтобы импортировать выбранный файл сейчас, выберите **Импортировать**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="fa3d1-121">Если во время импорта возникают ошибки, вы можете просмотреть журнал выполнения или промежуточные данные, чтобы увидеть ошибки, которые необходимо исправить, чтобы обеспечить успешный импорт.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="fa3d1-122">Если вам нужно импортировать более одного формата файла, вы должны создать отдельные задания импорта для каждого типа формата.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="fa3d1-123">Переназначение транзакций по кредитной карте для уволенных сотрудников</span><span class="sxs-lookup"><span data-stu-id="fa3d1-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="fa3d1-124">После прекращения записи сотрудника его учетная запись служб Active Directory Domain Services (AD DS) отключается.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="fa3d1-125">Однако могут существовать активные транзакции по кредитным картам, которые все равно должны быть учтены в расходах и возмещены.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="fa3d1-126">На странице **Транзакции по кредитной карте** вы можете переназначить сотрудника для любой транзакции по кредитной карте, для которой связанный сотрудник был отключен.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="fa3d1-127">Выберите одну или несколько транзакций по кредитной карте, затем выберите **Переназначить транзакции**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="fa3d1-128">Затем вы можете выбрать другого сотрудника, которому будут назначены операции по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="fa3d1-129">После переназначения транзакций по кредитной карте их можно выбрать для отчета о расходах и оплатить с помощью обычного процесса возмещения расходов по отчету о расходах.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="fa3d1-130">Удаление транзакций по кредитной карте</span><span class="sxs-lookup"><span data-stu-id="fa3d1-130">Delete credit card transactions</span></span> 

<span data-ttu-id="fa3d1-131">Иногда после импорта транзакций по кредитной карте может потребоваться удалить некоторые транзакции.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="fa3d1-132">Это может быть связано с тем, что транзакции дублируются или данные могут быть неточными.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="fa3d1-133">Администраторы могут использовать функцию **Удалить транзакции по кредитной карте** для выбора и удаления транзакций по кредитным картам, которые **не прикреплены** к отчету о расходах.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="fa3d1-134">Перейдите **Периодические задачи** > **Удаление транзакций по кредитной карте**.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="fa3d1-135">Выберите **Фильтр** и предоставьте информацию для идентификации записей, которые нужно включить.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="fa3d1-136">Выберите **ОК**, чтобы удалить записи.</span><span class="sxs-lookup"><span data-stu-id="fa3d1-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
