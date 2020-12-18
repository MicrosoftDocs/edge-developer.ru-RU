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
# <span data-ttu-id="9da63-103">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="9da63-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="9da63-104">При написании приложения универсальной платформы Windows \(UWP\) можно использовать классы, методы и свойства в среде разработки Windows почти так же, как и для использования объектов, методов и свойств JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9da63-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="9da63-105">В этом разделе представлены вводимые сведения и ссылки на разделы, в которых поясняются основные понятия использования API-api в среде разработки Windows в JavaScript, в том числе описание представления типов в среде runtime Windows, использование асинхронных методов времени работы Windows, а также прослушивание событий и обработка событий в среде запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="9da63-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="9da63-106">Для общей языковой документации ознакомьтесь со справочной библиотекой [JavaScript][MDNJavascriptReference] MDN.</span><span class="sxs-lookup"><span data-stu-id="9da63-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9da63-107">Функции времени работы Windows недоступны для приложений, которые работают в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9da63-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="9da63-108">Справочная документация по времени работы Windows</span><span class="sxs-lookup"><span data-stu-id="9da63-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="9da63-109">Справочную документацию см. в [справочнике по времени работы Windows.][UwpApiIndex]</span><span class="sxs-lookup"><span data-stu-id="9da63-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="9da63-110">Примеры кода доступны в JavaScript, а также на C++, C# и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9da63-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="9da63-111">Написание компонентов времени работы Windows на C++, C# или Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9da63-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="9da63-112">Инструкции и рекомендации по написанию компонентов времени разработки Windows, которые можно использовать в JavaScript, см. в руководстве по созданию компонентов времени разработки Windows на [C++][WindowsUwpWinrtCpp] и созданию компонентов времени разработки Windows на [C# и Visual Basic.][WindowsUwpWinrtCsharpVb]</span><span class="sxs-lookup"><span data-stu-id="9da63-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="9da63-113">Соглашения casing с функциями времени работы Windows</span><span class="sxs-lookup"><span data-stu-id="9da63-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="9da63-114">Соглашения о casing для функций времени работы Windows в JavaScript немного отличаются от соглашений для других языков:</span><span class="sxs-lookup"><span data-stu-id="9da63-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="9da63-115">Пространства имен и классы находятся в случае Pascal:</span><span class="sxs-lookup"><span data-stu-id="9da63-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="9da63-116">Члены классов, включая методы и свойства, а также члены структур и нумерации, находятся в "верблюжих" случаях:</span><span class="sxs-lookup"><span data-stu-id="9da63-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="9da63-117">Имена событий находятся в нижнем случае:</span><span class="sxs-lookup"><span data-stu-id="9da63-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="9da63-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9da63-118">See also</span></span>  

[<span data-ttu-id="9da63-119">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="9da63-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="9da63-120">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="9da63-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="9da63-121">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="9da63-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="9da63-122">Представление типов среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="9da63-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="9da63-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9da63-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
