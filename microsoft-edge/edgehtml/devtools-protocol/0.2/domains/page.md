---
description: Ссылка На протокол DevTools Версии 0.2 (EdgeHTML) для домена Страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools Версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398849"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="63dc9-104">Домен страницы — протокол DevTools Версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="63dc9-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="63dc9-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="63dc9-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="63dc9-106">Категория</span><span class="sxs-lookup"><span data-stu-id="63dc9-106">Classification</span></span> | <span data-ttu-id="63dc9-107">Участники</span><span class="sxs-lookup"><span data-stu-id="63dc9-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="63dc9-108">Методы</span><span class="sxs-lookup"><span data-stu-id="63dc9-108">Methods</span></span>](#methods) | <span data-ttu-id="63dc9-109">[включить,](#enable) [отключить,](#disable) [перейти,](#navigate) [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="63dc9-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |  
| [<span data-ttu-id="63dc9-110">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="63dc9-110">Events</span></span>](#events) | <span data-ttu-id="63dc9-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="63dc9-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |  
| [<span data-ttu-id="63dc9-112">Типы</span><span class="sxs-lookup"><span data-stu-id="63dc9-112">Types</span></span>](#types) | <span data-ttu-id="63dc9-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="63dc9-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |  

## <a name="methods"></a><span data-ttu-id="63dc9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="63dc9-114">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="63dc9-115">"Включить"</span><span class="sxs-lookup"><span data-stu-id="63dc9-115">enable</span></span>  

<span data-ttu-id="63dc9-116">Включает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="63dc9-116">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="63dc9-117">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="63dc9-117">disable</span></span>  

<span data-ttu-id="63dc9-118">Отключение уведомлений домена страницы.</span><span class="sxs-lookup"><span data-stu-id="63dc9-118">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="63dc9-119">переход</span><span class="sxs-lookup"><span data-stu-id="63dc9-119">navigate</span></span>  

<span data-ttu-id="63dc9-120">Перемещает текущую страницу на данный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="63dc9-120">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="63dc9-121">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-121">Parameters</span></span> | <span data-ttu-id="63dc9-122">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-122">Type</span></span> | <span data-ttu-id="63dc9-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-123">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-124">url</span><span class="sxs-lookup"><span data-stu-id="63dc9-124">url</span></span> | `string` | <span data-ttu-id="63dc9-125">URL-адрес для навигации по странице.</span><span class="sxs-lookup"><span data-stu-id="63dc9-125">URL to navigate the page to.</span></span> |  
| <span data-ttu-id="63dc9-126">frameId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="63dc9-126">frameId \(optional\)</span></span> | [<span data-ttu-id="63dc9-127">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-127">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-128">Frame id для навигации.</span><span class="sxs-lookup"><span data-stu-id="63dc9-128">Frame id to navigate.</span></span>  <span data-ttu-id="63dc9-129">Если не указано, будет перемещаться на верхней странице.</span><span class="sxs-lookup"><span data-stu-id="63dc9-129">If not specified, will navigate the top page.</span></span> |  

| <span data-ttu-id="63dc9-130">Возвращает</span><span class="sxs-lookup"><span data-stu-id="63dc9-130">Returns</span></span> | <span data-ttu-id="63dc9-131">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-131">Type</span></span> | <span data-ttu-id="63dc9-132">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-132">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-133">frameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-133">frameId</span></span> | [<span data-ttu-id="63dc9-134">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-134">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-135">Frame id, который будет перемещаться.</span><span class="sxs-lookup"><span data-stu-id="63dc9-135">Frame id that will be navigated.</span></span> |  

---  

### <a name="getframetree"></a><span data-ttu-id="63dc9-136">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="63dc9-136">getFrameTree</span></span>  

<span data-ttu-id="63dc9-137">Возвращает представленную структуру дерева кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-137">Returns present frame tree structure.</span></span>  

| <span data-ttu-id="63dc9-138">Возвращает</span><span class="sxs-lookup"><span data-stu-id="63dc9-138">Returns</span></span> | <span data-ttu-id="63dc9-139">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-139">Type</span></span> | <span data-ttu-id="63dc9-140">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-140">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-141">frameTree</span><span class="sxs-lookup"><span data-stu-id="63dc9-141">frameTree</span></span> | [<span data-ttu-id="63dc9-142">FrameTree</span><span class="sxs-lookup"><span data-stu-id="63dc9-142">FrameTree</span></span>](#frametree) | <span data-ttu-id="63dc9-143">Представленная структура дерева кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-143">Present frame tree structure.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="63dc9-144">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="63dc9-144">Events</span></span>  

### <a name="frameattached"></a><span data-ttu-id="63dc9-145">frameAttached</span><span class="sxs-lookup"><span data-stu-id="63dc9-145">frameAttached</span></span>  

<span data-ttu-id="63dc9-146">Уволено, когда кадр был присоединен к родительскому.</span><span class="sxs-lookup"><span data-stu-id="63dc9-146">Fired when frame has been attached to its parent.</span></span>  

| <span data-ttu-id="63dc9-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-147">Parameters</span></span> | <span data-ttu-id="63dc9-148">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-148">Type</span></span> | <span data-ttu-id="63dc9-149">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-149">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-150">frameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-150">frameId</span></span> | [<span data-ttu-id="63dc9-151">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-151">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-152">Id прикрепленного кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-152">Id of the frame that has been attached.</span></span> |  
| <span data-ttu-id="63dc9-153">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-153">parentFrameId</span></span> | [<span data-ttu-id="63dc9-154">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-154">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-155">Идентификатор родительского кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-155">Parent frame identifier.</span></span> |  
| <span data-ttu-id="63dc9-156">stack \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="63dc9-156">stack \(optional\)</span></span> | [<span data-ttu-id="63dc9-157">Runtime.StackTrace</span><span class="sxs-lookup"><span data-stu-id="63dc9-157">Runtime.StackTrace</span></span>](./runtime.md#stacktrace) | <span data-ttu-id="63dc9-158">Трассировка стека JavaScript при присоединении кадра устанавливается только в том случае, если кадр инициировался из сценария.</span><span class="sxs-lookup"><span data-stu-id="63dc9-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span> |  

---  

### <a name="framedetached"></a><span data-ttu-id="63dc9-159">frameDetached</span><span class="sxs-lookup"><span data-stu-id="63dc9-159">frameDetached</span></span>  

<span data-ttu-id="63dc9-160">В случае, если кадр отсоединяется от родительского.</span><span class="sxs-lookup"><span data-stu-id="63dc9-160">Fired when frame has been detached from its parent.</span></span>  

| <span data-ttu-id="63dc9-161">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-161">Parameters</span></span> | <span data-ttu-id="63dc9-162">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-162">Type</span></span> | <span data-ttu-id="63dc9-163">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-163">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-164">frameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-164">frameId</span></span> | [<span data-ttu-id="63dc9-165">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-165">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-166">ID отсоединяемого кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-166">ID of the frame that has been detached.</span></span> |  

---  

### <a name="framenavigated"></a><span data-ttu-id="63dc9-167">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="63dc9-167">frameNavigated</span></span>  

<span data-ttu-id="63dc9-168">Уволен после завершения навигации по кадру.</span><span class="sxs-lookup"><span data-stu-id="63dc9-168">Fired once navigation of the frame has completed.</span></span>  

| <span data-ttu-id="63dc9-169">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-169">Parameters</span></span> | <span data-ttu-id="63dc9-170">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-170">Type</span></span> | <span data-ttu-id="63dc9-171">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-171">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-172">кадр</span><span class="sxs-lookup"><span data-stu-id="63dc9-172">frame</span></span> | [<span data-ttu-id="63dc9-173">Кадр</span><span class="sxs-lookup"><span data-stu-id="63dc9-173">Frame</span></span>](#frame) | <span data-ttu-id="63dc9-174">Объект Frame.</span><span class="sxs-lookup"><span data-stu-id="63dc9-174">Frame object.</span></span> |  

---  

### <a name="loadeventfired"></a><span data-ttu-id="63dc9-175">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="63dc9-175">loadEventFired</span></span>  

<span data-ttu-id="63dc9-176">Соответствует `window.onload` событию.</span><span class="sxs-lookup"><span data-stu-id="63dc9-176">Corresponds to the `window.onload` event.</span></span>  

| <span data-ttu-id="63dc9-177">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-177">Parameters</span></span> | <span data-ttu-id="63dc9-178">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-178">Type</span></span> | <span data-ttu-id="63dc9-179">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-179">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-180">timestamp</span><span class="sxs-lookup"><span data-stu-id="63dc9-180">timestamp</span></span> | `number` | <span data-ttu-id="63dc9-181">Количество миллисекунд с эпохи.</span><span class="sxs-lookup"><span data-stu-id="63dc9-181">Number of milliseconds since epoch.</span></span> |  

---  

### <a name="domcontenteventfired"></a><span data-ttu-id="63dc9-182">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="63dc9-182">domContentEventFired</span></span>  

<span data-ttu-id="63dc9-183">Соответствует `document.onDOMContentLoaded` событию.</span><span class="sxs-lookup"><span data-stu-id="63dc9-183">Corresponds to the `document.onDOMContentLoaded` event.</span></span>  

| <span data-ttu-id="63dc9-184">Параметры</span><span class="sxs-lookup"><span data-stu-id="63dc9-184">Parameters</span></span> | <span data-ttu-id="63dc9-185">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-185">Type</span></span> | <span data-ttu-id="63dc9-186">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-187">timestamp</span><span class="sxs-lookup"><span data-stu-id="63dc9-187">timestamp</span></span> | `number` | <span data-ttu-id="63dc9-188">Количество миллисекунд с эпохи.</span><span class="sxs-lookup"><span data-stu-id="63dc9-188">Number of milliseconds since epoch.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="63dc9-189">Типы</span><span class="sxs-lookup"><span data-stu-id="63dc9-189">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="63dc9-190">Строка FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-190">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="63dc9-191">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-191">Unique frame identifier.</span></span>  

&nbsp;  

---  

### <a name="frame-object"></a><span data-ttu-id="63dc9-192">Объект Frame</span><span class="sxs-lookup"><span data-stu-id="63dc9-192">Frame object</span></span>  

<a name="frame"></a>  

<span data-ttu-id="63dc9-193">Сведения о кадре на странице.</span><span class="sxs-lookup"><span data-stu-id="63dc9-193">Information about the Frame on the Page.</span></span>  

| <span data-ttu-id="63dc9-194">Свойства</span><span class="sxs-lookup"><span data-stu-id="63dc9-194">Properties</span></span> | <span data-ttu-id="63dc9-195">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-195">Type</span></span> | <span data-ttu-id="63dc9-196">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-196">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-197">id</span><span class="sxs-lookup"><span data-stu-id="63dc9-197">id</span></span> | [<span data-ttu-id="63dc9-198">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-198">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-199">Уникальный идентификатор frame.</span><span class="sxs-lookup"><span data-stu-id="63dc9-199">Frame unique identifier.</span></span> |  
| <span data-ttu-id="63dc9-200">parentId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="63dc9-200">parentId \(optional\)</span></span> | [<span data-ttu-id="63dc9-201">FrameId</span><span class="sxs-lookup"><span data-stu-id="63dc9-201">FrameId</span></span>](#frameid) | <span data-ttu-id="63dc9-202">Уникальный идентификатор родительской рамки.</span><span class="sxs-lookup"><span data-stu-id="63dc9-202">Parent frame unique identifier.</span></span> |  
| <span data-ttu-id="63dc9-203">имя \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="63dc9-203">name \(optional\)</span></span> | `string` | <span data-ttu-id="63dc9-204">Имя фрейма, указанное в теге.</span><span class="sxs-lookup"><span data-stu-id="63dc9-204">Frame's name as specified in the tag.</span></span> |  
| <span data-ttu-id="63dc9-205">url</span><span class="sxs-lookup"><span data-stu-id="63dc9-205">url</span></span> | `string` | <span data-ttu-id="63dc9-206">URL-адрес документа кадра.</span><span class="sxs-lookup"><span data-stu-id="63dc9-206">Frame document's URL.</span></span> |  
| <span data-ttu-id="63dc9-207">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="63dc9-207">securityOrigin</span></span> | `string` | <span data-ttu-id="63dc9-208">Происхождение безопасности кадрового документа.</span><span class="sxs-lookup"><span data-stu-id="63dc9-208">Frame document's security origin.</span></span> |  
| <span data-ttu-id="63dc9-209">mimeType</span><span class="sxs-lookup"><span data-stu-id="63dc9-209">mimeType</span></span> | `string` | <span data-ttu-id="63dc9-210">MimeType кадра документа, определяемого браузером.</span><span class="sxs-lookup"><span data-stu-id="63dc9-210">Frame document's mimeType as determined by the browser.</span></span> |  

---  

### <a name="frametree-object"></a><span data-ttu-id="63dc9-211">Объект FrameTree</span><span class="sxs-lookup"><span data-stu-id="63dc9-211">FrameTree object</span></span>  

<a name="frametree"></a>  

<span data-ttu-id="63dc9-212">Сведения об иерархии Frame.</span><span class="sxs-lookup"><span data-stu-id="63dc9-212">Information about the Frame hierarchy.</span></span>  

| <span data-ttu-id="63dc9-213">Свойства</span><span class="sxs-lookup"><span data-stu-id="63dc9-213">Properties</span></span> | <span data-ttu-id="63dc9-214">Тип</span><span class="sxs-lookup"><span data-stu-id="63dc9-214">Type</span></span> | <span data-ttu-id="63dc9-215">Сведения</span><span class="sxs-lookup"><span data-stu-id="63dc9-215">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63dc9-216">кадр</span><span class="sxs-lookup"><span data-stu-id="63dc9-216">frame</span></span> | [<span data-ttu-id="63dc9-217">Кадр</span><span class="sxs-lookup"><span data-stu-id="63dc9-217">Frame</span></span>](#frame) | <span data-ttu-id="63dc9-218">Сведения о кадре для этого элемента дерева.</span><span class="sxs-lookup"><span data-stu-id="63dc9-218">Frame information for this tree item.</span></span> |  
| <span data-ttu-id="63dc9-219">childFrames \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="63dc9-219">childFrames \(optional\)</span></span> | [<span data-ttu-id="63dc9-220">FrameTree[]</span><span class="sxs-lookup"><span data-stu-id="63dc9-220">FrameTree[]</span></span>](#frametree) | <span data-ttu-id="63dc9-221">Кадры для детей.</span><span class="sxs-lookup"><span data-stu-id="63dc9-221">Child frames.</span></span> |  

---  
