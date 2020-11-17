---
title: Обеспечение оценки работы для проекта в процессе продаж
description: Как обеспечить оценки работы для проекта в процессе продаж в Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083238"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Обеспечение оценки работы для проекта в процессе продаж (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Во время процесса продаж можно разработать оценки продаж с нуля со строками предложения. Возможности [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] в [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] обеспечивают более научный и определенный способ работы с оценками продаж за счет разбивки рабочих элементов и связанных атрибутов, которые улучшают оценки для проекта в структурной декомпозиции работ.  
  
 После выигрыша продажи можно использовать связанную структурную декомпозицию работ в своем плане проекта, настраивая ее при необходимости для успешного завершения своего проекта.  
  
## <a name="link-a-project-to-a-quote-line"></a>Связь проекта со строкой предложения с расценками  
 При создании строки предложения с расценками на основе проекта можно создать новый проект из строки предложения с расценками. Затем можно использовать шаблоны проектов, которые являются либо предварительно настроенными стандартные планами проекта или финансовыми оценками, общими для организации, или скопировать план проекта и оценки из прошлого проекта. При создании проекта выбор шаблона проекта обеспечивает основу для настройки плана проекта, оценок и требований роли. После создания своего проекта из предложения с расценками проект автоматически связывается со строкой предложения с расценками.  
  
## <a name="project-estimate-components"></a>Компоненты оценки проекта  
 Структурная декомпозиция работ в проекте обеспечивает способ разбивки рабочих элементов на задачи, ведение иерархии задач и назначение оценки необходимых усилий для завершения каждой задачи. Также можно связать роли с задачей, чтобы указать оценку типа ресурса, который требуются для завершения задачи и расписание.  
  
 Структурная декомпозиция работ позволяет определить оценки по усилиям и расписанию. По умолчанию в проекте используются прайс-листы по умолчанию, определенные ранее. Стоимость и цены продажи, определенные в прайс-листах, помогают определить финансовые оценки по разбивке работ по проекту.  
  
 Если проект связан с предложением с расценками и в предложении с расценками есть другой прайс-лист, отличный от прайс-листа по умолчанию, прайс-лист предложения с расценками используется для финансовых оценок.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Импорт оценок проекта в предложение с расценками  
 После внесения оценок проекта в проект можно импортировать эти оценки в строку предложения с расценками:  
  
-   В **Сведения строки предложения с расценками** щелкните **Импортировать из оценок**. 

-   Выберите, следует ли импортировать оценки проекта по типу транзакции, роли или уровню узла структурной декомпозиции работ.  
  
### <a name="see-also"></a>См. также  
 [Руководство менеджера по проектам](../psa/project-manager-guide.md)