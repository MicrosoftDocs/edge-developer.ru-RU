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

# <a name="console-api-reference"></a>Ссылка на API консоли  

Используйте методы API консоли для записи сообщений на консоль из JavaScript.  Для интерактивного знакомства с этой темой перейдите к разделу Начало работы с ведением журнала [сообщений на консоли.][DevtoolsConsoleLog]  Для таких удобных методов, как или доступных только из области консоли, перейдите к ссылке `debug()` `monitorEvents()` [API API консоли utilities.][DevtoolConsoleUtilities] ****  

---  

## <a name="assert"></a>утверждения  

```javascript
console.assert(expression, object)
```

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Записывает [ошибку](#error) на консоль при `expression` оценке `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Результат примера console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   Рис. 1. Результат `console.assert()` примера  
:::image-end:::  

---  

## <a name="clear"></a>clear  

```javascript
console.clear()
```

Очищает консоль.  

```javascript
console.clear();  
```  

Если [включен журнал сохранения,][DevtoolsConsoleReferenceLevel] [четкий](#clear) метод отключен.  

### <a name="see-also"></a>См. также  

*   [Очистка консоли][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>количество  

```javascript
console.count([label])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Записывает количество раз, когда метод [подсчета](#count) вызывался в одной строке и с той же `label` строкой .  Чтобы сбросить количество, используйте метод [countReset.](#countreset)  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Результат примера console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   Рис. 2. Результат `console.count()` примера  
:::image-end:::  

---  

## <a name="countreset"></a>countReset  

```javascript
console.countReset([label])
```  

Сбрасывает количество.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a>отладка  

```javascript
console.debug(object [, object, ...])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Verbose`

Идентично [журналу,](#log) за исключением разного уровня журнала.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Результат примера console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   Рис. 3. Результат `console.debug()` примера  
:::image-end:::  

---  

## <a name="dir"></a>dir  

```javascript
console.dir(object)
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Печать представления JSON указанного объекта.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Пример console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   Рис. 4. Результат `console.dir()` примера  
:::image-end:::  

---  

## <a name="dirxml"></a>dirxml  

```javascript
console.dirxml(node)
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Печать XML-представления потомков `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Результат примера console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Рис. 5. Результат `console.dirxml()` примера  
:::image-end:::  

---  

## <a name="error"></a>ошибка  

```javascript
console.error(object [, object, ...])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Error`  

Принты `object` на консоль, форматирование ее как ошибку, и включает трассировку стека.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Пример console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   Рис. 6. Результат `console.error()` примера  
:::image-end:::  

---  

## <a name="group"></a>группа  

```javascript
console.group(label)
```  

Визуально группит сообщения вместе до тех пор, пока не будет использован метод [groupEnd.](#groupend)  Используйте метод [groupCollapsed,](#groupcollapsed) чтобы обвалить группу при первоначальном входе в консоль.  

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
   Рис. 7. Результат `console.group()` примера  
:::image-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

То же, [что](#log) и метод журнала, за исключением того, что группа сначала разрушается при входе в консоль.  

---  

## <a name="groupend"></a>groupEnd  

```javascript
console.groupEnd(label)
```  

Остановка визуальной группировки сообщений.  Перейдите к [групповому методу.](#group)  

---  

## <a name="info"></a>"Сведения"  

```javascript
console.info(object [, object, ...])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Идентично [методу журнала.](#log)  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Результат примера console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   Рис. 8. Результат `console.info()` примера  
:::image-end:::  

---  

## <a name="log"></a>журнал  

```javascript
console.log(object [, object, ...])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Печать сообщения на консоли.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Пример console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   Рис. 9. Результат `console.log()` примера  
:::image-end:::  

---  

## <a name="table"></a>таблица  

```javascript
console.table(array)
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Регистрит массив объектов в качестве таблицы.  

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
   Рис. 10. Результат `console.table()` примера  
:::image-end:::  

---  

## <a name="time"></a>time  

```javascript
console.time([label])
```  

Запускает новый timer.  Используйте метод [TimeEnd,](#timeend) чтобы остановить время и распечатать время, заданное консоли.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Пример console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   Рис. 11. Результат `console.time()` примера  
:::image-end:::  

---  

## <a name="timeend"></a>TimeEnd  

```javascript
console.timeEnd([label])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Останавливает отмерить время.  Перейдите к [методу времени.](#time)  

---  

## <a name="trace"></a>трассировка  

```javascript
console.trace()
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Info`  

Печать трассировки стека на консоль.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Результат примера console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   Рис. 12. Результат `console.trace()` примера  
:::image-end:::  

---  

## <a name="warn"></a>предупреждение  

```javascript
console.warn(object [, object, ...])
```  

[Уровень журнала:][DevtoolsConsoleReferencePersist] `Warning`  

Напечатает предупреждение консоли.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Результат примера console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   Рис. 13. Результат `console.warn()` примера  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с ведением журнала сообщений в консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Ссылка на API API консоли utilities"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Очистить консоль - консоль ссылки"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Упорязать сообщения по загрузкам страниц - Консольная ссылка"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтр по уровню журнала — консольная ссылка"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium)"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/api) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
