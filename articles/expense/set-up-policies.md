---
title: Определение политик расходов
description: Вы можете определить политики расходов, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896657"
---
# <a name="define-expense-policies"></a>Определение политик расходов

_**Относится к:** Project Operations для сценариев на основе ресурсов/нескладируемых запасов, упрощенное развертывание — от сделки до выставления счетов-фактур_

Вы можете определить политики, которым ваши сотрудники должны следовать при вводе и отправке отчетов о расходах и заявок на командировки.         
Внедрение политик расходов может помочь вам эффективно управлять расходами.         

Например, вы можете установить политику расходов на гостиницу в Нью-Йорке, которая гласит, что суточные расходы не могут превышать 250 долларов США.       
Если работник отправляет отчет о расходах или заявку на командировку, где стоимость номера превышает эту сумму, система уведомит         
сотрудника, что сумма политики для расходов была превышена. Вы можете настроить сообщение, которое работник будет получать, когда вы        
определили политику.      
        
Можно определить три типа политик:         
        
- **Предупреждение**: позволяет работнику подавать отчет о расходах или заявку на командировку, но расходы будут отмечены для всех утверждающих и         
  для последующего отчета.        

- **Ошибка**: требует, чтобы работник пересмотрел расходы в соответствии с политикой перед отправкой отчета о расходах или заявки на командировку.        
 
 - **Обоснование**: требует от работника или менеджера ввести обоснование превышения суммы по политике перед подачей отчета о расходах или заявки на командировку.        

## <a name="policy-tips"></a>Советы по политикам
Вот несколько советов, которые могут помочь вам при создании новых политик для управления расходами: 

- Политики действуют по датам, что означает, что политика не вступит в силу, если она создана с датой, более поздней, чем дата, когда произошли расходы. Например, вы сегодня создаете новую политику, чтобы обеспечить максимальные расходы на питание в размере 50 долларов США. Любые существующие расходы, введенные на вчерашний день, не будут проверяться на соответствие этой политике.
- При создании политики для категории расходов, которая может быть детализирована, рассмотрите возможность добавления условия для типа строки расходов. Некоторые политики, например требование получения квитанции, могут не иметь смысла для детализированных строк. В этом случае политика применяется только к строке заголовка или строке без детализации. 
- По умолчанию политики управления расходами сравниваются с исходной сущностью. Для внутрихолдинговых сценариев вы можете вместо этого настроить политику, которая будет оцениваться по целевой сущности (заемной сущности). Чтобы применить политики к целевой сущности, включите функцию **Оценивать политику расходов по сравнению с юридическим лицом-заемщиком** в рабочей области **Управление функциями**.

## <a name="when-to-evaluate-policies"></a>Когда оценивать политики

В параметрах управления расходами вы можете выбрать оценку политик управления расходами при сохранении строки или при отправке отчета о расходах. Если вы выберете оценку при сохранении строки, пользователи получат более раннее представление о том, что им нужно сделать, чтобы сразу заполнить отчет о расходах. В противном случае вы можете отложить оценку политики и сэкономить время, выполнив проверку в конце, во время отправки в рабочий процесс.
