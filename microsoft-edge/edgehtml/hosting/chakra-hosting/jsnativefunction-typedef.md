---
description: Функция вызова.
title: JsNativeFunction Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235125"
---
# <span data-ttu-id="b18a0-103">JsNativeFunction Typedef</span><span class="sxs-lookup"><span data-stu-id="b18a0-103">JsNativeFunction Typedef</span></span>

<span data-ttu-id="b18a0-104">Функция вызова.</span><span class="sxs-lookup"><span data-stu-id="b18a0-104">A function callback.</span></span>  
  
## <span data-ttu-id="b18a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b18a0-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="b18a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b18a0-106">Parameters</span></span>  
 <span data-ttu-id="b18a0-107">вызываемая</span><span class="sxs-lookup"><span data-stu-id="b18a0-107">callee</span></span>  
 <span data-ttu-id="b18a0-108">Объект, `Function` который представляет вызываемую функцию.</span><span class="sxs-lookup"><span data-stu-id="b18a0-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="b18a0-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="b18a0-109">isConstructCall</span></span>  
 <span data-ttu-id="b18a0-110">Указывает, является ли этот вызов регулярным или новым.</span><span class="sxs-lookup"><span data-stu-id="b18a0-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="b18a0-111">arguments</span><span class="sxs-lookup"><span data-stu-id="b18a0-111">arguments</span></span>  
 <span data-ttu-id="b18a0-112">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="b18a0-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="b18a0-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="b18a0-113">argumentCount</span></span>  
 <span data-ttu-id="b18a0-114">Количество аргументов.</span><span class="sxs-lookup"><span data-stu-id="b18a0-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="b18a0-115">Значение свойства или возвращаемая величина</span><span class="sxs-lookup"><span data-stu-id="b18a0-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="b18a0-116">Результат вызова, если он есть.</span><span class="sxs-lookup"><span data-stu-id="b18a0-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="b18a0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b18a0-117">Requirements</span></span>  
 <span data-ttu-id="b18a0-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="b18a0-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b18a0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b18a0-119">See Also</span></span>  
 [<span data-ttu-id="b18a0-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b18a0-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
