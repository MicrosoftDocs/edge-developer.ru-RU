---
description: Запускает сериализованный сценарий.
title: JsRunSerializedScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46f293d76bf0944c1cdedae917735c505798f4ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235799"
---
# <span data-ttu-id="735d9-103">Функция JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="735d9-103">JsRunSerializedScript Function</span></span>

<span data-ttu-id="735d9-104">Запускает сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="735d9-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="735d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="735d9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="735d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="735d9-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="735d9-107">Исходный код сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="735d9-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="735d9-108">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="735d9-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="735d9-109">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="735d9-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="735d9-110">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="735d9-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="735d9-111">Результат запуска сценария(если он есть).</span><span class="sxs-lookup"><span data-stu-id="735d9-111">The result of running the script, if any.</span></span> <span data-ttu-id="735d9-112">Этот параметр может иметь null.</span><span class="sxs-lookup"><span data-stu-id="735d9-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="735d9-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="735d9-113">Return Value</span></span>  
 <span data-ttu-id="735d9-114">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="735d9-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="735d9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="735d9-115">Remarks</span></span>  
 <span data-ttu-id="735d9-116">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="735d9-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="735d9-117">Буфер не сохраняется в памяти механизмом сценариев, поэтому код должен поддерживать его в памяти до тех пор, пока он может использоваться для выполнения сценариев.</span><span class="sxs-lookup"><span data-stu-id="735d9-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="735d9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="735d9-118">Requirements</span></span>  
 <span data-ttu-id="735d9-119">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="735d9-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="735d9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="735d9-120">See Also</span></span>  
 [<span data-ttu-id="735d9-121">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="735d9-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
