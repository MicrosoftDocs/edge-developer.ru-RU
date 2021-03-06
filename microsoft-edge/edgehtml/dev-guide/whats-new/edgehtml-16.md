---
description: В этом руководстве представлен обзор компонентов и стандартов разработчика, включенных в EdgeHTML 16.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399199"
---
# <a name="whats-new-in-edgehtml-16"></a><span data-ttu-id="0eede-104">Новые возможности в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="0eede-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="0eede-105">Вот список новых и обновленных функций, отправляемых на веб-платформе [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) в рамках обновления Создатели падения [Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Сборка 16299\).</span><span class="sxs-lookup"><span data-stu-id="0eede-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="0eede-106">Изменения в определенных сборках предварительного просмотра предварительной версии Windows см. в [веб-сайте Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="0eede-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="0eede-107">Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="0eede-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <a name="new-and-updated-features"></a><span data-ttu-id="0eede-108">Новые и обновленные функции</span><span class="sxs-lookup"><span data-stu-id="0eede-108">New and updated features</span></span>  

### <a name="css-grid-layout"></a><span data-ttu-id="0eede-109">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="0eede-109">CSS Grid Layout</span></span>  

<span data-ttu-id="0eede-110">Microsoft Edge теперь поддерживает неоконченную реализацию [макета сетки CSS.](https://www.w3.org/TR/css-grid-1)</span><span class="sxs-lookup"><span data-stu-id="0eede-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="0eede-111">[Схема сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двухмерную систему макета на основе сетки, которая обеспечивает больше плавности макета, чем это возможно, при расположении с помощью поплавков или скриптов.</span><span class="sxs-lookup"><span data-stu-id="0eede-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="0eede-112">В приведенной ниже примере используется схема сетки CSS для создания структуры базовой веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="0eede-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="0eede-113">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="0eede-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="0eede-114">См. макет <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетки Pen CSS </a> от MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="0eede-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <a name="css-object-fit-and-object-position"></a><span data-ttu-id="0eede-115">Объектная и объектная позиция CSS</span><span class="sxs-lookup"><span data-stu-id="0eede-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="0eede-116">EdgeHTML 16 представляет поддержку свойств CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) и [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="0eede-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="0eede-117">Эти свойства контролируют положение и размер замененного контента в поле контента.</span><span class="sxs-lookup"><span data-stu-id="0eede-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <a name="developer-tools"></a><span data-ttu-id="0eede-118">Средства разработчика</span><span class="sxs-lookup"><span data-stu-id="0eede-118">Developer Tools</span></span>  

<span data-ttu-id="0eede-119">В этом выпуске мы начали основные усилия по рефакторингу Microsoft Edge DevTools для повышения надежности и производительности, а также добавили кучу новых функций, которые можно начать использовать сегодня в сборках [Windows Insider.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="0eede-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="0eede-120">Дополнительные новости о том, что изменилось, ознакомьтесь с руководством Microsoft [Edge DevTools!](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="0eede-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <a name="javascript"></a><span data-ttu-id="0eede-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0eede-121">JavaScript</span></span>  

<span data-ttu-id="0eede-122">[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) строится на оптимизации производительности Javascript предыдущих выпусков, расширяя возможности двигателя Chakra для отсрочки или повторного отодвигания функций, использования многоморфных кэшей и оптимизации функций с помощью `try` / `finally` блоков.</span><span class="sxs-lookup"><span data-stu-id="0eede-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="0eede-123">Кроме того, функции, которые впервые были предварительно предварительно представлены в EdgeHTML 15, теперь стабильны и включены по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="0eede-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <a name="new-features"></a><span data-ttu-id="0eede-124">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="0eede-124">New features</span></span>  

<span data-ttu-id="0eede-125">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0eede-125">On by default</span></span>  

*   <span data-ttu-id="0eede-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([демонстрация](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="0eede-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="0eede-127">Общая память и атомы</span><span class="sxs-lookup"><span data-stu-id="0eede-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a><span data-ttu-id="0eede-128">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="0eede-128">Payment Request API</span></span>  

<span data-ttu-id="0eede-129">API [запроса](../windows-integration/payment-request-api.md) платежей — это открытый меж браузерный стандарт, который позволяет браузерам выступать в качестве посредника между продавцами, потребителями и методами оплаты \(например, кредитными картами\), которые потребители хранят в облаке.</span><span class="sxs-lookup"><span data-stu-id="0eede-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="0eede-130">API в EdgeHTML 16 был обновлен в соответствии с последней спецификацией API запроса [платежей](https://w3c.github.io/payment-request) W3C.</span><span class="sxs-lookup"><span data-stu-id="0eede-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="0eede-131">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="0eede-131">This includes:</span></span>  

*   <span data-ttu-id="0eede-132">Поддержка `canMakePayment()` метода</span><span class="sxs-lookup"><span data-stu-id="0eede-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="0eede-133">Поддержка `requestId` свойства</span><span class="sxs-lookup"><span data-stu-id="0eede-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="0eede-134">Поддержка `id` свойства</span><span class="sxs-lookup"><span data-stu-id="0eede-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="0eede-135">Значение по умолчанию для `complete()` параметра `result` метода изменено с "" на "неизвестный"</span><span class="sxs-lookup"><span data-stu-id="0eede-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <a name="service-workers"></a><span data-ttu-id="0eede-136">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="0eede-136">Service Workers</span></span>  

<span data-ttu-id="0eede-137">[Сотрудники служб](https://www.w3.org/TR/service-workers-1) — это сценарии, управляемые событиями, которые работают на фоне веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="0eede-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="0eede-138">Сотрудники службы обеспечивают функции, ранее доступные только с помощью локальных приложений, таких как перехват и обработка запросов из сети, управление и обработка фоновой синхронизации, локальное хранилище и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="0eede-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="0eede-139">Поддержка для сотрудника службы по-прежнему находится в разработке, но вы можете проверить свою PWA в Microsoft Edge с помощью нашей экспериментальной поддержки сотрудника службы, включив функцию работника службы `about:flags` в .</span><span class="sxs-lookup"><span data-stu-id="0eede-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <a name="webvr"></a><span data-ttu-id="0eede-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="0eede-140">WebVR</span></span>  

<span data-ttu-id="0eede-141">WebVR для Microsoft Edge добавил поддержку [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="0eede-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="0eede-142">Эти контроллеры имеют точное положение в пространстве, позволяя тонко взаимодействовать с цифровыми объектами в виртуальной реальности.</span><span class="sxs-lookup"><span data-stu-id="0eede-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры движения" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="0eede-144">Контроллеры движения</span><span class="sxs-lookup"><span data-stu-id="0eede-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="0eede-145">Веб-видеорегистратор также оптимизирован для поддержки двух различных типов работы.</span><span class="sxs-lookup"><span data-stu-id="0eede-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="0eede-146">**Компьютеры смешанной реальности** Windows — настольные компьютеры и ноутбуки с интегрированной графикой.</span><span class="sxs-lookup"><span data-stu-id="0eede-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="0eede-147">При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со 60 кадрами в секунду.</span><span class="sxs-lookup"><span data-stu-id="0eede-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="0eede-148">**Windows Mixed Reality Ultra PCs** — настольные компьютеры и ноутбуки с дискретной графикой.</span><span class="sxs-lookup"><span data-stu-id="0eede-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="0eede-149">При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со 90 кадрами в секунду.</span><span class="sxs-lookup"><span data-stu-id="0eede-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="0eede-150">Обе установки будут поддерживать один и тот же захватывающий видео и игровой опыт.</span><span class="sxs-lookup"><span data-stu-id="0eede-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="0eede-151">Дополнительные сведения о предстоящих обновлениях смешанной реальности Windows вы можете узнать в блоге блога [обновления windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="0eede-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="0eede-152">Для руководств и демонстраций перенахлопайся в Руководство по разработчику [Веб-видеорегистратора.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="0eede-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="0eede-153">Так как спецификация WebVR еще находится в разработке, реализация Microsoft Edge может измениться позже.</span><span class="sxs-lookup"><span data-stu-id="0eede-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <a name="new-apis-in-edgehtml-16"></a><span data-ttu-id="0eede-154">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="0eede-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="0eede-155">Полный список новых API в EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="0eede-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="0eede-156">Они перечислены в формате `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="0eede-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="0eede-157">Несмотря на то, что следующие API выставлены в DOM, поведение некоторых из них по-прежнему находится в разработке.</span><span class="sxs-lookup"><span data-stu-id="0eede-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="0eede-158">Обратитесь [к статусу платформы Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) для официального слова о поддержке функций.</span><span class="sxs-lookup"><span data-stu-id="0eede-158">Refer to [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="0eede-159">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="0eede-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="0eede-160">См. новые <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> API pen в EdgeHTML 16 </a> msEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="0eede-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <a name="previous-edgehtml-releases"></a><span data-ttu-id="0eede-161">Предыдущие выпуски EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="0eede-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="0eede-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="0eede-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="0eede-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="0eede-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="0eede-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="0eede-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="0eede-165">EdgeHTML 15 / Сборка Windows 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="0eede-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
