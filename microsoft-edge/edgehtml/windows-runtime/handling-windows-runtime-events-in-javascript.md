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
# <a name="handling-windows-runtime-events-in-javascript"></a>Обработка событий среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

События во время запуска Windows не представлены в JavaScript так же, как в C++ или платформа .NET Framework.  Они не являются свойствами класса, а представляются как идентификаторы строки \(lowercase\) для класса и `addEventListener` `removeEventListener` методов.  Например, можно добавить обработчик событий для [события Geolocator.PositionChanged,][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] передав строку `positionchanged` `Geolocator.addEventListener` методу:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Вы также можете установить `locator.onpositionchanged` свойство:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Еще одним отличием между .NET/C++ и JavaScript является количество параметров, принятых обработитором событий.  В .NET/C++обработщику требуется два: отправитель событий и данные событий.  В JavaScript эти два объекта объединены в единый `Event` объект.  В следующем примере параметр содержит как отправитель события \(свойство\) так и свойства данных событий `ev` `target` \(здесь, просто `position` \).  Свойства данных событий — это свойства, которые задокументированы для каждого события.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.  

## <a name="see-also"></a>См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  
