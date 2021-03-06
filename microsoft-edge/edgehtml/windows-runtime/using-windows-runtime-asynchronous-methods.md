---
description: Использование асинхронных методов среды выполнения Windows
title: Использование асинхронных методов среды выполнения Windows
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c7e8ac4690525ee89a06eccf843531c2c7a20324
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398156"
---
# <a name="using-windows-runtime-asynchronous-methods"></a><span data-ttu-id="2d5e4-103">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="2d5e4-103">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="2d5e4-104">Многие методы выполнения Windows, особенно методы, которые могут занять много времени, являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-104">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="2d5e4-105">Эти методы обычно возвращают асинхронное действие или операцию \(например, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , или `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="2d5e4-105">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="2d5e4-106">Эти методы представлены в JavaScript [шаблоном CommonJS/Promises/A.][CommonjsWikiPromises]</span><span class="sxs-lookup"><span data-stu-id="2d5e4-106">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="2d5e4-107">То есть они возвращают объект Promise, который имеет функцию , для которой необходимо предоставить функцию, которая обрабатывает результат, если операция будет [][PreviousVersionsWindowsAppsBr229728] `completed` успешной.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-107">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="2d5e4-108">Если вы не хотите предоставлять обработник ошибок, [][PreviousVersionsWindowsAppsHr701079] вместо функции следует использовать сделанную `then` функцию.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-108">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2d5e4-109">Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-109">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="examples-of-asynchronous-methods"></a><span data-ttu-id="2d5e4-110">Примеры асинхронных методов</span><span class="sxs-lookup"><span data-stu-id="2d5e4-110">Examples of asynchronous methods</span></span>  

<span data-ttu-id="2d5e4-111">В следующем примере функция принимает параметр, который представляет `then` завершенную стоимость `createResourceAsync` метода.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-111">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="2d5e4-112">В этом случае, если метод сбой, он возвращает обещание в состоянии `createResourceAsync` ошибки, но не бросает исключение.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-112">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="2d5e4-113">Вы можете справиться с ошибкой, используя `then` функцию следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-113">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="2d5e4-114">Если вы не хотите явно обрабатывать ошибку, но хотите, чтобы она была исключением, вы можете использовать `done` функцию вместо нее.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-114">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="2d5e4-115">Вы также можете отобразить прогресс, достигнутый к завершению с помощью третьей функции.</span><span class="sxs-lookup"><span data-stu-id="2d5e4-115">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

<span data-ttu-id="2d5e4-116">Дополнительные сведения об асинхронном программировании см. в программе [Asynchronous Programming in JavaScript.][PreviousVersionsWindowsAppsHh700330]</span><span class="sxs-lookup"><span data-stu-id="2d5e4-116">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d5e4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2d5e4-117">See also</span></span>  

[<span data-ttu-id="2d5e4-118">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="2d5e4-118">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.then method | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронное программирование в JavaScript (HTML) | Документы Майкрософт"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Метод Promise.done | Документы Майкрософт"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Обещания | CommonJS Spec Wiki"  
