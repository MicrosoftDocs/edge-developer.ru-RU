---
description: Обработка событий в среде запуска Windows в JavaScript.
title: Обработка событий среды выполнения Windows в JavaScript
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e0a3e35c908c766c0308903381b271f5ccdb27a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235668"
---
# <span data-ttu-id="4651c-103">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="4651c-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="4651c-104">События в среде разработки Windows не представлены в JavaScript так же, как на C++ или .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4651c-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="4651c-105">Они не являются свойствами класса, а представлены в качестве идентификаторов строки \(lowercase\), которые передаются в методы `addEventListener` и `removeEventListener` класс.</span><span class="sxs-lookup"><span data-stu-id="4651c-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="4651c-106">Например, можно добавить обработчик событий для события [Geolocator.PositionChanged,][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] передав строку `positionchanged` `Geolocator.addEventListener` методу:</span><span class="sxs-lookup"><span data-stu-id="4651c-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="4651c-107">Вы также можете настроить `locator.onpositionchanged` свойство:</span><span class="sxs-lookup"><span data-stu-id="4651c-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="4651c-108">Еще одно различие между .NET/C++ и JavaScript — количество параметров, принятых обработом событий.</span><span class="sxs-lookup"><span data-stu-id="4651c-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="4651c-109">В .NET/C++ обработщик принимает два: отправитель события и данные события.</span><span class="sxs-lookup"><span data-stu-id="4651c-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="4651c-110">В JavaScript эти два объекта объединены в один `Event` объект.</span><span class="sxs-lookup"><span data-stu-id="4651c-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="4651c-111">В следующем примере параметр содержит отправитель события \(свойство\) и свойства данных события `ev` `target` \(здесь, просто `position` \).</span><span class="sxs-lookup"><span data-stu-id="4651c-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="4651c-112">Свойства данных события задокументированы для каждого события.</span><span class="sxs-lookup"><span data-stu-id="4651c-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="4651c-113">Функции времени работы Windows недоступны для приложений, которые работают в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4651c-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="4651c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4651c-114">See also</span></span>  

[<span data-ttu-id="4651c-115">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="4651c-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  
