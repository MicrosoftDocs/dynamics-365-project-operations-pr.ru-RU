---
title: Оценка ресурсов
description: Эта тема предоставляет информацию о том, как рассчитываются оценки ресурсов в Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928600"
---
# <a name="resource-estimates"></a>Оценка ресурсов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Оценки ресурсов основаны на поэтапных усилиях, определенных в структурной декомпозиции работ вместе с применимыми ценовыми измерениями. Обычно расчет выполняется по формуле **ставка/час для каждой роли x часы.** Повременные усилия для каждого ресурса хранятся в записи о назначении ресурсов. Цены хранятся в заранее определенном прайс-листе. Преобразование единиц осуществляется на основании действующего прайс-листа.

![Оценки ресурсов](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Себестоимость и валюта себестоимости по умолчанию

Значения себестоимости по умолчанию берутся из подразделения.

## <a name="default-bill-rate-and-sales-currency"></a>Ставка и валюта продаж по умолчанию

Цены продажи применяется один раз за сделку. Иерархия цен продажи по умолчанию следующая:

1. Предприятие
2. Клиент
3. Предложение с расценками/контракт