---
description: Найдите сведения о поддерживаемых ключах манифеста, а также их известных проблемах и несовместимости Chrome.
title: Расширения — поддерживаемые ключи манифеста
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f8413193ddb834eb7e31e4101c2b027c48bc501d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235820"
---
# Поддерживаемые ключи манифеста  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Каждое расширение имеет файл манифеста в формате JSON с именем manifest.js. Этот файл предоставляет важные сведения для расширения от его имени до его разрешений. Если не указано в примечате ниже, свойства манифеста Microsoft Edge следуют той же реализации, что и Chrome.

Вот пример [JSON-файла манифеста Microsoft Edge.](./supported-manifest-keys/json-manifest-example.md)

## Необходимые ключи

Требуются следующие ключи:

Раздел | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :--------------
[author](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Рекомендуемые ключи

Рекомендуется использовать следующие ключи:

Раздел | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :--------------
browser_specific_settings | | Указывает предпочтительное состояние расширения в браузере. Браузер может или не учитывать его в будущих выпусках, в зависимости от таких факторов, как репутация расширения или общее количество кнопок, уже в адресной панели пользователя. Это можно использовать для того, чтобы указать положение значка по `browserAction` умолчанию. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> Не поддерживается в Chrome.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[значки](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | В настоящее время игнорируется в Microsoft Edge.



## browser_action или page_action клавиш

Можно включить только один из следующих ключей (или нет):

Раздел | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | Microsoft Edge не поддерживает следующий синтаксис:  `browser_action : {"default_icon" : "icon.png" }`   <br/>Должен быть указан размер значков. <br/>Предпочтительные размеры: 20px, 25px, 30px, 40px. <br/> Другие поддерживаемые размеры: 19, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | Microsoft Edge не поддерживает следующий синтаксис:  `page_action : {"default_icon" : "icon.png" }`   <br/>Должен быть указан размер значков. <br/>Предпочтительные размеры: 20px, 25px, 30px, 40px. <br/>Другие поддерживаемые размеры: 19, 35px, 38px.|

## Необязательные ключи

Следующие ключи являются необязательными:

Раздел | Известные проблемы | Несовместимости Chrome
:------------ | :------------- | :--------------
[фон](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Persistent — обязательное поле для Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | Политика безопасности контента страницы блокирует websockets в скриптах контента, создавая неопределенные исключения. | В настоящее время расширения Microsoft Edge поддерживают только ограничения [политики по умолчанию:](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy) `script-src 'self'; object-src 'self'` |
[incognito](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[permissions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Поддерживаемые разрешения
Поддерживаются [следующие](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) разрешения:


| Разрешение         | Описание                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<all_urls\>       | Позволяет сценариям фона и контента взаимодействовать со всеми веб-страницами с дополнительными [привилегиями.](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions)                                                                                  |
| contextMenus       | Предоставляет доступ к `contextMenus` API. Это позволяет добавлять элементы в контекстное меню Microsoft Edge.                                                                                                                                                                                     |
| cookies            | Предоставляет доступ к `cookies` API. Это позволяет запрашивать и изменять файлы cookie, а также уведомления при их изменении.                                                                                                                                                           |
| geolocation        | Разрешить расширению использовать API HTML5, не `geolocation` запросив у пользователя разрешение.                                                                                                                                                                                   |
| idle               | Предоставляет доступ к `idle` API. Это позволяет обнаруживать изменения состояния простоя компьютера.                                                                                                                                                                                    |
| хранилище            | Предоставляет доступ к `storage` API. Это позволяет хранить, искомые и отслеживать изменения данных пользователя.                                                                                                                                                                             |
| tabs               | Предоставляет доступ к `tabs` API для взаимодействия с системой вкладок браузера. Это позволяет создавать, изменять и изменять вкладки в браузере, включая URL-адреса, связанные с каждой вкладками.                                                                                       |
| unlimitedStorage   | Позволяет [storage.local](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) иметь неограниченное хранилище (в зависимости от системных ресурсов) вместо 5 МБ. Максимальное хранилище на пару "ключ-значение" также увеличивается с 5 МБ до неограниченного (в зависимости от системных ресурсов). |
| webNavigation      | Предоставляет доступ к `webNavigation` API. Это позволяет получать уведомления о состоянии запросов навигации.                                                                                                                                                              |
| webRequest         | Предоставляет доступ к `webRequest` API. Это позволяет наблюдать и анализировать трафик, а также перехват, блокировку или изменение запроса в ходе его прогона.                                                                                                                               |
| webRequestBlocking | Обязательно, если расширение использует `webRequest` API в блокирующем порядке.                                                                                                                                                                                                           |

'""'
