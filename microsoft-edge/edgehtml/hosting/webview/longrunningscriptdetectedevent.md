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
# <a name="longrunningscriptdetectedevent-object"></a><span data-ttu-id="25c20-104">Объект LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="25c20-104">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="25c20-105">Предоставляет сведения [для MSWebViewLongRunningScriptDetected.](../webview/index.md#mswebviewlongrunningscriptdetected)</span><span class="sxs-lookup"><span data-stu-id="25c20-105">Provides information for [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span></span>  

## <a name="properties"></a><span data-ttu-id="25c20-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="25c20-106">Properties</span></span>  

### <a name="executiontime"></a><span data-ttu-id="25c20-107">executionTime</span><span class="sxs-lookup"><span data-stu-id="25c20-107">executionTime</span></span>  

<span data-ttu-id="25c20-108">Получает количество миллисекунд, которые [](../webview/index.md) элемент веб-просмотров выполняет долгосрочный сценарий.</span><span class="sxs-lookup"><span data-stu-id="25c20-108">Gets the number of milliseconds that the [webview](../webview/index.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a><span data-ttu-id="25c20-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25c20-109">Property value</span></span>  

<span data-ttu-id="25c20-110">Тип: **длинный**</span><span class="sxs-lookup"><span data-stu-id="25c20-110">Type: **long**</span></span>  

### <a name="stoppagescriptexecution"></a><span data-ttu-id="25c20-111">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="25c20-111">stopPageScriptExecution</span></span>  

<span data-ttu-id="25c20-112">Останавливает длительное выполнение скрипта в [элементе веб-просмотров.](../webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="25c20-112">Stops a long-running script executing in the [webview](../webview/index.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a><span data-ttu-id="25c20-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25c20-113">Property value</span></span>  

<span data-ttu-id="25c20-114">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25c20-114">Type: **Boolean**</span></span>  
