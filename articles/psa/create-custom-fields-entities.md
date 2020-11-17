---
title: Создание настраиваемых полей и сущностей
description: В этом разделе объясняется, как создавать наборы параметров и сущности в вашем собственном решении на платформе Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083257"
---
# <a name="create-custom-fields-and-entities"></a>Создание настраиваемых полей и сущностей 

Выполните следующие шаги в любое время, когда требуется создать настраиваемый набор параметров или сущность на платформе Power Apps.  
Процедуры в данном разделе необходимо выполнить с помощью веб-интерфейса Project Service Automation (PSA).

> [!IMPORTANT]
> Рекомендуется внести все изменения настраиваемых измерений ценообразования в отдельном решении. Эта важная рекомендация гарантирует гибкость в будущем для обновления или удаления изменений по мере необходимости, поможет с повторным использованием вашей работы и упростит перенос этих изменений в другой экземпляр. После внесения всех требуемых изменений экспортируйте это решение как **Управляемое решение** и импортируйте его в другие экземпляры, чтобы повторно использовать настройку ценообразования.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Создание настраиваемых полей и наборов параметров в решении измерений ценообразования

Изменение ценообразования может быть набором параметров или сущностью. Оба необходимо создать в вашем решении ценообразования. Шаги данной процедуры объясняют, как создавать измерения на основе сущности измерения на основе набора параметров.

### <a name="entity-based-dimensions"></a>Измерения на основе сущности

1. В PSA щелкните **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**.
2. В обозревателе решений в левой навигационной панели выберите **Сущности**.
3. Щелкните **Создать** для создания новой сущности с названием **Стандартный заголовок**. Введите остальные обязательные сведения, затем щелкните **Сохранить**.

> ![Определение сущности стандартного заголовка](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Измерения на основе набора параметров 
Можно создать два измерения на основе набора параметров. Используйте **Место работы ресурса** для отслеживания цены места работы **Дом** и работы **На месте** , и используйте **Рабочие часы ресурса** со значениями **Обычные** и **Сверхурочные** для применения наценки после завершения работы.


1. В PSA щелкните **Параметры** > **Решения** и затем дважды щелкните **Измерения ценообразования \<your organization name>**. 
2. В обозревателе решений в левой навигационной панели выберите **Наборы параметров**. 
3. Щелкните **Создать** для создания нового набора параметров, введите остальное обязательные сведения, затем нажмите **Сохранить**.

> ![Измерение ценообразования на основе набора параметров под названием "Место работы ресурса" ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Измерение ценообразования на основе набора параметров под названием "Рабочие часы ресурса" ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Создание данные для измерений на основе сущности

Можно создавать данные для измерений на основе сущности вручную или с помощью импорта Microsoft Excel или служебных вызовов. Используйте шаги в этой процедуре для создания двух стандартных заголовков, **Системный инженер** и **Главный системный инженер** из измерения на основе сущности, **Стандартный заголовок**. Если данные, которые нужно создать, небольшие, как в следующем примере, можно использовать стандартную форму.

1. В PSA щелкните **Расширенный поиск**. Выделите сущность **Стандартный заголовок** , затем щелкните **Результаты**. Отображаются все строки в сущности **Стандартный заголовок**.
2. Нажмите кнопку **Создать**. В поле **Имя** введите "Системный инженер" и нажмите кнопку **Сохранить**.
3. Закройте форму. 
4. Повторите шаги с 1 по 3 для создания другого стандартного заголовка для "Главный системный инженер".

> ![Демонстрационные данные для сущности стандартного заголовка ](media/ST-data.png)

