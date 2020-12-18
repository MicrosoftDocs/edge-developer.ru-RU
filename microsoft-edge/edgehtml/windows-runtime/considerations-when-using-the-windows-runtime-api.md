---
description: Вопросы, которые следует учитывать при использовании API времени работы Windows.
title: Рекомендации по использованию API среды выполнения Windows
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 718a23646ec9a82c1d53a2669d7cdbf218647e41
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235482"
---
# Рекомендации по использованию API среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

В JavaScript можно использовать почти все элементы API времени работы Windows.  Однако есть некоторые аспекты представления элементов в среде runtime Windows на JavaScript, которые следует помнить.  

> [!IMPORTANT]
> Сведения о создании компонентов времени работы Windows на C++, C# или Visual Basic и их [][WindowsUwpComponentsCreatingCpp] потреблении в Java [Visual Basic Script][WindowsUwpComponentsCreatingCsharpVb]см. в под этой теме.  

## Особые случаи в представлении javaScript типов времени работы Windows  

:::row:::
   :::column span="1":::
      Строки  
   :::column-end:::
   :::column span="3":::
      Неинициализированная строка передается методу времени runtime Windows в качестве строки "undefined", а строка, задав для нее, передается в качестве строки `null` "null".  \(Это справедливо всякий раз, когда строка или значение приводится к строке.\) Перед тем как передать строку методу времени запуска Windows, необходимо инициализировать ее как пустую строку `null` `undefined` \(""\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Интерфейсы  
   :::column-end:::
   :::column span="3":::
      Невозможно реализовать интерфейс времени выполнения Windows в JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Массивы  
   :::column-end:::
   :::column span="3":::
      Массивы в среде разработки Windows не могут меняться, поэтому методы, которые меняют их в JavaScript, не работают в массивах времени запуска Windows.  
      *   Массивы: если передать значение массива JavaScript методу времени работы Windows, массив будет скопирован.  Методу времени работы Windows не удастся изменить массив или его члены и вернуть его в приложение JavaScript.  Однако можно использовать типированные массивы \(например, [Int32Array Object][MDNInt32array]\), которые не копируется.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Структуры  
   :::column-end:::
   :::column span="3":::
      Структуры времени работы Windows — это объекты в JavaScript.  Если вы хотите передать структуру времени работы Windows методу времени работы Windows, не выдайте ее с помощью ключевого `new` слова.  Вместо этого создайте объект и добавьте соответствующие члены и их значения.  Имена участников должны быть в "верблюжьем" примере: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Объекты  
   :::column-end:::
   :::column span="3":::
      Объекты JavaScript не такие, как объекты управляемого кода \( `System.Object` \).  Вы не можете передать объект JavaScript методу времени работы Windows, для который требуется `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Удостоверение объекта  
   :::column-end:::
   :::column span="3":::
      В большинстве случаев объекты, переданные между временем работы Windows и JavaScript, не изменяются.  Обдвижок JavaScript поддерживает карту известных объектов.  Когда объект возвращается из точки windows Runtime, он соразмерно карте, и если он не существует, создается новый объект.  Эта же процедура следует для объектов, которые представляют интерфейсы, возвращаемые методами времени работы Windows.  Существует два типа исключений:  
      
      *   Объекты, которые возвращаются при вызове в окну windows, а затем добавляют новые свойства \(expando\), не сохраняют свои новые свойства при их возвращении в окну windows Runtime.  Однако когда они возвращаются в приложение JavaScript, так как они совпадают с существующим объектом, возвращенный объект имеет свойства expando.  
      *   Структуры и делегаты в windows Runtime нельзя идентифицировать как идентичные ранее использованным структурам или делегатам.  При каждом возвращении структуры или делегата она получает новую ссылку.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Конфликты имен  
   :::column-end:::
   :::column span="3":::
      У нескольких интерфейсов времени работы Windows могут быть члены с одинаковыми именами.  Если они объединены в одном объекте JavaScript (который может быть представлением класса или интерфейса времени работы), члены будут представлены с помощью полного имени.  Вы можете вызвать эти члены, используя следующий синтаксис:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      В следующем коде два интерфейса имеют метод Draw, а класс времени выполнения реализует оба интерфейса.  
      
      ```cpp
      namespace CollisionExample {
          interface InterfaceA
          {
              HRESULT Draw([in] Int32 a);
          }
          interface InterfaceB
          {
              HRESULT Draw([in] HString a);
          }
          runtimeclass ExampleObject {
            interface InterfaceA
            interface InterfaceB
          }
      }
      ```  
      
      Вот как можно вызвать вышеперечисленный код в JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` parameters  
   :::column-end:::
   :::column span="3":::
      Если метод времени работы Windows имеет несколько параметров, в JavaScript метод имеет объект JavaScript в качестве возвращаемого значения, а объект имеет свойства, соответствующие `out` `out` параметру.  Например, рассмотрим следующую подпись времени работы Windows на C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      Версия этой подписи JavaScript:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      В этом примере `returnValue` это объект JavaScript, который имеет два поля: `first` и `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Статические члены  
   :::column-end:::
   :::column span="3":::
      В windows Runtime определяются как статические члены, так и члены экземпляра.  В JavaScript статические члены добавляются в объект, связанный с классом или интерфейсом времени работы Windows.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Дополнительные сведения о представлении JavaScript базовых типов в среде разработки Windows см. в представлении [javaScript типов времени windows.][WindowsRuntimeJavascriptTypes]  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление типов времени работы Windows на JavaScript | Документы Майкрософт"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты времени работы Windows с C++/CX | Документы Майкрософт"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты времени работы Windows с C# и Visual Basic | Документы Майкрософт"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
