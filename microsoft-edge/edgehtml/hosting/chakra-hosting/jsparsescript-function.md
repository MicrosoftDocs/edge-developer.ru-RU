---
description: Проансирует сценарий и возвращает функцию, представляющую сценарий.
title: JsParseScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235637"
---
# <span data-ttu-id="d568b-103">Функция JsParseScript</span><span class="sxs-lookup"><span data-stu-id="d568b-103">JsParseScript Function</span></span>

<span data-ttu-id="d568b-104">Проансирует сценарий и возвращает функцию, представляющую сценарий.</span><span class="sxs-lookup"><span data-stu-id="d568b-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="d568b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d568b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="d568b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d568b-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="d568b-107">Сценарий для различета.</span><span class="sxs-lookup"><span data-stu-id="d568b-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="d568b-108">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="d568b-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="d568b-109">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="d568b-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="d568b-110">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="d568b-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="d568b-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d568b-111">Return Value</span></span>  
 <span data-ttu-id="d568b-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="d568b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d568b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d568b-113">Remarks</span></span>  
 <span data-ttu-id="d568b-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="d568b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d568b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d568b-115">Requirements</span></span>  
 <span data-ttu-id="d568b-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="d568b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d568b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d568b-117">See Also</span></span>  
 [<span data-ttu-id="d568b-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d568b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
