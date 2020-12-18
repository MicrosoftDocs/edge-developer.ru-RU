---
description: Получает внутренний набор данных в JsrtContext.
title: JsGetContextData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235427"
---
# <span data-ttu-id="a4b89-103">Функция JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="a4b89-103">JsGetContextData Function</span></span>

<span data-ttu-id="a4b89-104">Получает внутренний набор данных в JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="a4b89-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="a4b89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4b89-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="a4b89-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4b89-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="a4b89-107">Контекст для получения данных.</span><span class="sxs-lookup"><span data-stu-id="a4b89-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="a4b89-108">Указатель на данные, в которые будут возвращаться данные.</span><span class="sxs-lookup"><span data-stu-id="a4b89-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="a4b89-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a4b89-109">Return Value</span></span>  
 <span data-ttu-id="a4b89-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="a4b89-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a4b89-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4b89-111">Remarks</span></span>  
 <span data-ttu-id="a4b89-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="a4b89-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a4b89-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a4b89-113">Requirements</span></span>  
 <span data-ttu-id="a4b89-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="a4b89-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a4b89-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a4b89-115">See Also</span></span>  
 [<span data-ttu-id="a4b89-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a4b89-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
