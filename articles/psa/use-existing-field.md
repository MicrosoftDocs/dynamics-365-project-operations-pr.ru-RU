---
title: измерение цен существующего поля в Project Service как измерение цен
description: В этом разделе представлена информация об использовании существующих полей Project Service в качестве измерений цен.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144189"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>измерение цен существующего поля в Project Service как измерение цен

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) имеет много полей в сущности **Фактические значения**, которые можно использовать в качестве измерений цен для ценообразования на основе ресурсов в проектных организациях. Например, общее поле **Резервируемый ресурс**. Небольшие компании, которые имеют менее 20-30 оплачиваемых ресурсов, могут обнаружить, что иметь тарифы выставления счетов и нормы затрат, специфичные для каждого ресурса — более простой подход. Однако по мере роста оплачиваемой рабочей силы, особые ставки могут стать проблематичными для поддержания, так как стоимость ресурсов и тарифы выставления счетов начинают меняться по мере продвижения ресурсов, получения большего опыта или приобретения других наборов навыков. Поскольку этот подход по-прежнему работает для компаний определенного размера, см. [Использование резервируемого ресурса как измерения цен](bookable-resource-pricing-dimension.md) чтобы понять, как можно использовать существующее поле Project Service в качестве измерения цен.

Другим примером является категория проводки. Клиенты и исполнители использовали категорию проводки в PSA для классификации работы и использования поля для расчета цены и расхода в зависимости от категории работы. Дополнительные сведения см. в разделе [Использование категории проводки как измерение цен](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]