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
# <a name="windows-runtime-datetime-and-timespan-representations"></a>Представления DateTime и TimeSpan среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Представление JavaScript дат и времени отличается от версии Windows Runtime.  Структура Windows Runtime [DateTime][UwpWindowsFoundationDatetime] представлена в [][MDNDate] JavaScript в качестве даты, которая имеет запасной магазин, который соответствует данным \(и отличается диапазоном и точностью от `DateTime` JavaScript `Date` \).  При изменении этого настраиваемого `Date` объекта он становится стандартным JavaScript `Date` и теряет точность.  Значения JavaScript можно передать в время запуска Windows и проверить диапазон, что может привести к `Date` `DateTime` исключениям.  

Структура [TimeSpan времени][UwpWindowsFoundationTimespan] запуска Windows преобразуется в миллисекунд и возвращается в качестве номера JavaScript.  

## <a name="see-also"></a>См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Структурировать DateTime | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Структурная | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
