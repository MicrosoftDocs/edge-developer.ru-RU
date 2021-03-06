---
description: В режиме событий timeline отображаются все события, срабатывав при записи.  Используйте ссылку на события временной шкалы, чтобы узнать больше о каждом типе событий временной шкалы.
title: Справка о событиях Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398667"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="timeline-event-reference"></a><span data-ttu-id="f6376-105">Справка о событиях Timeline</span><span class="sxs-lookup"><span data-stu-id="f6376-105">Timeline Event reference</span></span>  

<span data-ttu-id="f6376-106">В режиме событий timeline отображаются все события, срабатывав при записи.</span><span class="sxs-lookup"><span data-stu-id="f6376-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="f6376-107">Используйте ссылку на события временной шкалы, чтобы узнать больше о каждом типе событий временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="f6376-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <a name="common-timeline-event-properties"></a><span data-ttu-id="f6376-108">Общие свойства событий временной шкалы</span><span class="sxs-lookup"><span data-stu-id="f6376-108">Common timeline event properties</span></span>  

<span data-ttu-id="f6376-109">Некоторые сведения присутствуют в событиях всех типов, а некоторые применяются только к определенным типам событий.</span><span class="sxs-lookup"><span data-stu-id="f6376-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="f6376-110">В этом разделе перечислены свойства, общие для различных типов событий.</span><span class="sxs-lookup"><span data-stu-id="f6376-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="f6376-111">Свойства, определенные определенным типам событий, перечислены в ссылках для последующих типов событий.</span><span class="sxs-lookup"><span data-stu-id="f6376-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="f6376-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6376-112">Property</span></span> | <span data-ttu-id="f6376-113">Когда показано</span><span class="sxs-lookup"><span data-stu-id="f6376-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-114">Совокупное время</span><span class="sxs-lookup"><span data-stu-id="f6376-114">Aggregated time</span></span> | <span data-ttu-id="f6376-115">Для событий с **вложенными событиями**время, заданной каждой категорией событий.</span><span class="sxs-lookup"><span data-stu-id="f6376-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="f6376-116">Стек вызовов</span><span class="sxs-lookup"><span data-stu-id="f6376-116">Call Stack</span></span> | <span data-ttu-id="f6376-117">Для событий с **детскими событиями**время, заданной каждой категорией событий.</span><span class="sxs-lookup"><span data-stu-id="f6376-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="f6376-118">Время ЦП</span><span class="sxs-lookup"><span data-stu-id="f6376-118">CPU time</span></span> | <span data-ttu-id="f6376-119">Сколько времени занял ЦП записанного события.</span><span class="sxs-lookup"><span data-stu-id="f6376-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="f6376-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="f6376-120">Details</span></span> | <span data-ttu-id="f6376-121">Другие сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="f6376-121">Other details about the event.</span></span> |  
| <span data-ttu-id="f6376-122">Duration \(at time-stamp\)</span><span class="sxs-lookup"><span data-stu-id="f6376-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="f6376-123">Сколько времени потребовалось на завершение события со всеми его детьми; timestamp — это время, в которое произошло событие, относительно времени начала записи.</span><span class="sxs-lookup"><span data-stu-id="f6376-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="f6376-124">Время самообнаправления</span><span class="sxs-lookup"><span data-stu-id="f6376-124">Self time</span></span> | <span data-ttu-id="f6376-125">Сколько времени заняло событие без детей.</span><span class="sxs-lookup"><span data-stu-id="f6376-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="f6376-126">Размер используемой кучи</span><span class="sxs-lookup"><span data-stu-id="f6376-126">Used Heap Size</span></span> | <span data-ttu-id="f6376-127">Количество памяти, используемой приложением при записи события, и дельта \(+/-\) изменяют размер используемой кучи с момента последней выборки.</span><span class="sxs-lookup"><span data-stu-id="f6376-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a><span data-ttu-id="f6376-128">События загрузки</span><span class="sxs-lookup"><span data-stu-id="f6376-128">Loading events</span></span>  

<span data-ttu-id="f6376-129">В этом разделе перечислены события, которые относятся к категории Loading и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="f6376-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="f6376-130">Событие</span><span class="sxs-lookup"><span data-stu-id="f6376-130">Event</span></span> | <span data-ttu-id="f6376-131">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-132">Parse HTML</span><span class="sxs-lookup"><span data-stu-id="f6376-132">Parse HTML</span></span> |  <span data-ttu-id="f6376-133">Microsoft Edge запустила алгоритм htmL-размыкания.</span><span class="sxs-lookup"><span data-stu-id="f6376-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="f6376-134">Finish Loading</span><span class="sxs-lookup"><span data-stu-id="f6376-134">Finish Loading</span></span> |  <span data-ttu-id="f6376-135">Запрос сети выполнен.</span><span class="sxs-lookup"><span data-stu-id="f6376-135">A network request completed.</span></span> |  
| <span data-ttu-id="f6376-136">Получение данных</span><span class="sxs-lookup"><span data-stu-id="f6376-136">Receive Data</span></span> |  <span data-ttu-id="f6376-137">Получены данные для запроса.</span><span class="sxs-lookup"><span data-stu-id="f6376-137">Data for a request was received.</span></span>  <span data-ttu-id="f6376-138">Существует одно или несколько событий получения данных.</span><span class="sxs-lookup"><span data-stu-id="f6376-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="f6376-139">Получение ответа</span><span class="sxs-lookup"><span data-stu-id="f6376-139">Receive Response</span></span> |  <span data-ttu-id="f6376-140">Начальный http-ответ от запроса.</span><span class="sxs-lookup"><span data-stu-id="f6376-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="f6376-141">Отправка запроса</span><span class="sxs-lookup"><span data-stu-id="f6376-141">Send Request</span></span> |  <span data-ttu-id="f6376-142">Отправлен запрос сети.</span><span class="sxs-lookup"><span data-stu-id="f6376-142">A network request has been sent.</span></span> |  

### <a name="loading-event-properties"></a><span data-ttu-id="f6376-143">Свойства событий загрузки</span><span class="sxs-lookup"><span data-stu-id="f6376-143">Loading event properties</span></span>  

| <span data-ttu-id="f6376-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6376-144">Property</span></span> | <span data-ttu-id="f6376-145">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-146">Ресурс</span><span class="sxs-lookup"><span data-stu-id="f6376-146">Resource</span></span> | <span data-ttu-id="f6376-147">URL-адрес запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6376-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="f6376-148">Preview</span><span class="sxs-lookup"><span data-stu-id="f6376-148">Preview</span></span> | <span data-ttu-id="f6376-149">Предварительный просмотр запрашиваемого ресурса \(только изображения\).</span><span class="sxs-lookup"><span data-stu-id="f6376-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="f6376-150">Метод запроса</span><span class="sxs-lookup"><span data-stu-id="f6376-150">Request Method</span></span> | <span data-ttu-id="f6376-151">МЕТОД HTTP, используемый для запроса \( `GET` или `POST` , например\).</span><span class="sxs-lookup"><span data-stu-id="f6376-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="f6376-152">Код состояния</span><span class="sxs-lookup"><span data-stu-id="f6376-152">Status Code</span></span> | <span data-ttu-id="f6376-153">Код ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="f6376-153">HTTP response code.</span></span> |  
| <span data-ttu-id="f6376-154">Тип MIME</span><span class="sxs-lookup"><span data-stu-id="f6376-154">MIME Type</span></span> | <span data-ttu-id="f6376-155">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6376-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="f6376-156">Закодированная длина данных</span><span class="sxs-lookup"><span data-stu-id="f6376-156">Encoded Data Length</span></span> | <span data-ttu-id="f6376-157">Длина запрашиваемого ресурса в bytes.</span><span class="sxs-lookup"><span data-stu-id="f6376-157">Length of requested resource in bytes.</span></span> |  

## <a name="scripting-events"></a><span data-ttu-id="f6376-158">События сценариев</span><span class="sxs-lookup"><span data-stu-id="f6376-158">Scripting events</span></span>  

<span data-ttu-id="f6376-159">В этом разделе перечислены события, которые относятся к категории Scripting и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="f6376-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="f6376-160">Событие</span><span class="sxs-lookup"><span data-stu-id="f6376-160">Event</span></span> | <span data-ttu-id="f6376-161">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-162">Кадр анимации</span><span class="sxs-lookup"><span data-stu-id="f6376-162">Animation Frame Fired</span></span> | <span data-ttu-id="f6376-163">Уволена запланированная анимационная рамка и вызван обработник вызова.</span><span class="sxs-lookup"><span data-stu-id="f6376-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="f6376-164">Отмена кадра анимации</span><span class="sxs-lookup"><span data-stu-id="f6376-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="f6376-165">Запланированный кадр анимации был отменен.</span><span class="sxs-lookup"><span data-stu-id="f6376-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="f6376-166">Событие GC</span><span class="sxs-lookup"><span data-stu-id="f6376-166">GC Event</span></span> |  <span data-ttu-id="f6376-167">Произошел сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="f6376-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="f6376-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="f6376-168">DOMContentLoaded</span></span> |  <span data-ttu-id="f6376-169">Событие [DOMContentLoaded][MDNWindowDOMContentLoadedEvent] было уволено браузером.</span><span class="sxs-lookup"><span data-stu-id="f6376-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="f6376-170">Это событие происходит при загрузке и размыве всего контента DOM страницы.</span><span class="sxs-lookup"><span data-stu-id="f6376-170">This event is fired when all of the DOM content of the page is loaded and parsed.</span></span> |  
| <span data-ttu-id="f6376-171">Оценка скрипта</span><span class="sxs-lookup"><span data-stu-id="f6376-171">Evaluate Script</span></span> | <span data-ttu-id="f6376-172">Был оценен сценарий.</span><span class="sxs-lookup"><span data-stu-id="f6376-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="f6376-173">Событие</span><span class="sxs-lookup"><span data-stu-id="f6376-173">Event</span></span> | <span data-ttu-id="f6376-174">Событие JavaScript \(например, `mousedown` или `key` \).</span><span class="sxs-lookup"><span data-stu-id="f6376-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="f6376-175">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="f6376-175">Function Call</span></span> | <span data-ttu-id="f6376-176">Вызов функции JavaScript верхнего уровня был выполнен \(появляется только при входе браузера в javaScript engine\).</span><span class="sxs-lookup"><span data-stu-id="f6376-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="f6376-177">Установка timer</span><span class="sxs-lookup"><span data-stu-id="f6376-177">Install Timer</span></span> | <span data-ttu-id="f6376-178">Был создан timer с [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] или [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="f6376-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="f6376-179">Кадр запроса анимации</span><span class="sxs-lookup"><span data-stu-id="f6376-179">Request Animation Frame</span></span> | <span data-ttu-id="f6376-180">Вызов `requestAnimationFrame()` запланил новый кадр.</span><span class="sxs-lookup"><span data-stu-id="f6376-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="f6376-181">Удаление timer</span><span class="sxs-lookup"><span data-stu-id="f6376-181">Remove Timer</span></span> | <span data-ttu-id="f6376-182">Ранее созданный timer был очищен.</span><span class="sxs-lookup"><span data-stu-id="f6376-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="f6376-183">Время</span><span class="sxs-lookup"><span data-stu-id="f6376-183">Time</span></span> |  <span data-ttu-id="f6376-184">Скрипт под [названием console.time()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="f6376-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="f6376-185">Время окончания</span><span class="sxs-lookup"><span data-stu-id="f6376-185">Time End</span></span> | <span data-ttu-id="f6376-186">Скрипт под [названием console.timeEnd()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="f6376-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="f6376-187">Отсев времени</span><span class="sxs-lookup"><span data-stu-id="f6376-187">Timer Fired</span></span> | <span data-ttu-id="f6376-188">Отсвеченный ото всех часов, запланированный с `setInterval()` помощью или `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="f6376-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="f6376-189">Изменение состояния готовности XHR</span><span class="sxs-lookup"><span data-stu-id="f6376-189">XHR Ready State Change</span></span> | <span data-ttu-id="f6376-190">Изменено готовое состояние XMLHTTPRequest.</span><span class="sxs-lookup"><span data-stu-id="f6376-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="f6376-191">XHR Load</span><span class="sxs-lookup"><span data-stu-id="f6376-191">XHR Load</span></span> | <span data-ttu-id="f6376-192">Готовая `XMLHTTPRequest` загрузка.</span><span class="sxs-lookup"><span data-stu-id="f6376-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <a name="scripting-event-properties"></a><span data-ttu-id="f6376-193">Свойства событий сценариев</span><span class="sxs-lookup"><span data-stu-id="f6376-193">Scripting event properties</span></span>  

| <span data-ttu-id="f6376-194">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6376-194">Property</span></span> | <span data-ttu-id="f6376-195">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-196">Timer ID</span><span class="sxs-lookup"><span data-stu-id="f6376-196">Timer ID</span></span> | <span data-ttu-id="f6376-197">ИД отмерить.</span><span class="sxs-lookup"><span data-stu-id="f6376-197">The timer ID.</span></span> |  
| <span data-ttu-id="f6376-198">Превышено время ожидания</span><span class="sxs-lookup"><span data-stu-id="f6376-198">Timeout</span></span> | <span data-ttu-id="f6376-199">Время, указанное в отоимке.</span><span class="sxs-lookup"><span data-stu-id="f6376-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="f6376-200">Повторы</span><span class="sxs-lookup"><span data-stu-id="f6376-200">Repeats</span></span> | <span data-ttu-id="f6376-201">Boolean, который указывает, повторяется ли отсвечив.</span><span class="sxs-lookup"><span data-stu-id="f6376-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="f6376-202">Вызов функции</span><span class="sxs-lookup"><span data-stu-id="f6376-202">Function Call</span></span> | <span data-ttu-id="f6376-203">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="f6376-203">A function that was invoked.</span></span> |  

## <a name="rendering-events"></a><span data-ttu-id="f6376-204">События визуализации</span><span class="sxs-lookup"><span data-stu-id="f6376-204">Rendering events</span></span>  

<span data-ttu-id="f6376-205">В этом разделе перечислены события, которые относятся к категории Rendering и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="f6376-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="f6376-206">Событие</span><span class="sxs-lookup"><span data-stu-id="f6376-206">Event</span></span> | <span data-ttu-id="f6376-207">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-208">Недействительный макет</span><span class="sxs-lookup"><span data-stu-id="f6376-208">Invalidate layout</span></span> | <span data-ttu-id="f6376-209">Макет страницы был признан недействительным из-за изменения DOM.</span><span class="sxs-lookup"><span data-stu-id="f6376-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="f6376-210">Макет</span><span class="sxs-lookup"><span data-stu-id="f6376-210">Layout</span></span> | <span data-ttu-id="f6376-211">Макет страницы завершен.</span><span class="sxs-lookup"><span data-stu-id="f6376-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="f6376-212">Стиль пересчета</span><span class="sxs-lookup"><span data-stu-id="f6376-212">Recalculate style</span></span> | <span data-ttu-id="f6376-213">Microsoft Edge пересчитал стили элементов.</span><span class="sxs-lookup"><span data-stu-id="f6376-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="f6376-214">Scroll</span><span class="sxs-lookup"><span data-stu-id="f6376-214">Scroll</span></span> | <span data-ttu-id="f6376-215">Содержимое вложенного представления было прокрутки.</span><span class="sxs-lookup"><span data-stu-id="f6376-215">The content of nested view was scrolled.</span></span> |  

### <a name="rendering-event-properties"></a><span data-ttu-id="f6376-216">Свойства отрисовки событий</span><span class="sxs-lookup"><span data-stu-id="f6376-216">Rendering event properties</span></span>  

| <span data-ttu-id="f6376-217">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6376-217">Property</span></span> | <span data-ttu-id="f6376-218">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-219">Недействительный макет</span><span class="sxs-lookup"><span data-stu-id="f6376-219">Layout invalidated</span></span> | <span data-ttu-id="f6376-220">Для записей layout трассировка кода, из-за чего макет был признан недействительным.</span><span class="sxs-lookup"><span data-stu-id="f6376-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="f6376-221">Узлы, которые нуждаются в макете</span><span class="sxs-lookup"><span data-stu-id="f6376-221">Nodes that need layout</span></span> | <span data-ttu-id="f6376-222">Для записей Layout количество узлов, отмеченных как нуждающийся макет до начала ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f6376-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="f6376-223">Как правило, это те узлы, которые были признаны недействительными кодом разработчика, а также путь вверх к корнею ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="f6376-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="f6376-224">Размер дерева макета</span><span class="sxs-lookup"><span data-stu-id="f6376-224">Layout tree size</span></span> | <span data-ttu-id="f6376-225">Для записей макета общее число узлов под корнем ретрансляторов \(узел, который Microsoft Edge запускает ретранслятор\).</span><span class="sxs-lookup"><span data-stu-id="f6376-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="f6376-226">Область макета</span><span class="sxs-lookup"><span data-stu-id="f6376-226">Layout scope</span></span> | <span data-ttu-id="f6376-227">Возможные значения \ (граница повторного макета является `Partial` частью DOM\) или `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="f6376-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="f6376-228">Элементы, затронутые</span><span class="sxs-lookup"><span data-stu-id="f6376-228">Elements affected</span></span> | <span data-ttu-id="f6376-229">Для пересчета записей стилей количество элементов, затронутых перерасчетом стиля.</span><span class="sxs-lookup"><span data-stu-id="f6376-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="f6376-230">Стили недействительны</span><span class="sxs-lookup"><span data-stu-id="f6376-230">Styles invalidated</span></span> | <span data-ttu-id="f6376-231">Для пересчета записей стилей предоставляется след стека кода, из-за чего стиль был признан недействительным.</span><span class="sxs-lookup"><span data-stu-id="f6376-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <a name="painting-events"></a><span data-ttu-id="f6376-232">События рисования</span><span class="sxs-lookup"><span data-stu-id="f6376-232">Painting events</span></span>  

<span data-ttu-id="f6376-233">В этом разделе перечислены события, которые относятся к категории Painting и их свойствам.</span><span class="sxs-lookup"><span data-stu-id="f6376-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="f6376-234">Событие</span><span class="sxs-lookup"><span data-stu-id="f6376-234">Event</span></span> | <span data-ttu-id="f6376-235">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-236">Композитные слои</span><span class="sxs-lookup"><span data-stu-id="f6376-236">Composite Layers</span></span> | <span data-ttu-id="f6376-237">Композитные слои изображений для движка отрисовки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f6376-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="f6376-238">Расшифровка изображения</span><span class="sxs-lookup"><span data-stu-id="f6376-238">Image Decode</span></span> | <span data-ttu-id="f6376-239">Расшифровка ресурса изображений.</span><span class="sxs-lookup"><span data-stu-id="f6376-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="f6376-240">Image Resize</span><span class="sxs-lookup"><span data-stu-id="f6376-240">Image Resize</span></span> | <span data-ttu-id="f6376-241">Изображение было реамизировано из его родных размеров.</span><span class="sxs-lookup"><span data-stu-id="f6376-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="f6376-242">Paint</span><span class="sxs-lookup"><span data-stu-id="f6376-242">Paint</span></span> | <span data-ttu-id="f6376-243">Композитные слои были окрашены в область дисплея.</span><span class="sxs-lookup"><span data-stu-id="f6376-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="f6376-244">При наведении на запись Paint выделяется область обновленного отображения.</span><span class="sxs-lookup"><span data-stu-id="f6376-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <a name="painting-event-properties"></a><span data-ttu-id="f6376-245">Свойства событий рисования</span><span class="sxs-lookup"><span data-stu-id="f6376-245">Painting event properties</span></span>  

| <span data-ttu-id="f6376-246">Свойство</span><span class="sxs-lookup"><span data-stu-id="f6376-246">Property</span></span> | <span data-ttu-id="f6376-247">Описание</span><span class="sxs-lookup"><span data-stu-id="f6376-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="f6376-248">Расположение</span><span class="sxs-lookup"><span data-stu-id="f6376-248">Location</span></span> | <span data-ttu-id="f6376-249">Для событий Paint x и y координаты прямоугольника краски.</span><span class="sxs-lookup"><span data-stu-id="f6376-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="f6376-250">Размеры</span><span class="sxs-lookup"><span data-stu-id="f6376-250">Dimensions</span></span> | <span data-ttu-id="f6376-251">Для событий Paint высота и ширина расписной области.</span><span class="sxs-lookup"><span data-stu-id="f6376-251">For Paint events, the height and width of the painted region.</span></span> |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f6376-252">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6376-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Ссылка на API консоли"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd — ссылка на API консоли"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Окно: событие DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> <span data-ttu-id="f6376-258">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6376-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f6376-259">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span><span class="sxs-lookup"><span data-stu-id="f6376-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f6376-261">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f6376-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
