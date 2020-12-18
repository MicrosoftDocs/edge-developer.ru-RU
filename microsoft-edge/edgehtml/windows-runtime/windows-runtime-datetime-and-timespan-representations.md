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
# <span data-ttu-id="2343a-103">Представления DateTime и TimeSpan среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="2343a-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="2343a-104">Представление дат и времени в JavaScript отличается от версии времени работы Windows.</span><span class="sxs-lookup"><span data-stu-id="2343a-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="2343a-105">Структура даты [][UwpWindowsFoundationDatetime] и времени в среде запуска [][MDNDate] Windows представлена в JavaScript как дата с хранилищем данных, которое соответствует данным \(и имеет другой диапазон и точность, чем `DateTime` JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="2343a-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="2343a-106">При изменении этого `Date` настраиваемого объекта он становится стандартным Кодом JavaScript `Date` и теряет точность.</span><span class="sxs-lookup"><span data-stu-id="2343a-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="2343a-107">Значения JavaScript могут быть переданы в итоге в итоге и будут проверены в диапазоне, что может привести к `Date` `DateTime` маршалингу исключений.</span><span class="sxs-lookup"><span data-stu-id="2343a-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="2343a-108">Структура [TimeSpan][UwpWindowsFoundationTimespan] в среде запуска Windows преобразуется в миллисекунд и возвращается в качестве номера JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2343a-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="2343a-109">См. также</span><span class="sxs-lookup"><span data-stu-id="2343a-109">See also</span></span>  

[<span data-ttu-id="2343a-110">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="2343a-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
