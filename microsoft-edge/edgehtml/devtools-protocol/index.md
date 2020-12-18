---
description: Используйте протокол Microsoft Edge DevTools для проверки и отладки браузера Microsoft Edge (EdgeHTML).
title: Протокол Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2ba81e51d3f9abd2aa2011993532566885ce553f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235560"
---
# Протокол средств разработчика в Microsoft Edge (EdgeHTML)

> [!NOTE]
> Протокол Microsoft Edge (EdgeHTML) DevTools работает только в Обновлениях Windows 10 за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. и более поздних сборках.

Средства разработчика могут использовать **протокол Microsoft Edge (EdgeHTML) DevTools для** проверки и отладки браузера Microsoft Edge (EdgeHTML). Он предоставляет набор методов и событий, [](0.2/domains/index.md) которые организованы в различные домены инструментирования обдвижка EdgeHTML.

 Клиенты-инструменты могут вызывать эти методы и отслеживать эти события с помощью сообщений веб-socket JSON, которые обмениваются с *сервером DevTools Server,* который находится в Microsoft Edge (EdgeHTML) или на портале устройств Windows. Microsoft Edge (EdgeHTML) DevTools использует [](0.2/clients.md#microsoft-edge-devtools-preview) этот протокол, чтобы включить удаленную отладку хост-компьютера с Microsoft Edge (EdgeHTML) с помощью автономного клиента DevTools, доступного из [Microsoft Store.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj)

Протокол Microsoft Edge (EdgeHTML) DevTools разработан для тесного согласования с протоколом Chrome DevTools (см. [W3C WICG для протоколов DevTools),](https://github.com/WICG/devtools-protocol/)хотя в этом выпуске имеются известные пробелы в отношении обеспечения связи.

## Использование протокола

Вот как присоединить настраиваемый клиент инструментов к серверу DevTools в Microsoft Edge (EdgeHTML). Если [вы](0.2/clients.md#microsoft-edge-devtools-preview) используете Microsoft Edge DevTools в качестве клиента, см. инструкции по удаленной отладке.

1. Запустите Microsoft Edge (EdgeHTML) с открытым портом удаленной отладки, указав URL-адрес, который вы хотите открыть. Например:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Если Edge уже запущен, параметр URL является необязательным. Рядом с адресной стойкой браузера появится кнопка, которая указывает, что сервер средств **разработчика** запущен:

    ![Сервер инструментов разработчика](media/developer-tools-server.png) 

2. Используйте эту [конечную точку HTTP](0.2/http.md) для получения списка подключенных конечных объектов страницы:

    ```http
    http://localhost:9222/json/list
    ```

3. Подключите к списку нужной страницы, чтобы выдать дополнительные команды протокола и получать сообщения о событиях через сервер `webSocketDebuggerUrl` socket [](0.2/domains/index.md) devtools.

## Состояние и отзывы

Версия [0.2](0.2/index.md) протокола DevTools предоставляет новые домены для отладки стилей и макета (только для чтения) и консольных API, а также основные функции отладки скриптов, введенные в версии [0.1.](0.1/index.md) В пользовательском интерфейсе Microsoft Edge DevTools это преобразуется в [****](../devtools-guide/console.md) функциональные возможности, доступные в панелях [**"Элементы",**](../devtools-guide/elements.md)"Консоль" и [**"Отладка".**](../devtools-guide/debugger.md)

Благодарим за попытку протокола Edge DevTools! Мы будем будем слышать ваши отзывы по:

 - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): идеи и запросы функций DevTools

 - [**Отслеживание проблем EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/): ошибки и проблемы платформы Protocol, DevTools и EdgeHTML

 - [**Microsoft Edge DevTools Feedback Hub**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): проблемы протокола и DevTools и предложения через приложение Центр отзывов

## Вопросы и ответы

#### Могут ли несколько клиентов подключаться к одному серверу DevTools?
Нет, не одновременно, когда клиенты отладки. Последний клиент для подключения начнется с предыдущего. В будущем, когда будут поддерживаться дополнительные средства, они, скорее всего, будут поддерживать одновременные клиентские подключения.

#### Нужно ли использовать 9222 в качестве порта Сервера DevTools?
Нет. Вы можете указать любой порт, но не забудьте выбрать порт, который еще не используется. Порт 9222 для удаленной отладки используется соглашением.

#### Как подключить пользовательский клиент инструментов к Microsoft Edge (EdgeHTML) с сервером DevTools Server?
Инструкции [*по подключению*](#using-the-protocol) к Microsoft Edge (EdgeHTML), запущенные на локальном компьютере, см. в инструкциях по протоколу, которые были указаны выше. Если вы хотите поддерживать удаленную отладку, вам потребуется разработать рабочий процесс пользователя для установки SSL-сертификата хост-компьютера на клиенте, например с диалогом установки, как использует [Microsoft Edge DevTools Preview.](./0.2/clients.md#microsoft-edge-devtools-preview)

#### If I'm remote debugging using Edge DevTools, do I need to start the host browser process with *--devtools-server-port* cmd line switch? 
Нет. При настройке удаленной отладки с помощью [Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview)параметр командной строки не требуется для запуска `--devtools-server-port` Edge. В этом случае на портале *устройств* с Windows сервер DevTools размещен от имени браузера.

#### Можно ли использовать протокол Edge DevTools для удаленной отладки WWAHost.exe или веб-приложения?
В настоящее время протокол Edge DevTools поддерживает только вкладки браузера. WWAHost.exe и процессов веб-просмотров не поддерживаются.
