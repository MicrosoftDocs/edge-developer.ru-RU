---
description: Выполняет проверку оператора `instanceof` JavaScript.
title: JsInstanceOf Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235684"
---
# <span data-ttu-id="ec5d9-103">Функция JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="ec5d9-103">JsInstanceOf Function</span></span>

<span data-ttu-id="ec5d9-104">Выполняет проверку оператора `instanceof` JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="ec5d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec5d9-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="ec5d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec5d9-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ec5d9-107">Объект для тестирования.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="ec5d9-108">Функция конструктора для тестирования.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="ec5d9-109">Является ли "object instanceof constructor" истинным.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="ec5d9-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ec5d9-110">Return Value</span></span>  
 <span data-ttu-id="ec5d9-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ec5d9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec5d9-112">Remarks</span></span>  
 <span data-ttu-id="ec5d9-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ec5d9-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ec5d9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ec5d9-114">Requirements</span></span>  
 <span data-ttu-id="ec5d9-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ec5d9-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec5d9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ec5d9-116">See Also</span></span>  
 [<span data-ttu-id="ec5d9-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ec5d9-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
