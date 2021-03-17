---
description: Используйте протокол Microsoft Edge DevTools для проверки и отладки браузера Microsoft Edge (EdgeHTML).
title: Протокол Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bc95f6c167479e958ffd16137176418aba872a43
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439312"
---
# <a name="microsoft-edge-edgehtml-devtools-protocol"></a>Протокол средств разработчика в Microsoft Edge (EdgeHTML)

> [!NOTE]
> Протокол Microsoft Edge (EdgeHTML) DevTools работает только в [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборках.

Средства разработчика могут использовать **протокол DevTools Microsoft Edge (EdgeHTML)** для проверки и отладки браузера Microsoft Edge (EdgeHTML). В нем содержится набор методов и событий, организованных в различные [домены](0.2/domains/index.md) инструментов двигателя EdgeHTML.

 Клиенты-инструменты могут вызывать эти методы и отслеживать эти события с помощью сообщений веб-розетки JSON, обменивающихся с *сервером DevTools Server,* который находится в Microsoft Edge (EdgeHTML) или на портале устройств Windows. Microsoft Edge (EdgeHTML) DevTools использует [](0.2/clients.md#microsoft-edge-devtools-preview) этот протокол, чтобы включить удаленную отладку хост-машины под управлением Microsoft Edge (EdgeHTML) из автономных клиентов DevTools, доступных в [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

Протокол Microsoft Edge (EdgeHTML) DevTools разработан для тесного согласования с протоколом Chrome DevTools (см. [W3C WICG для протоколов DevTools),](https://github.com/WICG/devtools-protocol/)хотя в этом выпуске имеются известные пробелы в связи с операционной доступностью.

## <a name="using-the-protocol"></a>Использование протокола

Вот как прикрепить настраиваемый клиент-инструментарий к серверу DevTools в Microsoft Edge (EdgeHTML). См. [инструкции по удаленной отладке,](0.2/clients.md#microsoft-edge-devtools-preview) если вы используете Microsoft Edge DevTools в качестве клиента.

1. Запустите Microsoft Edge (EdgeHTML) с открытым портом удаленной отладки, указав URL-адрес, который необходимо открыть. Пример:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Если edge уже запущен, параметр URL необязательный. Рядом со панели адресов браузера появится кнопка, которая указывает на запущенный сервер средств разработчика: ****

    ![Сервер средств разработчика](media/developer-tools-server.png) 

2. Используйте эту [конечную точку HTTP,](0.2/http.md) чтобы получить список приложенных целевых объектов страницы:

    ```http
    http://localhost:9222/json/list
    ```

3. Подключись к перечисленной странице, чтобы выдавать дополнительные команды протокола и получать сообщения о событиях через `webSocketDebuggerUrl` сервер розетки [](0.2/domains/index.md) devtools.

## <a name="status-and-feedback"></a>Состояние и обратная связь

[Версия 0.2](0.2/index.md) протокола DevTools предоставляет новые домены для отладки стилей и макетов (только для чтения) и API консоли, а также функции отладки скриптов, внедренные в версии [0.1](0.1/index.md). В пользовательском интерфейсе Microsoft Edge DevTools это приводит к функциональным возможностям, доступным в панелях [**Elements,**](../devtools-guide/elements.md) [**Console**](../devtools-guide/console.md) и [**Debugger.**](../devtools-guide/debugger.md)

Спасибо за попытку edge DevTools Протокол! Мы хотели бы услышать ваши отзывы по:

<!-- - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools feature ideas and requests-->  

 - [**Отслеживание проблем EdgeHTML:**](https://developer.microsoft.com/microsoft-edge/platform/issues/)ошибки и проблемы платформы Protocol, DevTools и EdgeHTML

 - [**Концентратор отзывов Microsoft Edge DevTools:**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344)проблемы и предложения по протоколу и DevTools с помощью приложения Feedback Hub

## <a name="faq"></a>Вопросы и ответы

#### <a name="can-multiple-clients-connect-to-the-same-devtools-server"></a>Может ли несколько клиентов подключиться к одному серверу DevTools?
Нет, не одновременно, когда клиенты отладки. Последний клиент, который должен подключиться, начнет предыдущий. В будущем, когда будут поддерживаться дополнительные средства, они, скорее всего, будут поддерживать одновременные клиентские подключения.

#### <a name="do-i-have-to-use-9222-as-the-devtools-server-port"></a>Нужно ли использовать 9222 в качестве порта DevTools Server?
Нет. Вы можете указать любой порт, хотя не забудьте выбрать тот, который еще не используется. Порт 9222 для удаленного отладки используется по конвенции.

#### <a name="how-do-i-connect-my-custom-tooling-client-to-microsoft-edge-edgehtml-running-the-devtools-server"></a>Как подключить настраиваемый клиент-инструментарий к Microsoft Edge (EdgeHTML) с сервером DevTools Server?
См. [*инструкции*](#using-the-protocol) по протоколу, которые указаны выше для крепится к Microsoft Edge (EdgeHTML), запущенным на локальной машине. Если требуется поддержка удаленного отладки, необходимо разработать рабочий процесс пользователя для установки SSL-сертификата SSL-компьютера хост-машины на клиента, например с помощью диалоговой установки в качестве предварительного просмотра Microsoft [Edge DevTools.](./0.2/clients.md#microsoft-edge-devtools-preview)

#### <a name="if-im-remote-debugging-using-edge-devtools-do-i-need-to-start-the-host-browser-process-with---devtools-server-port-cmd-line-switch"></a>Если я удаленно отладку с помощью Edge DevTools, нужно ли начинать процесс браузера хост-браузера с помощью переключателя cmd-строки *devtools-server-port?* 
Нет. При настройке удаленной отладки с помощью предварительного просмотра [Microsoft Edge DevTools](./0.2/clients.md#microsoft-edge-devtools-preview)переключатель командной строки не требуется `--devtools-server-port` для запуска Edge. В этом случае *на* портале устройств Windows от имени браузера размещен сервер DevTools.

#### <a name="can-i-use-the-edge-devtools-protocol-to-remotely-debug-a-wwahostexe-or-webview-process"></a>Можно ли использовать протокол Edge DevTools для удаленного отладки процесса WWAHost.exe веб-просмотров?
В настоящее время в протоколе Edge DevTools поддерживаются только вкладки браузера. WWAHost.exe и процессы веб-просмотров не поддерживаются.
