---
title: Применение демонстрационных данных настройки и конфигурации — облегченное развертывание
description: Эта тема предоставляет информацию о том, как применить демонстрационные данные настройки и конфигурации для Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089135"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Применение демонстрационных данных настройки и конфигурации для Project Operations — облегченное развертывание 

_**Облегченное развертывание — от сделки до счетов-проформ_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Предварительные условия

Перед тем как начать настройку, вы должны иметь подготовленную среду Common Data Service (CDS) для Dynamics 365 Project Operations.


## <a name="instructions"></a>Инструкции

1. Загрузите [пакет основных данных](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Перейдите в папку *ProjOpsDemoDataSetupAndMaster — интегрированный CMT* и запустите исполняемый файл, *DataMigrationUtility*.
3. На странице 1 мастера настройки Common Data Service (CMT) выберите **Импортировать данные**, затем выберите **Продолжить**.

    ![Миграция конфигурации](./media/1ConfigurationMigration.png)

4. На странице 2 мастера CMT выберите **Microsoft 365** как **Тип развертывания**.
5. Установите флажки **Показать список доступных организаций** и **Показать расширенный**.
6. Выберите регион своего клиента, введите свои учетные данные, затем выберите **Войти**.

   ![Вход в конфигурацию](./media/2ConfigurationSignin.png)

7. На странице 3 из списка организаций в клиенте выберите организацию, в которую вы хотите импортировать демонстрационные данные, затем выберите **Войти**.
8. На странице 4 выберите ZIP-файл *MasterAndSetupData* из распакованной папки, *ProjOpsDemoDataSetupAndMaster — интегрированный CMT*.

   ![ZIP-файл](./media/3ZipFile.png)

   ![Выберите файл](./media/4SelectAFile.png)

9. После выбора ZIP-файла выберите **Импортировать данные**.

   ![Импортировать данные](./media/5ImportData.png)

10. Импорт будет выполняться примерно от двух до десяти минут в зависимости от скорости вашей сети. После его завершения выйдите из мастера CMT. 
11. Проверьте свою организацию на наличие данных по следующим 20 сущностям:

    -   Валюта
    -   Учетная запись
    -   Подразделение
    -   Контакт
    -   Единица
    -   Группа единиц измерения
    -   Прайс-лист
    -   Прайс-лист параметров проекта 
    -   Периодичность выставления счетов
    -   Категория резервируемого ресурса
    -   Категория проводки
    -   Категория расходов
    -   Цена роли
    -   Цена категории проводки
    -   Характеристика
    -   Резервируемый ресурс
    -   Назначение категории резервируемого ресурса
    -   Характеристика резервируемого ресурса

    ![Завершите импорт](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]