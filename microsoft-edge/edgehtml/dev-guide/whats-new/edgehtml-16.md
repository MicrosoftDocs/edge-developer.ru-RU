---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: В этом руководстве представлен обзор новых функций и API в EdgeHTML 16.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7697114546153555d947903eda6bf8477cca3516
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235467"
---
# <span data-ttu-id="e8bc6-104">Новые возможности EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="e8bc6-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e8bc6-105">Вот список новых и обновленных функций, которые поставляются в веб-платформе [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) в составе [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, сборка 16299\).</span><span class="sxs-lookup"><span data-stu-id="e8bc6-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="e8bc6-106">Изменения в конкретных сборках Windows Insider Preview см. в записях microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="e8bc6-107">Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="e8bc6-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="e8bc6-108">Новые и обновленные функции</span><span class="sxs-lookup"><span data-stu-id="e8bc6-108">New and updated features</span></span>  

### <span data-ttu-id="e8bc6-109">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="e8bc6-109">CSS Grid Layout</span></span>  

<span data-ttu-id="e8bc6-110">Microsoft Edge теперь поддерживает реализацию макета [сетки CSS](https://www.w3.org/TR/css-grid-1)без префикса.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="e8bc6-111">[Макет сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двухмерную систему макета на основе сетки, которая обеспечивает более плавность макета, чем это возможно, при расположении с помощью с плавающей заместки или сценариев.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="e8bc6-112">В примере ниже для создания структуры для базовой веб-страницы используется макет сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="e8bc6-113">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="e8bc6-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="e8bc6-114">См. макет <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетки CSS пера </a> от MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="e8bc6-115">CSS object-fit and object-position</span><span class="sxs-lookup"><span data-stu-id="e8bc6-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="e8bc6-116">EdgeHTML 16 поддерживает свойства CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) и [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="e8bc6-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="e8bc6-117">Эти свойства контролируют положение и размер замененного содержимого в поле содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="e8bc6-118">Средства разработчика</span><span class="sxs-lookup"><span data-stu-id="e8bc6-118">Developer Tools</span></span>  

<span data-ttu-id="e8bc6-119">В этом выпуске мы начали основные усилия по рефакторингу Microsoft Edge DevTools для повышения надежности и производительности, а также добавили ряд новых функций, которые вы можете начать использовать уже сегодня в сборках для программы [insider Для Windows.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="e8bc6-120">Подробнее об изменениях можно узнать в руководстве По разработке для [Microsoft Edge.](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="e8bc6-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="e8bc6-121">JavaScript</span></span>  

<span data-ttu-id="e8bc6-122">[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) строится на оптимизации производительности JavaScript предыдущих выпусков, расширяя возможность ядра Chakra откладывать или повторно откладывать функции, использовать многоморфные кэши и оптимизировать функции с помощью `try` / `finally` блоков.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="e8bc6-123">Кроме того, функции, которые были предварительно представлены в EdgeHTML 15, теперь стабильны и включены по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="e8bc6-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="e8bc6-124">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="e8bc6-124">New features</span></span>  

<span data-ttu-id="e8bc6-125">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e8bc6-125">On by default</span></span>  

*   <span data-ttu-id="e8bc6-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="e8bc6-127">Общая память и атомарные</span><span class="sxs-lookup"><span data-stu-id="e8bc6-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="e8bc6-128">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="e8bc6-128">Payment Request API</span></span>  

<span data-ttu-id="e8bc6-129">[API](../windows-integration/payment-request-api.md) запроса платежей — это открытый кросс браузерный стандарт, который позволяет браузерам действовать в качестве посредника между продавцами, потребителями и методами оплаты (например, кредитными картами),которые потребители хранили в облаке.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="e8bc6-130">API в EdgeHTML 16 обновлен в соответствии с последней спецификацией [API](https://w3c.github.io/payment-request) запроса платежей W3C.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="e8bc6-131">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="e8bc6-131">This includes:</span></span>  

*   <span data-ttu-id="e8bc6-132">Поддержка `canMakePayment()` метода</span><span class="sxs-lookup"><span data-stu-id="e8bc6-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="e8bc6-133">Поддержка `requestId` свойства</span><span class="sxs-lookup"><span data-stu-id="e8bc6-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="e8bc6-134">Поддержка `id` свойства</span><span class="sxs-lookup"><span data-stu-id="e8bc6-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="e8bc6-135">Значение по умолчанию для параметра метода `complete()` `result` изменилось с " " на "unknown"</span><span class="sxs-lookup"><span data-stu-id="e8bc6-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="e8bc6-136">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="e8bc6-136">Service Workers</span></span>  

<span data-ttu-id="e8bc6-137">[Service Workers](https://www.w3.org/TR/service-workers-1) — это сценарии на основе событий, которые запускаются в фоновом режиме веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="e8bc6-138">Сотрудники службы обеспечивают функции, которые ранее были доступны только в таких приложениях, как перехват и обработка запросов из сети, управление фоновой синхронизацией, локальное хранилище и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="e8bc6-139">Поддержка сотрудников службы еще находится на стадии разработки, но вы можете протестировать PWA в Microsoft Edge с помощью нашей экспериментальной поддержки рабочих служб, включив в нее функцию работы `about:flags` службы.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="e8bc6-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="e8bc6-140">WebVR</span></span>  

<span data-ttu-id="e8bc6-141">WebVR для Microsoft Edge добавлена поддержка [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="e8bc6-142">Эти контроллеры имеют точное положение в пространстве, позволяя точно взаимодействовать с цифровыми объектами в виртуальной реальности.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры движения" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="e8bc6-144">Контроллеры движения</span><span class="sxs-lookup"><span data-stu-id="e8bc6-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="e8bc6-145">WebVR также был оптимизирован для поддержки двух различных типов работы.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="e8bc6-146">**Компьютеры Windows Mixed Reality** — настольные компьютеры и ноутбуки со встроенной графикой.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="e8bc6-147">При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со частотой 60 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="e8bc6-148">**Компьютеры Windows Mixed Reality—** настольные компьютеры и ноутбуки с дискретной графикой.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="e8bc6-149">При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со частотой 90 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="e8bc6-150">Обе программы установки поддерживают одно и то же иммерсивное видео и игровое время.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="e8bc6-151">Дополнительные сведения о предстоящих обновлениях Windows Mixed Reality можно узнать в записи блога об обновлении праздников [Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="e8bc6-152">Руководства и демонстрации можно найти в руководстве разработчика [WebVR.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="e8bc6-153">Так как спецификация WebVR еще находится в разработке, реализация Microsoft Edge может измениться позже.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="e8bc6-154">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="e8bc6-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="e8bc6-155">Ниже полный список новых API в EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="e8bc6-156">Они перечислены в формате `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="e8bc6-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="e8bc6-157">Несмотря на то что в модели DOM есть следующие API, все еще возможно, что некоторые из них находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="e8bc6-158">Официальное слово о поддержке функций можно найти в статусе платформы [Microsoft Edge.](https://developer.microsoft.com/microsoft-edge/platform/status)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="e8bc6-159">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="e8bc6-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="e8bc6-160">См. API-код для новых перьев в <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> EdgeHTML 16 от </a> MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</span><span class="sxs-lookup"><span data-stu-id="e8bc6-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="e8bc6-161">Предыдущие выпуски EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="e8bc6-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="e8bc6-162">EdgeHTML 12 / Сборка Windows 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="e8bc6-163">EdgeHTML 13 / Сборка Windows 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="e8bc6-164">EdgeHTML 14 / Сборка Windows 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="e8bc6-165">EdgeHTML 15 / Сборка Windows 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="e8bc6-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
