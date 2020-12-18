---
description: Выполняет сценарий.
title: JsRunScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d61771991e1d22a9d71a928d785390b814a992a8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235800"
---
# <span data-ttu-id="0ae73-103">Функция JsRunScript</span><span class="sxs-lookup"><span data-stu-id="0ae73-103">JsRunScript Function</span></span>

<span data-ttu-id="0ae73-104">Выполняет сценарий.</span><span class="sxs-lookup"><span data-stu-id="0ae73-104">Executes a script.</span></span>  
  
## <span data-ttu-id="0ae73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ae73-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="0ae73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ae73-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="0ae73-107">Сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="0ae73-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="0ae73-108">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="0ae73-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="0ae73-109">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="0ae73-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="0ae73-110">Результат скрипта, если он есть.</span><span class="sxs-lookup"><span data-stu-id="0ae73-110">The result of the script, if any.</span></span> <span data-ttu-id="0ae73-111">Этот параметр может иметь null.</span><span class="sxs-lookup"><span data-stu-id="0ae73-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="0ae73-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0ae73-112">Return Value</span></span>  
 <span data-ttu-id="0ae73-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="0ae73-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0ae73-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ae73-114">Remarks</span></span>  
 <span data-ttu-id="0ae73-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="0ae73-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0ae73-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0ae73-116">Requirements</span></span>  
 <span data-ttu-id="0ae73-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="0ae73-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0ae73-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0ae73-118">See Also</span></span>  
 [<span data-ttu-id="0ae73-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0ae73-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
