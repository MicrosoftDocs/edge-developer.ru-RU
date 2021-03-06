---
description: Эмулировать недостатки зрения в Microsoft Edge DevTools.
title: Эмулировать недостатки зрения в Microsoft Edge DevTools (цветовая слепота)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: eec3c95bac93e600acf1887c8d31cea2173c6aee
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397876"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="c8af0-104">Имитация дефектов зрения</span><span class="sxs-lookup"><span data-stu-id="c8af0-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="c8af0-105">Чтобы лучше удовлетворять потребности пользователей [][ColorblindawarenessMain] с дефицитом цветового зрения \(цветовая слепота\), [Microsoft Edge DevTools][DevtoolsIndex] позволяет имитировать определенные недостатки цветового зрения.</span><span class="sxs-lookup"><span data-stu-id="c8af0-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="c8af0-106">Средство **эмулировать недостатки зрения** имитирует следующие категории.</span><span class="sxs-lookup"><span data-stu-id="c8af0-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="c8af0-107">Дефицит цветового зрения</span><span class="sxs-lookup"><span data-stu-id="c8af0-107">Color vision deficiency</span></span> | <span data-ttu-id="c8af0-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="c8af0-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c8af0-109">Размытое зрение</span><span class="sxs-lookup"><span data-stu-id="c8af0-109">Blurred vision</span></span> | <span data-ttu-id="c8af0-110">Пользователю трудно сосредоточиться на тонкостях.</span><span class="sxs-lookup"><span data-stu-id="c8af0-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="c8af0-111">Протанопия</span><span class="sxs-lookup"><span data-stu-id="c8af0-111">Protanopia</span></span> | <span data-ttu-id="c8af0-112">Пользователь не может воспринимать красный свет.</span><span class="sxs-lookup"><span data-stu-id="c8af0-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="c8af0-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="c8af0-113">Deuteranopia</span></span> | <span data-ttu-id="c8af0-114">Пользователь не может воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="c8af0-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="c8af0-115">Тританопия</span><span class="sxs-lookup"><span data-stu-id="c8af0-115">Tritanopia</span></span> | <span data-ttu-id="c8af0-116">Пользователь не может воспринимать синий свет.</span><span class="sxs-lookup"><span data-stu-id="c8af0-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="c8af0-117">Ахроматопсия</span><span class="sxs-lookup"><span data-stu-id="c8af0-117">Achromatopsia</span></span> | <span data-ttu-id="c8af0-118">Пользователь не может воспринимать любой цвет, который уменьшает весь цвет до серого.</span><span class="sxs-lookup"><span data-stu-id="c8af0-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <a name="navigate-to-the-rendering-tools"></a><span data-ttu-id="c8af0-119">Перейдите к средствам визуализации</span><span class="sxs-lookup"><span data-stu-id="c8af0-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="c8af0-120">Для имитации дефицита зрения, применяемой для вашего веб-продукта, откройте [средства визуализации.][DevtoolsRenderingToolsIndex]</span><span class="sxs-lookup"><span data-stu-id="c8af0-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="c8af0-121">Чтобы открыть средства визуализации, выберите `...` элемент меню на панели инструментов</span><span class="sxs-lookup"><span data-stu-id="c8af0-121">To open the Rendering Tools, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="c8af0-122">Выбор **дополнительных средств**</span><span class="sxs-lookup"><span data-stu-id="c8af0-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="c8af0-123">Выберите **отрисовку**</span><span class="sxs-lookup"><span data-stu-id="c8af0-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств визуализации" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="c8af0-125">Открытие **средств визуализации**</span><span class="sxs-lookup"><span data-stu-id="c8af0-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="c8af0-126">Меню **rendering** отображается в ящике.</span><span class="sxs-lookup"><span data-stu-id="c8af0-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="c8af0-127">Прокрутите вниз `Emulate vision deficiencies` к элементу меню и выберите выпадаемое меню, чтобы отобразить параметры.</span><span class="sxs-lookup"><span data-stu-id="c8af0-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню Эмулировать недостатки зрения в ящике визуализации" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="c8af0-129">Меню **недостатков эмулировать** зрение в **ящике rendering**</span><span class="sxs-lookup"><span data-stu-id="c8af0-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8af0-130">Выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="c8af0-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню "Эмуляция недостатков зрения"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="c8af0-132">Параметры **меню "Подражать недостаткам** зрения"</span><span class="sxs-lookup"><span data-stu-id="c8af0-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8af0-133">В главных окнах отображается моделирование выбранного параметра, примененного к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="c8af0-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Отображение с помощью моделирования **Blurred Vision**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="c8af0-135">Отображение с помощью **моделирования размытого зрения**</span><span class="sxs-lookup"><span data-stu-id="c8af0-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Отображение с помощью моделирования **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="c8af0-137">Отображение с помощью **моделирования Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="c8af0-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a><span data-ttu-id="c8af0-138">Используйте командное меню</span><span class="sxs-lookup"><span data-stu-id="c8af0-138">Use the Command Menu</span></span>  

<span data-ttu-id="c8af0-139">Вы также можете использовать **командное меню для** доступа к различным имитациям.</span><span class="sxs-lookup"><span data-stu-id="c8af0-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="c8af0-140">Выберите `Control` + `Shift` + `P` \(Windows/Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**</span><span class="sxs-lookup"><span data-stu-id="c8af0-140">Select `Control`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="c8af0-142">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="c8af0-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8af0-143">Введите `emulate` , выберите то, что вы хотите имитировать и выбрать `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c8af0-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры моделирования, доступные в командном меню" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="c8af0-145">Различные параметры моделирования, доступные в **командном меню**</span><span class="sxs-lookup"><span data-stu-id="c8af0-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="c8af0-146">Средства **эмулирования** недостатков зрения имитируют приближения того, как человек с каждым недостатком может видеть ваш продукт.</span><span class="sxs-lookup"><span data-stu-id="c8af0-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="c8af0-147">Каждый человек отличается, поэтому недостатки зрения различаются по серьезности от человека к человеку.</span><span class="sxs-lookup"><span data-stu-id="c8af0-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="c8af0-148">Чтобы лучше удовлетворять потребности пользователей, избегайте любых цветовых сочетаний, которые могут быть проблемой.</span><span class="sxs-lookup"><span data-stu-id="c8af0-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="c8af0-149">Средства **эмулировать недостатки зрения** не являются полной оценкой доступности вашего продукта.</span><span class="sxs-lookup"><span data-stu-id="c8af0-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="c8af0-150">Вместо этого средства **эмулировать** недостатки зрения должны дать вам хороший первый шаг, чтобы избежать проблем.</span><span class="sxs-lookup"><span data-stu-id="c8af0-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevToolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Анализ производительности выполнения | Документы Майкрософт"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация цветовой слепой осведомленности"  

[AmfcbMain]: https://www.amfcb.org "Американский фонд цветных слепых (AFCB)"  
