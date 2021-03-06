---
description: Рекомендации по использованию API среды выполнения Windows
title: Рекомендации по использованию API среды выполнения Windows
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399346"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a>Рекомендации по использованию API среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

В JavaScript можно использовать практически каждый элемент API времени запуска Windows.  Однако есть некоторые аспекты представления JavaScript элементов windows Runtime, которые следует иметь в виду.  

> [!IMPORTANT]
> Сведения о создании компонентов windows Runtime в C++, C# или Visual Basic и их потреблении в JavaScript см. в руб. Создание компонентов времени запуска Windows в [C++][WindowsUwpComponentsCreatingCpp] и Создание компонентов времени запуска Windows в [C# и Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a>Особые случаи в представлении JavaScript типов windows runtime  

:::row:::
   :::column span="1":::
      Strings  
   :::column-end:::
   :::column span="3":::
      Неинициальная строка передается методу windows Runtime в качестве строки "undefined", а строка, задаваемая в качестве строки `null` "null".  \(Это верно, когда значение или значение принудилось к строке.\) Перед тем, как передать строку методу запуска Windows, следует инициализировать ее как пустую строку `null` `undefined` \("\").  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Интерфейсы  
   :::column-end:::
   :::column span="3":::
      Невозможно реализовать интерфейс windows Runtime в JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Массивы  
   :::column-end:::
   :::column span="3":::
      Массивы времени запуска Windows не являются resizable, поэтому методы, которые меняют массивы в JavaScript, не работают на массивах времени запуска Windows.  
      *   Массивы. Если передать значение массива JavaScript методу запуска Windows, массив копируется.  Метод windows Runtime не может изменять массив или его членов и возвращать его в приложение JavaScript.  Однако можно использовать типированные массивы \(например, [Объект Int32Array\),][MDNInt32array]которые не копируется.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Структуры  
   :::column-end:::
   :::column span="3":::
      Структуры времени запуска Windows — это объекты в JavaScript.  Если вы хотите передать структуру времени запуска Windows методу windows runtime, не моментально перенастройте структуру с помощью ключевого `new` слова.  Вместо этого создайте объект и добавьте соответствующие участники и их значения.  Имена участников должны быть в случае верблюда: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Объекты  
   :::column-end:::
   :::column span="3":::
      Объекты JavaScript не то же самое, что управляемые объекты кода `System.Object` \( \).  Вы не можете передать объект JavaScript методу windows Runtime, который требует `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Идентификатор объекта  
   :::column-end:::
   :::column span="3":::
      В большинстве случаев объекты, переданные между временем запуска Windows и JavaScript, не изменяются.  В движке JavaScript поддерживается карта известных объектов.  Когда объект возвращается из времени запуска Windows, он совпадает с картой, и если он не существует, создается новый объект.  Такая же процедура для объектов, которые представляют интерфейсы, возвращаемые методами windows Runtime.  Существует два вида исключений:  
      
      *   Объекты, возвращаемые после вызова во время запуска Windows, а затем добавлены новые свойства \(expando\) не сохраняют свои новые свойства при их возвращении в время запуска Windows.  Однако, когда они возвращаются в приложение JavaScript, так как они соответствуют существующему объекту, возвращенный объект имеет свойства expando.  
      *   Структуры и делегаты в Windows Runtime не могут быть идентифицированы как идентичные ранее используемым структурам или делегатам.  Каждый раз, когда структура или делегат возвращается, она получает новую ссылку.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Столкновения имен  
   :::column-end:::
   :::column span="3":::
      В нескольких интерфейсах windows Runtime могут быть члены с одинаковыми именами.  Если они объединены в один объект JavaScript (который может быть представлением класса запуска или интерфейса), участники представлены с полностью квалифицированными именами.  Вы можете вызвать этих членов, используя следующий синтаксис:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      В следующем коде два интерфейса имеют метод Draw, а класс выполнения реализует оба интерфейса.  
      
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
      
      Вот как можно вызвать вышеуказанный код в JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` параметры  
   :::column-end:::
   :::column span="3":::
      Если метод запуска Windows имеет несколько параметров, в JavaScript метод имеет объект JavaScript в качестве возвращаемого значения, а объект имеет свойства, соответствующие `out` `out` параметру.  Например, рассмотрим следующую подпись времени запуска Windows в C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      Версия JavaScript этой подписи:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      В этом `returnValue` примере объект JavaScript имеет два поля: `first` и `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Статические участники  
   :::column-end:::
   :::column span="3":::
      Время запуска Windows определяет как статических участников, так и экземпляров.  В JavaScript к объекту, связанному с классом или интерфейсом Windows Runtime, добавляются статические участники.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Дополнительные сведения о представлении JavaScript базовых типов запуска Windows см. в [javaScript Representation of Windows Runtime Types.][WindowsRuntimeJavascriptTypes]  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов запуска Windows | Документы Майкрософт"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты windows runtime с C++/CX | Документы Майкрософт"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты windows runtime с C# и Visual Basic | Документы Майкрософт"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
