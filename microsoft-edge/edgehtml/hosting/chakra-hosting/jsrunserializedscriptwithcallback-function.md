---
description: Запускает сериализованный сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.
title: JsRunSerializedScriptWithCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235798"
---
# <span data-ttu-id="e1e3d-104">Функция JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="e1e3d-104">JsRunSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="e1e3d-105">Запускает сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-105">Runs a serialized script.</span></span> <span data-ttu-id="e1e3d-106">Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="e1e3d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1e3d-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="e1e3d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1e3d-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="e1e3d-109">Callback called when the source code of the script needs to be loaded.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="e1e3d-110">Callback called when the serialized script and source code are no longer needed.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="e1e3d-111">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="e1e3d-112">Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="e1e3d-113">Этот контекст передается в scriptLoadCallback и scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="e1e3d-114">Расположение, из который поступил сценарий.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="e1e3d-115">Результат запуска сценария(если он есть).</span><span class="sxs-lookup"><span data-stu-id="e1e3d-115">The result of running the script, if any.</span></span> <span data-ttu-id="e1e3d-116">Этот параметр может иметь null.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="e1e3d-117">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e1e3d-117">Return Value</span></span>  
 <span data-ttu-id="e1e3d-118">Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e1e3d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1e3d-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e1e3d-120">Этот API пока не доступен для приложений Магазина.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="e1e3d-121">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e1e3d-122">Время работы будет удерживать буфер, пока не будут собраны все экземпляры функций, созданных из буфера.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="e1e3d-123">Затем он будет вызывать scriptUnloadCallback, чтобы сообщить вызываемой, что ее можно безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="e1e3d-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="e1e3d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e1e3d-124">Requirements</span></span>  
 <span data-ttu-id="e1e3d-125">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e1e3d-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1e3d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="e1e3d-126">See Also</span></span>  
 [<span data-ttu-id="e1e3d-127">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1e3d-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
