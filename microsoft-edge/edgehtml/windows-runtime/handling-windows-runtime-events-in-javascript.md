---
description: Обработка событий среды выполнения Windows в JavaScript
title: Обработка событий среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 08562f7ebff0c02b96bfc8229238a62463b95451
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397526"
---
# <a name="handling-windows-runtime-events-in-javascript"></a><span data-ttu-id="4d65d-103">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="4d65d-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="4d65d-104">События во время запуска Windows не представлены в JavaScript так же, как в C++ или платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4d65d-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="4d65d-105">Они не являются свойствами класса, а представляются как идентификаторы строки \(lowercase\) для класса и `addEventListener` `removeEventListener` методов.</span><span class="sxs-lookup"><span data-stu-id="4d65d-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="4d65d-106">Например, можно добавить обработчик событий для [события Geolocator.PositionChanged,][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] передав строку `positionchanged` `Geolocator.addEventListener` методу:</span><span class="sxs-lookup"><span data-stu-id="4d65d-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="4d65d-107">Вы также можете установить `locator.onpositionchanged` свойство:</span><span class="sxs-lookup"><span data-stu-id="4d65d-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="4d65d-108">Еще одним отличием между .NET/C++ и JavaScript является количество параметров, принятых обработитором событий.</span><span class="sxs-lookup"><span data-stu-id="4d65d-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="4d65d-109">В .NET/C++обработщику требуется два: отправитель событий и данные событий.</span><span class="sxs-lookup"><span data-stu-id="4d65d-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="4d65d-110">В JavaScript эти два объекта объединены в единый `Event` объект.</span><span class="sxs-lookup"><span data-stu-id="4d65d-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="4d65d-111">В следующем примере параметр содержит как отправитель события \(свойство\) так и свойства данных событий `ev` `target` \(здесь, просто `position` \).</span><span class="sxs-lookup"><span data-stu-id="4d65d-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="4d65d-112">Свойства данных событий — это свойства, которые задокументированы для каждого события.</span><span class="sxs-lookup"><span data-stu-id="4d65d-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="4d65d-113">Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4d65d-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d65d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4d65d-114">See also</span></span>  

[<span data-ttu-id="4d65d-115">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="4d65d-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  
