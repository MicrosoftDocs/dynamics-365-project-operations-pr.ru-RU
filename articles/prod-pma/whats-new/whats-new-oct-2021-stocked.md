---
title: Новые возможности или изменения в октябре 2021 г. — Project Operations для сценариев на основе запасов/производственных заказов
description: Эта статья содержит информацию об обновлениях качества, доступных в выпуске Project Operations за октябрь 2021 года для сценариев на основе запасов/производства.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029959"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Новые возможности или изменения в октябре 2021 г. — Project Operations для сценариев на основе запасов/производственных заказов

_**Применяется к:** Project Operations для сценариев на основе запасов/производственных заказов_

Эта статья применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Управление и учет по проектам в среде Dynamics 365 Finance версии 10.0.22
 
## <a name="quality-updates"></a>Обновления качества

| Область функций | Номер ссылки | Обновление качества |
|--------------|------------------|----------------|
| Управление и учет по проектам | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Незавершенное производство (НЗП) по проекту и суммы начисленной выручки неправильно сторнируются при разноске внутрихолдингового счета-фактуры клиента. |
| Управление и учет по проектам | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Функция **Предотвратить закрытие проекта, если существуют открытые транзакции** не работает. |
| Управление и учет по проектам | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Классификация выставления счетов в накладной с произвольным текстом не заполняет автоматически измерения из проектов, когда эта функция включена. |
| Управление и учет по проектам | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | В внутрихолдинговых сценариях суммы незавершенного производства (НЗП) и суммы начисленной выручки неправильно сторнируются при разноске счета-фактуры по проекту. |
| Управление и учет по проектам | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Суммы дебета и кредита меняются местами, когда надстройка Microsoft Excel используется с журналом расходов по проекту и поле **Тип корр. счета** установлено на **Проект**. |
| Управление и учет по проектам | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Сумма, разнесенная по проводкам по проекту, завышена в заказе на закупку по проекту, который включает складские номенклатуры и имеет невычитаемые суммы налога, когда флажок **UseTax** отмечен. |
| Управление и учет по проектам | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Система разделяет сумму между отчетами о прибылях и убытках по проекту и отчетами о НЗП по проекту. |
| Управление и учет по проектам | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Запасы в наличии неверны после корректировки требования по частично возвращенной номенклатуре. |
| Управление и учет по проектам | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Имена ресурсов дублируются в Project Operations, когда они редактируются в Microsoft Project. |
| Управление и учет по проектам | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Отчеты о внутрихолдинговых расходах, в которых есть затраты по внутрихолдинговым ожидающим счетам поставщиков по расчетам с поставщиками, сначала разносятся в тип разноски **Проект - затраты НЗП**. Однако во время обработки связанные с оценкой затраты разносятся с типом разноски **Затраты проекта** вместо ожидаемого типа разноски **Внутрихолдинговая стоимость**. |
| Управление и учет по проектам | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Результаты удержания поставщика в проводках по расходам по проекту не отображаются. |
| Управление и учет по проектам | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Табель учета рабочего времени должен округлять сумму транзакции в валюте транзакции до указанного числа десятичных знаков для всех распределений бухгалтерского учета и записей распределения общего журнала. |
| Управление и учет по проектам | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Количества потребностей в номенклатурах проекта автоматически обновляются при утверждении плановых заказов. |
| Управление и учет по проектам | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Номер ваучера, баланс поставщика типа транзакции и номер счета не могут быть сторнированы в счете-фактуре предоплаты заказа на покупку. |
| Управление и учет по проектам | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Счет-фактура внутрихолдингового поставщика не работает, если включена интеграция накладных поставщика. |
| Управление и учет по проектам | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Когда вы создаете журнал расходов по проекту, сумма затрат отображается в поле **Кредит**. |
| Управление и учет по проектам | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Условия оплаты по счетам-фактурам проекта не работают должным образом. |
| Управление и учет по проектам | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Ваучеры табеля учета рабочего времени можно использовать повторно, если номерная серия настроена как непрерывная. |
| Управление и учет по проектам | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | ФРАНЦИЯ: логика **Сумма удержания вручную** не соответствует логике **Сумма автоматического удержания** в предложении счета-фактуры контракта по проекту. |
| Управление и учет по проектам | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Когда удержание поставщика разблокировано, в разноске ваучера есть неверные дополнительные строки. |
| Управление и учет по проектам | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Когда поле **Дата счета** на странице **Создать предложение по накладной** изменяется, может возникнуть следующая ошибка: «Ссылка на объект не указывает на экземпляр объекта». |
| Управление и учет по проектам | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ошибка возникает, когда вы пытаетесь утвердить табель учета времени из рабочего процесса **TSLine**, и существует политика табеля учета времени для субботы и воскресенья. |
| Управление и учет по проектам | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Тип номенклатуры начального сальдо проекта исключен из **Сводные данные о транзакциях предложения по счету-фактуре**, когда рассчитывается общая сумма счета-фактуры предложения по счету-фактуре. |
| Управление и учет по проектам | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Если стоимость потребления в производственном заказе проекта равна 0 (нулю), при попытке оценить возникает следующая ошибка: «Попытка деления на нуль». |
| Управление и учет по проектам | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Мобильное приложение табеля учета рабочего времени проекта для Android перестает отвечать. Проблема связана с **TimeEntryDataManager ArgumentNullException**. |
| Управление и учет по проектам | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Журнал интеграции Project Operations дает сбой при его разноске из-за отсутствия измерений для учетной записи. Однако учетная запись, в которой отсутствуют измерения, не является учетной записью, в которую вы выполняете разноску. |
| Управление и учет по проектам | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Фильтр **ToDate** в поиске не очищается, когда он удаляется из диалогового окна **Выбрать** на странице **Разнести затраты**. |
| Управление и учет по проектам | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Сбросить все распределение** терпит неудачу и показывает ошибку для табелей учета рабочего времени, созданных для проекта типа **Только время**. |
| Управление и учет по проектам | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Вкладка **Проект** недоступна для редактирования в незавершенном счете-фактуре поставщика, когда номенклатуре присвоена категория закупки. |
| Управление и учет по проектам | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Панель навигации отсутствует, если вы не вошли в Project Operations Dataverse. |
| Управление и учет по проектам | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Для проводок корректировки внутрихолдингового проекта возникают проблемы в компании-получателе. |
| Управление и учет по проектам | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Утвержденные затраты для проекта рассчитывают неправильное количество и себестоимость, если заказ на покупку был обработан **процессом заказа на закупку на конец года** в Главной книге. |
| Управление и учет по проектам | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Когда производственный заказ по проекту, в котором есть заказы контроля качества, сообщается как завершенный, возникает следующая ошибка: «Ни одна из виртуальных проводок не отмечена складской проводкой». |
| Управление и учет по проектам | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | При разноске накладной по расчетам с поставщиками, связанной с проектом, возникает следующая ошибка: «Нумерованный текст Проект - стоимость - номенклатура не существует». |
| Управление и учет по проектам | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Косвенные затраты удваиваются при начислении выручки вручную. |
| Управление и учет по проектам | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Начисленная выручка и проводка незавершенной работы не производят транзакций. |
| Управление и учет по проектам | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Активация ожидаемой цены не выполняется для номенклатуры стандартных затрат, если существует полученный заказ на покупку по проекту. |
| Управление и учет по проектам | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Сторнированное значение НЗП из разноски счета отличается от исходного разнесенного значения НЗП из записи времени. |
| Управление и учет по проектам | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Имеется проблема с разнесением выручки по счету проекта в случаях применения удержания, когда транзакции ваучера не сбалансированы должным образом. |
| Управление и учет по проектам | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Создание оценки после разноски предложения по счету блокирует импорт строк коррекции в Project Operations. |
| Управление и учет по проектам | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Изменение записи вехи с полностью выставленными счетами не должно быть возможным. |
| Управление и учет по проектам | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | При использовании автоматических затрат счет-фактура внутрихолдингового клиента для табеля учета времени не может быть разнесена, и отображается сообщение об ошибке. |
| Управление и учет по проектам | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Адрес подпроекта обновляется неправильно. |
| Управление и учет по проектам | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Себестоимость потребностей в номенклатуре обновляется с учетом закупочной цены для консолидированных заказов на покупку. |
| Управление и учет по проектам | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Разнесенная стоимость неверна после обновления покупной цены и включения параметра **Активировать управление изменениями**. |
| Проезд и расходы | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Все расходы пользователя могут быть видны при поиске категории в мобильном приложении "Расходы". |
| Проезд и расходы | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Неправильные суммы по проводкам по поставщику и налогу с продаж разносятся из расхода, созданного из проводки по кредитной карте. |
| Проезд и расходы | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Когда вы обновляете страницу отчета о затратах, отображается предупреждающее сообщение, не имеющее отношения к ситуации. |
| Проезд и расходы | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Неправильный промежуточный утверждающий используется, когда вы удаляете промежуточного утверждающего, а затем повторно отправляете через рабочий процесс. |
| Проезд и расходы | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Возникает ошибка разноски, связанная с настройкой вехи. |
| Проезд и расходы | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Распределение не обновляет юридическое лицо, когда непривязанная транзакция повторно добавляется в отчет о расходах по внутрихолдинговому расходу. |

### <a name="regulatory-updates"></a>Нормативные обновления

Сведения о нормативных обновлениях для приложений для управления финансами и операциями см. в разделе [Нормативные обновления](/dynamics365/finance/localizations/regulatory-updates). Вы также можете войти в Microsoft Dynamics Lifecycle Services (LCS) и использовать инструмент поиска проблем для просмотра запланированных нормативных обновлений. Поиск проблем позволяет выполнять поиск по стране или региону, типу функции и выпуску.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]