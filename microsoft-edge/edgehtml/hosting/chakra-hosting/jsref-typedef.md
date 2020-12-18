---
description: Ссылка на объект, который принадлежит сборщику мусора Chakra.
title: JsRef Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235128"
---
# <span data-ttu-id="73ed2-103">JsRef Typedef</span><span class="sxs-lookup"><span data-stu-id="73ed2-103">JsRef Typedef</span></span>

<span data-ttu-id="73ed2-104">Ссылка на объект, который принадлежит сборщику мусора Chakra.</span><span class="sxs-lookup"><span data-stu-id="73ed2-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="73ed2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73ed2-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="73ed2-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73ed2-106">Remarks</span></span>  
 <span data-ttu-id="73ed2-107">Время запуска Chakra автоматически отслеживает ссылки JsRef, если они хранятся в локальных переменных или в параметрах (например, в стеке).</span><span class="sxs-lookup"><span data-stu-id="73ed2-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="73ed2-108">Для хранения JsRef в другом месте, кроме стека, необходимо вызывать JsAddRef и JsRelease для управления жизненным сроком жизни объекта, в противном случае сборщик мусора может освободить объект, пока он еще используется.</span><span class="sxs-lookup"><span data-stu-id="73ed2-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="73ed2-109">Требования</span><span class="sxs-lookup"><span data-stu-id="73ed2-109">Requirements</span></span>  
 <span data-ttu-id="73ed2-110">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="73ed2-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="73ed2-111">См. также</span><span class="sxs-lookup"><span data-stu-id="73ed2-111">See Also</span></span>  
 [<span data-ttu-id="73ed2-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="73ed2-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
