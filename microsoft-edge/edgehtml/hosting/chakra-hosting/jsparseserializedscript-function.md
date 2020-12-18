---
description: Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий.
title: JsParseSerializedScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 66ecabb9d96c3f339625f93858444f55d25fd4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235636"
---
# <span data-ttu-id="c86c8-103">Функция JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="c86c8-103">JsParseSerializedScript Function</span></span>

<span data-ttu-id="c86c8-104">Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий.</span><span class="sxs-lookup"><span data-stu-id="c86c8-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="c86c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c86c8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c86c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c86c8-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="c86c8-107">Сценарий для различета.</span><span class="sxs-lookup"><span data-stu-id="c86c8-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="c86c8-108">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="c86c8-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="c86c8-109">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="c86c8-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="c86c8-110">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="c86c8-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="c86c8-111">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="c86c8-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="c86c8-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="c86c8-112">Return Value</span></span>  
 <span data-ttu-id="c86c8-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="c86c8-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c86c8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c86c8-114">Remarks</span></span>  
 <span data-ttu-id="c86c8-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="c86c8-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c86c8-116">Буфер не сохраняется в памяти механизмом сценариев, поэтому код должен поддерживать его в памяти до тех пор, пока он может использоваться для выполнения сценариев.</span><span class="sxs-lookup"><span data-stu-id="c86c8-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="c86c8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c86c8-117">Requirements</span></span>  
 <span data-ttu-id="c86c8-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="c86c8-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c86c8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c86c8-119">See Also</span></span>  
 [<span data-ttu-id="c86c8-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c86c8-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
