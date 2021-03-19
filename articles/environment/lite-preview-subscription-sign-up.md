---
title: Регистрация на подписку на предварительную версию — облегченное развертывание
description: Эта тема предоставляет информацию о том, как подписаться на развертывание и развернуть развертывание Project Operations Lite — от сделки до счетов-проформ.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290060"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Регистрация на подписку на предварительную версию — облегченное развертывание 

В этом разделе объясняется, как подписаться на предварительное предложение партнера и выполнить облегченное развертывание Dynamics 365 Project Operations — от сделки до счетов-проформ.

> [!NOTE]
> Этот процесс изменится в следующих выпусках Project Operations.

## <a name="prerequisites"></a>Предварительные условия

- Вы получите электронное письмо с приглашением принять участие в предварительной версии. Вы можете запросить предварительную версию на [веб-сайте Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Пользователь, развертывающий предварительную версию, должен иметь права глобального администратора клиента Azure.
- Ознакомьтесь со всеми условиями.

## <a name="subscribe"></a>Подписаться

Когда вы получите утверждение [запроса на предварительную версию](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), вы получите два предложения от Microsoft по электронной почте. Эти предложения позволяют развернуть предварительную версию Project Operations:

- Пробная предварительная версия Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations — пробная предварительная версия

> [!IMPORTANT]
> Только один человек, администратор клиента, в организации должен выполнять эту задачу. Если вы не являетесь подписчиком этого выпуска, подождите, пока ваша организация не будет зарегистрирована и вы не получите свои учетные данные.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Пробная предварительная версия Dynamics 365 Project Operations (CRM) 

Прежде чем начать, убедитесь, что вы вошли в браузер с рабочей учетной записью пользователя в клиенте, где вы хотите получить предварительную версию Project Operations.

1. Активируйте код первого предложения **Dynamics 365 Project Operations (CRM) — Пробная предварительная версия**, вставив его в URL-адрес браузера.

![Активировать предложение](./media/16RedeemFirstOfferNew.png)

2. Подтвердите ваш заказ.
![Подтвердите заказ](./media/17ConfirmOrderNew.png)

Вы увидите, что предложение подтверждения было успешно погашено.

![Подтверждение](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations — пробная предварительная версия

Повторите те же шаги, что и с первым кодом предложения. Обязательно добавьте второй код предложения, используя ту же учетную запись пользователя, которая использовалась с первым кодом предложения.

## <a name="assign-licenses"></a>Назначение лицензий

> [!IMPORTANT]
> Вам понадобится административный доступ к порталу Microsoft 365 вашей организации, чтобы выполнить следующие шаги.


1. Перейдите в [Центр администрирования Microsoft 365](https://portal.office.com/), чтобы назначить лицензии вашим пользователям.

![Домашняя страница центра администрирования](./media/14AdminPortal.png)

2. На странице **Активные пользователи** выберите пользователей, которым вы хотите назначить лицензию.

![Назначение лицензий](./media/15AssignLicenses.png)

3. Убедитесь, что выбраны лицензии **Предварительная версия Dynamics 365 Project Operations (CRM)** и **Предварительная версия Office 365 Project Operations**. 
4. Выберите **Сохранить изменения**.

## <a name="create-a-new-cds-environment"></a>Создание новой среды CDS

1. Подготовьте новую среду развертывания CDS Project Operations, следуя инструкциям в теме [Модель развертывания CDS](lite-deployment.md). При выборе типа среды обязательно используйте вариант **Пробная версия (по подписке)**.
![Создать окружение](./media/19CreateEnvironment.png)

2. Выберите параметр **Включение приложений Dynamics 365** и оставьте поле **Автоматически развернуть эти приложения** пустым.  
3. Выберите **Сохранить**, чтобы создать среду.

![Добавить базу данных](./media/20CreateEnvironment1.png)

4. После создания среды установите решение **Microsoft Dynamics 365 Project Operations**. 

![Установка решения](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Установка демонстрационных данных конфигурации и настройки CDS

Установите демонстрационные данные конфигурации и настройки CDS, следуя инструкциям в теме [Применение демонстрационных данных настройки и конфигурации](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]