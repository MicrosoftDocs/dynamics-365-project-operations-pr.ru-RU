---
title: Обновите Project Operations в вашей среде Finance
description: В этой теме содержится информация о том, как обновить Project Operations в вашей среде Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816641"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Обновите Project Operations в вашей среде Finance

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_


В этой теме содержится информация о том, как обновить Dynamics 365 Project Operations в вашей среде Dynamics 365 Finance. Для обновления Project Operations до Обновление 5 (UR5) требуются три процедуры:

- [Импортируйте пакет в предварительный проект](#import)
- [Примените обновление](#apply)
- [Обновите вашу среду Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Импортируйте пакет в ваш проект LCS

1. Войдите в [Lifecycle Services (LCS)](https://lcs.dynamics.com/) как владелец проекта или менеджер среды.
2. Из списка проектов выберите ваш проект LCS.
3. На странице **Проект** в группе **Среды** откройте среду, которую вы хотите обновить.
4. Убедитесь, что среда работает. Если она не запущена, запустите среду.
5. В разделе **Новый выпуск** под **Доступные обновления**, выберите **Просмотр сведений об обновлении** для 10.0.15.

![Кнопка "Просмотр сведений об обновлении"](media/view-update.png)

6. На странице **Двоичные обновления** выберите **Сохранить пакет**.
7. На странице **Просмотреть и сохранить обновления** выберите **Сохранить пакет**.
8. В открывшейся области **Сохранить пакет в библиотеке активов** введите имя пакета и затем выберите **Сохранить пакет**.
9. Когда LCS закончит сохранение пакета, кнопка **Готово** будет включена. Нажмите кнопку **Готово**. LCS проверит пакет. Проверка может занять от нескольких минут до одного часа.


## <a name="apply-the-package-update"></a><a name="apply"></a>Примените обновление пакета

1. В LCS на страница **Сведения о среде**, выберите **Обслуживание** > **Применить обновления**.
2. В списке выберите пакет, который вы сохранили ранее, а затем выберите **Применить**.
3. Выбрать **Да**, чтобы подтвердить, что вы хотите развернуть пакет.

![Диалоговое окно подтверждения развертывания пакета](media/confirm-package-deployment.png)

4. Выбрать **Да**, чтобы подтвердить, что вы хотите обновить приложение.

![Диалоговое окно подтверждения обновления приложения](media/confirm-application-update.png)

Начнется развертывание и обновление приложения. 

На странице **Сведения о среде**, в правом верхнем углу, статус среды обновится до **Обслуживание**. Примерно через два часа обновление будет завершено. Информация о выпуске приложения обновится до **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** и статус среды обновится до **Развернута**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Обновите вашу среду Dataverse

1. Войдите в в [центр администрирования Power Platform](https://admin.powerplatform.com/).
2. В списке найдите и откройте среду, которую вы использовали для установки Project Operations.
3. На страница **Среды**, выберите **Ресурс** > **Приложения Dynamics 365**.
4. В списке найдите **Microsoft Dynamics 365 Project Operations**, а в столбец **Состояние** выберите **Доступно обновление**.
5. Выберите флажок **Я согласен с условиями обслуживания**, а затем выберите **Обновить**. Будет установлена последняя версия решения.

После завершения установки у вас будет установлена версия 4.5.0.134.

## <a name="configure-new-features"></a>Настройка новых функций

### <a name="enable-dual-write-mapping"></a>Включить сопоставление с двойной записью

После завершения обновления сред Finance и Dataverse, вы можете включить необходимые сопоставления с двойной записью. Выполните следующие процедуры, чтобы включить сопоставления с двойной записью.

- [Обновление настроек безопасности в среде Customer Engagement](#security)
- [Обновить информационные объекты](#refresh)
- [Обновите и запустите сопоставления с двойной записью](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Обновление настроек безопасности в среде Dataverse

Следующие обновления привилегий безопасности для объектов требуются как часть обновления UR5.

1. В вашей среде Dataverse перейдите в **Параметры**, а в группа **Система** выберите **Безопасность** .

![Параметры среды Dataverse](media/Picture21.png)

2. Выбор **ролей безопасности**.
3. В списке ролей выберите **пользователь приложения с двойной записью** и выберите вкладку **Настраиваемые объекты**. 
4. Убедитесь, что роль установлена на **Чтение** и разрешения **Добавить к** для:

      - **Тип обменного курса валют**
      - **План счетов** 
      - **Финансовый календарь** 
      - **Реестр**

5. После обновления роли безопасности перейдите к **Параметры** > **Безопасность** > **Рабочие группы**. Убедитесь, что роль **пользователь приложения с двойной записью** была применена к рабочей группе. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Обновить информационные объекты из обновления

1. В вашей среде Finance откройте рабочая область **Управление данными**, а затем откройте страница **Параметры структуры**.
2. На вкладка **Параметры объекта** выберите **Обновить список сущностей**.
3. Выбрать **Закрыть**, чтобы подтвердить обновление объекта.

 > [!NOTE]
 > Эта процедура займет от приблизительно 20 минут. Вы получите уведомление, когда обновление будет завершено.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Обновить сопоставления с двойной записью

1. В рабочая область **Управление данными** выберите **Двойная запись**.
2. Выбрать **Применить решения**, выберите оба решения в списке, а затем выберите **Применить**.
3. На странице **Двойная запись** выберите следующие сопоставления таблиц, а затем выберите **Остановить**.

    - **Фактические данные интеграции Project Operations (msdyn_actuals)**
    - **Категории расходов проекта интеграции Project Operations (msdyn_expensecategories)**
    - **Фактические данные интеграции Project Operations сущность экспорта расходов по проекту (msdyn_expenses)**

4. На странице **Версия сопоставления таблиц** примените новую версию сопоставления к каждому из трех объектов.
5. На странице **Двойная запись** выберите выполнение, чтобы перезапустить сопоставления.
6. Из списка сопоставлений выберите сопоставление **Реестр (msdyn_ledgers)** со всеми обязательными компонентами и выберите флажок **Начальная синхронизация**. 
7. В поле **Главная запись для начальной синхронизации** выберите **Приложения Finance and Operations**, а затем выберите **Выполнить**.
 
 ![Синхронизация сопоставления реестра](media/DW6.png)
 