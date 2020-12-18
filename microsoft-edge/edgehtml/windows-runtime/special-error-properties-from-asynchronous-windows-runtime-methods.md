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
# Специальные свойства ошибок из асинхронных методов среды выполнения Windows.  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Отлажить асинхронные методы времени работы Windows в JavaScript может быть сложно, так как ошибка может возникнуть из глубины стека вызовов.  У объекта JavaScript есть дополнительные свойства, которые отображаются только в том случае, если ошибка произошла из асинхронного метода windows Runtime, когда приложение работает в режиме `Error` отлаживания.  
  
## Свойства специальных ошибок  

Объект ошибки, который является результатом неудачной асинхронной операции в режиме отлаживания, имеет следующие специальные свойства:  

*   `asyncOpSource` \(Object\) Получает сведения об исходном расположении, в котором был выполнен вызов, в котором произошла ошибка.  Свойство \(String\) отображает расположение в коде пользователя, искомом `asyncOpSource.originatingCall` асинхронной операции.  
*   asyncOpType \(String\) Получает имя типа асинхронной операции, который вызывает ошибку.  
    
Дополнительные сведения об ошибках с асинхронными операциями см. в:  
  
*   [Обработка ошибок с помощью обещаний][PreviousVersionsWindowsAppsHh700337]  
*   [Устранение ошибок в времени работы Windows][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью обещаний (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок в времени работы Windows (HTML) | Документы Майкрософт"  
