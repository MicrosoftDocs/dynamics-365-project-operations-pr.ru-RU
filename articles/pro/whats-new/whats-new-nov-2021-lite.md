---
title: Что нового в ноябре 2021 г. — облегченное развертывание Project Operations
description: В этой статье содержится информация об обновлениях качества, доступных в выпуске облегченного развертывания Project Operations за ноябрь 2021 года.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913820"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Что нового в ноябре 2021 г. — облегченное развертывание Project Operations

_Относится к: облегченное развертывание — от сделки до счетов-проформ_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Функции, входящие в данный выпуск

В состав этого выпуска входят следующие функции:

- Программные интерфейсы (API) планирования проектов теперь поддерживают возможность создания и удаления сегментов проекта

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-in-dataverse"></a>Project Operations в Dataverse

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Выставление счетов и цены | 2358236 | Коррекция накладной должна допускать исправления со строками нулевой цены. |
| Управление ресурсами | 2410072 | Разрешить настройку ресурса, который назначен задаче в качестве менеджера проекта. |
| Выставление счетов и цены | 2430234 | Устранить проблему с расчетом эффективности затрат. |
| Время и расходы | 2436978 | Разрешить вводить время в формате чч:мм. |
| Выставление счетов и цены | 2448623 | Разрешить обновление прайс-листов после того, как они будут связаны с организационным подразделением. |
| Время и расходы | 2460396 | Разрешить удаление записи времени путем очистки ячейки. |
| Выставление счетов и цены | 2467386 | Разрешить удаление проекта, в котором есть задача, даже если задача связана с выигранным предложением. |
| Время и расходы | 2461744 | Представление **Мои неудачные утверждения** содержит только утверждения проектов на этапе **Отправлено**. |
| Время и расходы | 2464082 | Удалить ссылку из утверждений проекта на набор утверждений при совпадении целевого статуса. |
| Время и расходы | 2468108 | Задание расписания не должно устанавливать статус **Обработка** для набора утверждения. |
| Время и расходы | 2471503 | Удалить наборы утверждений, которым уже семь дней. |
| Выставление счетов и цены | 2480687 | Ссылку на строку предложения не должна удаляться при создании вехи строки предложения. |