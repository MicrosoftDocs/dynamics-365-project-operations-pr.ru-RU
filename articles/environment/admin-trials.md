---
title: Регистрация на пробные версии Project Operations
description: В этой теме представлена информация о том, как развернуть пробную версию Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/04/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c8ae111acffb45fef1c2e6435849471ae331796
ms.sourcegitcommit: 05ee415093d152b5b9e1203c3db0ea7f0c5a75a5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2021
ms.locfileid: "7599229"
---
# <a name="sign-up-for-project-operations-trials"></a>Регистрация на пробные версии Project Operations 

_**Применяется к:** Project Operations для сценариев на основе ресурсов/отсутствия запасов, облегченное развертывание — от сделки до выставления счетов-проформ, Project Operations для сценариев на основе запасов/производства_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме объясняется, как подписаться на предварительное предложение партнера и развернуть среду Dynamics 365 Project Operations.

С новой пробной версией Project Operations вы можете автоматически развернуть любой из трех поддерживаемых сценариев развертывания, заполнив анкету, в которой даны рекомендации по наилучшему подходу к развертыванию. В этой теме представлена информация о том как:

- Воспользоваться пробным предложением.
- Начать подготовку.
- Настроить двойную запись.
- Подробнее о Project Operations. 

В следующей таблице приведены подробные сведения о новом пробном предложении.

| **Элемент предложения**               | **Подробности**                                  |
|------------------------------|----------------------------------------------|
| Тип предложения                   | Этот тип предложения является интересом администратора, поэтому для его использования требуется администратор клиента. |
| Использование предложения                    | Один раз для клиента                          |
| Срок действия предложения               | 30 календарных дней                             |
| Активации на клиента       | 1                                            |
| Количество пользователей              | 25                                           |
| Расширение                    | 1 продление, 30 календарных дней               |
| Количество пробных сред | 3                                            |


## <a name="admin-trial-details"></a>Сведения о пробной версии администратора
В следующей таблице перечислены сведения о пробной версии и их применимость к каждому типу развертывания.

| **Позиция**                      | **Облегченное**                                     | **Нескладируемые материалы** | **Складируемые материалы** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Предоставленные данные для настройки           | Да                                          | Да                       | Да (USSI)            |
| Транзакционные данные            | No                                           | No                        | No                    |
| Время подготовки в минутах  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Предварительные условия
Чтобы развернуть пробную версию Dynamics 365 Project Operations, должны быть выполнены следующие необходимые условия.

- Регистрация для [Dynamics 365 Project Operations — предварительная пробная версия](https://www.aka.ms/try-po).
- Пользователь, развертывающий предварительную версию, должен иметь права глобального администратора клиента Azure.

> [!IMPORTANT]
> Только один человек в организации, администратор клиента, должен выполнять эту задачу. Если вы не являетесь подписчиком этого выпуска, подождите, пока ваша организация не будет зарегистрирована и вы не получите свои учетные данные.

### <a name="dynamics-365-project-operations---preview-trial"></a>Пробная предварительная версия Dynamics 365 Project Operations 

Прежде чем начать, войдите в браузер с рабочей учетной записью пользователя в клиенте, где вы хотите получить предварительную версию Project Operations.

1. Активируйте код первого предложения **Dynamics 365 Project Operations — Пробная предварительная версия**, вставив его в URL-адрес браузера.

    ![Активировать предложение](./media/16RedeemFirstOfferNew.png)

2. Подтвердите ваш заказ.

    ![Подтвердите заказ](./media/17ConfirmOrderNew.png)

  Вы увидите, что предложение успешно принято.

   ![Подтверждение](./media/18OrderConfirmationNew.png)

  Вы будете перенаправлены в [центр администрирования Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Анкета и подготовка

1.  Перейдите в [центр администрирования Power Platform](https://admin.powerplatform.com/projectoperationstrial) и заполните анкету.  
2.  Просмотрите рекомендуемый тип развертывания и выберите **Начать настройку** для инициализации подготовки.
3.  Просмотрите условия и нажмите **Начать**.

   После начала подготовки вы будете перенаправлены в список сред в центре администрирования Power Platform. Пока идет подготовка, состояние вашей среды — **PreparingInstance**.
 
  Когда подготовка завершена, состояние вашей среды будет **Готово**. Подготовка среды включает развертывание демонстрационных данных.
 
4.  Выберите соответствующий URL-адрес Microsoft Dataverse и URL-адреса приложений Finance and Operations для проверки развертывания.

## <a name="configuring-dual-write"></a>Настройка двойной записи
Только для развертываний нескладируемых материалов настройте сопоставления с двойной записью. Для получения дополнительной информации см. [Версии сопоставления Project Operations с двойной записью](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Назначение лицензий

Вам понадобится административный доступ к порталу Microsoft 365 вашей организации, чтобы выполнить следующие шаги.

1. Перейти в [Центр администрирования Microsoft 365](https://portal.office.com/), чтобы назначить лицензии вашим пользователям.

   ![Домашняя страница центра администрирования](./media/14AdminPortal.png)

2. На странице **Активные пользователи** выберите пользователей, которым вы хотите назначить лицензию.

   ![Назначение лицензий](./media/15AssignLicenses.png)

3. Убедитесь, что выбрана лицензия **Предварительная версия Dynamics 365 Project Operations** и выберите **Сохранить изменения**.

## <a name="additional-resources"></a>Дополнительные ресурсы

Следующие ресурсы содержат полезные рекомендации, когда вы начнете свое знакомство с Project Operations:

- [Серия видео. Обзор Project Operations, подробные обзоры функций и дорожная карта](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Определение типа развертывания](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Вопросы и ответы

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Что делать, если мне нужен ALM или ELM для моей среды приложений Finance and Operations?

- Для партнеров, которым требуются возможности полного управления жизненным циклом среды, см. [Запрос лицензии на партнерскую среду-песочницу](https://experience.dynamics.com/requestlicense), чтобы ознакомиться с новым предложением партнера. 
- Для партнеров, которым требуется дополнительная информация о правах на внутреннее использование, см. [Права на внутреннее использование для облака и программного обеспечения (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Можно ли продлить пробную версию более чем на 30 дней?
Чтобы продлить пробную версию, выполните следующие действия.

1. В центре **администрирования Microsoft 365** выберите **Выставление счетов** > **Ваши продукты**.
2. Выберите **Dynamics 365 Project Operations (CE) — Предварительная версия (пробная)**.
3. В **Дата окончания срока действия**, выберите **Продлить дату**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Можно ли перейти с упрощенного развертывания на развертывание сценария на основе ресурсов/нескладируемых запасов?
В настоящее время нет поддержки для обновления среды с упрощенной на развертывание на основе нескладируемых запасов.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Можно ли получить доступ к Lifecycle Services (LCS) для моих сред Finance?  
№ Для этих пробных версий развертывание осуществляется через центр администрирования Power Platform. Доступ к среде Finance ограничен.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Можно ли установить пробную версию в существующей среде?
Если у вас есть существующая среда, вам будет разрешено установить упрощенное развертывание в существующей среде продаж Dataverse из центра администрирования Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]