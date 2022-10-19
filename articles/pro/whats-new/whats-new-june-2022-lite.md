---
title: Новые возможности в июне 2022 г. — облегченное развертывание Project Operations
description: В этой статье содержится информация об исправлениях, доступных в выпуске облегченного развертывания Microsoft Dynamics 365 Project Operations за июнь 2022 года.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031209"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Новые возможности в июне 2022 г. — облегченное развертывание Project Operations

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Project Operations в среде Dataverse версии 4.43.0.77 или 4.43.0.119

## <a name="quality-updates"></a>Обновления качества

| Область функций | Номер ссылки | Обновление качества |
| --- | --- | --- |
| Субподряд | 2708885 | Исправлено сообщение об ошибке, которое появляется, когда пользователь создает запись заголовка резервирования резервируемого ресурса, в которой указан ни один резервируемый ресурс. |
| Планирование и отслеживание проектов | 2629441 | Исправлена логика запуска рабочего процесса, чтобы предотвратить бесконечный цикл при обновлении задач проекта. |
| Время и расходы | 2641209 | Импорт записей времени из назначений/резервирований должен сохранять ссылку на резервируемый ресурс. |
| Планирование и отслеживание проектов | 2651148 | Заголовок документа проекта должен быть защищен.|
| Планирование и отслеживание проектов | 2653145 | Добавлены проверки, гарантирующие невозможность создания записи проекта с недопустимыми символами в имени. |
| Время и расходы | 2654710 | Исправлена фильтрация на странице **Утверждения**. |
| Выставление счетов и ценообразование | 2667805 | Добавлены проверки, помогающие предотвратить создание фактических данных о продажах с выставлением счетов, если не существует резервных фактических данных о продажах без выставления счетов. |
| Выставление счетов и ценообразование | 2668378 | Добавлены проверки, помогающие предотвратить добавление пользовательского измерения цены, если не указано логическое имя и имя поля. |
| Время и расходы | 2700428 | Улучшена логика утверждений, чтобы гарантировать, что другие наборы утверждений для проекта могут быть обработаны, даже если один из наборов утверждений задерживается в системных заданиях. |