---
description: Специальные свойства ошибок из асинхронных методов среды выполнения Windows.
title: Специальные свойства ошибок из асинхронных методов среды выполнения Windows.
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398842"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a><span data-ttu-id="965ed-103">Специальные свойства ошибок из асинхронных методов среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="965ed-103">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="965ed-104">В JavaScript может быть сложно отлажить асинхронные методы запуска Windows, так как ошибка может быть выброшена из глубины стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="965ed-104">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="965ed-105">Объект JavaScript обладает дополнительными свойствами, которые отображаются только в том случае, если ошибка выброшена из метода асинхронного запуска Windows, когда приложение работает в `Error` отлаживаемом режиме.</span><span class="sxs-lookup"><span data-stu-id="965ed-105">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <a name="special-error-properties"></a><span data-ttu-id="965ed-106">Свойства специальных ошибок</span><span class="sxs-lookup"><span data-stu-id="965ed-106">Special error properties</span></span>  

<span data-ttu-id="965ed-107">Объект ошибки, который является результатом асинхронной операции windows Runtime в режиме отлаживания, обладает следующими специальными свойствами:</span><span class="sxs-lookup"><span data-stu-id="965ed-107">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="965ed-108">\(Object\) Получает сведения о исходном расположении, где был сделан вызов, который произвел ошибку.</span><span class="sxs-lookup"><span data-stu-id="965ed-108">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="965ed-109">Свойство \(String\) отображает расположение в коде пользователя, зародив `asyncOpSource.originatingCall` асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="965ed-109">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="965ed-110">asyncOpType \(String\) получает имя типа асинхронной операции, который поднял ошибку.</span><span class="sxs-lookup"><span data-stu-id="965ed-110">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="965ed-111">Дополнительные сведения об ошибках с асинхронными операциями см. в этой ссылке.</span><span class="sxs-lookup"><span data-stu-id="965ed-111">For more information about errors with asynchronous operations, see:</span></span>  

*   [<span data-ttu-id="965ed-112">Обработка ошибок с помощью обещаний</span><span class="sxs-lookup"><span data-stu-id="965ed-112">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="965ed-113">Устранение ошибок во время работы Windows</span><span class="sxs-lookup"><span data-stu-id="965ed-113">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок во время работы Windows (HTML) | Документы Майкрософт"  
