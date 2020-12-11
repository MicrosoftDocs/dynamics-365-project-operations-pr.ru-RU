---
title: Новые возможности в ноябре 2020 года — облегченное развертывание Project Operations — от сделки до счетов-проформ
description: Эта тема предоставляет информацию об обновлениях качества, доступных в облегченном развертывании Project Operations выпуска за ноябрь 2020 г., — от сделки до выставления счетов-проформ.
author: sigitac
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa95406a27e6d32d2be75303904547b59f24c8b2
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367192"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Новые возможности в ноябре 2020 года — облегченное развертывание Project Operations — от сделки до счетов-проформ

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

В следующей таблице перечислены обновления для Project Operations в среде CDS версии 4.4.0.70.

| Область функций                 | Номер ссылки | Обновление качества                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Управление возможными сделками       | 2036993          | Строка сметы и строки контракта на назначение ресурсов обновляются в выигрышных предложениях с расценками, если строка предложения с расценками имеет тип **Все задачи**.                                                 |
|   Управление возможными сделками       | 2071514          | Невозможно создать счет для вехи с фиксированной ценой по контракту, в котором включено выставление счетов на основе задач.                                                                          |
| Выставление счетов и ценообразование          | 2070392          | Строки контракта по проекту в счете увеличиваются каждый раз, когда выбирается **Обновление проводок по счету**.                                                                       |
| Планирование проектов             | 2043336          | Невозможно удалить запись участника рабочей группы проекта.                                                                                                                                    |
| Планирование проектов             | 2046013          | Несогласованное поведение для столбцов тегов оценок во время загрузки и при изменении типа временной фазы.                                                                                   |
| Планирование проектов             | 2046647          | Время начала и окончания отличается на час, когда требования к ресурсам формируются из участников проектной группы.                                                                      |
| Планирование проектов             | 2053879          | (Согласно предстоящему выпуску CDS) PublishUnassignedAssignments прерывает попытку сохранить задачу, когда появляется ошибка "Значение, переданное для ConditionOperator.In, пусто". |
| Планирование проектов             | 2055501          | Оставление поля **Дата начала проекта** пустым вызывает сбой в расписании.                                                                                                      |
| Планирование проектов             | 2066817          | Невозможно создать универсальный ресурс с помощью средства выбора людей на вкладке **Задачи**.                                                                                               |
| Планирование проектов             | 2067034          | Кнопка **Показать сведения** недоступна на странице **Сведения о задаче**.                                                                                                         |
| Управление ресурсами          | 2046667          | Универсальные участники рабочей группы не удаляются даже после того, как все ресурсы заполнены.                                                                                                     |
| Время и быстрая запись расходов | 2047499          | Кнопка **Создать** на странице ввода времени открывает страницу **Создать подпись электронной почты**.                                                                                               |
| Время и быстрая запись расходов | 2059859          | Неожиданное всплывающее окно открывается при создании записи о расходе.                                                                                                                         |
| Прочее                        | 2044181          | [Удаление заказа на покупку] — Ошибка "Запись недоступна" возникает при попытке удалить решения ядра **msdyn_ProjectServiceCore_Patch** и msdyn Project Service.        |