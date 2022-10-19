---
title: Перенос вех выставления счетов с полностью выставленными счетами при прямой миграции
description: В этой статье поясняется, как перенести этапы выставления счетов с фиксированной ценой, по которым выставлены счета клиенту, для открытых контрактов проектов перед датой ввода в эксплуатацию.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028718"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Перенос вех выставления счетов с полностью выставленными счетами при прямой миграции

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

## <a name="scenario"></a>Сценарий

Contoso вводит в эксплуатацию Microsoft Dynamics 365 Project Operations для сценариев на основе ресурсов/без запасов. В рамках прямой миграции специалисты по внедрению должны перенести открытые контракты проектов из старой системы. Некоторые контракты проектов включают строки контрактов, в которых используется метод выставления счетов с фиксированной ценой, и за которые уже частично выставлены счета конечному клиенту. Специалистам по внедрению необходимо перенести эти вехи выставления счетов с признаком **Счет клиента разнесен**, потому что они должны быть включены в общую стоимость контракта в целях признания выручки. Однако сальдо клиентов в модуле "Расчеты с клиентами" и главной книге не должны быть затронуты.

## <a name="solution"></a>Решение

### <a name="prerequisites"></a>Предварительные условия

- Необходимо установить Dynamics 365 Finance 10.0.24 или более позднюю версию.
- Среда, в которой будут выполняться действия по переносу, должна находиться в режиме обслуживания. Во время переноса вех не должны выполняться никакие другие действия.
- Действия по переносу должны выполняться в точности так, как описано здесь, и они могут использоваться только для прямой миграции. Майкрософт не поддерживает никакие другие варианты использования этой возможности.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Создание версии сопоставления двойной записи вех строки контракта интеграции Project Operations, предназначенной для прямой миграции 

1. Убедитесь, что целевое сопоставление для сущности **Промежуточные этапы строк контракта интеграции Project Operations** является актуальным. 

    1. В Finance выберите **Управление данными** \> **Сущности данных**, после чего выберите сущность **Промежуточные этапы строк контракта интеграции Project Operations**. 
    2. Выберите **Изменить целевые сопоставления**. 
    3. На странице **Сопоставить промежуточные данные с целевыми** выберите **Создать сопоставление** и подтвердите, что вы хотите создать сопоставление.

2. Остановите и обновите сопоставление двойной записи **Промежуточные этапы строк контракта интеграции Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Выберите **Управление данными** \> **Двойная запись**, выберите сопоставление и откройте сведения о нем. 
    2. Выберите **Остановить** и подождите, пока система останавливает сопоставление. 
    3. Выберите **Обновить таблицы**.

3. Добавьте сопоставление для состояния проводки.

    1. Выберите **Добавить сопоставление**.
    2. В новой строке в столбце **Приложения для управления финансами и операциями** выберите поле **TRANSSTATUS \[TRANSSTATUS\]**.
    3. В столбце **Microsoft Dataverse** выберите **msdyn\_invoicestatus \[Статус счета\]**.
    4. В столбце **Тип сопоставления** выберите стрелку вправо (**\>**).
    5. В появившемся диалоговом окне в поле **Направление синхронизации** выберите **Из Dataverse в приложения для управления финансами и операциями**.
    6. Выберите **Добавить преобразование**.
    7. В поле **Тип преобразования** выберите **ValueMap**.
    8. Выберите **Добавить сопоставление значений**.
    9. В левом поле введите **4**. В правом поле введите **192350001**. 
    10. Нажмите **Сохранить** и закройте диалоговое окно.

4. Выберите **Сохранить как**, чтобы сохранить версию сопоставления двойной записи. 
5. В области **Добавить таблицу** в поле **Издатель** выберите **Издатель по умолчанию**.
6. В поле **Версия** введите версию.
7. В поле **Описание** введите примечание об этой версии сопоставления, предназначенной для прямой миграции. 
8. Выберите **Сохранить**.
9. Запустите сопоставление.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Перенос вех, по которым выставлены счета, в среду Dataverse

1. В среде Dataverse для Project Operations создайте вехи со статусом счета **Готово для выставления счета**. На этом этапе не переносите вехи, по которым не были выставлены счета.

    > [!NOTE]
    > Прежде чем переносить вехи выставления счетов, убедитесь, что финансовые аналитики, связанные со строкой контракта по проекту, заданы должным образом. После завершения переноса отредактировать финансовые аналитики будет невозможно.

2. После переноса всех вех остановите следующие сопоставления двойной записи:

    - Промежуточные этапы строк контракта интеграции Project Operations (msdyn\_contractlinescheduleofvalues)
    - Фактические данные интеграции Project Operations (msdyn\_actuals)
    - Предложение по счетам по проекту V2 (счета)

    Чтобы остановить сопоставления, выполните следующие действия:

    1. В Finance выберите **Управление данными** \> **Двойная запись**, выберите сопоставление и откройте сведения о нем.
    2. Выберите **Остановить** и подождите, пока система останавливает сопоставление.

3. В среде Dataverse для Project Operations создайте и подтвердите счета-проформы для вех выставления счетов. 

    1. На карте сайта перейдите к контрактам проектов, выберите контракты, а затем выберите **Создать счета**.
    2. После создания счетов откройте их из меню **Счета** меню на карте сайта, а затем выберите **Подтвердить**.

    В результате этого шага создаются необходимые записи в среде Dataverse. Однако финансы и расчеты с клиентами при этом не затрагиваются, поскольку ранее перечисленные сопоставления двойной записи были остановлены.

4. После подтверждения всех счетов-проформ верните все сопоставления записи в их исходное состояние.

    1. Измените версию сопоставления двойной записи **Промежуточные этапы строк контракта интеграции Project Operations** (**msdyn\_contractlinescheduleofvalues**) обратно на исходную. 
    2. Выберите сопоставление двойной записи в списке сопоставлений, выберите **Версия сопоставления таблиц**, а затем выберите исходную версию сопоставления таблиц.
    3. Выберите **Сохранить**.
    4. Перезапустите следующие сопоставления двойной записи:

        - Промежуточные этапы строк контракта интеграции Project Operations (msdyn\_contractlinescheduleofvalues)
        - Фактические данные интеграции Project Operations (msdyn\_actuals)
        - Предложение по счетам по проекту V2 (счета)

Вехи перенесены, и система готова к следующим этапам процесса прямой миграции.