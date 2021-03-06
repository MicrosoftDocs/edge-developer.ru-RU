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
# <a name="using-the-windows-runtime-in-javascript"></a><span data-ttu-id="47f7e-103">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="47f7e-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="47f7e-104">При написании приложения Универсальной платформы Windows \(UWP\) можно использовать классы, методы и свойства Windows так же, как и родной объект, методы и свойства JavaScript.</span><span class="sxs-lookup"><span data-stu-id="47f7e-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="47f7e-105">В этом разделе представлены вводные сведения и ссылки на темы, которые объясняют основные понятия использования API времени запуска Windows в JavaScript, в том числе разъяснение того, как представлены типы запуска Windows, как использовать асинхронные методы запуска Windows, а также как прослушивать и обрабатывать события во время запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="47f7e-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="47f7e-106">Для общей языковой документации ознакомьтесь с справочной библиотекой [JavaScript][MDNJavascriptReference] MDN.</span><span class="sxs-lookup"><span data-stu-id="47f7e-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="47f7e-107">Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="47f7e-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="windows-runtime-reference-documentation"></a><span data-ttu-id="47f7e-108">Справочная документация по windows runtime</span><span class="sxs-lookup"><span data-stu-id="47f7e-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="47f7e-109">Справочная документация см. [в справке о времени запуска Windows.][UwpApiIndex]</span><span class="sxs-lookup"><span data-stu-id="47f7e-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="47f7e-110">Примеры кода доступны в JavaScript, а также в C++, C# и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="47f7e-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a><span data-ttu-id="47f7e-111">Написание компонентов времени запуска Windows в C++, C# или Visual Basic</span><span class="sxs-lookup"><span data-stu-id="47f7e-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="47f7e-112">Инструкции и рекомендации по написанию компонентов windows runtime, которые можно использовать в JavaScript, см. в статьи Создание компонентов времени запуска Windows в [C++][WindowsUwpWinrtCpp] и Создание компонентов времени запуска Windows в C# и [Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="47f7e-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <a name="casing-conventions-with-windows-runtime-features"></a><span data-ttu-id="47f7e-113">Конвенции casing с функциями windows Runtime</span><span class="sxs-lookup"><span data-stu-id="47f7e-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="47f7e-114">Конвенции casing для функций windows Runtime в JavaScript немного отличаются от соглашений для других языков:</span><span class="sxs-lookup"><span data-stu-id="47f7e-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="47f7e-115">Пространства имен и классы находятся в случае Pascal:</span><span class="sxs-lookup"><span data-stu-id="47f7e-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="47f7e-116">Члены классов, включая методы и свойства, а также члены структур и перемерий, находятся в случае верблюда:</span><span class="sxs-lookup"><span data-stu-id="47f7e-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="47f7e-117">Имена событий находятся в нижнем случае:</span><span class="sxs-lookup"><span data-stu-id="47f7e-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a><span data-ttu-id="47f7e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="47f7e-118">See also</span></span>  

[<span data-ttu-id="47f7e-119">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="47f7e-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="47f7e-120">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="47f7e-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="47f7e-121">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="47f7e-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="47f7e-122">Представление типов среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="47f7e-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="47f7e-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span><span class="sxs-lookup"><span data-stu-id="47f7e-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
