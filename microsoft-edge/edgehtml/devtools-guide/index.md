---
description: Знакомство со средствами разработчика в Microsoft Edge (EdgeHTML)
title: Средства разработчика в Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235361"
---
# Средства разработчика в Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

Средства разработчика в Microsoft EDGE (EdgeHTML) созданы с помощью [TypeScript][|::ref1::|Index] на платформе с [открытым исходным кодом][GithubMicrosoftChakracore], оптимизированным для современных интерфейсных рабочих процессов. Теперь Средства разработчика стали доступны в виде [отдельного приложения Windows 10][MicrosoftStoreEdgeDevtoolsPreview] в магазине Microsoft Store!  

Дополнительные сведения о новых возможностях см. в статье [Средства разработчика в последнем обновлении Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Основные средства  

:::image type="complex" source="./media/devtools.png" alt-text="Средства разработчика в Microsoft Edge (EdgeHTML)":::
   Средства разработчика в Microsoft Edge (EdgeHTML)
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Средства разработчика в Microsoft Edge \(EdgeHTML\) включают следующее:  

*   Панель [Элементы][DevtoolsGuideEdgehtml|::ref2::|] для редактирования HTML и CSS, изучения свойств специальных возможностей, просмотра прослушивателей событий и определения точек останова для изменений DOM  
*   [Консоль][DevtoolsGuideEdgehtml|::ref3::|] для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также для запуска JavaScript в контексте выбранного окна или кадра  
*   [Отладчик][DevtoolsGuideEdgehtml|::ref4::|] для пошагового выполнения кода, настройки контрольных значений и точек останова, динамического редактирования кода и проверки кэша веб-хранилища и файлов cookie  
*   Панель [Сеть][DevtoolsGuideEdgehtml|::ref5::|] для отслеживания и проверки запросов и ответов из кэша сети и браузера  
*   Панель [Производительность][DevtoolsGuideEdgehtml|::ref6::|] для профилирования времени и системных ресурсов, запрашиваемых вашим сайтом  
*   Панель[Память][DevtoolsGuideEdgehtml|::ref7::|] для оценки использования ресурсов памяти и сравнения моментальных снимков кучи в разных состояниях среды выполнения кода.  
*   Панель [Хранилище][DevtoolsGuideEdgehtml|::ref8::|] для просмотра и управления веб-хранилищем, IndexedDB, файлами cookie и кэшированием данных  
*   Панель [Служебные сценарии][DevtoolsGuideEdgehtmlServiceworkers] для управления и отладки своих сервисных сценариев  
*   Панель [Эмуляция][DevtoolsGuideEdgehtml|::ref9::|] для тестирования сайта с помощью различных профилей браузера, разрешений экрана и координат местоположения GPS  

Не забудьте отправить свои [отзывы и запросы функций](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [!TIP]
> [Тестируйте в Microsoft Edge \ (EdgeHTML\) без использования любого браузера][BrowserstackEdgehtml].  
> Команда Microsoft Edge сотрудничала с [BrowserStack,][BrowserstackEdgehtml], чтобы предоставить возможность бесплатного динамического и автоматизированного тестирования в Microsoft Edge \ (EdgeHTML\).  

## Приложение Microsoft Store  

**Средства разработчика Microsoft Edge \(EdgeHTML\)** теперь [доступны][DevtoolsGuideEdgehtmlWhatsnew] в виде автономного [приложения Windows 10 из магазина Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], в дополнение ко встроенным в браузер функциональным средствам \(`F12`\).  В версии из магазина предусмотрена панель **средства выбора** для подключения к открытым локальным и удаленным конечным объектам страницы и макету с вкладками для удобного переключения между экземплярами Средств разработчика.  

### Локальная отладка  

Для локальной отладки страницы просто запустите приложение Средства разработчика в Microsoft Edge.  На панели **Локальные** средства выбора выводится список всех активных процессов EdgeHTML для работы с содержимым, в том числе открытые вкладки Microsoft Edge, выполняемые [PWA][PwasEdgehtmlIndex] \ (процессы `WWAHost.exe`\) и элементы управления[webview][HostingWebview].  Выберите нужный конечный объект, чтобы вложить и открыть новый экземпляр вкладки Средства разработчика.  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Локальная панель приложения Средства разработчика":::
   Локальная панель приложения Средства разработчика
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Удаленная отладка  

Приложение Средства разработчика в Microsoft Edge предлагает базовую поддержку для отладки страниц на удаленном компьютере благодаря новому выпуску [протокола средства разработчика][DevtoolsProtocolEdgehtmlIndex].  В последнем выпуске предусмотрен удаленный доступ к базовым функциям на панелях [Отладчик][DevtoolsGuideEdgehtml|::ref10::|], [Элементы][DevtoolsGuideEdgehtml|::ref11::|] \ (только для чтения) и [Консоль][DevtoolsGuideEdgehtml|::ref12::|].  Удаленная отладка ограничена узлами рабочего стола, на которых выполняется Microsoft Edge \(EdgeHTML), с поддержкой других узлов EdgeHTML и устройств с Windows 10, которые поступят в следующих выпусках.  

Чтобы приступить к работе, ознакомьтесь с разделом [*Средства разработчика в Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] в документации [Протокол средств разработчика][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Удаленная панель приложения Средства разработчика":::
   Удаленная панель приложения Средства разработчика
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Общие сочетания клавиш  

> [!IMPORTANT]
> Все сочетания клавиш были проверены в последней версии Windows.  
> Если вам не удается использовать сочетание клавиш, то обновите свою копию Windows.  

Эти сочетания клавиш управляют главным окном Средств разработчика и должны работать во всех средствах.  

| Действие | Установленное напрямую доверие |  
|:--- |:--- |  
| Показать/скрытьСредства разработчика \(открывает последнюю просмотренную панель) | `F12`, `Ctrl`+`Shift`+`I` |  
| Включение или отключение стыковки \(Разблокировать/Внизу/Справа) | `Ctrl`+`Shift`+`D` |  
| Открыть файл | `Ctrl`+`P`, `Ctrl`+`O` |  
| Отображение не редактируемого открытого исходного HTML-кода в отладчике | `Ctrl`+`U` |  
| Показать или скрыть консоль в нижней части любого другого средства  | `Ctrl`+`` ` `` |  
| Переключиться на Элементы \ (проводник DOM) | `Ctrl`+`1` |  
| Переключиться на Консоль |  `Ctrl`+`2` |  
| Переключиться в режим Отладчика | `Ctrl`+`3` |  
| Переключиться на Сеть | `Ctrl`+`4` |  
| Переключиться на Производительность | `Ctrl`+`5` |  
| Переключиться на Память | `Ctrl`+`6` |  
| Переключиться на Эмуляцию | `Ctrl`+`7` |  
| Документ справки | `F1` |  
| Следующее средство | `Ctrl`+`F6` |  
| Предыдущее средство | `Ctrl`+`Shift`+`F6` |  
| Предыдущее средство \ (из истории) | `Ctrl`+`Shift`+`[` |  
| Следующее средство \ (из истории) | `Ctrl`+`Shift`+`]` |  
| Следующий подкадр | `F6` |  
| Предыдущий подкадр | `Shift`+`F6` |  
| Следующее соответствие в поле поиска | `F3` |  
| Предыдущее соответствие в поле поиска | `Shift`+`F3` |  
| Поиск в поле поиска | `Ctrl`+`F` |  
| Перемещение фокуса на консоль в нижней части экрана | `Alt`+`Shift`+`I` |  
| Запуск Средств разработчика на консоли | `Ctrl`+`Shift`+`J` |  
| Обновить страницу. | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Если в процессе отладки вы приостановили процесс в точке останова, то используйте действие **Обновить страницу**, чтобы сперва возобновить работу среды выполнения.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

Отправьте свой отзыв, чтобы помочь улучшить Microsoft Edge \(EdgeHTML\) Средства разработчика.  Просто откройте средства \(`F12`), а затем нажмите кнопку [Отправить отзыв](#microsoft-edge-edgehtml-developer-tools).  

Станьте участником [программы предварительной оценки Windows][WindowsInsiderProgram], чтобы предварительно просматривать [новейшие функции в Средствах разработчика][DevtoolsGuideEdgehtmlWhatsnew]  Используйте приложение Центра отзывов Windows, чтобы публиковать, голосовать, отслеживать и поддерживать общие предложения и вопросы о Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Консоль"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Отладчик"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Элементы"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Эмуляция"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Память"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Сеть"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Производительность"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Служебные сценарии"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Хранилище"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "Средства разработчика в последнем обновлении для Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Протокол средств разработчика в Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительный просмотр Средств разработчика в Microsoft Edge — Клиенты протокола средств разработчика"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) для приложений Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Прогрессивные веб-приложения (EdgeHTML) на Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительный просмотр средств разработчика в Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Программа предварительной оценки Windows"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Браузер Microsoft Edge, бесплатное тестирование | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
