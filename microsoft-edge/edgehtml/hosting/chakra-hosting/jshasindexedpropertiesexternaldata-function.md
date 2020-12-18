---
description: Определяет, есть ли у объекта индексные свойства во внешних данных.
title: JsHasIndexedPropertiesExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235802"
---
# <span data-ttu-id="04a3d-103">Функция JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="04a3d-103">JsHasIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="04a3d-104">Определяет, есть ли у объекта индексные свойства во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="04a3d-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="04a3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04a3d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="04a3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04a3d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="04a3d-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="04a3d-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="04a3d-108">Имеет ли объект индексные свойства во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="04a3d-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="04a3d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="04a3d-109">Return Value</span></span>  
 <span data-ttu-id="04a3d-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="04a3d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="04a3d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04a3d-111">Remarks</span></span>  
 <span data-ttu-id="04a3d-112">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="04a3d-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="04a3d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="04a3d-113">Requirements</span></span>  
 <span data-ttu-id="04a3d-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="04a3d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04a3d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="04a3d-115">See Also</span></span>  
 [<span data-ttu-id="04a3d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="04a3d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
