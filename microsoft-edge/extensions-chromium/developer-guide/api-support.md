---
description: Список поддерживаемых API, которые можно использовать при создании расширений Microsoft Edge.
title: Поддерживаемые API для расширений Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, api расширения, разработчик, веб-разработка
ms.openlocfilehash: 20e924b5c973b9ecd433feeb3a772c6d17746369
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398107"
---
# <a name="supported-apis-for-microsoft-edge-extensions"></a>Поддерживаемые API для расширений Microsoft Edge

В следующей таблице приводится список API, которые можно использовать при создании расширений для браузера Microsoft Edge \(Chromium\).

| API                                   | Описание                                            
|---------------------------------------|----------------------------------------------------------|
| [будильники](https://developer.chrome.com/extensions/alarms) | Запланировать запуск кода периодически или в указанное время в будущем. |
| [закладки](https://developer.chrome.com/extensions/bookmarks) | Создание, организация и обработка закладок. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Используйте действия браузера, чтобы разместить значки на панели инструментов в Microsoft Edge. Вы также можете использовать действия браузера для добавления инструмента, значка или всплывающее окна. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Удалите данные просмотра из локального профиля пользователя. |
| [команды](https://developer.chrome.com/extensions/commands) | Добавьте ярлыки клавиатуры, которые запускают действия в расширении. Например, действие для открытия браузера или отправки команды в расширение. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | В общем, параметры контента позволяют настраивать поведение Microsoft Edge на каждом сайте, а не глобально. Измените параметры, которые контролируют, могут ли веб-сайты использовать такие функции, как cookie, JavaScript и плагины. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Добавление элементов в контекстное меню в Microsoft Edge. Элементы меню могут применяться к различным объектам, таким как изображения, гиперссылки и страницы. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Запрос и изменение файлов cookie и получение уведомлений при изменении. |
| [отладка](https://developer.chrome.com/extensions/debugger) | Прикрепить одну или несколько вкладок к взаимодействию с сетью инструментов, отменить JavaScript, изменить DOM, изменить CSS и так далее. Используйте вкладку tabId отладки для таргетинга вкладок с помощью sendCommand и событий маршрутов с помощью tabId от вызовов onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Принимайте меры в зависимости от содержимого страницы, не требуя разрешения на чтение контента страницы. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Обеспечивает больше конфиденциальности путем блокировки или изменения сетевых запросов путем указания декларативных правил. Разрешить расширениям изменять сетевые запросы без перехвата запроса и просмотра контента. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Захват содержимого экрана, отдельных окон или вкладок. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Взаимодействие с инспектным окном.  Например, получение ID вкладок страниц, оценка кода, обновление страниц или получение ресурсов на странице. |
| [devtools.network](https://developer.chrome.com/extensions/devtools_network) | Извлечение сведений о сетевых запросах, отображаемом средствами разработчика в панели Network. |
| [devtools.panels](https://developer.chrome.com/extensions/devtools.panels) | Интеграция расширения в пользовательский интерфейс окна Средства разработчика путем создания собственных панелей, доступа к существующим панелям или добавления боковых панелей. |
| [загрузки](https://developer.chrome.com/extensions/downloads) | Программным образом запускайте, отслеживайте, манипулирует и ищите скачивания. |
| [enterprise.hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Получите производителя и модель аппаратной платформы, на которой работает браузер. Этот API доступен только для расширений, установленных корпоративной политикой. |
| [события](https://developer.chrome.com/extensions/events) | Распространенные типы, используемые API, которые вызывают события, чтобы уведомить вас о том, когда происходит интересное событие. |
| [расширение](https://developer.chrome.com/extensions/extension) | На любой странице расширения можно использовать утилиты этого API. Она включает поддержку обмена сообщениями между расширениями и скриптами контента, которая описана в передаче сообщений. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Содержит объявления типов для расширений Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Управление настройками шрифтов в Microsoft Edge. |
| [журнал](https://developer.chrome.com/extensions/history) | Взаимодействие с записью посещаемых страниц браузера. В истории браузера можно добавлять, удалять или запрашивать URL-адреса. Чтобы переопредить страницу истории с помощью собственной версии, перейдите на переопределять страницы. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Реализация интернационализации во всем приложении или расширении. |
| [праздный](https://developer.chrome.com/extensions/idle) | Обнаружение изменений состояния простаиваемой машины. |
| [управление](https://developer.chrome.com/extensions/management) | Управление списком установленных или запущенных расширений. Это полезно для расширений, переопределять встроенную страницу New Tab. |
| [уведомления](https://developer.chrome.com/extensions/notifications) | Создайте богатые уведомления с помощью шаблонов и отобразите их в системной подноске. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Регистрация ключевых слов в адресной панели Microsoft Edge, также известной как omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Добавьте значки в панель инструментов Microsoft Edge справа от панели адресов. Действия страницы — это действия, которые можно принять на текущей странице и не применимы к всем страницам. Действия страницы отображаются серыми при неактивности. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Сохранение вкладок в качестве файлов MHTML.|
| [разрешения](https://developer.chrome.com/extensions/permissions) | Извлечение объявленных необязательных разрешений во время запуска, а не во время установки. Этот API можно использовать для отображения пользователям необходимых и утвержденных разрешений. |
| [выключение](https://developer.chrome.com/extensions/power) | Переопределять функции управления питанием системы. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Используйте события для запроса принтеров, их возможностей и отправки заданий печати. |
| [конфиденциальность](https://developer.chrome.com/extensions/privacy) | Функции управления в Microsoft Edge, влияющие на конфиденциальность пользователя. Этот API зависит от прототипа для получения и настройки `EdgeSetting` `types` конфигурации Microsoft Edge. |
| [прокси](https://developer.chrome.com/extensions/proxy) | Управление настройками прокси для Microsoft Edge. Этот API зависит от прототипа API для получения и настройки `EdgeSetting` `types` прокси-конфигурации Microsoft Edge. |
| [время запуска](https://developer.chrome.com/extensions/runtime) | Извлекать фоновую страницу, возвращать сведения о манифесте, а также слушать и реагировать на события в жизненном цикле приложения или расширения. Можно также преобразовать относительный путь URL-адресов в полностью квалифицированные URL-адреса. |
| [сеансы](https://developer.chrome.com/extensions/sessions) | Запрос и восстановление вкладок и окон из сеанса просмотра. |
| [хранилище](https://developer.chrome.com/extensions/storage) | Хранение, извлечение и отслеживание изменений в пользовательских данных. |
| [system.memory](https://developer.chrome.com/extensions/system_memory) | The `system.memory` API. |
| [system.storage](https://developer.chrome.com/extensions/system_storage) | Запрос сведений о устройствах хранения. Вы также можете получать уведомления при присоединении или отсоединениях устройств хранения. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Взаимодействие с потоками мультимедиа вкладок. |
| [вкладки](https://developer.chrome.com/extensions/tabs) | Взаимодействуйте с системой вкладок браузера для создания, изменения и изменения вкладок. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Доступ к верхним сайтам, также называемым большинством посещаемых сайтов, которые отображаются на новой странице вкладки. Эти сайты не включают ярлыки, настроенные пользователем. |
| [tts](https://developer.chrome.com/extensions/tts) | Воспроизведения синтезированной текстовой речи (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Реализация двигателя с текстом на речь (TTS) с помощью расширения. Расширения, которые регистрируются для использования этого API, получают события, содержащие произнесенные слова и другие параметры. Расширения могут использовать любую доступную веб-технологию для синтеза и вывода речи, а также отправлять события обратно в функцию вызова, чтобы сообщить о состоянии. |
| [типы](https://developer.chrome.com/extensions/types) | Введите объявления для Microsoft Edge. |
| [webNavigation](https://developer.chrome.com/extensions/webNavigation) | Получение уведомлений о состоянии запросов на навигацию. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Наблюдение и анализ трафика. Перехват, блокировка или изменение запросов. |
| [windows](https://developer.chrome.com/extensions/windows) | Взаимодействие с окнами браузера для создания, изменения и изменения окон в браузере. |



## <a name="unsupported-extension-apis"></a>Неподтвердимые API расширения

Microsoft Edge не поддерживает следующие API расширения:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` — В качестве альтернативы можно использовать для получения маркера `launchWebAuthFlow` OAuth2 для проверки подлинности пользователей.
* `chrome.instanceID`.


## <a name="additional-considerations-for-supported-apis"></a>Дополнительные соображения для поддерживаемых API

* Пользователь должен быть подписан в Microsoft Edge с помощью учетной записи MSA или Azure Active Directory `chrome.identity.getProfileUserInfo` для использования. Если пользователь подписан в Microsoft Edge с помощью локальной учетной записи Active Directory, API возвращает значения электронной почты и `null` ID.

* Microsoft Edge не поддерживает расширения, использующие платежи Chrome Web Store, так как он использует для запроса маркеров для пользователей, `identity.getAuthtoken` вписав их. Эти маркеры отправляются в API лицензирования на основе REST. 


<!-- links -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developer.chrome.com/apps/external_extensions).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
