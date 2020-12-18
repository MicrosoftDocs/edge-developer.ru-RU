---
description: Извлекает указатель строки строки.
title: JsStringToPointer Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235458"
---
# <span data-ttu-id="806be-103">Функция JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="806be-103">JsStringToPointer Function</span></span>

<span data-ttu-id="806be-104">Извлекает указатель строки строки.</span><span class="sxs-lookup"><span data-stu-id="806be-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="806be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="806be-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="806be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="806be-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="806be-107">Строка, преобразуемая в указатель строки.</span><span class="sxs-lookup"><span data-stu-id="806be-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="806be-108">Указатель строки.</span><span class="sxs-lookup"><span data-stu-id="806be-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="806be-109">Длина строки.</span><span class="sxs-lookup"><span data-stu-id="806be-109">The length of the string.</span></span>  
  
## <span data-ttu-id="806be-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="806be-110">Return Value</span></span>  
 <span data-ttu-id="806be-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="806be-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="806be-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="806be-112">Remarks</span></span>  
 <span data-ttu-id="806be-113">Эта функция извлекает строку указателя строки.</span><span class="sxs-lookup"><span data-stu-id="806be-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="806be-114">Он не будет `JsErrorInvalidArgument` работать, если тип значения не является строкой.</span><span class="sxs-lookup"><span data-stu-id="806be-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="806be-115">Время жизни возвращаемой строки будет таким же, как и время жизни значения, из него поступило, однако указатель строки не считается ссылкой на значение (и поэтому не позволит его собрать).</span><span class="sxs-lookup"><span data-stu-id="806be-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="806be-116">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="806be-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="806be-117">Требования</span><span class="sxs-lookup"><span data-stu-id="806be-117">Requirements</span></span>  
 <span data-ttu-id="806be-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="806be-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="806be-119">См. также</span><span class="sxs-lookup"><span data-stu-id="806be-119">See Also</span></span>  
 [<span data-ttu-id="806be-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="806be-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
