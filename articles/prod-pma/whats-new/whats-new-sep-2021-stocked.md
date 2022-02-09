---
title: Новые возможности или изменения в сентябре 2021 г. — Project Operations для сценариев на основе запасов/производственных заказов
description: Эта тема содержит информацию об обновлениях качества, доступных в выпуске Project Operations за сентябрь 2021 года для сценариев на основе запасов/производства.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815855"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Новые возможности или изменения в сентябре 2021 г. — Project Operations для сценариев на основе запасов/производственных заказов

_**Применяется к:** Project Operations для сценариев на основе запасов/производственных заказов_

Этот тема применяется к следующим компонентам и версиям Microsoft Dynamics 365 Project Operations:

- Управление проектами и бухгалтерский учет в среде Dynamics 365 Finance версии 10.0.21
 
## <a name="quality-updates"></a>Обновления качества

| Область функций | Номер ссылки | Обновление качества |
|---|---|---|
| Управление и учет по проектам | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Если роли руководителя по покупкам предоставлен доступ к одному юридическому лицу, она также получает доступ ко всем проектам во всех юридических лицах. |
| Управление и учет по проектам | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Проблема округления налога на добавленную стоимость (НДС) возникает, когда кредит-нота сопоставляется с исходным счетом-фактурой проекта. |
| Управление и учет по проектам | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Используйте альтернативный бюджет проекта для проверки бюджета. |
| Управление и учет по проектам | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Ценовая группа **Цена продажи час** не рассчитывается в иерархической структуре работ для предложений по проектам. |
| Управление и учет по проектам | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Удаление оценки не работает, когда включена функция **Включить валюту контракта по проекту для расчета оценки**. |
| Управление и учет по проектам | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Факторизация налога с продаж по количеству добавляется к сумме продажной цены, когда налог за использование используется в налоговой группе журнала расходов по проекту. |
| Управление и учет по проектам | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Условный налог не рассчитывается правильно для последнего платежа, когда к счетам по заказу на покупку применяется удержание поставщика и предоплата. |
| Управление и учет по проектам | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Трассировка корректировки не работает для журналов начального сальдо. |
| Управление и учет по проектам | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Распределение версии бюджета проекта по периодам** распределяется по всем бюджетным периодам. Когда распределение отправлено, запись не очищается. |
| Управление и учет по проектам | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Проводки незавершенного производства (НЗП) в главной книге имеют неправильную сумму. |
| Управление и учет по проектам | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Утверждение журнала часов по проекту не работает. |
| Управление и учет по проектам | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Цена продажи корректировки проекта не обновляется с учетом косвенных затрат, если лимит финансирования не отмечен. |
| Управление и учет по проектам | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Невозможно создать потребность в номенклатуре, если по заголовку таблицы продаж выставлен счет и резервный заказ на покупку для существующих строк завершен. |
| Управление и учет по проектам | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Сумма удержания для правила выставления счетов, имеющего веху для другого проекта, не разносится в соответствующем идентификаторе проекта, который был выбран для вехи. Вместо этого она разносится для первого проекта. |
| Управление и учет по проектам | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Когда вы выбираете **Набор финансовых аналитик** в предложении по счету, возникает следующая ошибка: «Невозможно преобразовать объект типа 'Dynamics.AX.Application.FormIntControl' в тип 'Dynamics.AX.Application.FormStringControl'». |
| Управление и учет по проектам | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Отчет **Счету по проекту** пропускает строки. |
| Управление и учет по проектам | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Ошибка возникает при расчете контроля затрат для инвестиционного проекта. |
| Управление и учет по проектам | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Метод **ProjTable::InitFromCustTable - canDeletePostalAddress** вызывает проблемы с производительностью. |
| Управление и учет по проектам | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Сообщение об ошибке должно быть более четким, чем «Неожиданная ошибка». |
| Управление и учет по проектам | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Пакетное задание разноски счета по проекту обрабатывает и разносит предложение по счету, даже если строки счета не были сгенерированы. |
| Управление и учет по проектам | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Проблема округления возникает, когда ключ конфигурации лицензии государственного сектора отключен. Неправильная себестоимость или продажная цена генерируется в часах табеля учета времени для контрактов с несколькими источниками-учредителями. |
| Управление и учет по проектам | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Цена продажи проекта в заказе на покупку по проекту, по которому выставлен счет-фактура, неправильно рассчитывается, когда установлена модель продажной цены **Процентная маржа**. |
| Управление и учет по проектам | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Система не учитывает активные дни между ними при расчете эффективной ставки оплаты труда для сотрудника. |
| Управление и учет по проектам | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Ошибка разноски возникает во внутрихолдинговом табеле учета времени из-за следующей ошибки проверки: «Для юридического лица не настроен торговый партнер». |
| Управление и учет по проектам | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Описание из заказа на покупку с категорией расходов не извлекается в разнесенном списке транзакций проекта. |
| Управление и учет по проектам | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Неправильное преобразование журналов номенклатур, разнесенных в проект. |
| Управление и учет по проектам | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Вы можете подтвердить заказ на покупку, даже если лимит финансирования был превышен. |
| Управление и учет по проектам | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Раздел **Исправление/отмена счета** накладной с произвольным текстом исчезает при выборе идентификатора проекта. |
| Управление и учет по проектам | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Возникают проблемы с производительностью, когда предложение по счету по проекту разносится из заказа на продажу по проекту, который включает складированный товар. |
| Управление и учет по проектам | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Счета-фактуры по покупке по проекту не могут быть разнесены из-за того, что возникает следующая ошибка: «Функция AccDistProcessorProjectExtension.createForProjectRevenueLine была неправильно вызвана». |
| Управление и учет по проектам | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Обновление создания пакетных заданий оценки проекта для поддержки выполнения нескольких подзадач. |
| Управление и учет по проектам | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Статус табеля учета времени не может быть обновлен до значения **Черновик**, когда рабочий процесс застревает в состоянии **Отменено**. |
| Управление и учет по проектам | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Суммы удержания не рассчитываются в предложении счета-фактуры кредитной ноты, если существует несколько строк. |
| Управление и учет по проектам | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Когда вы пытаетесь изменить сумму в сгенерированном счете из заказа на покупку, возникает следующая ошибка: «Транзакции по ваучеру не балансируются на XX/XX/XXXX. (валюта учета: 0,00 — валюта отчета: 0,01)". |
| Управление и учет по проектам | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | При разноске предложения по счету по проекту в пакетном режиме возникает проблема с производительностью из-за соединения с **GeneralJournalAccountEntry**. |
| Управление и учет по проектам | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | При разноске табеля учета времени возникают проблемы с производительностью. |
| Управление и учет по проектам | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Иерархия калькуляций в структурной декомпозиции работ неправильно выровнена после развертывания всех задач или после развертывания одной задачи вручную. |
| Управление и учет по проектам | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Шаблон Excel предложения с ценами по проекту нельзя добавить в меню **Открыть в Excel**. |
| Управление и учет по проектам | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Номер налогового освобождения для юридического лица не включается в распечатанный счет по проекту. |
| Управление и учет по проектам | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Ошибка отсутствия обновления финансовых данных в единице инвентаря, когда проект корректируется в соответствии с кредитными линиями. |
| Управление и учет по проектам | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | После применения KB 461935 вы не сможете разносить оценки, если переключитесь на непрерывные номерные серии. |
| Управление и учет по проектам | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** приводит к тому, что мобильное приложение табеля учета времени по проекту для Android перестает отвечать. |
| Управление и учет по проектам | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Сторнированное значение НЗП из разноски счета отличается от исходного разнесенного значения НЗП из записи времени. |
| Управление и учет по проектам | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | В случаях применения удержания транзакции ваучера не сбалансированы, когда разносится выручка по счету для проекта. |
| Управление и учет по проектам | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Когда функция **Повышение производительности планирования ресурсов проекта** включена, десятичные значения неправильно округляются для доступности ресурсов и емкости. |
| Управление и учет по проектам | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Когда функция **Создание оценок проекта с использованием нескольких пакетных задач** включена, создание оценок в пакете, состоящем из нескольких подзадач, работает только для текущего периода. |
| Проезд и расходы | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Политики заявок на командировки игнорируются, и рабочий процесс утверждается без ошибок. |
| Проезд и расходы | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Приложение мобильных расходов не сохраняет следующую информацию в строке расходов:</p><ul><li>ИД проекта</li><li>Должен ли выставляться счет для расхода</li><li>Номер действия</li></ul> |
| Проезд и расходы | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Поле **Прикрепленные квитанции** установлено как **Да**, даже если к строке расходов не приложена никакая квитанция. |
| Проезд и расходы | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | При изменении категории расходов на **Личное** появляется ошибка. |
| Проезд и расходы | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Вы не можете прикрепить квитанцию или редактировать родительские расходы после того, как транзакция по кредитной карте разделена на личный расход. |
| Проезд и расходы | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Политика расходов для внутрихолдинговых транзакций, которая имеет идентификатор проекта, работает неправильно. |
| Проезд и расходы | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Разнесенная информация о дате отсутствует в разнесенных отчетах о расходах. |
| Проезд и расходы | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | В мобильном приложении "Расходы" есть проблемы с методом оплаты. |
| Проезд и расходы | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Заявка на командировку, созданная для одного работника, может использоваться для отчета о расходах другого сотрудника до даты делегирования. |
| Проезд и расходы | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Когда вы создаете расход, изменения значений финансовой аналитики не обновляется должным образом на уровне распределения по счетам в рабочей области **Управление расходами**. |
| Проезд и расходы | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Статус утверждения строки основных расходов не синхронизируется со статусом утверждения рабочего процесса детализированной строки. |
| Проезд и расходы | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ошибка возникает, если вы разносите отчет о расходах и включено возмещение налогов. |
| Проезд и расходы | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Представитель не может удалить расходные документы уволенного сотрудника. |
| Проезд и расходы | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Удаление строки расходов занимает больше времени, чем ожидалось, и влияет на производительность. |
| Проезд и расходы | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** вызывает потерянную запись **TaxUncommitted**, так как удаляется только **SourceDocumentLine**. |
| Проезд и расходы | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** не учитывает **trvExpTrans.ReferenceDataAreaId** для создания новой номерной серии. |

## <a name="regulatory-updates"></a>Нормативные обновления

Для получения информации о нормативных обновлениях для приложений Finance and Operations см. раздел [Нормативные обновления](/dynamics365/finance/localizations/regulatory-updates). Вы также можете войти в Microsoft Dynamics Lifecycle Services (LCS) и использовать инструмент поиска проблем для просмотра запланированных нормативных обновлений. Поиск проблем позволяет выполнять поиск по стране или региону, типу функции и выпуску.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]