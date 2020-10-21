---
title: Строки возможной сделки на основе проектов (Pro)
description: В этом разделе представлена информация о строках возможных сделок на основе проекта. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896387"
---
# <a name="project-based-opportunity-lines-pro"></a>Строки возможной сделки на основе проектов (Pro)

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Строки возможных сделок на основе проекта доступны только в возможных сделках на основе проекта. У записей возможных сделок на основе проекта в поле **Тип** установлено значение **На основе работы**.

Строки возможных сделок на основе проекта — это позиции строки, которые будут доставлены клиенту с использованием проекта. Однако проект не может быть привязан к строке возможной сделки на основе проекта. Проекты можно привязать к позициям строки из этапа **Предложение с расценками** и далее, потому что обычно возможная сделка находится на ранней стадии жизненного цикла сделки. Решение о том, сколько проектов будет использовано для выполнения работ для клиента, принимается позже на этапе продаж. Вы можете использовать фазу возможной сделки для определения отдельных компонентов поставки для клиента. Решения, касающиеся фактического количества проектов, используемых для доставки этих компонентов, могут быть отложены до тех пор, пока не станет известно больше информации о самой работе.

Ниже приведены поля в строке возможной сделки на основе проекта:

| **Поле** | **Расположение** | **Релевантность, цель и руководство** | **Воздействие на последующие элементы** |
| --- | --- | --- | --- |
| Тип продукта | Вкладке "Общие" (скрытая) | Вы можете выбрать один из следующих параметров:</br>- Сервис на основе проекта (доступно только при установленном Dynamics 365 Project Operations)</br>- Продукт (доступно только при установленных приложениях Project Operations и Dynamics 365 Sales) | Значение этого поля установлено на **Сервис на основе проекта**, когда вы создаете строку возможной сделки на основе проекта из сетки строк на основе проекта в возможной сделке. <br> Если вы измените или переопределите это значение, функциональность проекта не будет включена для ваших позиций строк на основе проекта. |
| Возможная сделка | Вкладка "Общие сведения" | Это поле доступно только для чтения и ссылается на родительскую запись возможной сделки, которой принадлежит данная позиция строки. | Это поле не оказывает влияния на последующую обработку. |
| Название | Вкладка "Общие сведения" | Это редактируемое текстовое поле можно использовать для краткого обозначения позиции строки. | Это значение переносится в строку предложения с расценками, когда вы создаете предложение с расценками из этой возможной сделки. |
| Бюджет клиента | Вкладка "Общие сведения" | Это редактируемое поле валюты можно использовать для отслеживания суммы, которую клиент готов потратить на эту позицию строки. | Это значение переносится в соответствующее поле в строке предложения с расценками, когда вы создаете предложение с расценками из этой возможной сделки. |
| Метод выставления счета | Вкладка "Общие сведения" | Это доступное для редактирования поле имеет следующие значения:</br>- Время и материал</br>- Фиксированная цена | Это значение переносится в соответствующее поле в строке предложения с расценками, когда вы создаете предложение с расценками из этой возможной сделки. После создания строки предложения с расценками поле блокируется и не может быть изменено. Назначьте этому полу как можно более точное значение. Если вам нужно изменить значение этого поля в строке предложения с расценками, удалите и заново создайте строку предложения с расценками. |