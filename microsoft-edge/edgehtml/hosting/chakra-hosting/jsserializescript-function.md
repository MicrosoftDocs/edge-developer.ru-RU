---
description: Сериализует сценарий с разбиение на буфер, чем можно использовать повторно.
title: JsSerializeScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235812"
---
# <span data-ttu-id="ddf81-103">Функция JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="ddf81-103">JsSerializeScript Function</span></span>

<span data-ttu-id="ddf81-104">Сериализует сценарий с разбиение на буфер, чем можно использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="ddf81-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="ddf81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddf81-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="ddf81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddf81-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="ddf81-107">Сценарий сериализации.</span><span class="sxs-lookup"><span data-stu-id="ddf81-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ddf81-108">Буфер, в который необходимо поместить сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="ddf81-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="ddf81-109">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="ddf81-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="ddf81-110">При вводе размер буфера вбайтах; При выходе размер буфера (в битах), необходимый для удержания сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="ddf81-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="ddf81-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ddf81-111">Return Value</span></span>  
 <span data-ttu-id="ddf81-112">Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ddf81-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ddf81-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddf81-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="ddf81-114">Разблокирует сценарий, а затем сохраняет его форму в независимом от времени работы формате.</span><span class="sxs-lookup"><span data-stu-id="ddf81-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="ddf81-115">Сериализованный сценарий затем можно десериализировать в любой время работы без необходимости повторного различета сценария.</span><span class="sxs-lookup"><span data-stu-id="ddf81-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="ddf81-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ddf81-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ddf81-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ddf81-117">Requirements</span></span>  
 <span data-ttu-id="ddf81-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ddf81-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ddf81-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ddf81-119">See Also</span></span>  
 [<span data-ttu-id="ddf81-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ddf81-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
