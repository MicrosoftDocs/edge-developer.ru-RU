---
description: Справка по домену DOM. Этот домен предоставляет операции чтения и записи DOM. Каждый узел DOM представлен своим зеркальным объектом с объектом `id` . Это можно использовать для получения дополнительных сведений о узле, его разрешения в оболочку объекта JavaScript и т. `id` д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Тыловой узел отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Сбор сведений о узлах, отправленных клиенту, несет ответственность клиент.<p>Обратите `iframe` внимание, что элементы-владельцы возвращают соответствующие элементы документа в качестве своих узлы.</p>
title: Домен DOM — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235566"
---
# <span data-ttu-id="98ff3-109">DOM</span><span class="sxs-lookup"><span data-stu-id="98ff3-109">DOM</span></span>

<span data-ttu-id="98ff3-110">Этот домен предоставляет операции чтения и записи DOM.</span><span class="sxs-lookup"><span data-stu-id="98ff3-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="98ff3-111">Каждый узел DOM представлен своим зеркальным объектом с объектом `id` .</span><span class="sxs-lookup"><span data-stu-id="98ff3-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="98ff3-112">Это `id` можно использовать для получения дополнительных сведений об узле, ее разрешения в оболочку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту.</span><span class="sxs-lookup"><span data-stu-id="98ff3-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="98ff3-113">Тыловой узел отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды.</span><span class="sxs-lookup"><span data-stu-id="98ff3-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="98ff3-114">Сбор сведений о узлах, отправленных клиенту, несет ответственность клиент.</span><span class="sxs-lookup"><span data-stu-id="98ff3-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="98ff3-115">Обратите `iframe` внимание, что элементы-владельцы возвращают соответствующие элементы документа в качестве их узлы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="98ff3-116">Методы</span><span class="sxs-lookup"><span data-stu-id="98ff3-116">Methods</span></span>**](#methods) | <span data-ttu-id="98ff3-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode , resolveNode](#requestnode), [setInspectedNode](#setinspectednode) [](#resolvenode)</span><span class="sxs-lookup"><span data-stu-id="98ff3-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="98ff3-118">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="98ff3-118">Events</span></span>**](#events) | <span data-ttu-id="98ff3-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="98ff3-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="98ff3-120">Типы</span><span class="sxs-lookup"><span data-stu-id="98ff3-120">Types</span></span>**](#types) | <span data-ttu-id="98ff3-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="98ff3-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="98ff3-122">Зависимости</span><span class="sxs-lookup"><span data-stu-id="98ff3-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="98ff3-123">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="98ff3-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="98ff3-124">Методы</span><span class="sxs-lookup"><span data-stu-id="98ff3-124">Methods</span></span>

### <span data-ttu-id="98ff3-125">"Включить"</span><span class="sxs-lookup"><span data-stu-id="98ff3-125">enable</span></span>
<span data-ttu-id="98ff3-126">Включает агент DOM для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="98ff3-127">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="98ff3-127">disable</span></span>
<span data-ttu-id="98ff3-128">Отключает агент DOM для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="98ff3-129">Отключение DOM сделает недопустимыми все ранее допустимые nodeId.</span><span class="sxs-lookup"><span data-stu-id="98ff3-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="98ff3-130">getDocument</span><span class="sxs-lookup"><span data-stu-id="98ff3-130">getDocument</span></span>
<span data-ttu-id="98ff3-131">Возвращает корневой узел DOM (и, при желании, поддерево) вызываемой.</span><span class="sxs-lookup"><span data-stu-id="98ff3-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="98ff3-132">Вызов `getDocument` аннулирует все ранее допустимые nodeIds</span><span class="sxs-lookup"><span data-stu-id="98ff3-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-133">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-134">depth</span><span class="sxs-lookup"><span data-stu-id="98ff3-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-135">Максимальная глубина, на которой должны быть извлечены дети, по умолчанию составляет 2.</span><span class="sxs-lookup"><span data-stu-id="98ff3-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="98ff3-136">Используйте -1 для всего подtree.</span><span class="sxs-lookup"><span data-stu-id="98ff3-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-137">1</span><span class="sxs-lookup"><span data-stu-id="98ff3-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="98ff3-138">Следует ли обходить iframes при возвращении подtree (по умолчанию — false).</span><span class="sxs-lookup"><span data-stu-id="98ff3-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-139">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-140">root</span><span class="sxs-lookup"><span data-stu-id="98ff3-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="98ff3-141">Итоговая точка узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="98ff3-142">highlightNode</span></span>
<span data-ttu-id="98ff3-143">Узел DOM Higlights с заданным идом или оболочкой объекта.</span><span class="sxs-lookup"><span data-stu-id="98ff3-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="98ff3-144">Должны быть указаны nodeId, backendNodeId или objectId.</span><span class="sxs-lookup"><span data-stu-id="98ff3-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-145">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-146">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-146">nodeId</span></span> <br/> <i><span data-ttu-id="98ff3-147">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-148">Идентификатор узла, который нужно выделить.</span><span class="sxs-lookup"><span data-stu-id="98ff3-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="98ff3-150">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="98ff3-151">Идентификатор выделяемого тылового узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-152">objectId</span><span class="sxs-lookup"><span data-stu-id="98ff3-152">objectId</span></span> <br/> <i><span data-ttu-id="98ff3-153">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="98ff3-154">JavaScript object id of the node to be highlighted.</span><span class="sxs-lookup"><span data-stu-id="98ff3-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="98ff3-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="98ff3-156">Дескриптор внешнего вида выделения.</span><span class="sxs-lookup"><span data-stu-id="98ff3-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-157">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-158">root</span><span class="sxs-lookup"><span data-stu-id="98ff3-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="98ff3-159">Итоговая точка узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="98ff3-160">hideHighlight</span></span>
<span data-ttu-id="98ff3-161">Скрывает текущее выделение узла DOM.</span><span class="sxs-lookup"><span data-stu-id="98ff3-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="98ff3-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="98ff3-162">requestChildNodes</span></span>
<span data-ttu-id="98ff3-163">Запросы на возврат детей узла с заданным идом вызываемой сети в виде `setChildNodes` событий.</span><span class="sxs-lookup"><span data-stu-id="98ff3-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="98ff3-164">будет запускаться для каждого узла, который ранее не вернул его узлы, начиная с запрашиваемого узла до указанной глубины.</span><span class="sxs-lookup"><span data-stu-id="98ff3-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-165">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-166">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-167">ИД узла для получения детей.</span><span class="sxs-lookup"><span data-stu-id="98ff3-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-168">depth</span><span class="sxs-lookup"><span data-stu-id="98ff3-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-169">Максимальная глубина, на которой должны быть извлечены дети, по умолчанию составляет 1.</span><span class="sxs-lookup"><span data-stu-id="98ff3-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="98ff3-170">Используйте -1 для всего подtree.</span><span class="sxs-lookup"><span data-stu-id="98ff3-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-171">1</span><span class="sxs-lookup"><span data-stu-id="98ff3-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="98ff3-172">Следует ли обходить iframes при возвращении подtree (по умолчанию — false).</span><span class="sxs-lookup"><span data-stu-id="98ff3-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-173">getAttributes</span><span class="sxs-lookup"><span data-stu-id="98ff3-173">getAttributes</span></span>
<span data-ttu-id="98ff3-174">Возвращает атрибуты для указанного узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-175">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-176">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-177">ИД узла, для который требуется получить attibutes.</span><span class="sxs-lookup"><span data-stu-id="98ff3-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-178">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-179">attributes</span><span class="sxs-lookup"><span data-stu-id="98ff3-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="98ff3-180">Массив между именами и значениями атрибутов узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="98ff3-181">getOuterHTML</span></span>
<span data-ttu-id="98ff3-182">Возвращает HTML-разметку узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-184">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-184">nodeId</span></span> <br/> <i><span data-ttu-id="98ff3-185">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-186">Идентификатор узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="98ff3-188">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="98ff3-189">Идентификатор заднего узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-190">objectId</span><span class="sxs-lookup"><span data-stu-id="98ff3-190">objectId</span></span> <br/> <i><span data-ttu-id="98ff3-191">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="98ff3-192">JavaScript object id of the node wrapper.</span><span class="sxs-lookup"><span data-stu-id="98ff3-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-193">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="98ff3-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-195">Внешняя разметка HTML.</span><span class="sxs-lookup"><span data-stu-id="98ff3-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="98ff3-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="98ff3-197">Ищет и соеди up Node Ids and resolves all parents for the specified Backend Node Ids</span><span class="sxs-lookup"><span data-stu-id="98ff3-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-198">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="98ff3-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="98ff3-200">ИД узлов, которые необходимо разрешить</span><span class="sxs-lookup"><span data-stu-id="98ff3-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-201">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="98ff3-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="98ff3-203">ИД узлов разрешенных узлов</span><span class="sxs-lookup"><span data-stu-id="98ff3-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="98ff3-204">querySelector</span></span>
<span data-ttu-id="98ff3-205">Выполняется `querySelector` на заданный узел.</span><span class="sxs-lookup"><span data-stu-id="98ff3-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-207">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-208">ИД узла для запроса.</span><span class="sxs-lookup"><span data-stu-id="98ff3-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-209">селектор</span><span class="sxs-lookup"><span data-stu-id="98ff3-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-210">Строка селектора.</span><span class="sxs-lookup"><span data-stu-id="98ff3-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-211">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-212">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-213">Результат селектора запросов.</span><span class="sxs-lookup"><span data-stu-id="98ff3-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="98ff3-214">querySelectorAll</span></span>
<span data-ttu-id="98ff3-215">Выполняется `querySelectorAll` на заданный узел.</span><span class="sxs-lookup"><span data-stu-id="98ff3-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-216">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-217">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-218">ИД узла для запроса.</span><span class="sxs-lookup"><span data-stu-id="98ff3-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-219">селектор</span><span class="sxs-lookup"><span data-stu-id="98ff3-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-220">Строка селектора.</span><span class="sxs-lookup"><span data-stu-id="98ff3-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-221">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="98ff3-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="98ff3-223">Результаты селектора запросов.</span><span class="sxs-lookup"><span data-stu-id="98ff3-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="98ff3-224">requestNode</span></span>
<span data-ttu-id="98ff3-225">Запрашивает, чтобы узел с заданным ид удаленного объекта был отправлен вызываемой.</span><span class="sxs-lookup"><span data-stu-id="98ff3-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="98ff3-226">Все узлы, которые формируют путь от узла к корню, также отправляются клиенту в виде серии `setChildNodes` уведомлений.</span><span class="sxs-lookup"><span data-stu-id="98ff3-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="98ff3-227">возвращает 0, если документ, содержащий запрашиваемого узла, ранее не запрашивался клиентом.</span><span class="sxs-lookup"><span data-stu-id="98ff3-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-228">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-229">objectId</span><span class="sxs-lookup"><span data-stu-id="98ff3-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="98ff3-230">JavaScript object Id to convert into node.</span><span class="sxs-lookup"><span data-stu-id="98ff3-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-231">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-232">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-233">ИД узла для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="98ff3-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="98ff3-234">resolveNode</span></span>
<span data-ttu-id="98ff3-235">Устраняет объект узла JavaScript для заданного NodeId или BackendNodeId.</span><span class="sxs-lookup"><span data-stu-id="98ff3-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-236">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-237">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-237">nodeId</span></span> <br/> <i><span data-ttu-id="98ff3-238">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-239">ИД узла, который требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="98ff3-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="98ff3-241">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="98ff3-242">ИД узла, который необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="98ff3-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-243">objectGroup</span><span class="sxs-lookup"><span data-stu-id="98ff3-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-244">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="98ff3-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-245">Возвращает</span><span class="sxs-lookup"><span data-stu-id="98ff3-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-246">объект</span><span class="sxs-lookup"><span data-stu-id="98ff3-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="98ff3-247">Оболочка объекта JavaScript для данного узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="98ff3-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="98ff3-249">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="98ff3-249">Experimental.</span></span> </b></span><span data-ttu-id="98ff3-250">Позволяет консоли ссылаться на предыдущий проверенный узел с заданным идом через $0-$4.</span><span class="sxs-lookup"><span data-stu-id="98ff3-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-251">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-252">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-253">ИД узла DOM, доступный с помощью API командной строки в размере 0–4 долларов США.</span><span class="sxs-lookup"><span data-stu-id="98ff3-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="98ff3-254">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="98ff3-254">Events</span></span>

### <span data-ttu-id="98ff3-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="98ff3-255">setChildNodes</span></span>
<span data-ttu-id="98ff3-256">Происходит, когда тыл хочет предоставить клиенту отсутствующие структуры DOM.</span><span class="sxs-lookup"><span data-stu-id="98ff3-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="98ff3-257">Это происходит при большинстве вызовов, запрашивающих nodeIds</span><span class="sxs-lookup"><span data-stu-id="98ff3-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-258">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-259">parentId</span><span class="sxs-lookup"><span data-stu-id="98ff3-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-260">Родительский узел для poplate с children.</span><span class="sxs-lookup"><span data-stu-id="98ff3-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-261">nodes</span><span class="sxs-lookup"><span data-stu-id="98ff3-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="98ff3-262">Массив child nodes.</span><span class="sxs-lookup"><span data-stu-id="98ff3-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="98ff3-263">attributeModified</span></span>
<span data-ttu-id="98ff3-264">Сработает, `Element` если изменен атрибут "атрибут".</span><span class="sxs-lookup"><span data-stu-id="98ff3-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-265">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-266">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-267">ИД узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="98ff3-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-268">name</span><span class="sxs-lookup"><span data-stu-id="98ff3-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-269">Имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="98ff3-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-270">value</span><span class="sxs-lookup"><span data-stu-id="98ff3-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-271">Значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="98ff3-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="98ff3-272">attributeRemoved</span></span>
<span data-ttu-id="98ff3-273">Список при `Element` удалении атрибута "атрибут".</span><span class="sxs-lookup"><span data-stu-id="98ff3-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-274">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-275">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-276">ИД узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="98ff3-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-277">name</span><span class="sxs-lookup"><span data-stu-id="98ff3-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-278">Имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="98ff3-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="98ff3-279">characterDataModified</span></span>
<span data-ttu-id="98ff3-280">Событие `DOMCharacterDataModified` Mirrors.</span><span class="sxs-lookup"><span data-stu-id="98ff3-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-281">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-282">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-283">ИД узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="98ff3-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="98ff3-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-285">Новое текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="98ff3-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="98ff3-286">childNodeInserted</span></span>
<span data-ttu-id="98ff3-287">Событие `DOMNodeInserted` Mirrors.</span><span class="sxs-lookup"><span data-stu-id="98ff3-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-288">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-290">ИД узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="98ff3-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-292">ИД предыдущего уровня вставляемого узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-293">node</span><span class="sxs-lookup"><span data-stu-id="98ff3-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="98ff3-294">Вставленные данные узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="98ff3-295">childNodeRemoved</span></span>
<span data-ttu-id="98ff3-296">Событие `DOMNodeRemoved` Mirrors.</span><span class="sxs-lookup"><span data-stu-id="98ff3-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-297">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ff3-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-299">ИД узла, который изменился.</span><span class="sxs-lookup"><span data-stu-id="98ff3-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-300">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-301">ИД удаляемого узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="98ff3-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="98ff3-302">documentUpdated</span></span>
<span data-ttu-id="98ff3-303">`Document`Ссвеяно, когда было полностью обновлено.</span><span class="sxs-lookup"><span data-stu-id="98ff3-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="98ff3-304">Более не допустимые ид узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="98ff3-305">Типы</span><span class="sxs-lookup"><span data-stu-id="98ff3-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="98ff3-306">RGBA</span><span class="sxs-lookup"><span data-stu-id="98ff3-306">RGBA</span></span> `object`

<span data-ttu-id="98ff3-307">Структура с цветом RGBA.</span><span class="sxs-lookup"><span data-stu-id="98ff3-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-308">Свойства</span><span class="sxs-lookup"><span data-stu-id="98ff3-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-309">r</span><span class="sxs-lookup"><span data-stu-id="98ff3-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-310">Красный компонент в диапазоне [0–255].</span><span class="sxs-lookup"><span data-stu-id="98ff3-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-311">g</span><span class="sxs-lookup"><span data-stu-id="98ff3-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-312">Зеленый компонент в диапазоне [0–255].</span><span class="sxs-lookup"><span data-stu-id="98ff3-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-313">b</span><span class="sxs-lookup"><span data-stu-id="98ff3-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-314">Синий компонент в диапазоне [0–255].</span><span class="sxs-lookup"><span data-stu-id="98ff3-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-315">а</span><span class="sxs-lookup"><span data-stu-id="98ff3-315">a</span></span> <br/> <i><span data-ttu-id="98ff3-316">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="98ff3-317">Альфа-компонент в диапазоне [0-1].</span><span class="sxs-lookup"><span data-stu-id="98ff3-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="98ff3-318">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="98ff3-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="98ff3-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="98ff3-319">HighlightConfig</span></span> `object`

<span data-ttu-id="98ff3-320">Данные конфигурации для выделения элементов страницы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-321">Свойства</span><span class="sxs-lookup"><span data-stu-id="98ff3-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="98ff3-322">contentColor</span></span> <br/> <i><span data-ttu-id="98ff3-323">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="98ff3-324">Цвет заливки в поле содержимого.</span><span class="sxs-lookup"><span data-stu-id="98ff3-324">The content box highlight fill color.</span></span> <span data-ttu-id="98ff3-325">Значение по умолчанию прозрачно.</span><span class="sxs-lookup"><span data-stu-id="98ff3-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="98ff3-326">paddingColor</span></span> <br/> <i><span data-ttu-id="98ff3-327">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="98ff3-328">Цвет заливки заполнения.</span><span class="sxs-lookup"><span data-stu-id="98ff3-328">The padding highlight fill color.</span></span> <span data-ttu-id="98ff3-329">Значение по умолчанию прозрачно.</span><span class="sxs-lookup"><span data-stu-id="98ff3-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-330">borderColor</span><span class="sxs-lookup"><span data-stu-id="98ff3-330">borderColor</span></span> <br/> <i><span data-ttu-id="98ff3-331">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="98ff3-332">Цвет заливки выделения границы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-332">The border highlight fill color.</span></span> <span data-ttu-id="98ff3-333">Значение по умолчанию прозрачно.</span><span class="sxs-lookup"><span data-stu-id="98ff3-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="98ff3-334">marginColor</span></span> <br/> <i><span data-ttu-id="98ff3-335">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="98ff3-336">Цвет заливки выделения полей.</span><span class="sxs-lookup"><span data-stu-id="98ff3-336">The margin highlight fill color.</span></span> <span data-ttu-id="98ff3-337">Значение по умолчанию прозрачно.</span><span class="sxs-lookup"><span data-stu-id="98ff3-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="98ff3-338">NodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-338">NodeId</span></span> `integer`

<span data-ttu-id="98ff3-339">Уникальный идентификатор узла DOM</span><span class="sxs-lookup"><span data-stu-id="98ff3-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="98ff3-340">Node</span><span class="sxs-lookup"><span data-stu-id="98ff3-340">Node</span></span> `object`

<span data-ttu-id="98ff3-341">Зеркальный объект, который представляет фактические узлы DOM.</span><span class="sxs-lookup"><span data-stu-id="98ff3-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="98ff3-342">Свойства</span><span class="sxs-lookup"><span data-stu-id="98ff3-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="98ff3-343">nodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-344">Идентификатор узла, используемый для ссылки на этот узел.</span><span class="sxs-lookup"><span data-stu-id="98ff3-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="98ff3-345">На тыловом узле будут происходить события DOM для узлов с узлом NodeId, известным клиенту</span><span class="sxs-lookup"><span data-stu-id="98ff3-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-346">parentId</span><span class="sxs-lookup"><span data-stu-id="98ff3-346">parentId</span></span> <br/> <i><span data-ttu-id="98ff3-347">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-348">Идентификатор узла родительского узла(если он есть).</span><span class="sxs-lookup"><span data-stu-id="98ff3-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="98ff3-350">Идентификатор заднего узла узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="98ff3-351">BackendNodeIds ссылается на узлы, которые могут быть известны клиенту, но не выдают события DOM для этого узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-352">nodeType</span><span class="sxs-lookup"><span data-stu-id="98ff3-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="98ff3-353">'s nodeType.</span><span class="sxs-lookup"><span data-stu-id="98ff3-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-354">nodeName</span><span class="sxs-lookup"><span data-stu-id="98ff3-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="98ff3-355">'s nodeName.</span><span class="sxs-lookup"><span data-stu-id="98ff3-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-356">localName</span><span class="sxs-lookup"><span data-stu-id="98ff3-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="98ff3-357">'s localName</span><span class="sxs-lookup"><span data-stu-id="98ff3-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-358">nodeValue</span><span class="sxs-lookup"><span data-stu-id="98ff3-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="98ff3-359">'s nodeValue</span><span class="sxs-lookup"><span data-stu-id="98ff3-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="98ff3-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="98ff3-361">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="98ff3-362">Количество детей для `Container` узлов.</span><span class="sxs-lookup"><span data-stu-id="98ff3-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-363">дети</span><span class="sxs-lookup"><span data-stu-id="98ff3-363">children</span></span> <br/> <i><span data-ttu-id="98ff3-364">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="98ff3-365">Узлы этого узла по запросу с их children.</span><span class="sxs-lookup"><span data-stu-id="98ff3-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-366">attributes</span><span class="sxs-lookup"><span data-stu-id="98ff3-366">attributes</span></span> <br/> <i><span data-ttu-id="98ff3-367">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="98ff3-368">Атрибуты узлов в виде плоского массива `Element` "[name1, value1, name2, value2]</span><span class="sxs-lookup"><span data-stu-id="98ff3-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="98ff3-369">documentURL</span></span> <br/> <i><span data-ttu-id="98ff3-370">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-371">URL-адрес `Document` документа, на который указывают узлы.</span><span class="sxs-lookup"><span data-stu-id="98ff3-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="98ff3-372">baseURL</span></span> <br/> <i><span data-ttu-id="98ff3-373">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="98ff3-374">URL-адрес `Document` документа, который узлы используют для завершения URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="98ff3-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-375">publicId</span><span class="sxs-lookup"><span data-stu-id="98ff3-375">publicId</span></span> <br/> <i><span data-ttu-id="98ff3-376">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="98ff3-377">PublicId узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-378">systemId</span><span class="sxs-lookup"><span data-stu-id="98ff3-378">systemId</span></span> <br/> <i><span data-ttu-id="98ff3-379">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="98ff3-380">SystemId узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-381">internalSubset</span><span class="sxs-lookup"><span data-stu-id="98ff3-381">internalSubset</span></span> <br/> <i><span data-ttu-id="98ff3-382">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="98ff3-383">InternalSubset узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-384">xmlVersion</span><span class="sxs-lookup"><span data-stu-id="98ff3-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="98ff3-385">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="98ff3-386">XML-версия узла в случае XML-документов.</span><span class="sxs-lookup"><span data-stu-id="98ff3-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-387">name</span><span class="sxs-lookup"><span data-stu-id="98ff3-387">name</span></span> <br/> <i><span data-ttu-id="98ff3-388">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="98ff3-389">Имя узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-390">value</span><span class="sxs-lookup"><span data-stu-id="98ff3-390">value</span></span> <br/> <i><span data-ttu-id="98ff3-391">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="98ff3-392">Значение узла.</span><span class="sxs-lookup"><span data-stu-id="98ff3-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-393">frameId</span><span class="sxs-lookup"><span data-stu-id="98ff3-393">frameId</span></span> <br/> <i><span data-ttu-id="98ff3-394">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="98ff3-395">ИД фрейма для элементов владельца кадра.</span><span class="sxs-lookup"><span data-stu-id="98ff3-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="98ff3-396">contentDocument</span></span> <br/> <i><span data-ttu-id="98ff3-397">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="98ff3-398">Контентный документ для элементов владельца кадра.</span><span class="sxs-lookup"><span data-stu-id="98ff3-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="98ff3-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="98ff3-399">isSVG</span></span> <br/> <i><span data-ttu-id="98ff3-400">необязательные</span><span class="sxs-lookup"><span data-stu-id="98ff3-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="98ff3-401">Имеет true, если узел является SVG.</span><span class="sxs-lookup"><span data-stu-id="98ff3-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="98ff3-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="98ff3-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="98ff3-403">Уникальный идентификатор узла DOM, используемый для ссылки на узел, который, возможно, не был передавлен на передний.</span><span class="sxs-lookup"><span data-stu-id="98ff3-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="98ff3-404">PseudoType</span><span class="sxs-lookup"><span data-stu-id="98ff3-404">PseudoType</span></span> `string`

<span data-ttu-id="98ff3-405">Псевдоэлементный тип.</span><span class="sxs-lookup"><span data-stu-id="98ff3-405">Pseudo element type.</span></span>

##### <span data-ttu-id="98ff3-406">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="98ff3-406">Allowed Values</span></span>
<span data-ttu-id="98ff3-407">first-line, first-letter, before, after, selection</span><span class="sxs-lookup"><span data-stu-id="98ff3-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="98ff3-408">Зависимости</span><span class="sxs-lookup"><span data-stu-id="98ff3-408">Dependencies</span></span>

[<span data-ttu-id="98ff3-409">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="98ff3-409">Runtime</span></span>](runtime.md)
