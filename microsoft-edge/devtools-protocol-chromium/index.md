---
description: Обновление протокола Microsoft Edge DevTools
title: Обновление протокола Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 15b13e2b93d1dbd013a82ea52b643071fa5b6f7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235608"
---
# <span data-ttu-id="f0e0e-103">Обзор протокола DevTools Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="f0e0e-104">С переходом платформы Microsoft Edge на Chromium протокол [Microsoft Edge (EdgeHTML) DevTools](../edgehtml/devtools-protocol/index.md) не будет получать дополнительные обновления.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](../edgehtml/devtools-protocol/index.md) will not be receiving any further updates.</span></span>  <span data-ttu-id="f0e0e-105">Протокол Microsoft Edge \(Chromium\) DevTools будет соответствовать API протокола Chrome DevTools в будущем.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="f0e0e-106">Документацию по этим доменам и методам можно найти, обратившись к средству просмотра протокола [Chrome DevTools.](https://chromedevtools.github.io/devtools-protocol/tot/)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>  

> [!NOTE]
> <span data-ttu-id="f0e0e-107">Любые методы с префиксом в протоколе `ms` [DevTools Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) больше не поддерживаются в протоколе Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](../edgehtml/devtools-protocol/index.md) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <span data-ttu-id="f0e0e-108">Использование протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="f0e0e-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="f0e0e-109">Вот как присоединить настраиваемый клиент инструментов к серверу DevTools в Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="f0e0e-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="f0e0e-110">Убедитесь, что все экземпляры Microsoft Edge \(Chromium\) закрыты.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="f0e0e-111">Запустите Microsoft Edge \(Chromium\) с удаленным портом отладки:.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="f0e0e-112">При желании можно запустить отдельный экземпляр Edge с использованием отдельного профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="f0e0e-113">Затем используйте конечную точку HTTP, чтобы получить список конечных объектов страниц с возможностью `list` прикрепления.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="f0e0e-114">Наконец, подключите нужный целевой объект и выдав команды/подпишитесь на сообщения о событиях через сервер `webSocketDebuggerUrl` веб-sockets DevTools.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <span data-ttu-id="f0e0e-115">Конечные точки HTTP протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="f0e0e-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="f0e0e-116">Протокол DevTools Microsoft Edge \(Chromium\) поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <span data-ttu-id="f0e0e-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="f0e0e-117">/json/version</span></span>  

<span data-ttu-id="f0e0e-118">Предоставляет сведения о браузере хост-компьютера и поддерживаемой версии протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="f0e0e-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-119">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-120">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-120">None</span></span>**  

**<span data-ttu-id="f0e0e-121">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-121">Return object</span></span>**  

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```  

## <span data-ttu-id="f0e0e-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="f0e0e-122">/json/protocol</span></span>  

<span data-ttu-id="f0e0e-123">Предоставляет всю поверхность API протокола, сериализованную как JSON.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="f0e0e-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-124">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-125">None</span></span>**  

**<span data-ttu-id="f0e0e-126">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-126">Return object</span></span>**  

<span data-ttu-id="f0e0e-127">Объект JSON, который представляет доступную поверхность API для текущей версии протокола.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <span data-ttu-id="f0e0e-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="f0e0e-128">/json/list</span></span>  

<span data-ttu-id="f0e0e-129">Предоставляет список кандидатов целевых объектов страницы для отладки.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="f0e0e-130">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-130">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-131">None</span></span>**  

**<span data-ttu-id="f0e0e-132">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-132">Return object</span></span>**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <span data-ttu-id="f0e0e-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="f0e0e-133">/json/close</span></span>  

<span data-ttu-id="f0e0e-134">Закрывает целевой процесс \(например, в Microsoft Edge \(Chromium\), закрывает вкладку страницы\).</span><span class="sxs-lookup"><span data-stu-id="f0e0e-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="f0e0e-135">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-135">Parameters</span></span>**  

<span data-ttu-id="f0e0e-136">Целевой ИД</span><span class="sxs-lookup"><span data-stu-id="f0e0e-136">Target ID</span></span>  

**<span data-ttu-id="f0e0e-137">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <span data-ttu-id="f0e0e-138">Удаленные инструменты для Microsoft Edge (бета-версия)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="f0e0e-139">Теперь вы можете установить удаленные инструменты [для Microsoft Edge (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) из [Microsoft Store.](https://www.microsoft.com/store/apps/windows)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="f0e0e-140">Это приложение позволяет удаленно отладить Microsoft Edge (Chromium), запущенный на устройстве с Windows 10, с компьютера разработчика.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="f0e0e-141">Чтобы узнать, как настроить устройство с Windows 10 и подключиться к нем с компьютера разработчика, перейдите к началу работы с удаленной отладке [устройств с Windows 10.](../devtools-guide-chromium/remote-debugging/windows.md)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="f0e0e-142">Удаленные инструменты [для Microsoft Edge (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) используют тот же протокол Microsoft Edge (Chromium) [DevTools, что и DevTools,](../devtools-guide-chromium/index.md) для связи с Microsoft Edge, запущенным на устройстве с Windows 10, которое нужно отладить.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="f0e0e-143">Перед каждым вызовом протокола приложение просто заранее и ид процесса `/msedge/` ( `pid` ).</span><span class="sxs-lookup"><span data-stu-id="f0e0e-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="f0e0e-144">Он поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-144">It supports the following HTTP endpoints.</span></span>  

### <span data-ttu-id="f0e0e-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="f0e0e-145">/msedge/json/list</span></span>  

<span data-ttu-id="f0e0e-146">Предоставляет список кандидатов всех процессов \(включая PWAs и все вкладки во всех экземплярах Microsoft Edge\) на устройстве `msedge.exe` с Windows 10 для отладки. [](../progressive-web-apps-chromium/index.md)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="f0e0e-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-147">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-148">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-148">None</span></span>**  

**<span data-ttu-id="f0e0e-149">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-149">Return object</span></span>**  

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, ...  ]
```  

### <span data-ttu-id="f0e0e-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="f0e0e-150">/msedge/</span></span>  

<span data-ttu-id="f0e0e-151">Функционально эквивалентно [/msedge/json/list.](#msedgejsonlist)</span><span class="sxs-lookup"><span data-stu-id="f0e0e-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <span data-ttu-id="f0e0e-152">/msedge/[pid]/json/list</span><span class="sxs-lookup"><span data-stu-id="f0e0e-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="f0e0e-153">Предоставляет список кандидатов целевых объектов страницы для экземпляра Microsoft Edge, который соответствует предоставленной `[pid]` для отладки.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="f0e0e-154">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-154">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-155">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-155">None</span></span>**  

**<span data-ttu-id="f0e0e-156">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-156">Return object</span></span>**  

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, ...  ]
```  

### <span data-ttu-id="f0e0e-157">/msedge/[pid]/json/version</span><span class="sxs-lookup"><span data-stu-id="f0e0e-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="f0e0e-158">Предоставляет сведения об экземпляре Microsoft Edge, который соответствует предоставленной версии и поддерживаемой версии `[pid]` протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="f0e0e-159">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-159">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-160">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-160">None</span></span>**  

**<span data-ttu-id="f0e0e-161">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-161">Return object</span></span>**  

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```  

### <span data-ttu-id="f0e0e-162">/msedge/[pid]/json/protocol/</span><span class="sxs-lookup"><span data-stu-id="f0e0e-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="f0e0e-163">Предоставляет всю поверхность API протокола, сериализованную как JSON для экземпляра Microsoft Edge, который соответствует `[pid]` предоставленному.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="f0e0e-164">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e0e-164">Parameters</span></span>**  

**<span data-ttu-id="f0e0e-165">Нет</span><span class="sxs-lookup"><span data-stu-id="f0e0e-165">None</span></span>**  

**<span data-ttu-id="f0e0e-166">Объект Return</span><span class="sxs-lookup"><span data-stu-id="f0e0e-166">Return object</span></span>**  

<span data-ttu-id="f0e0e-167">Объект JSON, который представляет доступную поверхность API для версии протокола, используемой экземпляром Microsoft Edge, который соответствует `[pid]` предоставленной версии.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
