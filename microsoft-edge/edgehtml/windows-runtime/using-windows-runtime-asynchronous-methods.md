---
description: Использование асинхронных методов в времени работы Windows.
title: Использование асинхронных методов среды выполнения Windows
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 26ed26e07049a9488aebe5fda92a65550474b51c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235417"
---
# Использование асинхронных методов среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Многие методы времени выполнения Windows, особенно методы, которые могут занять много времени, являются асинхронными.  Эти методы обычно возвращают асинхронное действие или операцию \(например, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , или `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Эти методы представлены в JavaScript шаблоном [CommonJS/Promises/A.][CommonjsWikiPromises]  То есть они возвращают объект Promise с функцией [then,][PreviousVersionsWindowsAppsBr229728]для которой необходимо предоставить функцию, которая обрабатывает результат в случае `completed` успешной операции.  Если вы не хотите предоставлять обработец ошибок, следует использовать функцию ["Готово",][PreviousVersionsWindowsAppsHr701079] а не `then` функцию.  

> [!IMPORTANT]
> Функции времени работы Windows недоступны для приложений, которые работают в Internet Explorer.  

## Примеры асинхронных методов  

В следующем примере функция принимает параметр, который представляет `then` завершенные значения `createResourceAsync` метода.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

В этом случае, если метод не удается, он возвращает обещание в состоянии `createResourceAsync` ошибки, но не выдает исключение.  Вы можете обработать ошибку, используя `then` функцию следующим образом.  

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

Если вы не хотите обрабатывать ошибку явным образом, но хотите, чтобы она вымыла исключение, можно использовать `done` функцию.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Вы также можете отобразить ход выполнения, используя третью функцию.  

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

Дополнительные сведения об асинхронном программировании см. в асинхронном [программировании на JavaScript.][PreviousVersionsWindowsAppsHh700330]  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Метод Promise.then | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронное программирование на JavaScript (HTML) | Документы Майкрософт"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Метод Promise.done | Документы Майкрософт"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Promises | Вики-сайт спецификации CommonJS"  
