---
description: Представления DateTime и TimeSpan среды выполнения Windows
title: Представления DateTime и TimeSpan среды выполнения Windows
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c2627826755f041a440112c3390ecb17d1f703ce
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398128"
---
# <a name="windows-runtime-datetime-and-timespan-representations"></a><span data-ttu-id="a857c-103">Представления DateTime и TimeSpan среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="a857c-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="a857c-104">Представление JavaScript дат и времени отличается от версии Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="a857c-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="a857c-105">Структура Windows Runtime [DateTime][UwpWindowsFoundationDatetime] представлена в [][MDNDate] JavaScript в качестве даты, которая имеет запасной магазин, который соответствует данным \(и отличается диапазоном и точностью от `DateTime` JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="a857c-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="a857c-106">При изменении этого настраиваемого `Date` объекта он становится стандартным JavaScript `Date` и теряет точность.</span><span class="sxs-lookup"><span data-stu-id="a857c-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="a857c-107">Значения JavaScript можно передать в время запуска Windows и проверить диапазон, что может привести к `Date` `DateTime` исключениям.</span><span class="sxs-lookup"><span data-stu-id="a857c-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

<span data-ttu-id="a857c-108">Структура [TimeSpan времени][UwpWindowsFoundationTimespan] запуска Windows преобразуется в миллисекунд и возвращается в качестве номера JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a857c-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a857c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="a857c-109">See also</span></span>  

[<span data-ttu-id="a857c-110">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="a857c-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Структурировать DateTime | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Структурная | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
