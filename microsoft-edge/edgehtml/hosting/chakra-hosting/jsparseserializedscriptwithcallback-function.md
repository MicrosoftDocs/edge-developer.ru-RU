---
description: Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.
title: JsParseSerializedScriptWithCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235630"
---
# <span data-ttu-id="5aa7b-104">Функция JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="5aa7b-104">JsParseSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="5aa7b-105">Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="5aa7b-106">Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="5aa7b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aa7b-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="5aa7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aa7b-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="5aa7b-109">Callback called when the source code of the script needs to be loaded.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="5aa7b-110">Callback called when the serialized script and source code are no longer needed.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="5aa7b-111">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="5aa7b-112">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="5aa7b-113">Этот контекст передается в scriptLoadCallback и scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="5aa7b-114">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="5aa7b-115">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="5aa7b-116">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="5aa7b-116">Return Value</span></span>  
 <span data-ttu-id="5aa7b-117">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5aa7b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5aa7b-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5aa7b-119">Этот API пока не доступен для приложений Магазина.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="5aa7b-120">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5aa7b-121">Время работы будет удерживать буфер, пока не будут собраны все экземпляры функций, созданных из буфера.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="5aa7b-122">Затем он будет вызывать scriptUnloadCallback, чтобы сообщить вызываемой, что ее можно безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="5aa7b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5aa7b-123">Requirements</span></span>  
 <span data-ttu-id="5aa7b-124">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="5aa7b-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5aa7b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5aa7b-125">See Also</span></span>  
 [<span data-ttu-id="5aa7b-126">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5aa7b-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
