---
title: Обновить домашнюю страницу
description: В этом разделе показан размещение важные сведения о новых возможностях и измененных в Dynamics 365 Project Service Automation, и о процессе обновления до новейшей версии.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083269"
---
# <a name="upgrade-home-page"></a>Обновить домашнюю страницу

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Обновление с версии PSA 2.x или 1.x до версии 3.x

### <a name="new-instances"></a>Новые экземпляры

По состоянию на 17 мая 2019 года, когда Project Service Automation выбран во время подготовки нового экземпляра, по умолчанию устанавливается версия 3.x.

### <a name="existing-instances"></a>Существующие экземпляры

Ранее клиенты, имеющие экземпляр PSA версии 2.x и нуждающиеся в обновлении до версии 3.x, которая является версией PSA на основе единого интерфейса клиента (UCI), должны были обращаться в службу поддержки Microsoft и предоставлять подробную информацию о своем экземпляре, чтобы служба поддержки могла включить экземпляр для обновления до версии 3.x. С 1 марта 2020 года клиенты, имеющие экземпляр PSA версии 2.x и нуждающиеся в обновлении до версии 3.x, смогут обновлять свои экземпляры непосредственно с портала администрирования, не обращаясь в службу поддержки Microsoft.  

> [!NOTE]
> PSA версии 3.x включает в себя значительные изменения. Она была построена в рамках единого интерфейса для обеспечения улучшенный интерфейс пользователя. Модернизированное приложение обеспечивает согласованный единый пользовательский интерфейс, отвечающий принципам гибкого дизайна для оптимального просмотра на любом экране или устройстве. В приложении произошли другие изменения. Некоторые из этих областей, которые были изменены, содержат цены, резервирование и назначение ресурсов, время, расходы и утверждения.

Перед началом процесса обновления рекомендуется выполнить следующие задачи:

- Убедитесь, что на указанном экземпляре установлены как Dynamics 365 Field Service, так и Project Service Automation. Если оба решения установятся, необходимо запланировать обновление обоих, прежде чем возобновить регулярное использование экземпляра.
- Внимательно просмотрите следующие разделы. Информированность и понимание изменений между версиями помогут вам в процессе обновления. Эти разделы содержат нужные сведения об основных изменениях в PSA, а также замечания и рекомендации по планированию обновления до версии 3.x.

    - [Что нового или измененного в Project Service Automation версии 3](whats-new-changed-v3.md)
    - [Моменты, которые следует учитывать при обновлении Project Service Automation версии 2.x или 1.x до версии 3](upgrade-v3.md)

- Обновите свой экземпляр в песочнице, чтобы оценить изменения в вашей реализации перед обновлением производственного экземпляра.

После того, как вы ознакомились с разделами, которые были упомянуты ранее, и готовы обновиться до PSA версии 3.x или версии на основе UCI, отправьте запрос в службу поддержки Майкрософт, чтобы сделать обновление доступным в Центре администрирования. В вашем запросе укажите детали вашего экземпляра.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Более старых версии (PSA версии 2.x) во вновь созданном экземпляре

По состоянию на 17-е мая 2019 года все новые экземпляры будут иметь UCI в качестве клиента по умолчанию. Для согласования с этим изменением, PSA версии 3.x и Field Service версии 8.x будут предоставлены по умолчанию, поскольку эти версии предназначены для работы с клиентом UCI.

Начиная с 1 марта 2020 года клиенты Dynamics PSA больше не смогут создавать новые среды с более старыми версиями PSA, например PSA версии 2.x или ниже. Любая новая среда будет иметь только версию 3.x PSA.

> [!NOTE]
> Для получения наилучших результатов при использовании более старых версий приложений Field Service и PSA перейдите на страницу **Параметры системы** и для поля **Использовать только единый интерфейс (рекомендуется)** , выберите **Нет** поскольку эти версии не предназначены для правильной загрузки в UCI. После отключения UCI можно открыть и запустить эти версии Field Service и PSA, используя старый веб-клиент. 