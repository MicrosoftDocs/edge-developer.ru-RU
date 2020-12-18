---
description: Эмулировать недостатки зрения в Microsoft Edge DevTools.
title: Эмуляция недостатков зрения в Microsoft Edge DevTools (дальтонизм)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230826"
---
# <span data-ttu-id="5079d-104">Имитация дефектов зрения</span><span class="sxs-lookup"><span data-stu-id="5079d-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="5079d-105">Для лучшего удовлетворения потребностей пользователей с недостатком цветового зрения [\(color][ColorblindawarenessMain] blindness\), Microsoft Edge [DevTools][DevtoolsIndex] позволяет моделировать определенные недостатки цветового зрения.</span><span class="sxs-lookup"><span data-stu-id="5079d-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="5079d-106">Средство **эмуляции недостатков зрения** имитирует следующие категории.</span><span class="sxs-lookup"><span data-stu-id="5079d-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="5079d-107">Недостаток цветового зрения</span><span class="sxs-lookup"><span data-stu-id="5079d-107">Color vision deficiency</span></span> | <span data-ttu-id="5079d-108">Сведения</span><span class="sxs-lookup"><span data-stu-id="5079d-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="5079d-109">Размытое зрение</span><span class="sxs-lookup"><span data-stu-id="5079d-109">Blurred vision</span></span> | <span data-ttu-id="5079d-110">Пользователю трудно сосредоточиться на подробных сведениях.</span><span class="sxs-lookup"><span data-stu-id="5079d-110">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="5079d-111">Протанопия</span><span class="sxs-lookup"><span data-stu-id="5079d-111">Protanopia</span></span> | <span data-ttu-id="5079d-112">Пользователь не может воспринимать красный свет.</span><span class="sxs-lookup"><span data-stu-id="5079d-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="5079d-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="5079d-113">Deuteranopia</span></span> | <span data-ttu-id="5079d-114">Пользователь не может воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="5079d-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="5079d-115">Тританопия</span><span class="sxs-lookup"><span data-stu-id="5079d-115">Tritanopia</span></span> | <span data-ttu-id="5079d-116">Пользователь не может воспринимать синий свет.</span><span class="sxs-lookup"><span data-stu-id="5079d-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="5079d-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="5079d-117">Achromatopsia</span></span> | <span data-ttu-id="5079d-118">Пользователь не может воспринимать какой-либо цвет, который уменьшает весь цвет до оттенка серого.</span><span class="sxs-lookup"><span data-stu-id="5079d-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="5079d-119">Переход к средствам отрисовки</span><span class="sxs-lookup"><span data-stu-id="5079d-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="5079d-120">Чтобы смоделировать недостаток зрения, применяемый к веб-продукту, откройте [инструменты отрисовки.][DevtoolsRenderingToolsIndex]</span><span class="sxs-lookup"><span data-stu-id="5079d-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="5079d-121">Чтобы открыть инструменты отрисовки, выберите пункт `...` меню на панели инструментов</span><span class="sxs-lookup"><span data-stu-id="5079d-121">To open the Rendering Tools, by choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="5079d-122">Выбрать</span><span class="sxs-lookup"><span data-stu-id="5079d-122">Choose</span></span> `More tools`  
1.  <span data-ttu-id="5079d-123">Выбрать</span><span class="sxs-lookup"><span data-stu-id="5079d-123">Choose</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств отрисовки" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="5079d-125">Открытие средств **отрисовки**</span><span class="sxs-lookup"><span data-stu-id="5079d-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="5079d-126">В **этом ящике** появится меню "Отрисовка".</span><span class="sxs-lookup"><span data-stu-id="5079d-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="5079d-127">Прокрутите вниз до `Emulate vision deficiencies` пункта меню и выберите его, чтобы отобразить параметры.</span><span class="sxs-lookup"><span data-stu-id="5079d-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню эмуляции недостатков зрения в отрисовке" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="5079d-129">Меню **"Эмуляция недостатков зрения"** в **отрисовке**</span><span class="sxs-lookup"><span data-stu-id="5079d-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5079d-130">Выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="5079d-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню эмуляции недостатков зрения" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="5079d-132">Параметры **меню "Эмуляция недостатков зрения"**</span><span class="sxs-lookup"><span data-stu-id="5079d-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5079d-133">В главных окнах отображается имитация выбранного параметра, примененного к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="5079d-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Отображение с помощью имитации **Размытое зрение**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="5079d-135">Отображение с помощью **имитации размытого** зрения</span><span class="sxs-lookup"><span data-stu-id="5079d-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Отображение с помощью имитации **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="5079d-137">Отображение с помощью **имитации Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="5079d-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="5079d-138">Использование меню команд</span><span class="sxs-lookup"><span data-stu-id="5079d-138">Use the Command Menu</span></span>  

<span data-ttu-id="5079d-139">Вы также можете использовать меню **команд для** доступа к различным имитациям.</span><span class="sxs-lookup"><span data-stu-id="5079d-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="5079d-140">Выберите `Control` + `Shift` + `P` \(Windows\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="5079d-140">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="5079d-142">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="5079d-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5079d-143">Введите `emulate` , выберите то, что нужно смоделировать, и `Enter` выберите.</span><span class="sxs-lookup"><span data-stu-id="5079d-143">Type `emulate`, choose what you want to simulate and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры имитации, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="5079d-145">Различные параметры имитации, доступные в меню **команд**</span><span class="sxs-lookup"><span data-stu-id="5079d-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="5079d-146">Средства **эмуляции недостатков зрения** имитируют приближение того, как человек с каждым недостатком может видеть ваш продукт.</span><span class="sxs-lookup"><span data-stu-id="5079d-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="5079d-147">Каждый человек разный, поэтому недостатки зрения различаются по степени серьезности от человека к человеку.</span><span class="sxs-lookup"><span data-stu-id="5079d-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="5079d-148">Чтобы лучше удовлетворить потребности пользователей, избегайте любых сочетаний цветов, которые могут быть проблемой.</span><span class="sxs-lookup"><span data-stu-id="5079d-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="5079d-149">Средства **эмуляции недостатков зрения** не являются полной оценкой доступности вашего продукта.</span><span class="sxs-lookup"><span data-stu-id="5079d-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="5079d-150">Вместо этого средства **эмуляции** недостатков зрения должны дать вам хороший первый шаг, чтобы избежать проблем.</span><span class="sxs-lookup"><span data-stu-id="5079d-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Анализ производительности в времени выполнения | Документы Майкрософт"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация по информированию о незрячих цветах"  

[AmfcbMain]: https://www.amfcb.org "American Foundation для дальтоник (AFCB)"  

