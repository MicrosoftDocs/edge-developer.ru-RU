---
description: Объект LongRunningScriptDetectedEvent
title: Объект LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, windows 10 apps, uwp, edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397945"
---
# <a name="longrunningscriptdetectedevent-object"></a>Объект LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Предоставляет сведения [для MSWebViewLongRunningScriptDetected.](../webview/index.md#mswebviewlongrunningscriptdetected)  

## <a name="properties"></a>Свойства  

### <a name="executiontime"></a>executionTime  

Получает количество миллисекунд, которые [](../webview/index.md) элемент веб-просмотров выполняет долгосрочный сценарий.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a>Значение свойства  

Тип: **длинный**  

### <a name="stoppagescriptexecution"></a>stopPageScriptExecution  

Останавливает длительное выполнение скрипта в [элементе веб-просмотров.](../webview/index.md)  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a>Значение свойства  

Тип: **Boolean**  
