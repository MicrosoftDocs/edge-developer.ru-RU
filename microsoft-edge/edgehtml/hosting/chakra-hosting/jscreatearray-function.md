---
description: Создает объект массива Javascript.
title: JsCreateArray Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34ce07055fa3d4d24188d7edbcedc3f08973e233
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235305"
---
# <span data-ttu-id="5e8ef-103">Функция JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="5e8ef-103">JsCreateArray Function</span></span>

<span data-ttu-id="5e8ef-104">Создает объект массива Javascript.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="5e8ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e8ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="5e8ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e8ef-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="5e8ef-107">Начальная длина массива.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="5e8ef-108">Новый объект массива.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-108">The new array object.</span></span>  
  
## <span data-ttu-id="5e8ef-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="5e8ef-109">Return Value</span></span>  
 <span data-ttu-id="5e8ef-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5e8ef-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e8ef-111">Remarks</span></span>  
 <span data-ttu-id="5e8ef-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="5e8ef-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5e8ef-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5e8ef-113">Requirements</span></span>  
 <span data-ttu-id="5e8ef-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="5e8ef-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5e8ef-115">См. также</span><span class="sxs-lookup"><span data-stu-id="5e8ef-115">See Also</span></span>  
 [<span data-ttu-id="5e8ef-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5e8ef-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
