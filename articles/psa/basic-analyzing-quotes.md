---
title: Анализ предложений с расценками по проекту
description: В этом разделе представлена информация об анализе предложений с расценками по проекту.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291275"
---
# <a name="analysis-of-project-quotes"></a>Анализ предложений с расценками по проекту

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation анализирует предложения с расценками по проекту для оценки прибыльности. Он также анализирует, насколько хорошо предложение с расценками соответствует ожиданиям клиента с точки зрения даты доставки или даты завершения, а также в отношении бюджета.

## <a name="profitability-analysis"></a>Анализ прибыльности

Project Service Automation анализирует доходность, используя валовую прибыль и скорректированную валовую прибыль.

- Значения валовой прибыли вычисляются с помощью следующей формулы:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Скорректированная валовая прибыль вычисляется с помощью следующей формулы:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Если значения валовой прибыли и скорректированной валовой прибыли значительно отличаются, большая часть работы в предложении с расценками классифицируется как неоплачиваемая.

## <a name="analysis-of-customer-expectations"></a>Анализ ожиданий клиента

Можно анализировать предложения с расценками и создать диаграммы для ожиданий клиентов по расписанию и бюджету, если ввести значения в следующие поля:

- Поле **Требуемая дата поставки** в заголовке предложения с расценками.
- Поле **Бюджет клиента** для каждой строки предложения с расценками (для строк на основе проекта и строк на основе продукта).

Анализ ожиданий клиентов относительно расписания выполняется путем сравнения последней даты окончания сведений строки предложения с расценками с требуемой датой поставки по всем строкам предложения с расценками в предложении.

Анализ ожиданий клиента о бюджете выполняется путем сравнения суммы общего бюджета клиента с суммой из предложения с расценками по всем строкам этого предложения с расценками.


[!INCLUDE[footer-include](../includes/footer-banner.md)]