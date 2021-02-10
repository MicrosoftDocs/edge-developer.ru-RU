---
description: Теперь в качестве средства "Новые возможности" можно использовать редактор визуальных шрифтов в области стилей, средства отладки CSS Flexbox и другие возможности.
title: Новые возможности DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0a8a5e69281ced9421733059b554bd8cb997c7cd
ms.sourcegitcommit: 085046a5885c68243b763aaf6809fea43452403a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313778"
---
# <span data-ttu-id="5d69d-104">Новые возможности DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="5d69d-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="5d69d-105">Новые возможности теперь — добро пожаловать</span><span class="sxs-lookup"><span data-stu-id="5d69d-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-106">Новое **средство "Что нового"** в Microsoft Edge DevTools теперь имеет новый внешний вид и новое имя:  **Welcome**.</span><span class="sxs-lookup"><span data-stu-id="5d69d-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="5d69d-107">В **средстве** приветствия по-прежнему отображаются последние новости и обновления DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d69d-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="5d69d-108">Теперь он также содержит ссылки на документацию Microsoft Edge DevTools, способы отправки отзывов и другие.</span><span class="sxs-lookup"><span data-stu-id="5d69d-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="5d69d-109">Чтобы **отобразить** средство приветствия после каждого обновления Microsoft Edge, после каждого обновления под заголовком выберите его рядом с вкладками **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="5d69d-110">Чтобы закрыть средство **приветствия,** выберите **X** в правой части заголовка вкладки.</span><span class="sxs-lookup"><span data-stu-id="5d69d-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="5d69d-111">Если вы предпочитаете исходное средство **"Что** нового", перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и удалите его рядом с вкладками "Включить  >  \*\*\*\* **приветствие".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Выделено средство приветствия" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="5d69d-113">Выделено **средство** приветствия</span><span class="sxs-lookup"><span data-stu-id="5d69d-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-114">Редактор визуальных шрифтов в области стилей</span><span class="sxs-lookup"><span data-stu-id="5d69d-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-115">При работе со шрифтами в CSS используйте новый визуальный редактор [шрифтов.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="5d69d-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="5d69d-116">Можно определить откатные шрифты и использовать ползунки для определения веса, размера, высоты строки и интервалов шрифта.</span><span class="sxs-lookup"><span data-stu-id="5d69d-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="5d69d-117">Редактор **шрифтов** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5d69d-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="5d69d-118">Переключение между единицами для разных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="5d69d-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="5d69d-119">Переключение между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="5d69d-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="5d69d-120">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="5d69d-120">Convert units</span></span>  
*   <span data-ttu-id="5d69d-121">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="5d69d-122">Чтобы включить этот эксперимент, перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и выберите в области стилей новый редактор шрифтов рядом с параметром "Включить новые средства  >  \*\*\*\* **редактора шрифтов".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="5d69d-123">Для получения дополнительных сведений перейдите к редактированию стилей и параметров шрифтов CSS в области стилей [в DevTools.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="5d69d-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="5d69d-124">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1093229.][CR1093229]</span><span class="sxs-lookup"><span data-stu-id="5d69d-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Редактор визуальных шрифтов выделен в области стилей" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="5d69d-126">Редактор **визуальных шрифтов** выделен в **области** стилей</span><span class="sxs-lookup"><span data-stu-id="5d69d-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-127">Средства отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="5d69d-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="5d69d-128">Функции отладки Flexbox находятся в активной разработке.</span><span class="sxs-lookup"><span data-stu-id="5d69d-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="5d69d-129">Чтобы включить эксперимент для следующих двух [][DevtoolsCustomizeIndexSettings]функций, перейдите к "Экспериментам параметров" и выберите этот параметр рядом с параметром "Включить новые функции отладки  >  \*\*\*\* **CSS Flexbox".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="5d69d-130">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1136394][CR1136394] и [1139949.][CR1139949]</span><span class="sxs-lookup"><span data-stu-id="5d69d-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <span data-ttu-id="5d69d-131">Новый значок Flexbox (flex) помогает идентифицировать и отображать гибкие контейнеры</span><span class="sxs-lookup"><span data-stu-id="5d69d-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-132">В **средстве Elements** новый значок Flexbox (flex) помогает идентифицировать контейнеры Flexbox в коде.</span><span class="sxs-lookup"><span data-stu-id="5d69d-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="5d69d-133">Выберите значок Flexbox \(flex\), чтобы включить или отключить эффект наложения, который описывает контейнер Flexbox.</span><span class="sxs-lookup"><span data-stu-id="5d69d-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="5d69d-134">Вы можете настроить цвет наложения в \*\*\*\* области макета, которая расположена рядом со стилями **и** **вычислениями.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5d69d-135">Чтобы включить и отключить эффект наложения, который описывает контейнер Flexbox, выберите значок Flexbox \( `flex` \).</span><span class="sxs-lookup"><span data-stu-id="5d69d-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5d69d-136">Вы можете настроить цвет наложения в \*\*\*\* области макета рядом со стилями **и** **вычислениями.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Значок Flexbox (flex) и выделенная веб-страницу" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="5d69d-138">Значок **Flexbox** \( `flex` \) и выделенная веб-страницу</span><span class="sxs-lookup"><span data-stu-id="5d69d-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Наложения Flexbox, выделенные в области макета" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="5d69d-140">Наложения **Flexbox,** выделенные в области **макета**</span><span class="sxs-lookup"><span data-stu-id="5d69d-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="5d69d-141">Отображение значков выравнивания и линий сетки при изменении макетов Flexbox с помощью свойств CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-141">Display alignment icons and gridlines when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-142">При редактировании CSS для макета Flexbox автозаполнения \*\*\*\* CSS в области стилей теперь отображают полезные значки рядом с соответствующими свойствами Flexbox.</span><span class="sxs-lookup"><span data-stu-id="5d69d-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="5d69d-143">Чтобы попробовать эту новую функцию, откройте средство **"Элементы"** и выберите гибкий контейнер.</span><span class="sxs-lookup"><span data-stu-id="5d69d-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="5d69d-144">Затем добавьте или измените свойство этого контейнера в **области** стилей.</span><span class="sxs-lookup"><span data-stu-id="5d69d-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5d69d-145">Теперь в меню автозаполнения отображаются значки, которые указывают на влияние таких свойств `align-content` выравнивания, как и `align-items` .</span><span class="sxs-lookup"><span data-stu-id="5d69d-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5d69d-146">Кроме того, в DevTools теперь отображается направляющая строка, которая поможет вам лучше просмотреть `align-items` свойство CSS.</span><span class="sxs-lookup"><span data-stu-id="5d69d-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="5d69d-147">Также `gap` поддерживается свойство CSS.</span><span class="sxs-lookup"><span data-stu-id="5d69d-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="5d69d-148">На следующем рисунке за установлено свойство CSS и отображается шаблон ветвления для `gap` `gap: 12px;` каждого пробела.</span><span class="sxs-lookup"><span data-stu-id="5d69d-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Меню автозаполнения, выделенное для свойств CSS, которые начинаются с выравнивания" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="5d69d-150">Меню автозаполнеия, выделенное для свойств CSS, которые начинаются с</span><span class="sxs-lookup"><span data-stu-id="5d69d-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Разрыв Flexbox в выделенной свойствах CSS и веб-странице" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="5d69d-152">Flexbox `gap` в свойствах CSS и выделенной веб-странице</span><span class="sxs-lookup"><span data-stu-id="5d69d-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5d69d-153">Быстрое добавление инструментов с помощью кнопки "Дополнительные средства"</span><span class="sxs-lookup"><span data-stu-id="5d69d-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-154">Теперь у вас есть новый способ открыть дополнительные средства в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d69d-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="5d69d-155">После того как вы \*\*\*\* включите этот эксперимент, значок "Дополнительные инструменты" будет отображаться в качестве знака плюса `+` () справа от главной панели.</span><span class="sxs-lookup"><span data-stu-id="5d69d-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="5d69d-156">Чтобы отобразить список других инструментов, добавляемого на главную панель, выберите значок "Дополнительные **средства"** `+` (\).</span><span class="sxs-lookup"><span data-stu-id="5d69d-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="5d69d-157">Чтобы включить этот эксперимент, [][DevtoolsCustomizeIndexSettings]перейдите к пункту "Эксперименты с настройками" и выберите этот пункт рядом с меню вкладок "Включить+ кнопка", чтобы открыть  >  \*\*\*\* **дополнительные инструменты.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Дополнительные средства, выделенные в DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="5d69d-159">**Дополнительные средства,** выделенные в DevTools</span><span class="sxs-lookup"><span data-stu-id="5d69d-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-160">Теперь вспомогательные технологии объявляют положение и количество предложений CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="5d69d-161">При редактировании CSS вы получаете в качестве простого окна функции.</span><span class="sxs-lookup"><span data-stu-id="5d69d-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="5d69d-162">Эта функция не была доступна пользователям вспомогательных технологий, так как она объявлена в Microsoft Edge версии 89.</span><span class="sxs-lookup"><span data-stu-id="5d69d-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="5d69d-163">Пользователь вспомогательных технологий теперь может перемещаться по предложениям CSS в **области** стилей.</span><span class="sxs-lookup"><span data-stu-id="5d69d-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="5d69d-164">В Microsoft Edge версии 88 и более ранних версиях технология поддержки, объявленная пользователем, перебрала список предложений при редактировании CSS в области `Suggestion` стилей. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5d69d-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="5d69d-165">В Microsoft Edge версии 89 пользователь вспомогательных технологий теперь слышит положение и количество текущих предложений.</span><span class="sxs-lookup"><span data-stu-id="5d69d-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="5d69d-166">Каждое предложение будет объявлено по мере того, как пользователь переходит по списку предложений, например предложений 3 из 5.</span><span class="sxs-lookup"><span data-stu-id="5d69d-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="5d69d-167">Чтобы узнать больше о написании CSS в DevTools, перейдите к [change CSS][DevtoolsCssReferenceChangeCss].</span><span class="sxs-lookup"><span data-stu-id="5d69d-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="5d69d-168">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1157329.][CR1157329]</span><span class="sxs-lookup"><span data-stu-id="5d69d-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="5d69d-169">Чтобы просмотреть видео, которое отображает и читает вслух несколько предложений, включив этот эксперимент, перейдите к voiceover, объявляя о параметрах [devtools](https://youtu.be/9TcUpleEwwA) на YouTube.</span><span class="sxs-lookup"><span data-stu-id="5d69d-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Предложение, выделено в области стилей" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="5d69d-171">Список, `suggestion` выделенный в области **стилей**</span><span class="sxs-lookup"><span data-stu-id="5d69d-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-172">Эмуляция Surface Duo и папки Samsung</span><span class="sxs-lookup"><span data-stu-id="5d69d-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="5d69d-173">Проверьте внешний вид веб-сайта или приложения на следующих устройствах в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d69d-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="5d69d-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d69d-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="5d69d-175">Папка "Сумяно"</span><span class="sxs-lookup"><span data-stu-id="5d69d-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="5d69d-176">**Включив** функции экспериментальной веб-платформы, вы получите доступ к новой функции [CSS-экрана][DualScreenWebCssMediaSpanning] и [API JavaScript для getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="5d69d-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="5d69d-177">Перейдите к функциям экспериментальной веб-платформы и перейдите к флагу и перейдите `edge://flags` **к ней.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="5d69d-178">Чтобы улучшить веб-сайт или приложение для двухэкранных и папок устройств, используйте следующие функции при [эмуляциях устройства.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="5d69d-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="5d69d-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]— это когда ваш веб-сайт \(или приложение\) отображается на обоих экранах.</span><span class="sxs-lookup"><span data-stu-id="5d69d-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="5d69d-180">[Отрисовка пространства][DualScreenIntroductionHowToWorkWithSeam]между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="5d69d-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="5d69d-181">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1054281.][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="5d69d-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Эмуляция двойного экрана" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="5d69d-183">Эмуляция двойного экрана</span><span class="sxs-lookup"><span data-stu-id="5d69d-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-184">Инструменты разработчика Microsoft Edge для Visual Studio code версии 1.1.2</span><span class="sxs-lookup"><span data-stu-id="5d69d-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="5d69d-185">В [Microsoft Edge Developer Tools для Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.2 для Microsoft Visual Studio Code были внесены следующие изменения по сравнению с предыдущим выпуском.</span><span class="sxs-lookup"><span data-stu-id="5d69d-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="5d69d-186">Microsoft Visual Studio Код автоматически обновляет расширения.</span><span class="sxs-lookup"><span data-stu-id="5d69d-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="5d69d-187">Чтобы вручную обновить расширение до версии 1.1.2, перейдите к обновлению [расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="5d69d-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="5d69d-188">Добавлена **кнопка закрытия экземпляра** для каждого элемента в целевом списке \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="5d69d-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="5d69d-189">Версия [Microsoft Edge DevTools][DevtoolsMain] с 84.0.522.63 до [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="5d69d-189">Bumped [Microsoft Edge DevTools][DevtoolsMain] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="5d69d-190">Включенный [отладок для Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] в качестве зависимости \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="5d69d-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="5d69d-191">Реализован параметр параметров для изменения тем расширения \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="5d69d-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="5d69d-192">Вы можете файлировать проблемы и вносить вклад в расширение в репозитарии [GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]</span><span class="sxs-lookup"><span data-stu-id="5d69d-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <span data-ttu-id="5d69d-193">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="5d69d-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="5d69d-194">Снимок экрана узла захвата за пределами области просмотра</span><span class="sxs-lookup"><span data-stu-id="5d69d-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="5d69d-195">В Microsoft Edge версии 89 снимки экрана узла более точны, захватывая полный узел, даже если содержимое узла не отображается в окнах просмотра.</span><span class="sxs-lookup"><span data-stu-id="5d69d-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="5d69d-196">В **средстве "Элементы"** наведите курсор на элемент, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите снимок экрана **узла захвата.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="5d69d-197">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1003629.][CR1003629]</span><span class="sxs-lookup"><span data-stu-id="5d69d-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Снимок экрана узла захвата, выделенного в контекстное меню в средстве "Элементы"" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="5d69d-199">**Снимок экрана узла** захвата, выделенного в контекстное меню в **средстве "Элементы"**</span><span class="sxs-lookup"><span data-stu-id="5d69d-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <span data-ttu-id="5d69d-200">Обновления средства "Элементы"</span><span class="sxs-lookup"><span data-stu-id="5d69d-200">Elements tool updates</span></span>  

#### <span data-ttu-id="5d69d-201">Поддержка принудительного принудительного состояния CSS :target</span><span class="sxs-lookup"><span data-stu-id="5d69d-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="5d69d-202">Теперь можно использовать DevTools для принудительного [использования псевдокласса CSS :target.][MdnDocsWebCssTarget]</span><span class="sxs-lookup"><span data-stu-id="5d69d-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="5d69d-203">Псевдокласс инициирует, когда уникальный элемент `:target` \(целевой элемент\) имеет фрагмент `id` URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5d69d-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="5d69d-204">Например, `http://www.example.com/index.html#section1` URL-адрес инициирует `:target` псевдокласс для HTML-элемента с `id="section1"` .</span><span class="sxs-lookup"><span data-stu-id="5d69d-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="5d69d-205">Чтобы попробовать демонстрацию с выделенной частью 1, перейдите к [разделу CSS :target demo.][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]</span><span class="sxs-lookup"><span data-stu-id="5d69d-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="5d69d-206">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1156628.][CR1156628]</span><span class="sxs-lookup"><span data-stu-id="5d69d-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Выделенная веб-страницу без принудительной CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="5d69d-208">Выделенная веб-страницу без принудительной CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="5d69d-210">Принудительный CSS и выделенная веб-страницу</span><span class="sxs-lookup"><span data-stu-id="5d69d-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="5d69d-211">Использование дублирующихся элементов для копирования элементов</span><span class="sxs-lookup"><span data-stu-id="5d69d-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="5d69d-212">Используйте новый ярлык **дубликата** элемента для клонирования элемента.</span><span class="sxs-lookup"><span data-stu-id="5d69d-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="5d69d-213">В **средстве "Элементы"** наведите курсор на элемент, откройте контекстное меню \(щелкните правой кнопкой мыши\), выберите элемент **Duplicate.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="5d69d-214">Под выбранным элементом создается новый элемент.</span><span class="sxs-lookup"><span data-stu-id="5d69d-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="5d69d-215">Чтобы скопировать элемент с помощью сочетания клавиш, выберите `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) или `Shift` + `Option` + `Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="5d69d-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="5d69d-216">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1150797.][CR1150797]</span><span class="sxs-lookup"><span data-stu-id="5d69d-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Элемент Duplicate выделен в контекстное меню элемента в средстве Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="5d69d-218">Элемент **Duplicate выделен** в контекстное меню элемента в **средстве Elements**</span><span class="sxs-lookup"><span data-stu-id="5d69d-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-219">Палитра для настраиваемого свойства CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="5d69d-220">Теперь **в** области стилей отображаются палитры для настраиваемого свойства CSS.</span><span class="sxs-lookup"><span data-stu-id="5d69d-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="5d69d-221">Чтобы перебирать форматы RGBA, HSLA и Hex значения цвета, удерживайте и выберите `Shift` палитру.</span><span class="sxs-lookup"><span data-stu-id="5d69d-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="5d69d-222">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1147016.][CR1147016]</span><span class="sxs-lookup"><span data-stu-id="5d69d-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Палитра для настраиваемого свойства CSS" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="5d69d-224">Палитра для настраиваемого свойства CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-225">Копирование классов и свойств CSS</span><span class="sxs-lookup"><span data-stu-id="5d69d-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="5d69d-226">Теперь можно быстрее копировать свойства CSS с помощью нескольких новых параметров в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="5d69d-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="5d69d-227">В **средстве "Элементы"** выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="5d69d-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="5d69d-228">Чтобы скопировать значение, \*\*\*\* в области стилей наведите курсор на класс CSS или свойство CSS, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите параметр копирования.</span><span class="sxs-lookup"><span data-stu-id="5d69d-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5d69d-229">Параметры копирования для класса CSS.</span><span class="sxs-lookup"><span data-stu-id="5d69d-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="5d69d-230">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d69d-230">Option</span></span> | <span data-ttu-id="5d69d-231">Сведения</span><span class="sxs-lookup"><span data-stu-id="5d69d-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="5d69d-232">Выбор копии</span><span class="sxs-lookup"><span data-stu-id="5d69d-232">Copy selector</span></span>** | <span data-ttu-id="5d69d-233">Скопируйте имя текущего селектора.</span><span class="sxs-lookup"><span data-stu-id="5d69d-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="5d69d-234">Правило копирования</span><span class="sxs-lookup"><span data-stu-id="5d69d-234">Copy rule</span></span>** | <span data-ttu-id="5d69d-235">Скопируйте правило текущего селектора.</span><span class="sxs-lookup"><span data-stu-id="5d69d-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="5d69d-236">Копирование всех объявлений</span><span class="sxs-lookup"><span data-stu-id="5d69d-236">Copy all declarations</span></span>** | <span data-ttu-id="5d69d-237">Скопируйте все объявления в рамках текущего правила, включая недостоверные и префиксные свойства.</span><span class="sxs-lookup"><span data-stu-id="5d69d-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5d69d-238">Параметры копирования для свойства CSS.</span><span class="sxs-lookup"><span data-stu-id="5d69d-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="5d69d-239">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d69d-239">Option</span></span> | <span data-ttu-id="5d69d-240">Сведения</span><span class="sxs-lookup"><span data-stu-id="5d69d-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="5d69d-241">Объявление копирования</span><span class="sxs-lookup"><span data-stu-id="5d69d-241">Copy declaration</span></span>** | <span data-ttu-id="5d69d-242">Скопируйте объявление текущей строки.</span><span class="sxs-lookup"><span data-stu-id="5d69d-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="5d69d-243">Свойство Copy</span><span class="sxs-lookup"><span data-stu-id="5d69d-243">Copy property</span></span>** | <span data-ttu-id="5d69d-244">Скопируйте свойство текущей строки.</span><span class="sxs-lookup"><span data-stu-id="5d69d-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="5d69d-245">Значение копирования</span><span class="sxs-lookup"><span data-stu-id="5d69d-245">Copy value</span></span>** | <span data-ttu-id="5d69d-246">Скопируйте значение текущей строки.</span><span class="sxs-lookup"><span data-stu-id="5d69d-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Копирование параметров класса CSS в контекстное меню" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="5d69d-248">Копирование параметров класса CSS в контекстное меню</span><span class="sxs-lookup"><span data-stu-id="5d69d-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Копирование параметров свойства CSS в контекстное меню" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="5d69d-250">Копирование параметров свойства CSS в контекстное меню</span><span class="sxs-lookup"><span data-stu-id="5d69d-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5d69d-251">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1152391.][CR1152391]</span><span class="sxs-lookup"><span data-stu-id="5d69d-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <span data-ttu-id="5d69d-252">Обновления файлов cookie</span><span class="sxs-lookup"><span data-stu-id="5d69d-252">Cookies updates</span></span>  

#### <span data-ttu-id="5d69d-253">Новый параметр для отображения файлов cookie, расшифровав URL-адреса</span><span class="sxs-lookup"><span data-stu-id="5d69d-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="5d69d-254">Теперь можно отобразить значение раскодирования URL-файлов cookie в области **файлов cookie.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="5d69d-255">Чтобы отобразить расшифровки файлов cookie, перейдите в области "Файлы cookie приложения", выберите любой файл cookie в списке и выберите следующий контрольный список, чтобы отобразить раскодирование \*\*\*\*  >  \*\*\*\* **URL-адреса.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="5d69d-256">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [997625.][CR997625]</span><span class="sxs-lookup"><span data-stu-id="5d69d-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Возможность отображения файлов cookie, расшифровав URL-адреса" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="5d69d-258">Возможность отображения файлов cookie, расшифровав URL-адреса</span><span class="sxs-lookup"><span data-stu-id="5d69d-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-259">Фильтрация и очистка видимых файлов cookie</span><span class="sxs-lookup"><span data-stu-id="5d69d-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="5d69d-260">В Microsoft Edge версии 88 \*\*\*\* или более ранней версии средство application предоставлялось только для очистки всех файлов cookie с помощью кнопки **"Очистить все файлы cookie".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="5d69d-261">В Microsoft Edge версии 89 теперь можно выбрать "Очистить отфильтрованные файлы **cookie",** чтобы удалить только отфильтрованные файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="5d69d-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="5d69d-262">Чтобы отфильтровать файлы cookie, перейдите к **файлу**  >  **cookie приложения**и введите текстовое сообщение **фильтра.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="5d69d-263">Чтобы удалить отображаемые файлы cookie, выберите кнопку **"Очистить фильтруйте файлы cookie".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="5d69d-264">Чтобы отобразить все остальные файлы cookie, очищает текст фильтра.</span><span class="sxs-lookup"><span data-stu-id="5d69d-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="5d69d-265">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [978059.][CR978059]</span><span class="sxs-lookup"><span data-stu-id="5d69d-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Очистка только видимых файлов cookie" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="5d69d-267">Очистка только видимых файлов cookie</span><span class="sxs-lookup"><span data-stu-id="5d69d-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-268">Новый параметр для очистки сторонних файлов cookie в области хранилища</span><span class="sxs-lookup"><span data-stu-id="5d69d-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="5d69d-269">По умолчанию DevTools очищает только файлы cookie от первого разработчика.</span><span class="sxs-lookup"><span data-stu-id="5d69d-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="5d69d-270">Чтобы очистить данные веб-сайта и только \*\*\*\* сторонние файлы cookie, перейдите в хранилище приложений и выберите  >  \*\*\*\* **"Очистить данные сайта".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="5d69d-271">Чтобы очистить данные веб-сайта и все файлы cookie, перейдите в **хранилище**  >  **приложений.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="5d69d-272">Включите сторонние \*\*\*\* файлы cookie и выберите "Очистить **данные сайта".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="5d69d-273">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1012337.][CR1012337]</span><span class="sxs-lookup"><span data-stu-id="5d69d-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Возможность очистки сторонних файлов cookie" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="5d69d-275">Возможность очистки сторонних файлов cookie</span><span class="sxs-lookup"><span data-stu-id="5d69d-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <span data-ttu-id="5d69d-276">Обновления сетевых инструментов</span><span class="sxs-lookup"><span data-stu-id="5d69d-276">Network tool updates</span></span>  

#### <span data-ttu-id="5d69d-277">Параметр сетевого журнала "Сохранить запись"</span><span class="sxs-lookup"><span data-stu-id="5d69d-277">Persist Record network log setting</span></span>  

<span data-ttu-id="5d69d-278">В Microsoft Edge версии 88 или более ранней версии DevTools сбрасывает параметр сетевого журнала записи при обновлении веб-страницы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5d69d-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="5d69d-279">В Microsoft Edge версии 89 DevTools теперь сохраняет параметр **сетевого** журнала записи.</span><span class="sxs-lookup"><span data-stu-id="5d69d-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="5d69d-280">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1122580.][CR1122580]</span><span class="sxs-lookup"><span data-stu-id="5d69d-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Запись сетевого журнала" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="5d69d-282">Запись сетевого журнала</span><span class="sxs-lookup"><span data-stu-id="5d69d-282">Record network log</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-283">Сетевой параметр теперь не является параметром регулирования</span><span class="sxs-lookup"><span data-stu-id="5d69d-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="5d69d-284">Параметр сетевой эмуляции **Online** теперь переименован в **"Без регулирования".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="5d69d-285">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1028078.][CR1028078]</span><span class="sxs-lookup"><span data-stu-id="5d69d-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Без параметра регулирования" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="5d69d-287">**Без параметра регулирования**</span><span class="sxs-lookup"><span data-stu-id="5d69d-287">**No throttling** option</span></span>  
:::image-end:::  

### <span data-ttu-id="5d69d-288">Новые параметры копирования в средстве "Консоль", "Источники" и области стилей</span><span class="sxs-lookup"><span data-stu-id="5d69d-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <span data-ttu-id="5d69d-289">Копирование объекта в средстве "Консоль" и "Источники"</span><span class="sxs-lookup"><span data-stu-id="5d69d-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="5d69d-290">Теперь можно копировать значения объектов в **средствах консоли** и **источников.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="5d69d-291">Возможность копирования значений объектов полезна при работе с большими объектами.</span><span class="sxs-lookup"><span data-stu-id="5d69d-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="5d69d-292">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1148353][CR1148353] и [1149859.][CR1149859]</span><span class="sxs-lookup"><span data-stu-id="5d69d-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5d69d-293">В **средстве консоли** наведите курсор на объект, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите **"Копировать объект".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5d69d-294">В средстве **источников** на точке останова наведите \*\*\*\* курсор на объект, во всплывающее окно "Объект" выделите объект, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите "Копировать **объект".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Копирование объекта в консоли" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="5d69d-296">Копирование объекта **в** консоли</span><span class="sxs-lookup"><span data-stu-id="5d69d-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Копирование объекта в источниках" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="5d69d-298">Копирование объекта в **источниках**</span><span class="sxs-lookup"><span data-stu-id="5d69d-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="5d69d-299">Копирование имени файла в области "Источники" и "Стили"</span><span class="sxs-lookup"><span data-stu-id="5d69d-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="5d69d-300">Теперь можно скопировать имя файла с помощью контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="5d69d-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="5d69d-301">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к вопросу [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="5d69d-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5d69d-302">В **средстве "Источники"** наведите курсор на имя файла, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Копировать имя файла".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5d69d-303">В области **"Элементы>** \*\*\*\* стили" наведите курсор на имя файла, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите "Копировать **имя файла".**</span><span class="sxs-lookup"><span data-stu-id="5d69d-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Копирование имени файла в источниках" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="5d69d-305">Копирование имени файла в **источниках**</span><span class="sxs-lookup"><span data-stu-id="5d69d-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Копирование имени файла в области стилей" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="5d69d-307">Копирование имени файла в **области стилей**</span><span class="sxs-lookup"><span data-stu-id="5d69d-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="5d69d-308">Обновления сведений о фрейме</span><span class="sxs-lookup"><span data-stu-id="5d69d-308">Updates to Frame details</span></span>  

#### <span data-ttu-id="5d69d-309">Сведения о рабочих службах в сведениях о фрейме</span><span class="sxs-lookup"><span data-stu-id="5d69d-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="5d69d-310">DevTools теперь перечисляет выделенный рабочий кадр службы в родительском кадре.</span><span class="sxs-lookup"><span data-stu-id="5d69d-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="5d69d-311">На следующем рисунке отображаются сведения о рабочих службах.</span><span class="sxs-lookup"><span data-stu-id="5d69d-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="5d69d-312">Чтобы отобразить сведения о рабочих службах, перейдите к **сотрудникам**службы кадров приложений, а затем  >  \*\*\*\*  >  `top`  >  \*\*\*\* выберите сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="5d69d-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="5d69d-313">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1122507.][CR1122507]</span><span class="sxs-lookup"><span data-stu-id="5d69d-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Сведения о рабочих службах в сведениях о кадрах" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="5d69d-315">**Сведения о рабочих** службах в **сведениях о кадрах**</span><span class="sxs-lookup"><span data-stu-id="5d69d-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-316">Измерение сведений о памяти в сведениях о кадрах</span><span class="sxs-lookup"><span data-stu-id="5d69d-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="5d69d-317">Теперь `performance.measureMemory()` состояние API отображается в разделе доступности **API.**</span><span class="sxs-lookup"><span data-stu-id="5d69d-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="5d69d-318">Новый `performance.measureMemory()` API оценивает использование памяти всей веб-страницей.</span><span class="sxs-lookup"><span data-stu-id="5d69d-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="5d69d-319">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139899.][CR1139899]</span><span class="sxs-lookup"><span data-stu-id="5d69d-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Измерение памяти" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="5d69d-321">Измерение памяти</span><span class="sxs-lookup"><span data-stu-id="5d69d-321">Measure Memory</span></span>  
:::image-end:::  

### <span data-ttu-id="5d69d-322">Отброшенные кадры в средстве "Производительность"</span><span class="sxs-lookup"><span data-stu-id="5d69d-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="5d69d-323">При [анализе производительности нагрузки в средстве "Производительность"][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]раздел **"Кадры"** пометит отброшенные кадры красным цветом.</span><span class="sxs-lookup"><span data-stu-id="5d69d-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="5d69d-324">Чтобы отобразить частоту кадров, наведите курсор на отброшенный кадр.</span><span class="sxs-lookup"><span data-stu-id="5d69d-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="5d69d-325">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1075865.][CR1075865]</span><span class="sxs-lookup"><span data-stu-id="5d69d-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Отброшенные кадры" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="5d69d-327">Отброшенные кадры</span><span class="sxs-lookup"><span data-stu-id="5d69d-327">Dropped frames</span></span>  
:::image-end:::  

#### <span data-ttu-id="5d69d-328">Новое вычисление цветовой контрастности — расширенный алгоритм perceptual Contrast Algorithm (APCA)</span><span class="sxs-lookup"><span data-stu-id="5d69d-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="5d69d-329">Расширенный [алгоритм perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] заменяет коэффициент контрастности рекомендаций [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] в [палитре цветов.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]</span><span class="sxs-lookup"><span data-stu-id="5d69d-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="5d69d-330">APCA — это новый способ вычисления контрастности.</span><span class="sxs-lookup"><span data-stu-id="5d69d-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="5d69d-331">Он основан на современных исследованиях цветового восприятия.</span><span class="sxs-lookup"><span data-stu-id="5d69d-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="5d69d-332">По сравнению с рекомендациями AA/AAA, APCA более зависит от контекста.</span><span class="sxs-lookup"><span data-stu-id="5d69d-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="5d69d-333">Контраст вычисляется на основе следующих пространственных свойств текста, цвета и контекста.</span><span class="sxs-lookup"><span data-stu-id="5d69d-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="5d69d-334">Пространственные свойства текста, которые включают вес и размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="5d69d-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="5d69d-335">Пространственные свойства цвета, которые включают воспринимаемую контрастность между текстом и фоном.</span><span class="sxs-lookup"><span data-stu-id="5d69d-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="5d69d-336">Пространственные свойства контекста, которые включают внешнее освещение, окружение и предназначение.</span><span class="sxs-lookup"><span data-stu-id="5d69d-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="5d69d-337">Чтобы включить этот эксперимент, [][DevtoolsCustomizeIndexSettings]перейдите к "Экспериментам с настройками" и выберите его рядом с параметром  >  \*\*\*\* Enable **new Advanced Perceptual Contrast Algorithm (APCA),** заменив предыдущее соотношение контрастности и рекомендации AA/AAA.</span><span class="sxs-lookup"><span data-stu-id="5d69d-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="5d69d-338">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1121900.][CR1121900]</span><span class="sxs-lookup"><span data-stu-id="5d69d-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA в палитре" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="5d69d-340">APCA в палитре</span><span class="sxs-lookup"><span data-stu-id="5d69d-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <span data-ttu-id="5d69d-341">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="5d69d-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="5d69d-342">Если вы используете Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d69d-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="5d69d-343">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="5d69d-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="5d69d-344">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5d69d-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Новые возможности DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Просмотр коэффициента контрастности текстового элемента в справочнике по специальным | Документы Майкрософт"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Change CSS - CSS reference | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Тестирование на устройствах с двумя и двумя экранами — эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного окна : эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Запись производительности загрузки — справочные данные по анализу производительности | Документы Майкрософт"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Изменение стилей и параметров шрифтов CSS в области стилей в devTools | Документы Майкрософт"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Обзор средств разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для двухэкранного обнаружения | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Раздел 1. CSS :target demo for What's New in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: включая отладок для Microsoft Edge в качестве зависимостей | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrading Edge DevTools version to 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Add single close buttons to instances panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Выберите характеристики шрифта и цвета фона, чтобы обеспечить полнейую контрастность для обеспечения | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Надежные типы | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый | Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — | Visual Studio кода"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Средства Microsoft Edge для Visual Studio кода | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR978059]: https://crbug.com/978059 "Проблема 978059: удаление файлов cookie при их фильтрации, удаление всех файлов cookie, а не только отфильтрованных файлов | Ошибки Chromium"  
[CR997625]: https://crbug.com/997625 "Проблема 997625: новый | Требуется возможность увидеть значение раскодирования URL-адреса в файлах cookie | Ошибки Chromium"  
[CR1003629]: https://crbug.com/1003629 "Проблема 1003629: узел захвата больше не делает снимок экрана с узлом под папкой. | Ошибки Chromium"  
[CR1012337]: https://crbug.com/1012337 "Проблема 1012337: очистка данных сайта уничтожает сеанс Google на других сайтах | Ошибки Chromium"  
[CR1028078]: https://crbug.com/1028078 "Проблема 1028078: в списке | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Проблема 1054281: запрос функций: DevTools должен эмулировать устройства с двумя и двумя экранами | Ошибки Chromium"  
[CR1075865]: https://crbug.com/1075865 "Проблема 1075865: показывать отброшенные кадры на временной шкале devtools | Ошибки Chromium"  
[CR1093229]: https://crbug.com/1093229 "Проблема 1093229: DevTools: предложение специализированного пользовательского интерфейса редактора шрифтов | Ошибки Chromium"  
[CR1121900]: https://crbug.com/1121900 "Проблема 1121900: DevTools: обновление логики вычисления контрастности для каждого нового спецификации | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1122580]: https://crbug.com/1122580 "Проблема 1122580: невозможно отключить запись в сети при перезагрузке | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139949]: https://crbug.com/1139949 "Проблема 1139949: наложение Flexbox | Ошибки Chromium"  
[CR1147016]: https://crbug.com/1147016 "Проблема 1147016: палитра не отображается в функции var(). | Ошибки Chromium"  
[CR1148353]: https://crbug.com/1148353 "Проблема 1148353: запрос на функции: копирование объекта из консоли devtools | Ошибки Chromium"  
[CR1149859]: https://crbug.com/1149859 "Проблема 1149859: [запрос функции][консоль] добавьте объект копирования в элемент буфера обмена в контекстное меню | Ошибки Chromium"  
[CR1150797]: https://crbug.com/1150797 "Проблема 1150797: добавление контекстного меню дублирующихся элементов в панели элементов | Ошибки Chromium"  
[CR1152391]: https://crbug.com/1152391 "Проблема 1152391: поддержка копирования контекстного меню CSS в панели стилей | Ошибки Chromium"  
[CR1155120]: https://crbug.com/1155120 "Проблема 1155120: [FR]Support copy file name and line number | Ошибки Chromium"  
[CR1156628]: https://crbug.com/1156628 "Проблема 1156628: DevTools: добавление поддержки функции состояния элемента ":target in force" | Ошибки Chromium"  
[CR1157329]: https://crbug.com/1157329 "Проблема 1157329. Доступность — диктор: диктор не объявляет количество и положение предложений, доступных для кода на вкладке "Стили" | Ошибки Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Папка | Сум США"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contrast (Enhanced) — как выполнить встречи с WCAG (краткий справочник) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Контраст (минимум) — как выполнить встречи с WCAG (краткий справочник) | W3C"  

> [!NOTE]
> <span data-ttu-id="5d69d-399">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d69d-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5d69d-400">Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/01/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="5d69d-400">The original page is found [here](https://developers.google.com/web/updates/2021/01/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5d69d-402">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d69d-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Местоимлятель spanning"  