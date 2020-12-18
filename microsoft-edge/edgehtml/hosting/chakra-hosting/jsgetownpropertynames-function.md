---
description: Получает список всех свойств объекта.
title: JsGetOwnPropertyNames Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d00788b6ef581b923413e5c71a63bb27398a326
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235109"
---
# <span data-ttu-id="430c3-103">Функция JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="430c3-103">JsGetOwnPropertyNames Function</span></span>

<span data-ttu-id="430c3-104">Получает список всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="430c3-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="430c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="430c3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="430c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="430c3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="430c3-107">Объект, из которого можно получить имена свойств.</span><span class="sxs-lookup"><span data-stu-id="430c3-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="430c3-108">Массив имен свойств.</span><span class="sxs-lookup"><span data-stu-id="430c3-108">An array of property names.</span></span>  
  
## <span data-ttu-id="430c3-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="430c3-109">Return Value</span></span>  
 <span data-ttu-id="430c3-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="430c3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="430c3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="430c3-111">Remarks</span></span>  
 <span data-ttu-id="430c3-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="430c3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="430c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="430c3-113">Requirements</span></span>  
 <span data-ttu-id="430c3-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="430c3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="430c3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="430c3-115">See Also</span></span>  
 [<span data-ttu-id="430c3-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="430c3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
