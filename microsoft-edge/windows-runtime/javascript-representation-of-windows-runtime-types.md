---
title: Представление типов среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows Runtime types [JavaScript]
- JavaScript, Windows Runtime types
ms.assetid: f4851802-8b40-4afa-ba6c-8a162a9a43cc
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b76c28d3448b8be6fbef1fd7e23b07b2eff8d087
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572856"
---
# Представление типов среды выполнения Windows в JavaScript  

В следующей таблице описано, как JavaScript представляет типы среды выполнения Windows.  

> [!IMPORTANT]
> Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## Типы среды выполнения Windows в JavaScript  

| Тип среды выполнения Windows | Представление JavaScript | Описание |  
|:--- |:--- |:--- |  
| `UInt8` | `Number` | Среда выполнения Windows `Uint8` — это 8-разрядное целое число без знака, представленное в виде номера JavaScript.  Значение JavaScript сначала преобразуется в номер JavaScript, после чего `ToUint32` выполняется процесс.  Если значение номера JavaScript выходит за пределы диапазона Uint8, результат будет применен к модулю 2 ^ 8. |  
| `Int32` | `Number` | Среда выполнения Windows `Int32` — это 32-разрядное целое число со знаком, представленное в виде номера JavaScript.  Значение JavaScript сначала преобразуется в номер JavaScript, после чего `ToInt32` выполняется процесс.  Если значение номера JavaScript выходит за пределы диапазона a `Int32` , результат будет применен к модулю 2 ^ 16. |  
| `Int64` | `Number` | Среда выполнения Windows `Int64` — это 64-разрядное целое число со знаком, представленное в виде стандартного числа, если оно попадает в диапазон \ [-2 ^ 53, 2 ^ 53 \].  Если он находится за пределами этого диапазона, он представлен в виде числового значения с настраиваемым резервным хранилищем, которое поддерживает полные биты 64 целочисленных данных.  Все математические операции на этих настраиваемых числовых значениях Int64 приводят к преобразованию значения в Стандартный номер в диапазоне \ [-2 ^ 53, 2 ^ 53].  Если значение находится за пределами этого диапазона, возникает ошибка типа.  Исключениями из этого процесса преобразования являются: `==` , `===` , `SameValue` и, и `RelationalComparison` операции, которые сравнивают аргументы, основанные на полном 64 битах при передаче двух представленных 64-битовых значений.  Если какой-либо из аргументов является стандартным номером JavaScript, эти операции также преобразуются в номер JavaScript перед сравнением.  Значение JavaScript напрямую присваивается, если оно имеет значение Int64. в противном случае результат применения `ToInteger` преобразования значения передается в среду выполнения Windows.  Если приведение типов завершается сбоем, возвращается исключение. |  
| `Uint64` | `Number` | Среда выполнения Windows `Uint64` — это неподписанное 64-разрядное целое число, представленное в виде стандартного числа, если оно попадает в диапазон \ [0, 2 ^ 53 \].  Если он находится за пределами этого диапазона, он представлен в виде числа с настраиваемым резервным хранилищем, поддерживающим полные биты 64 целочисленных данных без знака.  Все математические операции с этими пользовательскими значениями UInt64 приводят к преобразованию значения в Стандартный номер в диапазоне \ [0, 2 ^ 53 \].  Если значение находится за пределами этого диапазона, возникает ошибка типа.  Исключениями из этого процесса преобразования являются: `==` , `===` , `SameValue` и, и `RelationalComparison` операции, которые сравнивают аргументы, основанные на полном 64 битах при передаче 2 64-разрядных значений.  Если какой-либо из аргументов является стандартным номером JavaScript, эти операции также преобразуются в номер JavaScript перед сравнением.  Значение JavaScript напрямую присваивается, если оно является значением UInt64. в противном случае `ToInteger` в среду выполнения Windows передается результат преобразования значения, а затем — по модулю 2 ^ 52.  Если преобразование типа завершается сбоем, возвращается исключение. |  
| `Single` | `Number` | Среда выполнения Windows `Single` — это число с плавающей точкой 32, представленное в виде номера JavaScript, выбирая ближайшее значение двойной точности для значения одинарной точности.  Значение JavaScript преобразуется в номер JavaScript, а затем проверяется, чтобы гарантировать, что значение может быть представлено в число с плавающей запятой с обычной точностью 32 – бит IEEE 754.  Если при преобразовании или проверке диапазонов происходит сбой, возвращается ошибка маршалинга. |  
| `Double` | `Number` | Среда выполнения Windows `Double` является 64-битным числом с плавающей запятой.  `ToNumber` используется для преобразования среды выполнения Windows `Double` в номер JavaScript.  Если преобразование завершается сбоем, возвращается ошибка маршалинга. |  
| `Boolean` | `Boolean` | Среда выполнения Windows `Boolean` — это 8-разрядное значение, в котором ноль `false` и любое значение, отличное от нуля `true` , представлены в виде JavaScript `Boolean` .  Значение JavaScript сначала преобразуется в код JavaScript `Boolean` `ToBoolean` .  Это означает, что функция среды выполнения Windows, объявленная как `void func(BOOL);` может быть написана на JavaScript как `obj.func("test");` .  Функция среды выполнения Windows вызывается с `BOOL` параметром, передаваемым как `TRUE` .  Если преобразование завершается сбоем, возвращается ошибка маршалинга. |  
| `Char16` | `String` | Среда выполнения Windows `Char16` — это 16-разрядный знак Юникода, представленный в виде строки JavaScript, содержащей один символ.  Значение JavaScript преобразуется в строку JavaScript, `ToString` а затем проверяется на предмет того, что строка состоит только из одного знака.  Один символ затем передается как `Char16` значение.  Если проверка преобразования или длины завершается сбоем, возвращается ошибка маршалинга. |  
| `String` | `String` | Среда выполнения Windows `String` является постоянной последовательностью `Char16` объектов.  Строки представлены как объекты JavaScript `String` .  Строки среды выполнения Windows не имеют различных значений `null` и пустых строк \ ("" \ ").  `null` и пустые строковые значения преобразуются в пустую строку JavaScript.  Примечание. при `null` передаче JavaScript в параметр среды выполнения Windows, который ожидает строку, она возвращает строковое значение null, а не `null` пустую строку \ ("" \ ").  Строки, передаваемые в среду выполнения Windows, всегда должны быть созданы для пустой строки. |  
| `Enumeration` | `Object` | Среда выполнения Windows `Enumeration` — это 32-разрядное целое число \ (со знаком или без знака) с соответствующим набором именованных констант.  В JavaScript перечисление представлено как объект, который содержит поле, предназначенное только для чтения, для каждого именованного значения.  Значения перечисления преобразуются в номера JavaScript, определенные ранее для `Int32` и `UInt32` .  При преобразовании значения JavaScript в перечисление среды выполнения Windows оно преобразуется, усекается и проверяются, как описано выше.  Однако полученное значение не проверяется на соответствие определенным именованным значениям, указанным в перечислении. |  
| `Structure` | `Object` | Среда выполнения Windows `Structure` — это разнородный набор именованных полей данных.  В JavaScript структура представлена как объект JavaScript, который содержит именованное свойство для каждого поля в структуре.  Если при преобразовании любого значения структуры происходит сбой, возвращается ошибка маршалинга.  Поля в объекте JavaScript, не имеющие эквивалентов в структуре среды выполнения Windows, игнорируются.  Примечание. структуру среды выполнения Windows нельзя создать в JavaScript с помощью `new` ключевого слова. |  
| `Array` | `Array` | Среда выполнения Windows `Array` преобразуется в массив JavaScript.  Однако массивы среды выполнения Windows не могут изменяться в размерах, поэтому некоторые операции с массивами JavaScript невозможны.  Для внутреннего `[[Class]]` Свойства преобразованного массива не задано значение "массив", поскольку оно не разрешено спецификацией ECMAScript 5.  Это означает, что `Array.isArray(v)` возвращает `false` .  Значение JavaScript преобразуется в массив среды выполнения Windows, как описано ниже. Если задано значение `null` или `undefined` оно преобразовано в native `null` .  Если внутреннее `[[Class]]` свойство имеет значение "массив", оно копируется в собственный массив, и передается ссылка на этот массив.  Если это преобразованный массив, как описано выше, передается базовый массив Native.  Примечание. Передача значения массива JavaScript методу среды выполнения Windows приводит к созданию полной копии массива. |  
| Delegate \ (обратный вызов функции) | `Function` | Делегат среды выполнения Windows — это ссылка на один метод.  Делегат среды выполнения Windows представлен в JavaScript как сценарий JavaScript `Function` , который гарантированно вызывается в нужном потоке.  При `Function` вызове метода аргументы преобразуются в эквивалентные типы параметров среды выполнения Windows.  Если количество аргументов JavaScript меньше, чем параметры делегата `in` , вызов делегата завершится сбоем.  Если в делегате больше аргументов JavaScript, чем есть `in` Параметры, дополнительные аргументы JavaScript игнорируются.  После вызова делегата `out` Параметры преобразуются в типы JavaScript и возвращаются.  Если собственный объект функции JavaScript преобразуется в делегат среды выполнения Windows, он переносится в делегат среды выполнения Windows соответствующего типа.  При вызове делегата `in` Параметры преобразуются в типы JavaScript.  После вызова делегата возвращаемое значение преобразуется в `out` Параметры делегата. |  
| Интерфейс | `Object` | Интерфейсы и группы интерфейсов не представлены непосредственно в JavaScript как объекты.  Однако интерфейсы представлены как параметры и возвращаемые типы методов среды выполнения Windows.  Экземпляр интерфейса среды выполнения Windows преобразуется следующим образом:<br /> <br /> 1. Если у вас есть допустимый класс среды выполнения, предоставляющих объект в качестве экземпляра этого класса.<br /> 2. Если не существует допустимого класса среды выполнения, предоставляющих объект в качестве экземпляра неименованного класса среды выполнения, который реализует именно тот интерфейс, для реализации которого известен экземпляр, и необходимые интерфейсы.<br /> <br /> Значение JavaScript проверяется, чтобы определить, является ли этот экземпляр классом среды выполнения или интерфейсом.  Если это так, а исходное значение среды выполнения Windows реализует интерфейс, объект передается в среду выполнения Windows. |  
| Классы среды выполнения | `Object` | Объекты в среде выполнения Windows могут быть экземплярами классов среды выполнения, которые реализуют один или несколько интерфейсов.  Объекты среды выполнения Windows представлены в JavaScript как объекты.  Объединение методов, свойств и событий, определенных во всех реализованных интерфейсах класса, представляет именованные свойства в прототипе объекта JavaScript.  Пользователи JavaScript могут напрямую получить доступ к любому члену класса.  У объектов среды выполнения Windows есть прототип, который содержит все члены из всех реализованных интерфейсов класса среды выполнения. |  
  
## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  