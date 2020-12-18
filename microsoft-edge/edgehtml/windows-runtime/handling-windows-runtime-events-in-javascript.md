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
# Обработка событий среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

События в среде разработки Windows не представлены в JavaScript так же, как на C++ или .NET Framework.  Они не являются свойствами класса, а представлены в качестве идентификаторов строки \(lowercase\), которые передаются в методы `addEventListener` и `removeEventListener` класс.  Например, можно добавить обработчик событий для события [Geolocator.PositionChanged,][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] передав строку `positionchanged` `Geolocator.addEventListener` методу:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Вы также можете настроить `locator.onpositionchanged` свойство:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Еще одно различие между .NET/C++ и JavaScript — количество параметров, принятых обработом событий.  В .NET/C++ обработщик принимает два: отправитель события и данные события.  В JavaScript эти два объекта объединены в один `Event` объект.  В следующем примере параметр содержит отправитель события \(свойство\) и свойства данных события `ev` `target` \(здесь, просто `position` \).  Свойства данных события задокументированы для каждого события.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Функции времени работы Windows недоступны для приложений, которые работают в Internet Explorer.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  
