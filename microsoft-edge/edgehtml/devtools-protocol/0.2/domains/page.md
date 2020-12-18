---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235187"
---
# <span data-ttu-id="08c40-104">Домен страницы — протокол DevTools версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="08c40-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="08c40-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="08c40-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="08c40-106">Методы</span><span class="sxs-lookup"><span data-stu-id="08c40-106">Methods</span></span>**](#methods) | <span data-ttu-id="08c40-107">[включить,](#enable) [отключить,](#disable) [перейти,](#navigate) [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="08c40-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="08c40-108">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="08c40-108">Events</span></span>**](#events) | <span data-ttu-id="08c40-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="08c40-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="08c40-110">Типы</span><span class="sxs-lookup"><span data-stu-id="08c40-110">Types</span></span>**](#types) | <span data-ttu-id="08c40-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="08c40-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="08c40-112">Методы</span><span class="sxs-lookup"><span data-stu-id="08c40-112">Methods</span></span>

### <span data-ttu-id="08c40-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="08c40-113">enable</span></span>
<span data-ttu-id="08c40-114">Включает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="08c40-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="08c40-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="08c40-115">disable</span></span>
<span data-ttu-id="08c40-116">Отключает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="08c40-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="08c40-117">переход</span><span class="sxs-lookup"><span data-stu-id="08c40-117">navigate</span></span>
<span data-ttu-id="08c40-118">Переходит на текущую страницу по заданным URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="08c40-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-120">url</span><span class="sxs-lookup"><span data-stu-id="08c40-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08c40-121">URL-адрес для навигации по странице.</span><span class="sxs-lookup"><span data-stu-id="08c40-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-122">frameId</span><span class="sxs-lookup"><span data-stu-id="08c40-122">frameId</span></span> <br/> <i><span data-ttu-id="08c40-123">необязательные</span><span class="sxs-lookup"><span data-stu-id="08c40-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-124">ИД кадра для навигации.</span><span class="sxs-lookup"><span data-stu-id="08c40-124">Frame id to navigate.</span></span> <span data-ttu-id="08c40-125">Если не указано, будет перемещаться по верхней странице.</span><span class="sxs-lookup"><span data-stu-id="08c40-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-126">Возвращает</span><span class="sxs-lookup"><span data-stu-id="08c40-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-127">frameId</span><span class="sxs-lookup"><span data-stu-id="08c40-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-128">ИД кадра, который будет перемещаться.</span><span class="sxs-lookup"><span data-stu-id="08c40-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="08c40-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="08c40-129">getFrameTree</span></span>
<span data-ttu-id="08c40-130">Возвращает представленную структуру дерева кадров.</span><span class="sxs-lookup"><span data-stu-id="08c40-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-131">Возвращает</span><span class="sxs-lookup"><span data-stu-id="08c40-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="08c40-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="08c40-133">Представляет структуру дерева кадров.</span><span class="sxs-lookup"><span data-stu-id="08c40-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="08c40-134">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="08c40-134">Events</span></span>

### <span data-ttu-id="08c40-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="08c40-135">frameAttached</span></span>
<span data-ttu-id="08c40-136">Собяно, когда фрейм присоединен к родительскому кадру.</span><span class="sxs-lookup"><span data-stu-id="08c40-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-137">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-138">frameId</span><span class="sxs-lookup"><span data-stu-id="08c40-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-139">ИД прикрепленного кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="08c40-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-141">Идентификатор родительского кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-142">stack</span><span class="sxs-lookup"><span data-stu-id="08c40-142">stack</span></span> <br/> <i><span data-ttu-id="08c40-143">необязательные</span><span class="sxs-lookup"><span data-stu-id="08c40-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="08c40-144">Трассировка стека JavaScript, когда кадр был прикреплен, устанавливается, только если фрейм инициировался сценарием.</span><span class="sxs-lookup"><span data-stu-id="08c40-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="08c40-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="08c40-145">frameDetached</span></span>
<span data-ttu-id="08c40-146">Происходит, когда фрейм отсоединяется от родительского кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-148">frameId</span><span class="sxs-lookup"><span data-stu-id="08c40-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-149">ИД отсоединяемого кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="08c40-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="08c40-150">frameNavigated</span></span>
<span data-ttu-id="08c40-151">Сгорел после завершения навигации по кадру.</span><span class="sxs-lookup"><span data-stu-id="08c40-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-153">frame</span><span class="sxs-lookup"><span data-stu-id="08c40-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="08c40-154">Объект Frame.</span><span class="sxs-lookup"><span data-stu-id="08c40-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="08c40-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="08c40-155">loadEventFired</span></span>
<span data-ttu-id="08c40-156">Соответствует событию window.onload.</span><span class="sxs-lookup"><span data-stu-id="08c40-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-158">timestamp</span><span class="sxs-lookup"><span data-stu-id="08c40-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="08c40-159">Количество миллисекунд с момента эпохи.</span><span class="sxs-lookup"><span data-stu-id="08c40-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="08c40-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="08c40-160">domContentEventFired</span></span>
<span data-ttu-id="08c40-161">Соответствует событию document.onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="08c40-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c40-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-163">timestamp</span><span class="sxs-lookup"><span data-stu-id="08c40-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="08c40-164">Количество миллисекунд с момента эпохи.</span><span class="sxs-lookup"><span data-stu-id="08c40-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="08c40-165">Типы</span><span class="sxs-lookup"><span data-stu-id="08c40-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="08c40-166">FrameId</span><span class="sxs-lookup"><span data-stu-id="08c40-166">FrameId</span></span> `string`

<span data-ttu-id="08c40-167">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="08c40-168">Кадр</span><span class="sxs-lookup"><span data-stu-id="08c40-168">Frame</span></span> `object`

<span data-ttu-id="08c40-169">Сведения о фрейме на странице.</span><span class="sxs-lookup"><span data-stu-id="08c40-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-170">Свойства</span><span class="sxs-lookup"><span data-stu-id="08c40-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-171">id</span><span class="sxs-lookup"><span data-stu-id="08c40-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-172">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-173">parentId</span><span class="sxs-lookup"><span data-stu-id="08c40-173">parentId</span></span> <br/> <i><span data-ttu-id="08c40-174">необязательные</span><span class="sxs-lookup"><span data-stu-id="08c40-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="08c40-175">Уникальный идентификатор родительского кадра.</span><span class="sxs-lookup"><span data-stu-id="08c40-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-176">name</span><span class="sxs-lookup"><span data-stu-id="08c40-176">name</span></span> <br/> <i><span data-ttu-id="08c40-177">необязательные</span><span class="sxs-lookup"><span data-stu-id="08c40-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08c40-178">Имя кадра, указанное в теге.</span><span class="sxs-lookup"><span data-stu-id="08c40-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-179">url</span><span class="sxs-lookup"><span data-stu-id="08c40-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08c40-180">URL-адрес документа фрейма.</span><span class="sxs-lookup"><span data-stu-id="08c40-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="08c40-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08c40-182">Источник безопасности документа frame.</span><span class="sxs-lookup"><span data-stu-id="08c40-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-183">mimeType</span><span class="sxs-lookup"><span data-stu-id="08c40-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="08c40-184">Тип mimeType кадра документа, определяемого браузером.</span><span class="sxs-lookup"><span data-stu-id="08c40-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="08c40-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="08c40-185">FrameTree</span></span> `object`

<span data-ttu-id="08c40-186">Сведения об иерархии frame.</span><span class="sxs-lookup"><span data-stu-id="08c40-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="08c40-187">Свойства</span><span class="sxs-lookup"><span data-stu-id="08c40-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="08c40-188">frame</span><span class="sxs-lookup"><span data-stu-id="08c40-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="08c40-189">Сведения о фрейме для этого элемента дерева.</span><span class="sxs-lookup"><span data-stu-id="08c40-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="08c40-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="08c40-190">childFrames</span></span> <br/> <i><span data-ttu-id="08c40-191">необязательные</span><span class="sxs-lookup"><span data-stu-id="08c40-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="08c40-192">Child frames.</span><span class="sxs-lookup"><span data-stu-id="08c40-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
