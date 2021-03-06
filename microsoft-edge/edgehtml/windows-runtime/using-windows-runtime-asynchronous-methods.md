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
# <a name="using-windows-runtime-asynchronous-methods"></a>Использование асинхронных методов среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Многие методы выполнения Windows, особенно методы, которые могут занять много времени, являются асинхронными.  Эти методы обычно возвращают асинхронное действие или операцию \(например, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , или `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Эти методы представлены в JavaScript [шаблоном CommonJS/Promises/A.][CommonjsWikiPromises]  То есть они возвращают объект Promise, который имеет функцию , для которой необходимо предоставить функцию, которая обрабатывает результат, если операция будет [][PreviousVersionsWindowsAppsBr229728] `completed` успешной.  Если вы не хотите предоставлять обработник ошибок, [][PreviousVersionsWindowsAppsHr701079] вместо функции следует использовать сделанную `then` функцию.  

> [!IMPORTANT]
> Функции windows Runtime недоступны для приложений, которые работают в Internet Explorer.  

## <a name="examples-of-asynchronous-methods"></a>Примеры асинхронных методов  

В следующем примере функция принимает параметр, который представляет `then` завершенную стоимость `createResourceAsync` метода.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

В этом случае, если метод сбой, он возвращает обещание в состоянии `createResourceAsync` ошибки, но не бросает исключение.  Вы можете справиться с ошибкой, используя `then` функцию следующим образом.  

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

Если вы не хотите явно обрабатывать ошибку, но хотите, чтобы она была исключением, вы можете использовать `done` функцию вместо нее.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Вы также можете отобразить прогресс, достигнутый к завершению с помощью третьей функции.  

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

Дополнительные сведения об асинхронном программировании см. в программе [Asynchronous Programming in JavaScript.][PreviousVersionsWindowsAppsHh700330]  

## <a name="see-also"></a>См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.then method | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронное программирование в JavaScript (HTML) | Документы Майкрософт"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Метод Promise.done | Документы Майкрософт"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Обещания | CommonJS Spec Wiki"  
