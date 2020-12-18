---
description: Использование точки запуска Windows в JavaScript.
title: Использование среды выполнения Windows в JavaScript
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10c90a225816cf32e01bc33648571c13a1aae090
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235418"
---
# Использование среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

При написании приложения универсальной платформы Windows \(UWP\) можно использовать классы, методы и свойства в среде разработки Windows почти так же, как и для использования объектов, методов и свойств JavaScript.  В этом разделе представлены вводимые сведения и ссылки на разделы, в которых поясняются основные понятия использования API-api в среде разработки Windows в JavaScript, в том числе описание представления типов в среде runtime Windows, использование асинхронных методов времени работы Windows, а также прослушивание событий и обработка событий в среде запуска Windows.  

Для общей языковой документации ознакомьтесь со справочной библиотекой [JavaScript][MDNJavascriptReference] MDN.  

> [!IMPORTANT]
> Функции времени работы Windows недоступны для приложений, которые работают в Internet Explorer.  

## Справочная документация по времени работы Windows  

Справочную документацию см. в [справочнике по времени работы Windows.][UwpApiIndex]  Примеры кода доступны в JavaScript, а также на C++, C# и Visual Basic.  

## Написание компонентов времени работы Windows на C++, C# или Visual Basic  

Инструкции и рекомендации по написанию компонентов времени разработки Windows, которые можно использовать в JavaScript, см. в руководстве по созданию компонентов времени разработки Windows на [C++][WindowsUwpWinrtCpp] и созданию компонентов времени разработки Windows на [C# и Visual Basic.][WindowsUwpWinrtCsharpVb]  

## Соглашения casing с функциями времени работы Windows  

Соглашения о casing для функций времени работы Windows в JavaScript немного отличаются от соглашений для других языков:  

*   Пространства имен и классы находятся в случае Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Члены классов, включая методы и свойства, а также члены структур и нумерации, находятся в "верблюжих" случаях:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Имена событий находятся в нижнем случае:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## См. также  

[Рекомендации по использованию API среды выполнения Windows][WindowsRuntimeConsiderationsApi]  
[Использование асинхронных методов среды выполнения Windows][WindowsRuntimeAsynchronousMethods]   
[Обработка событий среды выполнения Windows в JavaScript][WindowsRuntimeEventsJavascript]   
[Представление типов среды выполнения Windows в JavaScript][WindowsRuntimeJavascriptTypes]   
[JavaScript Projection of Windows Runtime DateTime and TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Вопросы, которые следует учитывать при использовании API времени работы Windows | Документы Майкрософт"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Обработка событий в среде запуска Windows в JavaScript | Документы Майкрософт"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление типов времени работы Windows на JavaScript | Документы Майкрософт"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Использование асинхронных методов в времени работы Windows | Документы Майкрософт"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Представления даты и времени в времени и времени в времени windows | Документы Майкрософт"  

[UwpApiIndex]: /uwp/api/index "Пространства имен UWP в Windows | Документы Майкрософт"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты времени работы Windows с C++/CX | Документы Майкрософт"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты времени работы Windows с C# и Visual Basic | Документы Майкрософт"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Справка по JavaScript | MDN"  
