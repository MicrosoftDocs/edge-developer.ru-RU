---
description: Поиск сведений о текущих и будущих API, а также их известных проблемах и несовместимости Chrome.
title: Расширения — поддерживаемые API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b8cf13f42c99779f23eaa7b941093752fb25b207
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235823"
---
# Поддерживаемые API  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ниже приводится подробный список поддерживаемых членов API. Разработка платформы расширения продолжается, поэтому регулярно проверяйте обновления!

> [!NOTE]
>  - В Microsoft Edge все API расширения находятся под пространством `browser` имен, `browser.browserAction.disable()` например.
>  - API расширений Microsoft Edge используют вызовы, а не обещания.


## Проблемы с переархивом

Следующие известные проблемы охватывают всю платформу расширения и будут устранены в ближайшем будущем:

- При использовании свойства CSS использование абсолютных URL-адресов будет работать не так, `url()` `ms-browser-extension://` как в Chrome. Чтобы обойти эту проблему, используйте относительные пути к ресурсам (начиная с корневого каталога расширений).
- `window.open()` не работает в фоновых сценариях расширения. Используйте `browser.windows.create()` вместо этого.
- Общие файлы cookie поддерживаются, но фоновый сценарий расширения не будет иметь доступа к файлам cookie сеанса, установленным на вкладке, прежде чем расширение будет включено. Эта проблема не влияет на постоянные файлы cookie.
- Если для расширения указаны только неподтверченные разрешения, то есть `activeTab`, попытка загрузки неоконченного расширения приведет к его удалить с отображением следующего сообщения: "Что-то пошло не так с вашими расширениями, поэтому нам пришлось переустановить их. Вам потребуется снова включить их".
- Запуск скачивания с помощью скрытого тега привязки не удастся из фоновых сценариев. Это следует сделать со страницы расширения.


## закладки

Поддерживаются `bookmarks` следующие API:

| API                                   | Известные проблемы                                             | Несовместимости Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [закладки](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [bookmarks.create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [bookmarks.remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [bookmarks.getTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [bookmarks.move](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [bookmarks.removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [bookmarks.update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## browserAction

Поддерживаются `browserAction` следующие API:

| API                                   | Известные проблемы                                             | Несовместимости Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [browserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [browserAction.disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [browserAction.enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [browserAction.getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [browserAction.setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [browserAction.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [browserAction.setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [browserAction.setPopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [browserAction.getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [browserAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` не сохраняется. <br/><br/> Параметр `imageData` не поддерживается. <br/><br/> `path` является требуемой.| |
| [browserAction.getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [browserAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenus

Поддерживаются `contextMenus` следующие API:

| API                    | Известные проблемы | Несовместимости Chrome
|------------------------|--------------|----------------------|
| [contextMenus](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [contextMenus.ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` не будет отодействоваться в контекстное меню действий страницы.| Microsoft Edge не поддерживает `"launcher"` `ContextType` .|
| [contextMenus.create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Если расширения не предоставляют, созданный не `contextmenuid` `id` является уникальным. | |
| [contextMenus.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [contextMenus.remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [contextMenus.removeAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [contextMenus.update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## cookies

Поддерживаются `cookies` следующие API:

| API                    | Известные проблемы | Несовместимости Chrome
|------------------------|--------------|----------------------|
| [cookies](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [cookies.get](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [cookies.getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Если URL-адрес не указан, файлы cookie извлекаются только для URL-адресов на открываемой вкладке. В Chrome этот файл получает все файлы cookie на компьютере пользователя. |
| [cookies.getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Всегда возвращает одно и то же хранилище файлов cookie по умолчанию с ИД "0". Все файлы cookie принадлежат этому магазину. |
| [cookies.onChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | Не поддерживается. |
| [cookies.remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [cookies.set](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## extension

Поддерживаются `extension` следующие API:

| API                                   | Известные проблемы | Несовместимости Chrome
|---------------------------------------|----------------------------------------------------------|-------------|
[extension](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[extension.getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[extension.getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[extension.getViews](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[extension.isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## i18n

Поддерживаются `i18n` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------| :-------- | :---------------------
[i18n](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n.getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n.getMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` при недопустимом исключении ключа вместо корректного сбоя. <br/><br/> `i18n.getMessage` аргумент ожидает строки, но также должен разрешить int или выбросить исключение. | |
[i18n.getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## idle

Поддерживаются `idle` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------| :-------- | :---------------------
[idle](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[idle.setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[idle.queryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## уведомления

Поддерживаются `notifications` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------| :-------- | :---------------------
[уведомления](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[уведомления. NotificationOptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[уведомления. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[notifications.clear](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[notifications.create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[notifications.getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[notifications.update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[notifications.onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[notifications.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[notifications.onClosed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
notifications.onPermissionLevelChanged | | |
notifications.getPermissionLevel | | |

## pageAction

Поддерживаются `pageAction` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :--------------------
[pageAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[pageAction.getPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[pageAction.getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[pageAction.hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[pageAction.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[pageAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | Параметр `imageData` не поддерживается. <br/><br/> `path` является требуемой. |
[pageAction.setPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[pageAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[pageAction.show](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## runtime

Поддерживаются `runtime` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :-------------------
[runtime](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[runtime.port.disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[runtime.port.onDisconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[runtime.port.postMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[runtime.connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[runtime.connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[runtime.getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[runtime.getManifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[runtime.getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[runtime.lastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[runtime.reload](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[runtime.sendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | Страницы расширения Microsoft Edge могут использовать `runtime.sendMessage` / `onMessage` для отправки сообщений себе. <br/><br/> `runtime.sendmessage` не поддерживается со страниц сайта. | Microsoft Edge не поддерживает этот `options` параметр.|
[runtime.sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[runtime.setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[runtime.onConnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[runtime.onInstalled](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[runtime.onMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` объект в `runtime.onMessage` событии не полностью реализован. | `MessageSender.tlsChannelId` Не поддерживается в Microsoft Edge.|

## хранилище

Поддерживаются `storage` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :------------------------
[хранилище](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[storage.local.get](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[storage.local.remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[storage.local.set](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[storage.local.clear](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[storage.local.getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` данные сохраняются в другом формате, чем Chrome, что приводит к возвращению другого значения при `storage.local.getBytesInUse` вызове.  <br/><br/>Ex: `storage.local.set({ "k": { "s": "âas" } }` возвращает 13 в Chrome и 50 в Microsoft Edge.|
[storage.sync.get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Если объединенная сумма символов в полях манифеста и полях манифеста превышает `name` `author` 31 символ, пространство `storage.sync` имен может не работать. | |
[storage.sync.remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[storage.sync.set](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[storage.onChanged](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## tabs

Поддерживаются `tabs` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :----------------
[tabs](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[tabs.captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[tabs.create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` и `openerTabId` не поддерживаются. |
[tabs.detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` игнорируется, хотя и проверяется. Выполнение сценария в определенном кадре пока не поддерживается. | |
[tabs.get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Страницы параметров, запрашивая вкладку не в их окне, не могут об этом вызове. | |
[tabs.getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[tabs.insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` игнорируется, хотя и проверяется. | `cssOrigin` не поддерживается. |
[tabs.onActivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[tabs.onAttached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[tabs.onCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[tabs.onDetached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[tabs.onRemoved](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[tabs.onReplaced](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[tabs.onUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | После этого URL-адрес не будет получен до перезапуска Microsoft Edge. | |
[tabs.query](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned`, `audible` и еще не `muted` поддерживаются. <br/><br/> `"popup"` `windowType` пока не поддерживается. | `highlighted` не поддерживается. <br/><br/> `"panel"`, `"app"` и `"devtools"` `windowType` не поддерживаются. |
[tabs.reload](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | Microsoft Edge не поддерживает обещания. |
[tabs.remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[tabs.sendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | Обмен сообщениями с определенным кадром еще не поддерживается. `tabs.sendMessage` никогда не отправляет ответ после обновления вкладки, если на вкладке получения нет `runtime.onMessage` прослушивателей. | |
[вкладки. Tab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`, `mutedInfo` `inPrivate` , , и свойства еще `width` не `height` поддерживаются. | `openerTabId`, `selected` и свойства не `highlighted` поддерживаются. |
[tabs.update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` и `muted` еще не поддерживаются. | `highlighted` и `selected` не поддерживаются. |


## webNavigation

Поддерживаются `webNavigation` следующие API:


| API                                                                                                                                                           | Известные проблемы                                | Несовместимости Chrome                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [webNavigation](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | Неправильные id-данные вкладок.                      | Фильтрация, TransitionTypes и TransitionQualifiers не поддерживаются. <br/><br/> Для вкладки все `processIds` будут одинаковыми. |
| [webNavigation.getAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | Не включает элементы object-as-iframe. |                                                                                                                             |
| [webNavigation.getFrame](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [webNavigation.onBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [webNavigation.onCommitted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [webNavigation.onCompleted](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [webNavigation.onCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [webNavigation.onDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [webNavigation.onErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [webNavigation.onHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [webNavigation.onReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [webNavigation.onTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | Не поддерживается.                                                                                                              |
| [webNavigation.TransitionType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [webNavigation.TransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## webRequest

Поддерживаются `webRequest` следующие API:

API | Известные проблемы | Несовместимости Chrome
:------ | :----- | :-------
[webRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` не поддерживается для синхронного `XmlHttpRequests` . | Сетевые запросы от расширений, например параметров, фоновых или всплывающих страниц, не поддерживаются.<br/><br/> Сетевые запросы `<object>` от и `<embed>` элементов не поддерживаются.<br/><br/> Для кэшных запросов невозможно изменить загон.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | Изменения обработок автоматически обрабатываются в Microsoft Edge.<br/><br/>Вызов этого не влияет.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` не поддерживается. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[onCompleted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

Поддерживаются `windows` следующие API:


| API                                                                                                                               | Известные проблемы                                                   | Несовместимости Chrome                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` объекты не поддерживают `alwaysOnTop` свойство в Microsoft Edge. <br/><br/>InPrivate не поддерживается. |
| [windows. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` и `"detached_panel"` не поддерживаются в Microsoft Edge.                                           |
| [windows.create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` параметр для разрывов вкладки не поддерживается.                                                       |
| [windows.get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [windows.getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` отсутствует `tabs` свойство. |                                                                                                                 |
| [windows.getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [windows.getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [windows.update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | Указание позиции не поддерживается.                          | `"minimized"`/`"maximized"`/`"fullscreen"` и `drawAttention` не поддерживаются в Microsoft Edge.             |
| [windows.onCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` фильтр не поддерживается.                                                                           |
| [windows.onFocusChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` фильтр не поддерживается.                                                                           |
| [windows. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` `"fullscreen"` не поддерживаются. | `"docked"` Не поддерживается в Microsoft Edge.                                                                  |
| [windows. WindowType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"`, `"app"` и `"devtools"` не поддерживаются в Microsoft Edge.                                       |
| [windows. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [windows. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
