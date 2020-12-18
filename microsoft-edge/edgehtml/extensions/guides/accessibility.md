---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Чтобы значок расширения был виден как в светлом, так и в темном режиме, следуйте руководству по специальным данным.
title: Accessibility - Extensions (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6e7dbd2ee66ac785be31eec7189b87e6a6bd91f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235758"
---
# <span data-ttu-id="ff41b-104">Accessibility - Extensions (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ff41b-104">Accessibility - Extensions (EdgeHTML)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="ff41b-105">Создание доступных значков расширений для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff41b-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="ff41b-106">Разработчикам сторонних расширений рекомендуется использовать ресурсы изображений, которые соответствуют строгим требованиям корпорации Майкрософт к специальным требованиям, чтобы значки были четко видны как для светлых, так и для темных тем.</span><span class="sxs-lookup"><span data-stu-id="ff41b-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="ff41b-107">Рекомендуется, чтобы все значки расширения были в соотношении 14:1 между цветом фона значка и основным цветом самого значка.</span><span class="sxs-lookup"><span data-stu-id="ff41b-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="ff41b-108">Для удовлетворения этих требований в расширениях, разработанных корпорацией Майкрософт, применяется визуальная обработка стикеров.</span><span class="sxs-lookup"><span data-stu-id="ff41b-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="ff41b-109">Примеры "наклейки"</span><span class="sxs-lookup"><span data-stu-id="ff41b-109">Examples of the "stickering"</span></span>

<span data-ttu-id="ff41b-110">Основная цель наклейки — сделать значок визуально доступным для любого цвета фона.</span><span class="sxs-lookup"><span data-stu-id="ff41b-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="ff41b-111">Для поддержки требований высокой контрастности рекомендуемое соотношение цветов между белым внешним росчерком и значком должно быть 14:1.</span><span class="sxs-lookup"><span data-stu-id="ff41b-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="ff41b-112">Хороший значок</span><span class="sxs-lookup"><span data-stu-id="ff41b-112">Good icon</span></span>
<span data-ttu-id="ff41b-113">С помощью наклеек в основном темный значок остается видимым на любом цвете фона.</span><span class="sxs-lookup"><span data-stu-id="ff41b-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![изображение значка, которое отображается на любом цвете фона](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="ff41b-115">Плохой значок</span><span class="sxs-lookup"><span data-stu-id="ff41b-115">Bad icon</span></span>
<span data-ttu-id="ff41b-116">Без наклеек значок может смешиваться в фоновом режиме и становится невозможным для увидеть.</span><span class="sxs-lookup"><span data-stu-id="ff41b-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![изображение смешивания значка на черный фон](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="ff41b-118">Значок расширения "Наклейка"</span><span class="sxs-lookup"><span data-stu-id="ff41b-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="ff41b-119">В следующих пяти шагах описан рекомендуемый метод создания значка расширения, который соответствует требованиям корпорации Майкрософт к специальным возможности.</span><span class="sxs-lookup"><span data-stu-id="ff41b-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="ff41b-120">Шаг 1</span><span class="sxs-lookup"><span data-stu-id="ff41b-120">Step 1</span></span>                                       | <span data-ttu-id="ff41b-121">Шаг 2</span><span class="sxs-lookup"><span data-stu-id="ff41b-121">Step 2</span></span>                                       | <span data-ttu-id="ff41b-122">Шаг 3</span><span class="sxs-lookup"><span data-stu-id="ff41b-122">Step 3</span></span>                                                                                 | <span data-ttu-id="ff41b-123">Шаг 4</span><span class="sxs-lookup"><span data-stu-id="ff41b-123">Step 4</span></span>                                                                          | <span data-ttu-id="ff41b-124">Шаг5</span><span class="sxs-lookup"><span data-stu-id="ff41b-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="ff41b-125">Задайте значок в указанной сетке.</span><span class="sxs-lookup"><span data-stu-id="ff41b-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="ff41b-126">Уменьшите размер значка на 2 пикселя.</span><span class="sxs-lookup"><span data-stu-id="ff41b-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="ff41b-127">Скопируйте значок и в paste на месте.</span><span class="sxs-lookup"><span data-stu-id="ff41b-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="ff41b-128">Создайте внешний росчерк размером 2 пикселя с скругленными углами.</span><span class="sxs-lookup"><span data-stu-id="ff41b-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="ff41b-129">Нарисуйте росчерк, отпустите составной путь и объединяйте оставшиеся фигуры.</span><span class="sxs-lookup"><span data-stu-id="ff41b-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="ff41b-130">Цвет внешнего росчерка белый и внутренний значок, как вы хотите.</span><span class="sxs-lookup"><span data-stu-id="ff41b-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![шаг 1](./../media/accessibility-step1.png) | ![шаг 2](./../media/accessibility-step2.png) | ![шаг 3](./../media/accessibility-step3.png)                                           | ![шаг 4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

