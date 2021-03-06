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
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a>Специальные свойства ошибок из асинхронных методов среды выполнения Windows.  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

В JavaScript может быть сложно отлажить асинхронные методы запуска Windows, так как ошибка может быть выброшена из глубины стека вызовов.  Объект JavaScript обладает дополнительными свойствами, которые отображаются только в том случае, если ошибка выброшена из метода асинхронного запуска Windows, когда приложение работает в `Error` отлаживаемом режиме.  
  
## <a name="special-error-properties"></a>Свойства специальных ошибок  

Объект ошибки, который является результатом асинхронной операции windows Runtime в режиме отлаживания, обладает следующими специальными свойствами:  

*   `asyncOpSource` \(Object\) Получает сведения о исходном расположении, где был сделан вызов, который произвел ошибку.  Свойство \(String\) отображает расположение в коде пользователя, зародив `asyncOpSource.originatingCall` асинхронную операцию.  
*   asyncOpType \(String\) получает имя типа асинхронной операции, который поднял ошибку.  
    
Дополнительные сведения об ошибках с асинхронными операциями см. в этой ссылке.  

*   [Обработка ошибок с помощью обещаний][PreviousVersionsWindowsAppsHh700337]  
*   [Устранение ошибок во время работы Windows][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок во время работы Windows (HTML) | Документы Майкрософт"  
