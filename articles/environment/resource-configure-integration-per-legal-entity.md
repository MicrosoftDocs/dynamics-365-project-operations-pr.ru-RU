---
title: Настройка интеграции Project Operations для каждого юридического лица
description: Эта тема предоставляет информацию о настройке интеграции по юридическому лицу в Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096768"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="e4e72-103">Настройка интеграции Project Operations для каждого юридического лица</span><span class="sxs-lookup"><span data-stu-id="e4e72-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="e4e72-104">_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_</span><span class="sxs-lookup"><span data-stu-id="e4e72-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e4e72-105">Эта тема проведет вас через шаги, необходимые для настройки Dynamics 365 Project Operations для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="e4e72-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="e4e72-106">Включение ключей функций в Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e4e72-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="e4e72-107">Выполните следующие шаги, чтобы включить необходимые функции.</span><span class="sxs-lookup"><span data-stu-id="e4e72-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="e4e72-108">В Dynamics 365 Finance перейдите в рабочую область **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="e4e72-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="e4e72-109">В поле **Список функций** найдите и включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="e4e72-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="e4e72-110">**Включение нескольких строк контракта для проекта**</span><span class="sxs-lookup"><span data-stu-id="e4e72-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="e4e72-111">**Включение Project Operations в Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="e4e72-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="e4e72-112">Если вы не видите в списке **Ключи функций** , убедитесь, что ваша версия Finance соответствует минимальным требованиям к версии (версия приложения 10.0.13 со всеми примененными обновлениями качества или выше).</span><span class="sxs-lookup"><span data-stu-id="e4e72-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="e4e72-113">Выберите **Проверить наличие обновлений** , чтобы обновить список функций.</span><span class="sxs-lookup"><span data-stu-id="e4e72-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="e4e72-114">Определение сценария развертывания Project Operations для юридического лица</span><span class="sxs-lookup"><span data-stu-id="e4e72-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="e4e72-115">Вы можете включить Project Operations в Dynamics 365 Customer Engagement на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="e4e72-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="e4e72-116">Вы можете иметь одно юридическое лицо, использующее Project Operations в Dynamics 365 Customer Engagement, для сценариев на основе ресурсов/отсутствия запасов.</span><span class="sxs-lookup"><span data-stu-id="e4e72-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="e4e72-117">В той же среде у вас может быть другое юридическое лицо, использующее Project Operations для сценариев складских запасов/производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="e4e72-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="e4e72-118">В Dynamics 365 Finance перейдите в раздел **Управление и учет по проектам** > **Настройка** > **Глобальные параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="e4e72-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="e4e72-119">В списке доступных юридических лиц выберите организации, у которых будут включены функции несколько строк контракта и Project Operations в Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="e4e72-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="e4e72-120">Оставьте невыбранными юридические лица, которые будут использовать Project Operations для сценариев складских запасов/производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="e4e72-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="e4e72-121">Юридическое лицо можно выбрать только в том случае, если у него нет существующих проектов.</span><span class="sxs-lookup"><span data-stu-id="e4e72-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="e4e72-122">Настройка параметров модуля управления и учета для проектов</span><span class="sxs-lookup"><span data-stu-id="e4e72-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="e4e72-123">Каждому юридическому лицу, использующему Project Operations в Dynamics 365 Customer Engagement, требуется набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e4e72-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="e4e72-124">Эти параметры настраиваются на вкладке **Project Operations** на странице **Параметры управления и учета по проектам**.</span><span class="sxs-lookup"><span data-stu-id="e4e72-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="e4e72-125">Это следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e4e72-125">The parameters are:</span></span>

  - <span data-ttu-id="e4e72-126">**Тип выставления счетов по умолчанию** : Project Operations использует фиксированный набор значений по умолчанию для типа выставления счетов, которые должны быть сопоставлены со свойствами строки Finance.</span><span class="sxs-lookup"><span data-stu-id="e4e72-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="e4e72-127">Создайте запись для каждого типа выставления счетов: **Не указано** , **Оплачиваемый** , **Не оплачиваемый** , **Бесплатный** и **Недоступно**.</span><span class="sxs-lookup"><span data-stu-id="e4e72-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="e4e72-128">**Значения по умолчанию для категорий проекта** : выберите категории проектов по умолчанию, которые будут использоваться для каждого типа транзакции.</span><span class="sxs-lookup"><span data-stu-id="e4e72-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="e4e72-129">Эти значения по умолчанию будут использоваться в **журнале интеграции Project Operations** и в сметах, где для фактических данных проекта не указана категория транзакции.</span><span class="sxs-lookup"><span data-stu-id="e4e72-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="e4e72-130">**Прогнозы** : выберите модель прогноза, которая будет использоваться для оценки времени и расходов.</span><span class="sxs-lookup"><span data-stu-id="e4e72-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
