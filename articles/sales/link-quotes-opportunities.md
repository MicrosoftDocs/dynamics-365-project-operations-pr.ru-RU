---
title: Создание предложений с расценками по проектам на основе возможных сделок
description: В этом разделе представлена информация о создании предложения с расценками по проекту из возможной сделки.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898548"
---
# <a name="create-project-quotes-from-opportunities"></a>Создание предложений с расценками по проектам на основе возможных сделок

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Предложения с расценками могут быть созданы на основе возможных сделок проекта следующими способами:

- С вкладки **Предложения с расценками** на странице **Возможная сделка проекта**
- Из потока процесса продаж возможных сделок
- Обновив ссылку на возможную сделку в существующем предложении с расценками

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>С вкладки "Предложения с расценками" на странице "Возможная сделка проекта"

Чтобы создать предложение с расценками по проекту на основе возможной сделки, выполните следующие действия.

1. Откройте страницу **Возможная сделка проекта** и выберите вкладку **Предложения с расценками**. 
2. На вложенной сетке **Предложения с расценками** выберите **+** для создания нового предложения с расценками по проекту на основе возможной сделки. Все строки возможной сделки и связанные прайс-листы проекта копируются в новое предложение с расценками из возможной сделки.

## <a name="from-the-opportunity-sales-process-flow"></a>Из потока процесса продаж возможных сделок

Чтобы создать предложение с расценками из потока процесса продаж возможной сделки, выполните следующие действия.

1. В потоке процесса продаж возможной сделки откройте возможную сделку.
2. Выберите стадию **Квалифицировать**. 
3. Выберите **Далее**, затем выберите **+ Создать**, чтобы создать новое предложение с расценками. Большая часть информации на вкладке **Сводка** для этого нового предложения с расценками будет по умолчанию взята из возможной сделки. 
4. Введите любую необходимую информацию, которая отсутствует, или при необходимости обновите значения по умолчанию на вкладке **Сводка**.
5. Нажмите кнопку **Сохранить**. Новое предложение с расценками создается и связывается с возможной сделкой. Теперь вы можете просмотреть информацию о предложении с расценками на вкладке **Предложения с расценками** страницы **Возможная сделка**. 

   Процесс продаж возможной сделки переходит на следующий этап, **Предложить**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Обновив ссылку на возможную сделку в существующем предложении с расценками

Существующее предложение с расценками может быть связано с возможной сделкой. Выполните следующие шаги, чтобы обновить информацию о возможной сделке в существующем предложении с расценками.

1. Откройте страницу **Предложение с расценками** и выберите вкладку **Сводка**.
2. В поле **Возможная сделка** выберите возможную сделку, которую вы хотите связать с предложением с расценками. Вы можете увидеть предложение с расценками в сетке **Предложения с расценками** возможной сделки. 
3. Используя процесс продаж возможных сделок, возможная сделка может быть перемещена на следующий этап, **Предложить**. 

   Когда вы перемещаете возможную сделку на этот этап, вы можете выбрать это предложение с расценками из списка предложений с расценками, связанных с этой возможной сделкой. Выбор этого предложения с расценками означает, что вы продолжаете работать с ним.

   Все остальные предложения с расценками, связанные с возможной сделкой, будут по-прежнему доступны и активны, пока одно из них не будет реализовано. Вы можете вернуть процесс продаж обратно на предыдущий этап **Квалифицировать** и выбрать другое предложение с расценками, чтобы двигаться дальше с ним.
