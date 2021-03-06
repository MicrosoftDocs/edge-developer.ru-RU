---
description: Используйте API консоли для записи сообщений на консоль.
title: Ссылка на API консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398051"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="console-api-reference"></a><span data-ttu-id="bbcd5-104">Ссылка на API консоли</span><span class="sxs-lookup"><span data-stu-id="bbcd5-104">Console API reference</span></span>  

<span data-ttu-id="bbcd5-105">Используйте методы API консоли для записи сообщений на консоль из JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="bbcd5-106">Для интерактивного знакомства с этой темой перейдите к разделу Начало работы с ведением журнала [сообщений на консоли.][DevtoolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="bbcd5-107">Для таких удобных методов, как или доступных только из области консоли, перейдите к ссылке `debug()` `monitorEvents()` [API API консоли utilities.][DevtoolConsoleUtilities] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bbcd5-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="bbcd5-108">утверждения</span><span class="sxs-lookup"><span data-stu-id="bbcd5-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="bbcd5-109">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="bbcd5-110">Записывает [ошибку](#error) на консоль при `expression` оценке `false` .</span><span class="sxs-lookup"><span data-stu-id="bbcd5-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Результат примера console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="bbcd5-112">Рис. 1. Результат `console.assert()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="bbcd5-113">clear</span><span class="sxs-lookup"><span data-stu-id="bbcd5-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="bbcd5-114">Очищает консоль.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="bbcd5-115">Если [включен журнал сохранения,][DevtoolsConsoleReferenceLevel] [четкий](#clear) метод отключен.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <a name="see-also"></a><span data-ttu-id="bbcd5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bbcd5-116">See also</span></span>  

*   [<span data-ttu-id="bbcd5-117">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="bbcd5-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="bbcd5-118">количество</span><span class="sxs-lookup"><span data-stu-id="bbcd5-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="bbcd5-119">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-120">Записывает количество раз, когда метод [подсчета](#count) вызывался в одной строке и с той же `label` строкой .</span><span class="sxs-lookup"><span data-stu-id="bbcd5-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="bbcd5-121">Чтобы сбросить количество, используйте метод [countReset.](#countreset)</span><span class="sxs-lookup"><span data-stu-id="bbcd5-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Результат примера console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="bbcd5-123">Рис. 2. Результат `console.count()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="bbcd5-124">countReset</span><span class="sxs-lookup"><span data-stu-id="bbcd5-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="bbcd5-125">Сбрасывает количество.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a><span data-ttu-id="bbcd5-126">отладка</span><span class="sxs-lookup"><span data-stu-id="bbcd5-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="bbcd5-127">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="bbcd5-128">Идентично [журналу,](#log) за исключением разного уровня журнала.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Результат примера console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="bbcd5-130">Рис. 3. Результат `console.debug()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <a name="dir"></a><span data-ttu-id="bbcd5-131">dir</span><span class="sxs-lookup"><span data-stu-id="bbcd5-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="bbcd5-132">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-133">Печать представления JSON указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Пример console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="bbcd5-135">Рис. 4. Результат `console.dir()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="bbcd5-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="bbcd5-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="bbcd5-137">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-138">Печать XML-представления потомков `node` .</span><span class="sxs-lookup"><span data-stu-id="bbcd5-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Результат примера console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="bbcd5-140">Рис. 5. Результат `console.dirxml()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <a name="error"></a><span data-ttu-id="bbcd5-141">ошибка</span><span class="sxs-lookup"><span data-stu-id="bbcd5-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="bbcd5-142">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="bbcd5-143">Принты `object` на консоль, форматирование ее как ошибку, и включает трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Пример console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="bbcd5-145">Рис. 6. Результат `console.error()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <a name="group"></a><span data-ttu-id="bbcd5-146">группа</span><span class="sxs-lookup"><span data-stu-id="bbcd5-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="bbcd5-147">Визуально группит сообщения вместе до тех пор, пока не будет использован метод [groupEnd.](#groupend)</span><span class="sxs-lookup"><span data-stu-id="bbcd5-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="bbcd5-148">Используйте метод [groupCollapsed,](#groupcollapsed) чтобы обвалить группу при первоначальном входе в консоль.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Пример console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="bbcd5-150">Рис. 7. Результат `console.group()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="bbcd5-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="bbcd5-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="bbcd5-152">То же, [что](#log) и метод журнала, за исключением того, что группа сначала разрушается при входе в консоль.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <a name="groupend"></a><span data-ttu-id="bbcd5-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="bbcd5-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="bbcd5-154">Остановка визуальной группировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="bbcd5-155">Перейдите к [групповому методу.](#group)</span><span class="sxs-lookup"><span data-stu-id="bbcd5-155">Navigate to the [group](#group) method.</span></span>  

---  

## <a name="info"></a><span data-ttu-id="bbcd5-156">"Сведения"</span><span class="sxs-lookup"><span data-stu-id="bbcd5-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="bbcd5-157">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-158">Идентично [методу журнала.](#log)</span><span class="sxs-lookup"><span data-stu-id="bbcd5-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Результат примера console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="bbcd5-160">Рис. 8. Результат `console.info()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <a name="log"></a><span data-ttu-id="bbcd5-161">журнал</span><span class="sxs-lookup"><span data-stu-id="bbcd5-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="bbcd5-162">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-163">Печать сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Пример console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="bbcd5-165">Рис. 9. Результат `console.log()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <a name="table"></a><span data-ttu-id="bbcd5-166">таблица</span><span class="sxs-lookup"><span data-stu-id="bbcd5-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="bbcd5-167">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-168">Регистрит массив объектов в качестве таблицы.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-168">Logs an array of objects as a table.</span></span>  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Пример console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="bbcd5-170">Рис. 10. Результат `console.table()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <a name="time"></a><span data-ttu-id="bbcd5-171">time</span><span class="sxs-lookup"><span data-stu-id="bbcd5-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="bbcd5-172">Запускает новый timer.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-172">Starts a new timer.</span></span>  <span data-ttu-id="bbcd5-173">Используйте метод [TimeEnd,](#timeend) чтобы остановить время и распечатать время, заданное консоли.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Пример console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="bbcd5-175">Рис. 11. Результат `console.time()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="bbcd5-176">TimeEnd</span><span class="sxs-lookup"><span data-stu-id="bbcd5-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="bbcd5-177">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-178">Останавливает отмерить время.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-178">Stops a timer.</span></span>  <span data-ttu-id="bbcd5-179">Перейдите к [методу времени.](#time)</span><span class="sxs-lookup"><span data-stu-id="bbcd5-179">Navigate to the [time](#time) method.</span></span>  

---  

## <a name="trace"></a><span data-ttu-id="bbcd5-180">трассировка</span><span class="sxs-lookup"><span data-stu-id="bbcd5-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="bbcd5-181">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="bbcd5-182">Печать трассировки стека на консоль.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Результат примера console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="bbcd5-184">Рис. 12. Результат `console.trace()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <a name="warn"></a><span data-ttu-id="bbcd5-185">предупреждение</span><span class="sxs-lookup"><span data-stu-id="bbcd5-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="bbcd5-186">[Уровень журнала:][DevtoolsConsoleReferencePersist]</span><span class="sxs-lookup"><span data-stu-id="bbcd5-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="bbcd5-187">Напечатает предупреждение консоли.</span><span class="sxs-lookup"><span data-stu-id="bbcd5-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Результат примера console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="bbcd5-189">Рис. 13. Результат `console.warn()` примера</span><span class="sxs-lookup"><span data-stu-id="bbcd5-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bbcd5-190">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bbcd5-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с ведением журнала сообщений в консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Ссылка на API API консоли utilities"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Очистить консоль - консоль ссылки"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Упорязать сообщения по загрузкам страниц - Консольная ссылка"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтр по уровню журнала — консольная ссылка"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium)"  

> [!NOTE]
> <span data-ttu-id="bbcd5-197">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bbcd5-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bbcd5-198">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/api) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="bbcd5-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bbcd5-200">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bbcd5-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
