---
description: Создает значение JavaScript, которое является проекцией `VARIANT` переданного.
title: JsVariantToValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235451"
---
# <span data-ttu-id="b2755-103">Функция JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="b2755-103">JsVariantToValue Function</span></span>

<span data-ttu-id="b2755-104">Создает значение JavaScript, которое является проекцией `VARIANT` переданного.</span><span class="sxs-lookup"><span data-stu-id="b2755-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="b2755-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2755-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="b2755-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2755-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="b2755-107">A `VARIANT` для проецируемых проектов.</span><span class="sxs-lookup"><span data-stu-id="b2755-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="b2755-108">Значение JavaScript, которое является проекцией `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="b2755-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="b2755-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b2755-109">Return Value</span></span>  
 <span data-ttu-id="b2755-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="b2755-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b2755-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2755-111">Remarks</span></span>  
 <span data-ttu-id="b2755-112">Проецируемые значения могут использоваться сценарием для вызова объекта автоматизации COM из скрипта.</span><span class="sxs-lookup"><span data-stu-id="b2755-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="b2755-113">Ведущие точки отвечают за принудительное применение правил потоков COM.</span><span class="sxs-lookup"><span data-stu-id="b2755-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="b2755-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="b2755-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b2755-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b2755-115">Requirements</span></span>  
 <span data-ttu-id="b2755-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="b2755-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b2755-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b2755-117">See Also</span></span>  
 [<span data-ttu-id="b2755-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b2755-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
