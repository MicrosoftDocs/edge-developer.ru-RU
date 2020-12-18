---
description: На этой странице представлен обзор новых функций предварительных сборков EdgeHTML для разработчиков.
title: Новые возможности EdgeHTML для разработчиков — руководство для разработчиков
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик, новые возможности в edge, новые API в edge, edgehtml, предварительные сборки edgehtml
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4ffe9876b4771478e520289ba1343e6c66a1b667
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235786"
---
# <span data-ttu-id="e2af2-104">Что нового в EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="e2af2-104">What's new in EdgeHTML</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="e2af2-105">Получите новейшие функции и API EdgeHTML, становясь в [insider Windows!](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="e2af2-105">Get the latest EdgeHTML features and APIs by becoming a [Windows Insider](https://insider.windows.com)!</span></span>  <span data-ttu-id="e2af2-106">Программа [программы insider Windows](https://insider.windows.com) предоставляет последние сборки Windows 10 сразу после их создания.</span><span class="sxs-lookup"><span data-stu-id="e2af2-106">The [Windows Insider Program](https://insider.windows.com) provides the latest Windows 10 builds as soon as they're available.</span></span>  

<span data-ttu-id="e2af2-107">Перенаправляйте руководство разработчика, чтобы увидеть новые функции и API, которые поставляются в текущем выпуске платформы Microsoft Edge, EdgeHTML 18 \(сборка 17763\). [](../dev-guide/index.md)</span><span class="sxs-lookup"><span data-stu-id="e2af2-107">Head over to the [Dev Guide](../dev-guide/index.md) to see the new features and APIs shipped in the current release of the Microsoft Edge platform, EdgeHTML 18 \(Build 17763\).</span></span>  

<span data-ttu-id="e2af2-108">Ниже приведены новые и обновленные API EdgeHTML в сборках Windows 10 Preview.</span><span class="sxs-lookup"><span data-stu-id="e2af2-108">Below are new and updated EdgeHTML APIs in Windows 10 Preview Builds.</span></span> <span data-ttu-id="e2af2-109">Они перечислены в формате `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="e2af2-109">They are listed in the format of `[interface name].[api name]`.</span></span>  <span data-ttu-id="e2af2-110">Полный список новых функций Microsoft Edge и [](https://developer.microsoft.com/microsoft-edge/platform/changelog) платформы см. [](../dev-guide/index.md) в руководстве разработчика по изменению или перенаправлении к новым функциям и API в текущем стабильном выпуске платформы Microsoft Edge, EdgeHTML 18.</span><span class="sxs-lookup"><span data-stu-id="e2af2-110">For a full list of new Microsoft Edge and platform features, check out [Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) or head over to the [Dev Guide](../dev-guide/index.md) to see new features and APIs shipped in the current stable release of the Microsoft Edge platform, EdgeHTML 18.</span></span>   

> [!WARNING] 
> <span data-ttu-id="e2af2-111">Некоторые сведения относятся к предварительно выпущенным продуктам, которые могут быть существенно изменены перед коммерческим выпусками.</span><span class="sxs-lookup"><span data-stu-id="e2af2-111">Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>  <span data-ttu-id="e2af2-112">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.</span><span class="sxs-lookup"><span data-stu-id="e2af2-112">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>  

## <span data-ttu-id="e2af2-113">Предварительная сборка 18272</span><span class="sxs-lookup"><span data-stu-id="e2af2-113">Preview Build 18272</span></span>  

<span data-ttu-id="e2af2-114">API не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e2af2-114">No API changes.</span></span>  

## <span data-ttu-id="e2af2-115">Предварительная сборка 18267</span><span class="sxs-lookup"><span data-stu-id="e2af2-115">Preview Build 18267</span></span>  

<span data-ttu-id="e2af2-116">API не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e2af2-116">No API changes.</span></span>  

## <span data-ttu-id="e2af2-117">Предварительная сборка 18262</span><span class="sxs-lookup"><span data-stu-id="e2af2-117">Preview Build 18262</span></span>  

<span data-ttu-id="e2af2-118">Добавлена новая поддержка API:</span><span class="sxs-lookup"><span data-stu-id="e2af2-118">Added new API support:</span></span>  

<iframe height='341' scrolling='no' title='<span data-ttu-id="e2af2-119">Предварительная сборка EdgeHTML 17682</span><span class="sxs-lookup"><span data-stu-id="e2af2-119">EdgeHTML Preview Build 17682</span></span>' src='//codepen.io/MSEdgeDev/embed/5a691c1840690352f409d3788b8167fa/?height=341&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="e2af2-120">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/5a691c1840690352f409d3788b8167fa/'> EdgeHTML Preview Build 17682 </a> by MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) on </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="e2af2-120">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/5a691c1840690352f409d3788b8167fa/'>EdgeHTML Preview Build 17682</a> by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>  </iframe>  

## <span data-ttu-id="e2af2-121">Предварительная сборка 18252</span><span class="sxs-lookup"><span data-stu-id="e2af2-121">Preview Build 18252</span></span>  

<span data-ttu-id="e2af2-122">API не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e2af2-122">No API changes.</span></span>  

## <span data-ttu-id="e2af2-123">Предварительная сборка 18247</span><span class="sxs-lookup"><span data-stu-id="e2af2-123">Preview Build 18247</span></span>  

<span data-ttu-id="e2af2-124">API не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e2af2-124">No API changes.</span></span>  

## <span data-ttu-id="e2af2-125">Предварительная сборка 18242</span><span class="sxs-lookup"><span data-stu-id="e2af2-125">Preview Build 18242</span></span>  

<span data-ttu-id="e2af2-126">API не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e2af2-126">No API changes.</span></span>  
