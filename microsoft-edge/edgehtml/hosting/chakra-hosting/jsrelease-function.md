---
description: Освобождает ссылку на объект сборки мусора.
title: JsRelease Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235284"
---
# <span data-ttu-id="f933e-103">Функция JsRelease</span><span class="sxs-lookup"><span data-stu-id="f933e-103">JsRelease Function</span></span>

<span data-ttu-id="f933e-104">Освобождает ссылку на объект сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="f933e-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="f933e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f933e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="f933e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f933e-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="f933e-107">Объект, на который нужно добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="f933e-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="f933e-108">Новое количество ссылок объекта (может передаваться в null).</span><span class="sxs-lookup"><span data-stu-id="f933e-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="f933e-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f933e-109">Return Value</span></span>  
 <span data-ttu-id="f933e-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="f933e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f933e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f933e-111">Remarks</span></span>  
 <span data-ttu-id="f933e-112">Удаляет ссылку на `JsRef` лад, созданный с помощью `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="f933e-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="f933e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f933e-113">Requirements</span></span>  
 <span data-ttu-id="f933e-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="f933e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f933e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f933e-115">See Also</span></span>  
 [<span data-ttu-id="f933e-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f933e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
