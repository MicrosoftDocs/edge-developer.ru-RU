---
description: Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.
title: JsInspectableToObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235686"
---
# <span data-ttu-id="ae070-103">Функция JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="ae070-103">JsInspectableToObject Function</span></span>

<span data-ttu-id="ae070-104">Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.</span><span class="sxs-lookup"><span data-stu-id="ae070-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="ae070-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae070-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="ae070-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae070-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="ae070-107">A `IInspectable` для проецируемых проектов.</span><span class="sxs-lookup"><span data-stu-id="ae070-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="ae070-108">Значение JavaScript, которое является проекцией `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="ae070-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="ae070-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ae070-109">Return Value</span></span>  
 <span data-ttu-id="ae070-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ae070-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ae070-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae070-111">Remarks</span></span>  
 <span data-ttu-id="ae070-112">Проецируемые значения могут использоваться сценарием для вызова объекта WinRT.</span><span class="sxs-lookup"><span data-stu-id="ae070-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="ae070-113">Ведущие точки отвечают за принудительное применение правил потоков COM.</span><span class="sxs-lookup"><span data-stu-id="ae070-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="ae070-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ae070-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ae070-115">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="ae070-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="ae070-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ae070-116">Requirements</span></span>  
 <span data-ttu-id="ae070-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ae070-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ae070-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ae070-118">See Also</span></span>  
 [<span data-ttu-id="ae070-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ae070-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
