---
title: Обработка событий среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3db0116a3d464c75fe754e73e41ff1d154f928e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572857"
---
# <span data-ttu-id="0b9ad-102">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="0b9ad-102">Handling Windows Runtime Events in JavaScript</span></span>  

<span data-ttu-id="0b9ad-103">События среды выполнения Windows не представляются таким же образом в JavaScript, как в C++ или .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-103">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="0b9ad-104">Они не являются свойствами класса, а представляют собой строковые идентификаторы (строчные), которые передаются в `addEventListener` методы и классы `removeEventListener` .</span><span class="sxs-lookup"><span data-stu-id="0b9ad-104">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="0b9ad-105">Например, вы можете добавить обработчик событий для события [геоPositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] , передав методу строку "PositionChanged" `Geolocator.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="0b9ad-105">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string "positionchanged" to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="0b9ad-106">Вы также можете задать `locator.onpositionchanged` свойство:</span><span class="sxs-lookup"><span data-stu-id="0b9ad-106">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="0b9ad-107">Еще одна разница между .NET и C++ и JavaScript — количеством параметров, полученных обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-107">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="0b9ad-108">В .NET/C++ обработчик принимает два: отправитель события и данные о событии.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-108">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="0b9ad-109">В JavaScript эти два объекта объединены в один `Event` объект.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-109">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="0b9ad-110">В приведенном ниже примере `ev` параметр имеет и отправителя события \ ( `target` свойство \), и свойства Data Events \ (здесь, просто `position` \).</span><span class="sxs-lookup"><span data-stu-id="0b9ad-110">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="0b9ad-111">Свойства данных события — это те, которые задокументированы для каждого события.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-111">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender:  " + ev.target);
    console.log("Position:  " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="0b9ad-112">Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0b9ad-112">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="0b9ad-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0b9ad-113">See Also</span></span>  

[<span data-ttu-id="0b9ad-114">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="0b9ad-114">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- image links -->  

 <!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс геоуказателей"  
