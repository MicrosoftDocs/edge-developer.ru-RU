---
description: Представления DateTime и TimeSpan среды выполнения Windows
title: Представления DateTime и TimeSpan среды выполнения Windows
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1ee3d601e727601aba03f2ff7efa532171b8f815
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235416"
---
# Представления DateTime и TimeSpan среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Представление дат и времени в JavaScript отличается от версии времени работы Windows.  Структура даты [][UwpWindowsFoundationDatetime] и времени в среде запуска [][MDNDate] Windows представлена в JavaScript как дата с хранилищем данных, которое соответствует данным \(и имеет другой диапазон и точность, чем `DateTime` JavaScript `Date` \).  При изменении этого `Date` настраиваемого объекта он становится стандартным Кодом JavaScript `Date` и теряет точность.  Значения JavaScript могут быть переданы в итоге в итоге и будут проверены в диапазоне, что может привести к `Date` `DateTime` маршалингу исключений.  

 Структура [TimeSpan][UwpWindowsFoundationTimespan] в среде запуска Windows преобразуется в миллисекунд и возвращается в качестве номера JavaScript.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
