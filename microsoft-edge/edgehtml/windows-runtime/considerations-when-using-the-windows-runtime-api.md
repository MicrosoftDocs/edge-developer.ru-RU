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
# <a name="considerations-when-using-the-windows-runtime-api"></a><span data-ttu-id="407cf-103">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="407cf-103">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="407cf-104">В JavaScript можно использовать практически каждый элемент API времени запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="407cf-104">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="407cf-105">Однако есть некоторые аспекты представления JavaScript элементов windows Runtime, которые следует иметь в виду.</span><span class="sxs-lookup"><span data-stu-id="407cf-105">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="407cf-106">Сведения о создании компонентов windows Runtime в C++, C# или Visual Basic и их потреблении в JavaScript см. в руб. Создание компонентов времени запуска Windows в [C++][WindowsUwpComponentsCreatingCpp] и Создание компонентов времени запуска Windows в [C# и Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="407cf-106">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a><span data-ttu-id="407cf-107">Особые случаи в представлении JavaScript типов windows runtime</span><span class="sxs-lookup"><span data-stu-id="407cf-107">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-108">Strings</span><span class="sxs-lookup"><span data-stu-id="407cf-108">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-109">Неинициальная строка передается методу windows Runtime в качестве строки "undefined", а строка, задаваемая в качестве строки `null` "null".</span><span class="sxs-lookup"><span data-stu-id="407cf-109">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="407cf-110">\(Это верно, когда значение или значение принудилось к строке.\) Перед тем, как передать строку методу запуска Windows, следует инициализировать ее как пустую строку `null` `undefined` \("\").</span><span class="sxs-lookup"><span data-stu-id="407cf-110">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-111">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="407cf-111">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-112">Невозможно реализовать интерфейс windows Runtime в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="407cf-112">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-113">Массивы</span><span class="sxs-lookup"><span data-stu-id="407cf-113">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-114">Массивы времени запуска Windows не являются resizable, поэтому методы, которые меняют массивы в JavaScript, не работают на массивах времени запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="407cf-114">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="407cf-115">Массивы. Если передать значение массива JavaScript методу запуска Windows, массив копируется.</span><span class="sxs-lookup"><span data-stu-id="407cf-115">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="407cf-116">Метод windows Runtime не может изменять массив или его членов и возвращать его в приложение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="407cf-116">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="407cf-117">Однако можно использовать типированные массивы \(например, [Объект Int32Array\),][MDNInt32array]которые не копируется.</span><span class="sxs-lookup"><span data-stu-id="407cf-117">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-118">Структуры</span><span class="sxs-lookup"><span data-stu-id="407cf-118">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-119">Структуры времени запуска Windows — это объекты в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="407cf-119">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="407cf-120">Если вы хотите передать структуру времени запуска Windows методу windows runtime, не моментально перенастройте структуру с помощью ключевого `new` слова.</span><span class="sxs-lookup"><span data-stu-id="407cf-120">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="407cf-121">Вместо этого создайте объект и добавьте соответствующие участники и их значения.</span><span class="sxs-lookup"><span data-stu-id="407cf-121">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="407cf-122">Имена участников должны быть в случае верблюда: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="407cf-122">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-123">Объекты</span><span class="sxs-lookup"><span data-stu-id="407cf-123">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-124">Объекты JavaScript не то же самое, что управляемые объекты кода `System.Object` \( \).</span><span class="sxs-lookup"><span data-stu-id="407cf-124">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="407cf-125">Вы не можете передать объект JavaScript методу windows Runtime, который требует `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="407cf-125">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-126">Идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="407cf-126">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-127">В большинстве случаев объекты, переданные между временем запуска Windows и JavaScript, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="407cf-127">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="407cf-128">В движке JavaScript поддерживается карта известных объектов.</span><span class="sxs-lookup"><span data-stu-id="407cf-128">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="407cf-129">Когда объект возвращается из времени запуска Windows, он совпадает с картой, и если он не существует, создается новый объект.</span><span class="sxs-lookup"><span data-stu-id="407cf-129">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="407cf-130">Такая же процедура для объектов, которые представляют интерфейсы, возвращаемые методами windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="407cf-130">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="407cf-131">Существует два вида исключений:</span><span class="sxs-lookup"><span data-stu-id="407cf-131">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="407cf-132">Объекты, возвращаемые после вызова во время запуска Windows, а затем добавлены новые свойства \(expando\) не сохраняют свои новые свойства при их возвращении в время запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="407cf-132">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="407cf-133">Однако, когда они возвращаются в приложение JavaScript, так как они соответствуют существующему объекту, возвращенный объект имеет свойства expando.</span><span class="sxs-lookup"><span data-stu-id="407cf-133">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="407cf-134">Структуры и делегаты в Windows Runtime не могут быть идентифицированы как идентичные ранее используемым структурам или делегатам.</span><span class="sxs-lookup"><span data-stu-id="407cf-134">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="407cf-135">Каждый раз, когда структура или делегат возвращается, она получает новую ссылку.</span><span class="sxs-lookup"><span data-stu-id="407cf-135">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-136">Столкновения имен</span><span class="sxs-lookup"><span data-stu-id="407cf-136">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-137">В нескольких интерфейсах windows Runtime могут быть члены с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="407cf-137">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="407cf-138">Если они объединены в один объект JavaScript (который может быть представлением класса запуска или интерфейса), участники представлены с полностью квалифицированными именами.</span><span class="sxs-lookup"><span data-stu-id="407cf-138">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="407cf-139">Вы можете вызвать этих членов, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="407cf-139">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="407cf-140">В следующем коде два интерфейса имеют метод Draw, а класс выполнения реализует оба интерфейса.</span><span class="sxs-lookup"><span data-stu-id="407cf-140">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
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
      
      <span data-ttu-id="407cf-141">Вот как можно вызвать вышеуказанный код в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="407cf-141">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="407cf-142">параметры</span><span class="sxs-lookup"><span data-stu-id="407cf-142">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-143">Если метод запуска Windows имеет несколько параметров, в JavaScript метод имеет объект JavaScript в качестве возвращаемого значения, а объект имеет свойства, соответствующие `out` `out` параметру.</span><span class="sxs-lookup"><span data-stu-id="407cf-143">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="407cf-144">Например, рассмотрим следующую подпись времени запуска Windows в C++.</span><span class="sxs-lookup"><span data-stu-id="407cf-144">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="407cf-145">Версия JavaScript этой подписи:</span><span class="sxs-lookup"><span data-stu-id="407cf-145">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="407cf-146">В этом `returnValue` примере объект JavaScript имеет два поля: `first` и `second` .</span><span class="sxs-lookup"><span data-stu-id="407cf-146">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="407cf-147">Статические участники</span><span class="sxs-lookup"><span data-stu-id="407cf-147">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="407cf-148">Время запуска Windows определяет как статических участников, так и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="407cf-148">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="407cf-149">В JavaScript к объекту, связанному с классом или интерфейсом Windows Runtime, добавляются статические участники.</span><span class="sxs-lookup"><span data-stu-id="407cf-149">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="407cf-150">Дополнительные сведения о представлении JavaScript базовых типов запуска Windows см. в [javaScript Representation of Windows Runtime Types.][WindowsRuntimeJavascriptTypes]</span><span class="sxs-lookup"><span data-stu-id="407cf-150">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов запуска Windows | Документы Майкрософт"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты windows runtime с C++/CX | Документы Майкрософт"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты windows runtime с C# и Visual Basic | Документы Майкрософт"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
