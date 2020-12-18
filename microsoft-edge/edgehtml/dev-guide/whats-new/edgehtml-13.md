---
description: На этой странице представлен обзор новых функций EdgeHTML 13.
title: Новые функции и API в EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235784"
---
# <span data-ttu-id="c8b8a-104">Новые возможности EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="c8b8a-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="c8b8a-105">Вот изменения, внесенные с помощью EdgeHTML 13, яма, который работает с браузером Microsoft Edge в первом крупном обновлении для Windows 10 \(11/2015, сборка 10586\). [](https://blogs.windows.com/windowsexperience/2015/11/12)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="c8b8a-106">Обзор изменений в общем браузере Microsoft Edge см. в обзоре [EdgeHTML 13,](https://blogs.windows.com/msedgedev/2015/11/16)нашего первого обновления платформы для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c8b8a-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="c8b8a-107">Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .</span><span class="sxs-lookup"><span data-stu-id="c8b8a-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="c8b8a-108">Возможности</span><span class="sxs-lookup"><span data-stu-id="c8b8a-108">Features</span></span>  

### <span data-ttu-id="c8b8a-109">CSS</span><span class="sxs-lookup"><span data-stu-id="c8b8a-109">CSS</span></span>  

<span data-ttu-id="c8b8a-110">EdgeHTML 13 поддерживает новые функции CSS, в том числе:</span><span class="sxs-lookup"><span data-stu-id="c8b8a-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="c8b8a-111">Псевдо-классы мутируемости CSS</span><span class="sxs-lookup"><span data-stu-id="c8b8a-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="c8b8a-112">Псевдо-классы диапазона CSS</span><span class="sxs-lookup"><span data-stu-id="c8b8a-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="c8b8a-113">Исходные [и](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) [неустановленные](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) ключевые слова CSS</span><span class="sxs-lookup"><span data-stu-id="c8b8a-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="c8b8a-114">Зашифрованные расширения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c8b8a-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="c8b8a-115">Microsoft Edge теперь поддерживает новые незашифрованные API зашифрованных [расширений](https://w3.org/TR/encrypted-media) мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8b8a-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="c8b8a-116">Зашифрованные расширения мультимедиа \(EME\) расширяют видео- и звуковые элементы, чтобы включить защищенный контент управления цифровыми правами (DRM\) без использования подключаемых модульов.  Дополнительные данные о EME: [зашифрованные расширения мультимедиа.](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="c8b8a-117">Графика</span><span class="sxs-lookup"><span data-stu-id="c8b8a-117">Graphics</span></span>  

<span data-ttu-id="c8b8a-118">EdgeHTML 13 представляет следующие графические обновления:</span><span class="sxs-lookup"><span data-stu-id="c8b8a-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="c8b8a-119">Многолинейная многояпка холста</span><span class="sxs-lookup"><span data-stu-id="c8b8a-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="c8b8a-120">Режимы на blending холста</span><span class="sxs-lookup"><span data-stu-id="c8b8a-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="c8b8a-121">element</span><span class="sxs-lookup"><span data-stu-id="c8b8a-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="c8b8a-122">Внешнее содержимое SVG</span><span class="sxs-lookup"><span data-stu-id="c8b8a-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="c8b8a-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c8b8a-123">JavaScript</span></span>  

<span data-ttu-id="c8b8a-124">EdgeHTML 13 включает основные улучшения и поддержку новых функций в [Chakra](https://blogs.windows.com/msedgedev/2015/09/30), обработчик JavaScript, включающий Microsoft Edge, в том числе:</span><span class="sxs-lookup"><span data-stu-id="c8b8a-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="c8b8a-125">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="c8b8a-125">New features</span></span>  

<span data-ttu-id="c8b8a-126">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c8b8a-126">On by default</span></span>  

*   <span data-ttu-id="c8b8a-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) по умолчанию \([запись блога](https://blogs.windows.com/msedgedev/2015/11/10), [демонстрация](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="c8b8a-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="c8b8a-129">Экспериментальные функции JavaScript</span><span class="sxs-lookup"><span data-stu-id="c8b8a-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="c8b8a-130">Включено с</span><span class="sxs-lookup"><span data-stu-id="c8b8a-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="c8b8a-131">[А async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="c8b8a-132">[Оператор Exponentiation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="c8b8a-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span><span class="sxs-lookup"><span data-stu-id="c8b8a-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="c8b8a-134">Ввод данных пользователем</span><span class="sxs-lookup"><span data-stu-id="c8b8a-134">User Input</span></span>  

<span data-ttu-id="c8b8a-135">Следующие функции, введенные в EdgeHTML 13, улучшают ввод данных пользователями:</span><span class="sxs-lookup"><span data-stu-id="c8b8a-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [\<meter\> <span data-ttu-id="c8b8a-136">element</span><span class="sxs-lookup"><span data-stu-id="c8b8a-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="c8b8a-137">обработник событий oninvalid для документа и окна элемента</span><span class="sxs-lookup"><span data-stu-id="c8b8a-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="c8b8a-138">Блокировка указателя</span><span class="sxs-lookup"><span data-stu-id="c8b8a-138">Pointer Lock</span></span>  

<span data-ttu-id="c8b8a-139">Microsoft Edge теперь поддерживает API блокировки указателя \(ранее называлась "Блокировка мыши"), чтобы получать доступ к необработанных перемещениям мыши, блокировать цель событий мыши в одном элементе, устраняя ограничения перемещения мыши в одном направлении и удаляя курсор из представления.</span><span class="sxs-lookup"><span data-stu-id="c8b8a-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="c8b8a-140">Новые API в EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="c8b8a-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="c8b8a-141">Ниже полный список новых API в EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="c8b8a-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="c8b8a-142">Они перечислены в формате `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="c8b8a-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="c8b8a-143">Новые API в EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="c8b8a-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="c8b8a-144">См. API-код для новых перьев <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> в EdgeHTML 13 в </a> Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> @MicrosoftEdgeDocumentation) на <a href='http://codepen.io'> </a> CodePen.</span><span class="sxs-lookup"><span data-stu-id="c8b8a-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  
