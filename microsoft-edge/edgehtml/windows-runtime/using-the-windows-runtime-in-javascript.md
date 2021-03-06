---
description: Использование среды выполнения Windows в JavaScript
title: Использование среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4e137526ce147cdeb82749474bd43d1b3697361b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399325"
---
# <a name="using-the-windows-runtime-in-javascript"></a>Использование среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

При написании приложения Универсальной платформы Windows \(UWP\) можно использовать классы, методы и свойства Windows так же, как и родной объект, методы и свойства JavaScript.  В этом разделе представлены вводные сведения и ссылки на темы, которые объясняют основные понятия использования API времени запуска Windows в JavaScript, в том числе разъяснение того, как представлены типы запуска Windows, как использовать асинхронные методы запуска Windows, а также как прослушивать и обрабатывать события во время запуска Windows.  

Для общей языковой документации ознакомьтесь с справочной библиотекой [JavaScript][MDNJavascriptReference] MDN.  

> [!IMPORTANT]
> Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.  

## <a name="windows-runtime-reference-documentation"></a>Справочная документация по windows runtime  

Справочная документация см. [в справке о времени запуска Windows.][UwpApiIndex]  Примеры кода доступны в JavaScript, а также в C++, C# и Visual Basic.  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a>Написание компонентов времени запуска Windows в C++, C# или Visual Basic  

Инструкции и рекомендации по написанию компонентов windows runtime, которые можно использовать в JavaScript, см. в статьи Создание компонентов времени запуска Windows в [C++][WindowsUwpWinrtCpp] и Создание компонентов времени запуска Windows в C# и [Visual Basic][WindowsUwpWinrtCsharpVb].  

## <a name="casing-conventions-with-windows-runtime-features"></a>Конвенции casing с функциями windows Runtime  

Конвенции casing для функций windows Runtime в JavaScript немного отличаются от соглашений для других языков:  

*   Пространства имен и классы находятся в случае Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Члены классов, включая методы и свойства, а также члены структур и перемерий, находятся в случае верблюда:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Имена событий находятся в нижнем случае:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a>См. также  

[Рекомендации по использованию API среды выполнения Windows][WindowsRuntimeConsiderationsApi]  
[Использование асинхронных методов среды выполнения Windows][WindowsRuntimeAsynchronousMethods]   
[Обработка событий среды выполнения Windows в JavaScript][WindowsRuntimeEventsJavascript]   
[Представление типов среды выполнения Windows в JavaScript][WindowsRuntimeJavascriptTypes]   
[JavaScript Projection of Windows Runtime DateTime and TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Соображения при использовании API для windows runtime | Документы Майкрософт"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Обработка событий запуска Windows в JavaScript | Документы Майкрософт"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов запуска Windows | Документы Майкрософт"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Использование асинхронных методов запуска Windows | Документы Майкрософт"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Представления даты и времени работы Windows | Документы Майкрософт"  

[UwpApiIndex]: /uwp/api/index "Пространства имен Windows UWP | Документы Майкрософт"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты windows runtime с C++/CX | Документы Майкрософт"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты windows runtime с C# и Visual Basic | Документы Майкрософт"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Справочные | MDN"  
