---
title: Копирование контрактов по проектам
description: В этой теме предоставлена информация о копировании контрактов по проектам в Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083093"
---
# <a name="copying-project-contracts"></a>Копирование контрактов по проектам

_**Относится к:** развертывание Lite — от сделки до счетов-проформ_

Вы можете легко создавать новые контракты по проектам, делая копии существующих контрактов одним из двух способов: 

  - На странице списка **Контракты по проекту** выберите контракт по проекту, затем выберите **Копировать**.
  - На странице сведений **Контракта по проектам** выберите **Копировать**.

Откроется диалоговая страница, на которой вы можете выбрать параметры скопированного контракта. Следующие поля включены в диалог. В зависимости от выбранных значений в этом диалоге процесс копирования может измениться.

| **Поле** | **Релевантность, цель и руководство** | **Воздействие на последующие элементы** |
| --- | --- | --- |
| Описание | Введите тему целевого контракта. Когда откроется страница диалога, система установит в этом поле название исходного контракта с добавленным словом **копия**. | Это поле не оказывает влияния на последующую обработку. |
| Клиент | Ссылка на запись компании или учетную запись клиента. Когда откроется диалог, система установит в этом поле организацию из исходного контракта. | Это поле является основным клиентом в контракте. |
| Единица по контракту | Подразделение, отвечающее за реализацию проектов, связанных с этой сделкой. Когда откроется страница диалога, система установит его равным контрактной единице в исходном контракте. | Подрядное подразделение — это подразделение компании, которое будет выполнять проекты после закрытия сделки. У каждой контрактной единицы есть валюта. Эта валюта используется для отчета о предполагаемых и фактических затратах, понесенных во время проекта. |
| Валюта | Валюта транзакций по сделке. Когда откроется страница диалога, система установит в этом поле валюту из исходного контракта. Валюту невозможно изменить. Если это так, то поле **Копировать цены** всегда установлено на значение **Нет** , потому что прайс-листы в исходном контракте больше не актуальны. | Валюта используется для прайс-листов по умолчанию, для построения финансовых оценок на основе контракта и для выставления счетов клиенту, когда сделка реализована. |
| Запрошенная дата доставки | Дата доставки, запрошенная клиентом. | Эта дата используется в качестве конечной даты при создании дат выставления счетов с определенной периодичностью. |
| Скопировать цены | Указывает, следует ли копировать цены по контракту из исходного контракта. | Если в поле задано значение **Да** , ссылки на прайс-листы проекта и продуктов копируются из исходного контракта в целевой. Если выбрано значение **Нет** , прайс-листы устанавливаются по умолчанию на основе последних прайс-листов, которые были настроены для организации или параметров проекта. |

Когда вы выбираете **ОК** на странице диалога, система создает копию контракта на основе выбранных параметров. Новый контракт откроется.

Следующая информация не копируется из **Исходного контракта** в **Целевой контракт** :

  - Расписания счетов
  - Клиенты контракта и строки контракта
  - Ссылка на проект по строкам контракта на основе проекта
  - Сведения о бюджете клиента

Поскольку эта информация специфична для каждого контракта, эти поля и записи не копируются. Копируются строки контракта для проектов и продуктов, оценки по сведениям строки контракта и значения, которые нельзя превышать на уровне контракта. Значения по умолчанию цены и ставки затрат зависят от выбора в поле **Копировать цены** на странице диалога **Параметры копирования**.