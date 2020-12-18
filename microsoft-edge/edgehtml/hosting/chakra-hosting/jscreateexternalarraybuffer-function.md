---
description: Создает объект Javascript `ArrayBuffer` для доступа к внешней памяти.
title: JsCreateExternalArrayBuffer Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235693"
---
# <span data-ttu-id="3724e-103">Функция JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="3724e-103">JsCreateExternalArrayBuffer Function</span></span>

<span data-ttu-id="3724e-104">Создает объект Javascript `ArrayBuffer` для доступа к внешней памяти.</span><span class="sxs-lookup"><span data-stu-id="3724e-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="3724e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3724e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="3724e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3724e-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="3724e-107">Указатель на внешнюю память.</span><span class="sxs-lookup"><span data-stu-id="3724e-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="3724e-108">Количество ветвей во внешней памяти.</span><span class="sxs-lookup"><span data-stu-id="3724e-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="3724e-109">Callback for when the object is finalized.</span><span class="sxs-lookup"><span data-stu-id="3724e-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="3724e-110">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="3724e-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="3724e-111">Пользовательское состояние, которое будет передано обратно в finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="3724e-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="3724e-112">Новый `ArrayBuffer` объект.</span><span class="sxs-lookup"><span data-stu-id="3724e-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="3724e-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3724e-113">Return Value</span></span>  
 <span data-ttu-id="3724e-114">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3724e-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3724e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3724e-115">Remarks</span></span>  
 <span data-ttu-id="3724e-116">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="3724e-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3724e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3724e-117">Requirements</span></span>  
 <span data-ttu-id="3724e-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3724e-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3724e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3724e-119">See Also</span></span>  
 [<span data-ttu-id="3724e-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3724e-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
