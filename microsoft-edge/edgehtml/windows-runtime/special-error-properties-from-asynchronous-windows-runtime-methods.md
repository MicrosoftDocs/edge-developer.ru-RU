---
description: Специальные свойства ошибок из асинхронных методов времени работы Windows.
title: Специальные свойства ошибок из асинхронных методов среды выполнения Windows.
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3557d0097d632f4058e46acbff748f7177d24ab1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235421"
---
# <span data-ttu-id="393ab-103">Специальные свойства ошибок из асинхронных методов среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="393ab-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="393ab-104">Отлажить асинхронные методы времени работы Windows в JavaScript может быть сложно, так как ошибка может возникнуть из глубины стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="393ab-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="393ab-105">У объекта JavaScript есть дополнительные свойства, которые отображаются только в том случае, если ошибка произошла из асинхронного метода windows Runtime, когда приложение работает в режиме `Error` отлаживания.</span><span class="sxs-lookup"><span data-stu-id="393ab-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="393ab-106">Свойства специальных ошибок</span><span class="sxs-lookup"><span data-stu-id="393ab-106">Special error properties</span></span>  

<span data-ttu-id="393ab-107">Объект ошибки, который является результатом неудачной асинхронной операции в режиме отлаживания, имеет следующие специальные свойства:</span><span class="sxs-lookup"><span data-stu-id="393ab-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="393ab-108">\(Object\) Получает сведения об исходном расположении, в котором был выполнен вызов, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="393ab-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="393ab-109">Свойство \(String\) отображает расположение в коде пользователя, искомом `asyncOpSource.originatingCall` асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="393ab-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="393ab-110">asyncOpType \(String\) Получает имя типа асинхронной операции, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="393ab-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="393ab-111">Дополнительные сведения об ошибках с асинхронными операциями см. в:</span><span class="sxs-lookup"><span data-stu-id="393ab-111">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="393ab-112">Обработка ошибок с помощью обещаний</span><span class="sxs-lookup"><span data-stu-id="393ab-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="393ab-113">Устранение ошибок в времени работы Windows</span><span class="sxs-lookup"><span data-stu-id="393ab-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью обещаний (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок в времени работы Windows (HTML) | Документы Майкрософт"  
