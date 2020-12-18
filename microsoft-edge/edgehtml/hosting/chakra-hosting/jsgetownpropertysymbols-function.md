---
description: Получает список всех свойств символов объекта.
title: JsGetOwnPropertySymbols Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235670"
---
# <span data-ttu-id="de2af-103">Функция JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="de2af-103">JsGetOwnPropertySymbols Function</span></span>

<span data-ttu-id="de2af-104">Получает список всех свойств символов объекта.</span><span class="sxs-lookup"><span data-stu-id="de2af-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="de2af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de2af-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="de2af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de2af-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="de2af-107">Объект, из которого можно получить символы свойства.</span><span class="sxs-lookup"><span data-stu-id="de2af-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="de2af-108">Массив символов свойств.</span><span class="sxs-lookup"><span data-stu-id="de2af-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="de2af-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="de2af-109">Return Value</span></span>  
 <span data-ttu-id="de2af-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="de2af-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="de2af-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de2af-111">Remarks</span></span>  
 <span data-ttu-id="de2af-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="de2af-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="de2af-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="de2af-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="de2af-114">Требования</span><span class="sxs-lookup"><span data-stu-id="de2af-114">Requirements</span></span>  
 <span data-ttu-id="de2af-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="de2af-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="de2af-116">См. также</span><span class="sxs-lookup"><span data-stu-id="de2af-116">See Also</span></span>  
 [<span data-ttu-id="de2af-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="de2af-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
