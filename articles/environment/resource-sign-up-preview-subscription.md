---
title: Регистрация на подписки на предварительную версию Project Operations для сценариев ресурсов/отсутствия запасов
description: Эта тема предоставляет информацию о том, как подписаться и развернуть roject Operations для сценариев на основе ресурсов/отсутствия запасов.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949042"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Регистрация на подписки на предварительную версию Project Operations для сценариев ресурсов/отсутствия запасов

_**Относится к:** Project Operations для сценариев на основе ресурсов/без запасов_

В этой теме объясняется, как подписаться на предварительную версию/предложение партнера и развернуть среду Project Operations для сценариев на основе ресурсов/отсутствия запасов.

## <a name="prerequisites"></a>Предварительные условия

- Вы получите электронное письмо с приглашением принять участие в предварительной версии. Вы можете запросить предварительную версию на [веб-сайте Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Пользователь, развертывающий предварительную версию, должен иметь права глобального администратора клиента Azure.
- Для развертывания среды Finance требуется действующая подписка Azure, за которую будет взиматься плата за среду. Вы можете использовать существующую подписку вашей организации или использовать [пробную версию Azure](https://azure.microsoft.com/en-us/free/) для начала. Среда CDS будет предоставляться бесплатно в течение ограниченного 30-дневного периода.

## <a name="subscribe"></a>Подписаться

Когда ваш [запрос на предварительную версию](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) будет утвержден, вы получите два предложения от Microsoft по электронной почте. Эти предложения позволяют развернуть предварительную версию Project Operations:

- Dynamics 365 Project Operations — пробная предварительная версия
- Пробная предварительная версия Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Только один человек, администратор клиента, в организации должен выполнять эту задачу. Если вы не являетесь подписчиком этого выпуска, подождите, пока ваша организация не будет зарегистрирована и вы не получите свои учетные данные.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations — пробная предварительная версия

1. Активируйте первое предложение, **Пробная версия Dynamics 365 Project Operations**, используя URL-адрес, указанный в приветственном письме.

![Первое предложение](./media/1FirstOffer.png)

2. Убедитесь, что вы вошли в систему как пользователь, принадлежащий к организации, которая будет подписываться на службу.
3. Продолжайте активировать предложение. 
4. Выберите **Да, добавить в мою учетную запись**.

![Активировать предложение](./media/2RedeemFirstOffer.png)

![Подтвердить предложение](./media/3ConfirmFirstOffer.png)

![Предложение активировано](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Пробная предварительная версия Dynamics 365 Finance

Повторите те же шаги со вторым предложением из приветственного письма.

## <a name="assign-licenses"></a>Назначение лицензий

> [!IMPORTANT]
> Вам понадобится административный доступ к порталу Office 365 вашей организации, чтобы выполнить следующие шаги.

1. Перейдите в [Центр администрирования Microsoft 365](https://portal.office.com/), чтобы назначить лицензии вашим пользователям.

![Портал администрирования Office](./media/5OfficeAdminPortal.png)

2. На странице **Активные пользователи** выберите пользователей, которым вы хотите назначить лицензию.

![Назначение лицензий](./media/6AssignLicenses.png)

3. Убедитесь, что выбрана лицензия Project Operations, и выберите **Сохранить изменения**. 

> [!NOTE]
> Пробное предложение Finance не нужно назначать пользователю.

## <a name="start-a-new-project-in-lcs"></a>Запуск нового проекта в LCS

Создайте новый проект LCS, как описано в теме [Запуск нового проекта в LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Добавление подписки Azure в проект LCS

Чтобы выполнить эту задачу, выполните действия, описанные в теме [Добавление подписки Azure в проект LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Развертывание демонстрационной среды Finance с помощью Project Operations для сценариев, связанных с ресурсами/отсутствием запасов

Следуйте инструкциям в теме [Подготовка новой среды](resource-provision-new-environment.md) для завершения развертывания. Используйте тип развертывания [демонстрационной среды](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) для предварительного просмотра.

## <a name="install-cds-setup-and-configuration-data"></a>Установка данных настройки и конфигурации CDS

Установите данные настройки и конфигурации CDS, как описано в теме [Настройка и применение данных конфигурации в Common Data Service](resource-apply-pro-setup-config-data.md).

