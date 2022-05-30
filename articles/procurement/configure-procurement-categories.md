---
title: Использование категорий закупаемой продукции в сочетании с заказами на покупку по проекту и ожидающими счетами поставщиков
description: В этой теме рассматривается, как настроить категории закупаемой продукции, которые можно использовать в сочетании с заказами на покупку по проектам и ожидающими счетами поставщиков
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613295"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Использование категорий закупаемой продукции в сочетании с заказами на покупку по проекту и ожидающими счетами поставщиков

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Специалисты по закупкам могут создавать и вести каталоги товаров и услуг, которые могут использоваться в заказах на покупку по проектам и ожидающих счетах поставщиков. [Каталоги закупаемой продукции](/dynamics365/supply-chain/procurement/procurement-catalogs) позволяют категоризировать покупки без необходимости настраивать и использовать каталог выпущенной продукции. Каждая категория закупаемой продукции может быть сопоставлена с категорией проекта для проводок по времени, расходам или товарам. После разноски ожидающего счета поставщика, в котором испольуется та или иная категория закупаемой продукции, система создает фактические значения времени, расходов и материалов по проекту, проводки по проекту и записи в субкнигах.

## <a name="minimum-version-requirements"></a>Минимальные требования к версиям

Для использования категорий закупаемой продукции в сочетании с заказами на покупку по проекту в в Microsoft Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов требуются следующие версии:

- Версия решения Project Operations Dataverse — 4.41.0.45 или более поздняя
- Среда Finance and Operations — версия 10.0.26 или более поздняя

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Запуск сопоставлений двойной записи для поддержки категорий закупаемой продукции

Убедитесь, что сопоставление для **сущности экспорта строки счета поставщика по проекту интеграции Project Operations msdyn\_projectvendorinvoicelines** использует версию 1.0.0.4 или более позднюю.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Включение функционального ключа для категорий закупаемой продукции

Выполните следующие действия, чтобы включить функциональнрсть для использования категорий закупаемой продукции в сочетании с заказами на покупку по проектам.

1. В Dynamics 365 Finance откройте рабочую область **Управление функциями**.
1. В списке функций найдите фукнцию **Использование категории закупаемой продукции в Project Operations для сценариев на основе ресурсов/не учитываемых в запасах номенклатур** и выберите **Включить**.

> [!IMPORTANT]
> В качестве предварительного условия необходимо также включить функцию **Включить ожидающие накладные поставщика в Project Operations для сценариев, основанных на ресурсах или не учитываемых в запасах**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Сопоставление категорий проектов в иерархии категорий закупаемой продукции

Выполните следующие действия, чтобы сопоставить категории проектов с категориями закупаемой продукции в иерархии **Категория закупаемой продукции**:

1. Перейдите в раздел **Закупки и источники \> Категории закупаемой продукции**.
1. Выберите **Изменить иерархию категорий**.
1. Выберите нужный узел иерархии категорий, а затем на вкладке **Назначение категорий проектов** свяжите этот узел с категорией проектов из категории **Время**, **Расход** или **Элемент проекта** (т. е. категории **Время по умолчанию** или **Расход по умолчанию**).
1. Выберите **Сохранить**.
1. Закройте страницу.

> [!NOTE]
> Сопоставление категории закупаемой продукции с категорией проекта не является обязательным. Если категория закупаемой продукции не сопоставлена, система будет использовать значение, заданное в поле **Товар** в разделе **Значения по умолчанию категорий проектов** на вкладке **Project Operations в Dynamics 365 Customer Engagement** страницы **Параметры модуля "Управление и учет по проектам"**.