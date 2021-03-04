---
title: Новые возможности в феврале 2021 г. — Project Operations для сценариев на основе ресурсов/без запасов
description: Эта тема предоставляет информацию об обновлениях качества, доступных в выпуске Project Operations за февраль 2021 г., для сценариев на основе ресурсов/без запасов.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141345"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Новые возможности в феврале 2021 г. — Project Operations для сценариев на основе ресурсов/без запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

Эта тема применяется к следующим компонентам и версиям Dynamics 365 Project Operations:

- Project Operations в среде Dataverse 4.7.0.95
- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.16 

## <a name="quality-updates"></a>Обновления качества

### <a name="project-operations-on-dataverse"></a>Project Operations на Dataverse

| **Область функций** | **Номер ссылки** | **Обновление качества** |
| --- | --- | --- |
| **Выставление счетов и цены** | 2053736 | Сведения строки счета теперь доступны в **Счет** > **Дополнительные сведения**. |
| **Выставление счетов и цены** | 2122613 | Действия **Активировать** и **Деактивировать** были удалены из сущностей ассоциации **Прайс-лист**. |
| **Выставление счетов и цены** | 2128606 | Решена проблема с **ullReferenceException** в подключаемый модуль **GetEstimatesForProject**. |
| **Развертывание и конфигурация** | 2139346 | Решена проблема с импортом неуправляемого решения **Dynamics365ProjectOperationsDualWrite**. |
| **Развертывание и конфигурация** | 2140569 | Решение Project нельзя устанавливать в средах Dataverse Teams. |
| **Развертывание и конфигурация** | 2086991 | Ограниченная настройка локализации веб-ресурсов. |
| **Управление возможными сделками** | 2136794 | Отображать правильное сообщение об ошибке, когда процессы **Подтвердить счет** или **Отметить счет как оплаченный** не работают. |
| **Управление возможными сделками** | 2139330 | Смена руководителя проекта по проекту не должна возвращать для ответственной компании значение по умолчанию. |
| **Управление возможными сделками** | 2146376 | Исправленная сумма налога в не подлежащей уплате фактической стоимости создается на основе подтверждения счета. |
| **Планирование и отслеживание проектов** | 2099879 | При развертывании среды Dataverse необходимо создать категорию транзакции по умолчанию со статическим идентификатором, а не создавать случайную категорию для каждой среды. |
| **Планирование и отслеживание проектов** | 2128577 | Исправлены привилегии пользователя службы Project на обновление категории транзакции при назначении ресурса. |
| **Планирование и отслеживание проектов** | 2164035 | Исправлены проблемы с функция **Копировать проект**. |
| **Запись времени** | 2129161 | Применяются более жесткие ограничения, чтобы пользователи не могли изменить и обновить введенную или утвержденную запись времени. |
| **Запись времени** | 2103572 | Утверждение времени для несвязанных с проектом записей времени не должно искать роль утверждающего проекта. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Управление и учет по проектам в Dynamics 365 Finance 

Для получения дополнительной информации об Управлении и учете по проектам в Dynamics 365 Finance, см. [Что нового в январе 2021 г. — Project Operations для сценариев на основе ресурсов/без запасов](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Нормативные обновления

Для получения информации о нормативных обновлениях для приложений Finance and Operations см. раздел [Нормативные обновления](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Еще один способ узнать о нормативных обновлениях — войти в Lifecycle Services (LCS) и просмотреть запланированные нормативные обновления с помощью инструмента поиска проблем. Поиск проблем позволяет искать по стране, типу функции и выпуску.


[!INCLUDE[footer-include](../includes/footer-banner.md)]