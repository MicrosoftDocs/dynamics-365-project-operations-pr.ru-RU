---
title: Копирование предложений с расценками на основе проектов
description: Эта тема предоставляет информацию о том, как копировать предложения с расценками на основе проекта в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928601"
---
# <a name="copy-project-based-quotes"></a>Копирование предложений с расценками на основе проектов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Вы можете легко создать новое предложение с расценками по проекту, скопировав существующее. 

- Чтобы скопировать предложение с расценками по проекту, на странице списка **Предложения с расценками по проекту** или на странице сведений **Предложение с расценками по проекту** выберите предложение с расценками по проекту, которое вы хотите скопировать, затем выберите **Копировать**.

Откроется диалоговая страница, на которой вы можете ввести параметры копии. В следующей таблице перечислены поля, включенные в диалоговую страницу. В зависимости от выбранных значений процесс копирования может измениться.

| **Поле** | **Релевантность, цель и руководство** | **Воздействие на последующие элементы** |
| --- | --- | --- |
| Описание | Введите соответствующую тему или имя целевого предложения с расценками. Когда откроется диалог, система установит его на тему исходного предложения с расценками с добавленным словом **-копия**. | |
| Потенциальный клиент | Ссылка на запись компании или учетную запись клиента. Когда откроется диалог, система установит его для учетной записи в исходном предложении с расценками. | Это поле является основным клиентом в предложении с расценками. |
| Единица по контракту | Подразделение, отвечающее за реализацию проектов, связанных с этой сделкой.
Когда откроется диалог, система установит его для контрактной единицы в исходном предложении с расценками. | Подрядное подразделение — это подразделение компании, которое будет выполнять проекты после закрытия сделки. У каждой контрактной единицы есть валюта. Валюта используется для отчета о предполагаемых и фактических затратах, понесенных во время выполнения проекта. |
| Валюта | Это валюта транзакций по сделке. Когда откроется диалог, система установит его для валюты в исходном предложении с расценками. Это можно изменить, и если это изменится, в поле **Копировать цены** всегда будет установлено значение **Нет**. Это потому, что прайс-листы по исходному предложению с расценками больше не актуальны. | Валюта используется для прайс-листа по умолчанию, для построения финансовой оценки на основе предложения с расценками и, в конечном итоге, для выставления счета клиенту, когда сделка реализована. |
| Запрошенная дата доставки | Это дата доставки, запрошенная клиентом. | Это используется в качестве конечной даты при создании дат выставления счетов с определенной периодичностью. |
| Скопировать цены | Значение "Да/Нет" указывает, следует ли копировать цены предложения с расценками из исходного предложения с расценками. | Если выбрано значение **Да**, прайс-лист проекта и ссылки на прайс-лист продуктов копируются из исходного предложения с расценками в целевое предложение с расценками. Если выбрано значение **Нет**, прайс-листы устанавливаются по умолчанию на основе последних прайс-листов, которые были настроены для учетной записи или параметров проекта. |

Когда вы выбираете **ОК** на странице диалога, система создает копию предложения с расценками по проекту на основе параметров, выбранных в диалоговом окне. Откроется новое предложение с расценками по проекту. 

> [!NOTE]
> Следующая информация не копируется из исходного предложения с расценками в целевое:
>
> - Расписания счетов
> - Предложение с расценками и клиенты строки предложения с расценками
> - Ссылка на проект в строках предложения с расценками на основе проекта — информация о бюджете клиента
>
>Поскольку эта информация очень специфична для каждого предложения с расценками, эти поля и записи не копируются. Копируются строки предложения для проектов и продуктов, оценки деталей строки предложения с расценками и значения, которые нельзя превышать на уровне предложения с расценками. Значения по умолчанию цены и ставки затрат зависят от параметра **Копировать цены**, выбранного на странице диалога **Параметры копирования**.