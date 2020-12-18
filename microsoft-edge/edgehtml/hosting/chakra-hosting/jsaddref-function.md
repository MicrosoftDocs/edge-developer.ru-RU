---
description: Добавляет ссылку на объект сборки мусора.
title: JsAddRef Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235336"
---
# <span data-ttu-id="6a972-103">Функция JsAddRef</span><span class="sxs-lookup"><span data-stu-id="6a972-103">JsAddRef Function</span></span>

<span data-ttu-id="6a972-104">Добавляет ссылку на объект сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="6a972-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="6a972-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a972-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="6a972-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a972-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="6a972-107">Объект, на который нужно добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="6a972-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="6a972-108">Новое количество ссылок объекта (может передаваться в null).</span><span class="sxs-lookup"><span data-stu-id="6a972-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="6a972-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6a972-109">Return Value</span></span>  
 <span data-ttu-id="6a972-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="6a972-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6a972-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a972-111">Remarks</span></span>  
 <span data-ttu-id="6a972-112">Это необходимо только для работок, которые не будут храниться `JsRef` где-либо в стеке.</span><span class="sxs-lookup"><span data-stu-id="6a972-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="6a972-113">Вызов гарантирует, что объект, на который ссылается, не будет `JsAddRef` `JsRef` освобожден, пока `JsRelease` не будет вызван.</span><span class="sxs-lookup"><span data-stu-id="6a972-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="6a972-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6a972-114">Requirements</span></span>  
 <span data-ttu-id="6a972-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="6a972-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6a972-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6a972-116">See Also</span></span>  
 [<span data-ttu-id="6a972-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6a972-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
