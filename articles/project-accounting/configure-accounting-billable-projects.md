---
title: Настройка учета для тарифицируемых проектов
description: Этот тема предоставляет информацию о вариантах учета для оплачиваемых проектов.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 32031742b1a9580b9ebdbaf6952a998733be5e8f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896161"
---
# <a name="configure-accounting-for-billable-projects"></a>Настройка учета для тарифицируемых проектов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Dynamics 365 Project Operations поддерживает различные варианты учета для оплачиваемых проектов, которые включают транзакции по времени и материалам, а также по фиксированной цене.

- **Транзакции по времени и материалам**: счета за эти транзакции выставляются по мере выполнения работы на основе потребления часов, расходов, номенклатур или комиссий по проекту. Эти транзакционные издержки могут быть сопоставлены с выручкой по каждой транзакции, и счета по проекту выставляются по мере выполнения работ. Выручка по проекту также может быть начислена в момент совершения транзакции. При выставлении счета выручка признается и, если применимо, сторнируется начисленная выручка.
- **Транзакции с фиксированной ценой**: счета за эти транзакции выставляется в соответствии с графиком выставления счетов, который основан на контракте по проекту. Выручка по операциям с фиксированной ценой может быть признана при выставлении счета или рассчитана и разнесена периодически в соответствии с методами **Завершенный контракт** или **Завершенный процент**.

Проект считается оплачиваемым, если он связан с одной или несколькими строками контракта. Строка контракта по проекту определяет для себя, какой метод выставления счетов и какие типы транзакций разрешены.

Например, Fabrikam Robotics выиграла проектный контракт с корпорацией Adatum на оптимизацию оборудования. Adatum выплатит фиксированную сумму в размере 10 000 долларов США для покрытия понесенных проектных расходов. Это метод выставления счетов с фиксированной ценой. Счет за время и комиссии по проекту будет выставлен по факту использования. Это метод выставления счетов за время и материалы. Все работы будут отслеживаться в рамках единого проекта под названием "Оптимизация оборудования Adatum".

Участник проектной группы представляет восемь часов работы над проектом оптимизации оборудования Adatum. Когда менеджер проекта утверждает это время, система использует метод выставления счетов по времени и материалам для создания фактических проводок, счета-фактуры и счета. Эта транзакция не будет включена в расчет оценки выручки с фиксированной ценой.

Другой участник проектной группы отправляет командировочные расходы в размере 2000,00 долларов США в счет проекта оптимизации оборудования Adatum. Когда менеджер проекта утверждает эту отправку, система использует метод выставления счетов с фиксированной ценой для создания фактических проводок и счета для этих расходов по проекту. На основании этой транзакции клиенту не выставляется счет. Вместо этого ему будет выставлен счет с использованием отдельно настроенных этапов выставления счетов. Эта транзакция по расходам, вместе с оценками расходов, будет включена в расчет оценки выручки с фиксированной ценой.

Принципы учета операций по проекту определены в профилях затрат и доходов проекта. Для каждой транзакции по проекту система определяет соответствующий профиль затрат и доходов проекта, используя правила профиля затрат и доходов проекта, которые были настроены.

## <a name="define-project-cost-and-revenue-profiles"></a>Определение профилей затрат и доходов по проекту 

Профили затрат и доходов проекта определяют правила учета транзакций по проекту. Эти профили настраиваются в управлении и учете по проекту. 

Выполните следующие шаги, чтобы создать новый профиль затрат и доходов по проекту. 

1. Перейдите в раздел **Управление и учет по проектам** > **Настройка** > **Разноска** > **Профили затрат и доходов по проекту**. 
2. Выберите **Создать** для создания нового профиля затрат и доходов по проекту.
3. В поле **Имя** введите имя и краткое описание профиля.
4. В поле **Метод выставления счетов** выберите **Время и материалы** или **Фиксированная цена**.
5. Разверните экспресс-вкладку **Книга учета**. Поля на этой вкладке определяют принципы бухгалтерского учета, которые используются, когда транзакции проекта регистрируются с помощью журнала интеграции Project Operations, а затем выставляются счета-фактуры через предложение счета-фактуры проекта.
6. Выберите соответствующие данные в следующих полях на экспресс-вкладке **Книга учета**:

    - **Разноска затрат - часы**:

       - *Не ГК*: затраты для транзакций по времени не будут разноситься в книгу учета при разноске журнала интеграции Project Operations. Однако бухгалтер может выполнить разноску затрат с помощью функции "Разноска затрат" позже.
       - **Баланс**: затраты для транзакций по времени будут дебетированы на тип счета главной книги *НЗП - Себестоимость* и кредитованы на *Счет распределения заработной платы* в настройке разноски книги учета. Бухгалтер будет использовать функцию "Разноска затрат", чтобы периодически перемещать эти затраты из балансового счета в счет прибылей и убытков.
       - **Прибыль и убыток**: при разноске журнала интеграции Project Operations затраты в транзакции по времени будут дебетованы на тип счета главной книги *Стоимость* и кредитованы на *Счет распределения заработной платы*, определенные на вкладке **Стоимость** на странице **Настройка разноски книги учета** (**Управление и учет по проектам** \> **Настройка** \> **Разноска** \> **Настройка разноски книги учета**). Это наиболее распространенная настройка для транзакций по времени и материалам.
        - *Никогда не вносить в книгу учета*: затраты для транзакций по времени никогда не будет разноситься в книгу учета.

    - **Разноска себестоимости - Расходы**:

         - **Баланс**: при разноске журнала интеграции Project Operations стоимость транзакции расходов будет списана с типа счета книги учета *НЗП - Себестоимость*, как определено на вкладке **Стоимость** на странице **Настройка разноски ГК** и зачислена на корреспондирующий счет в строке журнала. Корреспондирующие счета по умолчанию для расходов определены в пункте **Управление и учет по проектам** > **Настройка** \> **Разноска** \> **Корреспондирующие счета по умолчанию для расходов**. Бухгалтер будет использовать функцию **Разноска затрат**, чтобы периодически перемещать эти затраты из балансового счета в счет прибылей и убытков.
        - **Прибыли и убытки**: при разноске журнала интеграции Project Operations стоимость транзакции расходов будет списана с типа счета книги учета *Стоимость*, как определено на вкладке **Стоимость** на странице **Настройка разноски ГК** и зачислена на корреспондирующий счет в строке журнала. Корреспондирующие счета по умолчанию для расходов определены в пункте **Управление и учет по проектам** \> **Настройка** \> **Разноска** \> **Корреспондирующие счета по умолчанию для расходов**.
       
    - **Выставление накладной по промежуточной накладной**:

        - **Баланс**: при разноске предложения по счету проекта транзакция по счету (этап выставления счетов) будет зачислена на тип счета книги учета *НЗП - Выставлены накладные - Промежуточные накладные*, как определено на вкладке **Доход** на странице **Настройка разноски книги учета**, и списывается с балансового счета клиента.
         - **Доходы и расходы**: при разноске предложения по счету проекта транзакция по счету (этап выставления счетов) будет зачислена на тип счета книги учета *Выручка по выставленным накладным - Промежуточные накладные*, как определено на вкладке **Доход** на странице **Настройка разноски книги учета**, и списывается с балансового счета клиента. Балансовые счета клиентов определены в пункте **Расчеты с клиентами** \> **Настройка** \> **Профили разноски по клиенту**.

   Когда вы определяете профили разноски для методов выставления счетов по времени и материалам, у вас есть возможность начислять доход по типу транзакции (часы, расходы и комиссии). Если для параметра **Начислить доход** установлено значение **Да**, операции продаж, для которых не выставлены счета, в журнале интеграции Project Operations будут записаны в главную книгу. Стоимость продажи списывается со счета **НЗП - сумма реализации** и зачисляется на счет **Начисленная выручка - Сумма реализации**, который был настроен на странице **Настройка разноски книги учета** на вкладке **Доход**. 
  
  > [!NOTE]
  > Опция **Начислить выручку** доступна только тогда, когда соответствующий тип транзакции **Стоимость** разносится на счет прибылей и убытков.
    
7. Разверните экспресс-вкладку **Оценка**. Поля на этой вкладке определяют параметры расчета для оценок выручки с фиксированной ценой. Поля на этой вкладке применяются только к профилям затрат и доходов проекта с методом выставления счетов **Фиксированная цена**.
8. Выберите соответствующие данные в следующих полях на экспресс-вкладке **Оценка**:

    - **Принцип, используемый для расчетов завершения проекта**:

        - **Завершенный контракт**: согласование затрат и признание выручки не происходит до конца проекта. Затраты отражаются как незавершенное производство в балансе до завершения проекта.
        - **Завершенный процент**: начисленная выручка рассчитывается и разносится в книгу учета каждый период на основе процента завершения проекта. Существует несколько методов расчета процента выполнения. Эти методы могут быть автоматическими в зависимости от конфигурации или ручными.
        - **Нет НЗП**: эта настройка используется для проектов с фиксированной ценой с коротким промежутком времени, когда счет-фактура и затраты происходят в один и тот же период. В этом случае значение поле **Выставление накладной по промежуточной накладной** на экспресс-вкладке **Книга учета** автоматически устанавливается на **Прибыли и убытки** для обеспечения признания выручки при выставлении счетов. Процесс оценки доходов не будет использоваться для этого профиля затрат и доходов по проекту.

    - **Принцип сопоставления**: это поле определяет, как рассчитанная стоимость продаж (начисленная выручка) будет разнесена в книгу учета.

        - Используя принцип **Стоимость продаж** система рассчитает стоимость продажи, сопоставив затраты и выручку, а затем разнеся ее как единую сумму.
        - Используя принцип **Производство и прибыль**, система разделит стоимость продажи на реализованные затраты и расчетную прибыль. Они разносятся отдельно.

    - **Шаблоны затрат**: позволяет группировать транзакции по проекту на основе типа транзакции и категории проекта и определять правила расчета процента завершения для этих групп.
    - **Коды периодов**: определите частоту, с которой рассчитываются оценки доходов для данного профиля затрат и доходов по проекту.
    - **Категории для оценки**: используется для разноски стоимости продаж (начисленной выручки) по проводкам проекта. Сначала настройте выделенную категорию проекта для типа транзакции **Сбор**, затем установите флаг **Оценить** для этой категории проектов. Затем, в зависимости от выбранного принципа сопоставления, выберите эту категорию проекта в значении **Продажи** или поле **Прибыль** в профиле затрат и доходов по проекту.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Примеры конфигураций профилей затрат и доходов по проекту

Время и материалы — нет НЗП

![Профиль затрат и доходов: время и материалы — нет НЗП](media/time-material-no-wip.png)

Время и материалы — НЗП (выручка)

![Профиль затрат и доходов: время и материалы — НЗП](media/time-material-with-wip.png)

Фиксированная цена — нет НЗП

![Профиль затрат и доходов: фиксированная цена — нет НЗП](media/fixed-price-no-wip.png)

Фиксированная цена — завершенный контракт

![Профиль затрат и доходов: фиксированная цена — завершенный контракт](media/fixed-price-completed-contract.png)

Фиксированная цена — процент завершения

![Профиль затрат и доходов: фиксированная цена — процент завершения](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Примеры событий учета для примеров профилей затрат и доходов по проекту.

| Событие учета                  | Время и материал — нет НЗП                       | Время и материал — НЗП                                                                                           | Фиксированная цена — нет НЗП                                            | Фиксированная цена — завершенный контракт                                                                            | Фиксированная цена — процент завершения                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Журналирование транзакций по времени    | Дебет — Стоимость <br>Кредит — Распределение заработной платы          | Дебет — Стоимость <br>Кредит — Распределение заработной платы <br>Дебет — Сумма продаж НЗП <br>Кредит — Начисленная выручка - Сумма реализации                | Дебет — Стоимость <br>Кредит — Распределение заработной платы                         | Дебет — Стоимость <br>Кредит — Распределение заработной платы                                                                    | Дебет — Стоимость <br>Кредит — Распределение заработной платы                       |
| Журналирование транзакций по расходам | Дебет — Стоимость <br>Кредит — Корреспондирующий счет для расходов | Дебет — Стоимость <br>Кредит — Корреспондирующий счет для расходов <br>Дебет — Сумма продаж НЗП <br>Кредит — Начисленная выручка - Сумма реализации      | Дебет — Стоимость <br>Кредит — Корреспондирующий счет для расходов                 | Дебет — Стоимость<br> Кредит — Корреспондирующий счет для расходов                                                            | Дебет — Стоимость <br>Кредит — Корреспондирующий счет для расходов               |
| Выставление счетов клиенту                | Дебет — Баланс клиента <br>Кредит — Выручка по счету | Дебет — Баланс клиента <br>Кредит — Выручка по счету <br>Кредит — НЗП - сумма реализации Дебет — Начисленная выручка - Сумма реализации | Дебет — Баланс клиента <br>Кредит — Выручка по выставленным накладным - Промежуточные накладные | Дебет — Баланс клиента <br>Кредит — НЗП - Выставлены накладные - Промежуточные накладные                                                  | Дебет — Баланс клиента <br>Кредит — НЗП - Выставлены накладные - Промежуточные накладные    |
| Разноска предполагаемого дохода             | Неприменимо                                   | Неприменимо                                                                                                    | Неприменимо                                                  | Дебет — НЗП - Себестоимость <br>Кредит — Стоимость                                                                         | Дебет — Сумма продаж НЗП <br>Кредит — Начисленная выручка - Сумма реализации |
| Устранить                         | Неприменимо                                   | Неприменимо                                                                                                    | Неприменимо                                                  | Кредит — НЗП - Себестоимость <br>Дебет — Стоимость <br>Кредит — Начисленная выручка - Сумма реализации <br>Дебет — НЗП - Выставлены накладные - Промежуточные накладные | Дебет — НЗП - Выставлены накладные - Промежуточные накладные <br>Кредит — Сумма продаж НЗП     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Настройка правил профиля затрат и доходов по проекту

Правила профиля затрат и доходов по проекту определяют профиль затрат и доходов по проекту, который должен использоваться при обработке любых оплачиваемых транзакций проекта. Определите правила, перейдя к пункту **Управление проектами и учет** \> **Настройка** \> **Разноска** \> **Правила профиля затрат и доходов по проекту**.

Правила могут быть определены контрактом проекта, группой проекта или конкретным проектом. Система всегда сначала выбирает правило с наивысшей степенью детализации.