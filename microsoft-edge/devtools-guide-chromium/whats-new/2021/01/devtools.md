---
description: Средство What's New теперь является Welcome, Visual Font Editor в области стилей, средства отладки CSS Flexbox и другие.
title: Новые возможности в DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2722da0093b3ba6521b5190e61bb208e02a2041e
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408341"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a><span data-ttu-id="f1c24-104">Что нового в DevTools (Microsoft Edge 89)</span><span class="sxs-lookup"><span data-stu-id="f1c24-104">What's New In DevTools (Microsoft Edge 89)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a><span data-ttu-id="f1c24-105">What's New is now Welcome</span><span class="sxs-lookup"><span data-stu-id="f1c24-105">What's New is now Welcome</span></span>  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-106">Средство **What's New** в Microsoft Edge DevTools теперь имеет новый внешний вид и новое имя:  **Welcome**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-106">The **What's New** tool in the Microsoft Edge DevTools now has a new appearance and a new name:  **Welcome**.</span></span>  <span data-ttu-id="f1c24-107">Средство **Welcome** по-прежнему отображает последние новости и обновления DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1c24-107">The **Welcome** tool still displays the latest DevTools news and updates.</span></span>  <span data-ttu-id="f1c24-108">Теперь он также включает ссылки на документацию Microsoft Edge DevTools, способы отправки отзывов и другие.</span><span class="sxs-lookup"><span data-stu-id="f1c24-108">It now also includes links to Microsoft Edge DevTools documentation, ways to submit feedback, and more.</span></span>  <span data-ttu-id="f1c24-109">Чтобы **отобразить** средство Welcome после каждого обновления в Microsoft Edge, выберите почтовый ящик рядом с вкладками **Open после** каждого обновления под заголовком.</span><span class="sxs-lookup"><span data-stu-id="f1c24-109">To display the **Welcome** tool after each update to Microsoft Edge, choose the checkbox next to **Open tab after each update** under the title.</span></span>  <span data-ttu-id="f1c24-110">Чтобы закрыть средство **Welcome,** выберите **X** в правой части заголовка вкладки.</span><span class="sxs-lookup"><span data-stu-id="f1c24-110">To close the **Welcome** tool, choose the **X** on the right-side of the tab title.</span></span>  <span data-ttu-id="f1c24-111">Если вы предпочитаете оригинальный инструмент **What's New,** перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и удалите почтовый ящик рядом со вкладками  >  \*\*\*\* **Enable Welcome.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-111">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Выделено средство Welcome" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   <span data-ttu-id="f1c24-113">Выделено средство **Welcome**</span><span class="sxs-lookup"><span data-stu-id="f1c24-113">The **Welcome** tool is highlighted</span></span>  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a><span data-ttu-id="f1c24-114">Редактор visual Font в области Стилей</span><span class="sxs-lookup"><span data-stu-id="f1c24-114">Visual Font Editor in the Styles pane</span></span>  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-115">При работе со шрифтами в CSS используйте новый визуальный [редактор шрифтов.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="f1c24-115">When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="f1c24-116">Вы можете определить откатные шрифты и использовать ползунки для определения веса, размера, высоты строки и интервалов.</span><span class="sxs-lookup"><span data-stu-id="f1c24-116">You may define fallback fonts, and use sliders to define font weight, size, line-height, and spacing.</span></span>  <span data-ttu-id="f1c24-117">Редактор **шрифта** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f1c24-117">The **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="f1c24-118">Переключение между единицами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="f1c24-118">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="f1c24-119">Переключатель между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="f1c24-119">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="f1c24-120">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="f1c24-120">Convert units</span></span>  
*   <span data-ttu-id="f1c24-121">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-121">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="f1c24-122">Чтобы включить этот эксперимент, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новые средства редактора шрифтов  >  \*\*\*\* в **области Стилей**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-122">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new Font Editor tools within Styles pane**.</span></span>  <span data-ttu-id="f1c24-123">Дополнительные сведения перейдите к редактированию стилей и параметров шрифтов CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="f1c24-123">For more information, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  <span data-ttu-id="f1c24-124">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1093229][CR1093229].</span><span class="sxs-lookup"><span data-stu-id="f1c24-124">To review the history of this feature in the Chromium open-source project, navigate to Issue [1093229][CR1093229].</span></span>  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Редактор visual Font выделен в области Стилей" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   <span data-ttu-id="f1c24-126">Редактор visual **Font выделен** в области **Стилей**</span><span class="sxs-lookup"><span data-stu-id="f1c24-126">The visual **Font editor** is highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a><span data-ttu-id="f1c24-127">Средства отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="f1c24-127">CSS Flexbox debugging tools</span></span>  

<span data-ttu-id="f1c24-128">Функции отладки Flexbox находятся в активной разработке.</span><span class="sxs-lookup"><span data-stu-id="f1c24-128">Flexbox debugging features are in active development.</span></span>  <span data-ttu-id="f1c24-129">Чтобы включить эксперимент для следующих двух функций, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новые  >  \*\*\*\* **функции отладки CSS Flexbox**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-129">To turn on the experiment for the following two features, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and choose the checkbox next to **Enable new CSS Flexbox debugging features**.</span></span>  <span data-ttu-id="f1c24-130">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1136394 и][CR1136394] [1139949][CR1139949].</span><span class="sxs-lookup"><span data-stu-id="f1c24-130">To review the history of this feature in the Chromium open-source project, navigate to Issues [1136394][CR1136394] and [1139949][CR1139949].</span></span>  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a><span data-ttu-id="f1c24-131">Новый значок Flexbox (flex) помогает определить и отобразить контейнеры flex</span><span class="sxs-lookup"><span data-stu-id="f1c24-131">New Flexbox (flex) icon helps identify and display flex containers</span></span>  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-132">В **инструменте Elements** новый значок Flexbox (flex) помогает определить контейнеры Flexbox в коде.</span><span class="sxs-lookup"><span data-stu-id="f1c24-132">In the **Elements** tool, the new Flexbox (flex) icon helps you identify Flexbox containers in your code.</span></span>  <span data-ttu-id="f1c24-133">Выберите значок Flexbox \(flex\) для того, чтобы включить или отключить эффект наложения, который описывает контейнер Flexbox.</span><span class="sxs-lookup"><span data-stu-id="f1c24-133">Choose the Flexbox \(flex\) icon to turn on or off the overlay effect that outlines a Flexbox container.</span></span>  <span data-ttu-id="f1c24-134">Можно настроить цвет наложения в области **Макет,** расположенной рядом со **Стили** и **Вычисления.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-134">You may customize the color of the overlay in the **Layout** pane, which is located next to **Styles** and **Computed**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1c24-135">Чтобы включить и отключить эффект наложения, который описывает контейнер Flexbox, выберите значок Flexbox `flex` \( \) .</span><span class="sxs-lookup"><span data-stu-id="f1c24-135">To turn on and off the overlay effect that outlines the Flexbox container, choose the Flexbox \(`flex`\) icon.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1c24-136">Вы можете настроить цвет наложения в области **Макет** рядом со **стили** и **вычисления**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-136">You may customize the color of the overlay in the **Layout** pane next to **Styles** and **Computed**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Выделены значок Flexbox (flex) и веб-страницы" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         <span data-ttu-id="f1c24-138">Значок и веб-страницы **Flexbox** `flex` \( \) выделены</span><span class="sxs-lookup"><span data-stu-id="f1c24-138">The **Flexbox** \(`flex`\) icon and webpage highlighted</span></span> :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Наложения Flexbox, выделенные в области Макет" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         <span data-ttu-id="f1c24-140">Наложения **Flexbox,** выделенные в области **Макет**</span><span class="sxs-lookup"><span data-stu-id="f1c24-140">The **Flexbox overlays** highlighted in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-gridlines-when-flexbox-layouts-change-using-css-properties"></a><span data-ttu-id="f1c24-141">Отображение значков выравнивания и линий сетки при изменении макетов Flexbox с помощью свойств CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-141">Display alignment icons and gridlines when Flexbox layouts change using CSS properties</span></span>  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-142">При редактировании CSS для макета Flexbox автокомплекты CSS в области **Стилей** теперь отображают полезные значки рядом с соответствующими свойствами Flexbox.</span><span class="sxs-lookup"><span data-stu-id="f1c24-142">When you edit CSS for your Flexbox layout, CSS autocompletes in the **Styles** pane now displays helpful icons next to relevant Flexbox properties.</span></span>  <span data-ttu-id="f1c24-143">Чтобы попробовать эту новую функцию, откройте средство **Elements** и выберите контейнер flex.</span><span class="sxs-lookup"><span data-stu-id="f1c24-143">To try this new feature, open the **Elements** tool and select a flex container.</span></span>  <span data-ttu-id="f1c24-144">Затем добавьте или измените свойство в этом контейнере в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-144">Then add or change a property on that container in the **Styles** pane.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1c24-145">В меню автозаполнения теперь отображаются значки, которые указывают влияние свойств выравнивания, таких как `align-content` и `align-items` .</span><span class="sxs-lookup"><span data-stu-id="f1c24-145">The autocomplete menu now displays icons that indicate the effect of alignment properties such as `align-content` and `align-items`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1c24-146">Кроме того, в DevTools теперь отображается направляющая строка, которая поможет вам лучше просмотреть `align-items` свойство CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-146">Additionally, DevTools now displays a guiding line to help you better review the `align-items` CSS property.</span></span>  <span data-ttu-id="f1c24-147">Поддерживается `gap` также свойство CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-147">The `gap` CSS property is supported as well.</span></span>  <span data-ttu-id="f1c24-148">На следующем рисунке за установлено свойство CSS и отображается шаблон штриховки для `gap` `gap: 12px;` каждого пробела.</span><span class="sxs-lookup"><span data-stu-id="f1c24-148">In the following figure, the `gap` CSS property is set to `gap: 12px;` and the hatching pattern for each gap is displayed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Меню автозаполнения, выделенное для свойств CSS, которые начинаются с выравнивания" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         <span data-ttu-id="f1c24-150">Меню autocomplete, выделенное для свойств CSS, которые начинаются с</span><span class="sxs-lookup"><span data-stu-id="f1c24-150">Autocomplete menu highlighted for CSS properties that start with</span></span> `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Пробел Flexbox в свойствах и веб-странице CSS выделен" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         <span data-ttu-id="f1c24-152">Flexbox `gap` в свойствах CSS и выделенной веб-странице</span><span class="sxs-lookup"><span data-stu-id="f1c24-152">Flexbox `gap` in CSS properties and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a><span data-ttu-id="f1c24-153">Быстро добавьте средства с помощью новой кнопки More Tools</span><span class="sxs-lookup"><span data-stu-id="f1c24-153">Add tools quickly with new More Tools button</span></span>  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-154">Теперь у вас есть новый способ открыть дополнительные средства в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1c24-154">You now have a new way to open more tools in the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="f1c24-155">После этого эксперимента значок **More Tools** отображается в качестве знака плюс `+` () справа от основной панели.</span><span class="sxs-lookup"><span data-stu-id="f1c24-155">After you turn on this experiment, the **More Tools** icon displays as a plus sign (`+`) to the right of the main panel.</span></span>  <span data-ttu-id="f1c24-156">Чтобы отобразить список других средств для добавления в главную панель, выберите значок **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="f1c24-156">To display a list of other tools to add to the main panel, choose the **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="f1c24-157">Чтобы включить этот эксперимент, перейдите к [параметрам][DevtoolsCustomizeIndexSettings]  >  **Эксперименты,** а затем выберите почтовый ящик рядом с включить + меню вкладки кнопки, чтобы **открыть больше средств**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-157">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**, and then choose the checkbox next to **Enable + button tab menus to open more tools**.</span></span>  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Дополнительные средства, выделенные в DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   <span data-ttu-id="f1c24-159">**Дополнительные средства,** выделенные в DevTools</span><span class="sxs-lookup"><span data-stu-id="f1c24-159">**More Tools** highlighted in DevTools</span></span>  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a><span data-ttu-id="f1c24-160">Вспомогательные технологии теперь объявляют положение и количество предложений CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-160">Assistive technologies now announce position and count of CSS suggestions</span></span>  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

<span data-ttu-id="f1c24-161">При редактировании CSS вы получаете отсев функций.</span><span class="sxs-lookup"><span data-stu-id="f1c24-161">When you edit CSS, you get a dropdown of features.</span></span>  <span data-ttu-id="f1c24-162">Эта функция была недоступна пользователям вспомогательных технологий, так как она объявлена в Microsoft Edge версии 89.</span><span class="sxs-lookup"><span data-stu-id="f1c24-162">This feature was not available to users of assistive technologies, since it is announced in Microsoft Edge version 89.</span></span>  <span data-ttu-id="f1c24-163">Пользователь вспомогательных технологий теперь может перемещаться по предложениям CSS в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-163">A user of assistive technologies may now navigate CSS suggestions in the **Styles** pane.</span></span>  <span data-ttu-id="f1c24-164">В microsoft Edge версии 88 и ранее вспомогательные технологии, объявленные пользователем, переходили по списку предложений при редактировании CSS в области `Suggestion` **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-164">In Microsoft Edge version 88 and earlier, assistive technology announced `Suggestion` as a user navigated through the list of suggestions when editing CSS in the **Styles** pane.</span></span>  <span data-ttu-id="f1c24-165">В microsoft Edge версии 89 пользователь вспомогательных технологий теперь слышит позицию и количество текущего предложения.</span><span class="sxs-lookup"><span data-stu-id="f1c24-165">In Microsoft Edge version 89, a user of assistive technology now hears the position and count of the current suggestion.</span></span>  <span data-ttu-id="f1c24-166">Каждое предложение объявляется по мере перемещения пользователя по списку предложений, таких как Предложение 3 из 5.</span><span class="sxs-lookup"><span data-stu-id="f1c24-166">Each suggestion is announced as the user navigates through the list of suggestions, such as Suggestion 3 of 5.</span></span>  <span data-ttu-id="f1c24-167">Чтобы узнать больше о написании CSS в DevTools, перейдите на [изменение CSS][DevtoolsCssReferenceChangeCss].</span><span class="sxs-lookup"><span data-stu-id="f1c24-167">To learn more about writing CSS in the DevTools, navigate to [Change CSS][DevtoolsCssReferenceChangeCss].</span></span>  <span data-ttu-id="f1c24-168">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1157329][CR1157329].</span><span class="sxs-lookup"><span data-stu-id="f1c24-168">To review the history of this feature in the Chromium open-source project, navigate to Issue [1157329][CR1157329].</span></span>  

<span data-ttu-id="f1c24-169">Чтобы просмотреть видео, которое отображает и читает вслух несколько предложений с включенным этим экспериментом, перейдите в voiceover, объявляя параметры [devtools](https://youtu.be/9TcUpleEwwA) на YouTube.</span><span class="sxs-lookup"><span data-stu-id="f1c24-169">To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.</span></span>  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Предложение, выделено в области Стилей" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   <span data-ttu-id="f1c24-171">Список, `suggestion` выделенный в области **Стилей**</span><span class="sxs-lookup"><span data-stu-id="f1c24-171">The `suggestion` list highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="f1c24-172">Эмулировать Surface Duo и Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="f1c24-172">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

<span data-ttu-id="f1c24-173">Проверьте внешний вид веб-сайта или приложения на следующих устройствах в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f1c24-173">Test the appearance of your website or app on the following devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="f1c24-174">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f1c24-174">Surface Duo</span></span>][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [<span data-ttu-id="f1c24-175">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="f1c24-175">Samsung Galaxy Fold</span></span>][SamsungUsMobileGalaxyFold]  
    
<span data-ttu-id="f1c24-176">**Включи функции экспериментальной** веб-платформы, чтобы получить доступ к новой функции экранирования экрана [CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]</span><span class="sxs-lookup"><span data-stu-id="f1c24-176">Turn on **Experimental Web Platform features** to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [getWindowSegments JavaScript API][DualScreenWebJavascriptGetwindowsegments].</span></span>  <span data-ttu-id="f1c24-177">Перейдите `edge://flags` к флажку рядом с функциями **экспериментальной веб-платформы**и перейдите к ней.</span><span class="sxs-lookup"><span data-stu-id="f1c24-177">Navigate to `edge://flags` and toggle the flag next to **Experimental Web Platform features**.</span></span>  <span data-ttu-id="f1c24-178">Чтобы улучшить веб-сайт или приложение для двухэкранных и складных устройств, используйте следующие функции при [эмулации устройства.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="f1c24-178">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="f1c24-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]— это когда веб-сайт \(или app\) отображается на обоих экранах.</span><span class="sxs-lookup"><span data-stu-id="f1c24-179">[Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>  
*   <span data-ttu-id="f1c24-180">[Отрисовка шва,][DualScreenIntroductionHowToWorkWithSeam]который является пространством между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="f1c24-180">[Rendering the seam][DualScreenIntroductionHowToWorkWithSeam], which is the space between the two screens.</span></span>  
    
<span data-ttu-id="f1c24-181">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1054281][CR1054281].</span><span class="sxs-lookup"><span data-stu-id="f1c24-181">To review the history of this feature in the Chromium open-source project, navigate to Issue [1054281][CR1054281].</span></span>  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Эмулировать двойной экран" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   <span data-ttu-id="f1c24-183">Эмулировать двойной экран</span><span class="sxs-lookup"><span data-stu-id="f1c24-183">Emulate dual-screen</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a><span data-ttu-id="f1c24-184">Средства разработки Microsoft Edge для Visual Studio версии кода 1.1.2</span><span class="sxs-lookup"><span data-stu-id="f1c24-184">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.2</span></span>  

<span data-ttu-id="f1c24-185">Средства [разработки Microsoft Edge для Visual Studio][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.2 для Microsoft Visual Studio код имеет следующие изменения со времени предыдущего выпуска.</span><span class="sxs-lookup"><span data-stu-id="f1c24-185">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.2 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="f1c24-186">Microsoft Visual Studio обновления кода автоматически.</span><span class="sxs-lookup"><span data-stu-id="f1c24-186">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="f1c24-187">Чтобы вручную обновить версию 1.1.2, перейдите к [обновлению расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="f1c24-187">To manually update to version 1.1.2, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

*   <span data-ttu-id="f1c24-188">Добавлена **кнопка Закрыть экземпляр** к каждому элементу в целевом списке \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span><span class="sxs-lookup"><span data-stu-id="f1c24-188">Added a **Close instance** button to each item on the target list \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)</span></span>  
*   <span data-ttu-id="f1c24-189">Неровная версия [Microsoft Edge DevTools][DevtoolsMain] с 84.0.522.63 до [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span><span class="sxs-lookup"><span data-stu-id="f1c24-189">Bumped [Microsoft Edge DevTools][DevtoolsMain] version from 84.0.522.63 to [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)</span></span>  
*   <span data-ttu-id="f1c24-190">Включено [debugger для Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] в качестве зависимостей \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span><span class="sxs-lookup"><span data-stu-id="f1c24-190">Included [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] as a dependency  \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)</span></span>  
*   <span data-ttu-id="f1c24-191">Реализованный параметр параметры для изменения тем расширения \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span><span class="sxs-lookup"><span data-stu-id="f1c24-191">Implemented settings option to change extension themes \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)</span></span>  
    
<span data-ttu-id="f1c24-192">Вы можете файл проблемы и внести свой вклад в расширение [на vscode-edge-devtools GitHub репо][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="f1c24-192">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="f1c24-193">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="f1c24-193">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a><span data-ttu-id="f1c24-194">Захват экрана узла за пределами viewport</span><span class="sxs-lookup"><span data-stu-id="f1c24-194">Capture node screenshot beyond viewport</span></span>  

<span data-ttu-id="f1c24-195">В microsoft Edge версии 89 скриншоты узлов более точны, захватывая полный узел, даже если содержимое узла не отображается в представлении.</span><span class="sxs-lookup"><span data-stu-id="f1c24-195">In Microsoft Edge version 89, node screenshots are more accurate, capturing the full node even if content from the node is not visible in the viewport.</span></span>  <span data-ttu-id="f1c24-196">В **инструменте Elements** наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите снимок экрана **узла Capture**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-196">In the **Elements** tool, hover  on an element, open the contextual menu \(right-click\), and choose **Capture node screenshot**.</span></span>  <span data-ttu-id="f1c24-197">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1003629][CR1003629].</span><span class="sxs-lookup"><span data-stu-id="f1c24-197">To review the history of this feature in the Chromium open-source project, navigate to Issue [1003629][CR1003629].</span></span>  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Снимок экрана узла, выделенного в контексте меню в средстве Elements" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   <span data-ttu-id="f1c24-199">**Снимок экрана** узла, выделенного в контексте меню в **средстве Elements**</span><span class="sxs-lookup"><span data-stu-id="f1c24-199">**Capture node screenshot** highlighted on the context menu in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="f1c24-200">Обновления инструмента Elements</span><span class="sxs-lookup"><span data-stu-id="f1c24-200">Elements tool updates</span></span>  

#### <a name="support-forcing-the-target-css-state"></a><span data-ttu-id="f1c24-201">Поддержка принудительного состояния :target CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-201">Support forcing the :target CSS state</span></span>  

<span data-ttu-id="f1c24-202">Теперь можно использовать DevTools для принудительного [использования псевдокласса][MdnDocsWebCssTarget] CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-202">You may now use DevTools to force the [:target][MdnDocsWebCssTarget] CSS pseudo-class.</span></span>  <span data-ttu-id="f1c24-203">Псевдокласс запускается, когда уникальный элемент \(целевой элемент\) имеет фрагмент `:target` `id` URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f1c24-203">The `:target` pseudo-class is triggered when a unique element \(the target element\) has an `id` that matches a fragment of the URL.</span></span>  <span data-ttu-id="f1c24-204">Например, `http://www.example.com/index.html#section1` `:target` URL-адрес запускает псевдокласс на элементе HTML с `id="section1"` помощью .</span><span class="sxs-lookup"><span data-stu-id="f1c24-204">For example, the `http://www.example.com/index.html#section1` URL triggers the `:target` pseudo-class on an HTML element with `id="section1"`.</span></span>  <span data-ttu-id="f1c24-205">Чтобы попробовать демонстрацию с выделенной частью 1, перейдите к [CSS:target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span><span class="sxs-lookup"><span data-stu-id="f1c24-205">To try a demo with section 1 highlighted, navigate to [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].</span></span>  <span data-ttu-id="f1c24-206">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1156628][CR1156628].</span><span class="sxs-lookup"><span data-stu-id="f1c24-206">To review the history of this feature in the Chromium open-source project, navigate to Issue [1156628][CR1156628].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Выделенная веб-страница без принудительного CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         <span data-ttu-id="f1c24-208">Веб-страницу, выделенную без принудительного CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-208">Webpage highlighted with no forced CSS</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` <span data-ttu-id="f1c24-210">CSS forced and webpage highlighted</span><span class="sxs-lookup"><span data-stu-id="f1c24-210">CSS forced and webpage highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a><span data-ttu-id="f1c24-211">Использование элементов Duplicate для копирования элементов</span><span class="sxs-lookup"><span data-stu-id="f1c24-211">Use Duplicate elements to copy elements</span></span>  

<span data-ttu-id="f1c24-212">Используйте новый ярлык **элемента Дубликат,** чтобы клонировать элемент.</span><span class="sxs-lookup"><span data-stu-id="f1c24-212">Use the new **Duplicate element** shortcut to clone an element.</span></span>  <span data-ttu-id="f1c24-213">В **инструменте Elements** наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\), выберите **элемент Дубликат**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-213">In the **Elements** tool, hover on an element, open the contextual menu \(right-click\), choose **Duplicate element**.</span></span>  <span data-ttu-id="f1c24-214">Новый элемент создается под выбранным элементом.</span><span class="sxs-lookup"><span data-stu-id="f1c24-214">A new element is created under the selected element.</span></span>  <span data-ttu-id="f1c24-215">Чтобы дублировать элемент с помощью клавиши, выберите `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) или `Shift` + `Option` + `Down Arrow` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="f1c24-215">To duplicate the element with a keyboard shortcut, select `Shift`+`Alt`+`Down Arrow` \(Windows/Linux\) or `Shift`+`Option`+`Down Arrow` \(macOS\).</span></span>  <span data-ttu-id="f1c24-216">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1150797][CR1150797].</span><span class="sxs-lookup"><span data-stu-id="f1c24-216">To review the history of this feature in the Chromium open-source project, navigate to Issue [1150797][CR1150797].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Элемент Duplicate выделен в контексте меню элемента в средстве Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   <span data-ttu-id="f1c24-218">Элемент **Duplicate выделен** в контексте меню элемента в **средстве Elements**</span><span class="sxs-lookup"><span data-stu-id="f1c24-218">The **Duplicate element** is highlighted in the context menu on an element in the **Elements** tool</span></span>  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a><span data-ttu-id="f1c24-219">Выбор цветов для настраиваемого свойства CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-219">Color pickers for custom CSS properties</span></span>  

<span data-ttu-id="f1c24-220">В **области Стилей** теперь отображаются цветовые выборщики для настраиваемого свойства CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-220">The **Styles** pane now displays color pickers for custom CSS properties.</span></span>  <span data-ttu-id="f1c24-221">Чтобы пройти цикл через форматы RGBA, HSLA и Hex цветового значения, удерживайте и выберите `Shift` выбор цвета.</span><span class="sxs-lookup"><span data-stu-id="f1c24-221">To cycle through the RGBA, HSLA, and Hex formats of the color value, hold `Shift` and choose the color picker.</span></span>  <span data-ttu-id="f1c24-222">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1147016][CR1147016].</span><span class="sxs-lookup"><span data-stu-id="f1c24-222">To review the history of this feature in the Chromium open-source project, navigate to Issue [1147016][CR1147016].</span></span>  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Выбор цветов для настраиваемого свойства CSS" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   <span data-ttu-id="f1c24-224">Выбор цветов для настраиваемого свойства CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-224">Color pickers for custom CSS properties</span></span>  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a><span data-ttu-id="f1c24-225">Копирование классов и свойств CSS</span><span class="sxs-lookup"><span data-stu-id="f1c24-225">Copy CSS classes and properties</span></span>  

<span data-ttu-id="f1c24-226">Теперь можно быстрее скопировать свойства CSS с помощью нескольких новых параметров в контекстной меню.</span><span class="sxs-lookup"><span data-stu-id="f1c24-226">You may now copy CSS properties quicker with a few new options in the contextual menu.</span></span>  <span data-ttu-id="f1c24-227">В **инструменте Elements** выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="f1c24-227">In the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="f1c24-228">Чтобы скопировать значение в области **Стилей,** наведите курс на класс CSS или свойство CSS, откройте контекстное меню \(правой кнопкой мыши\) и выберите вариант копирования.</span><span class="sxs-lookup"><span data-stu-id="f1c24-228">To copy the value, in the **Styles** pane, hover on a CSS class or a CSS property, open a contextual menu \(right-click\), and choose the copy option.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1c24-229">Копирование параметров для класса CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-229">Copy options for a CSS class.</span></span>  
      
      | <span data-ttu-id="f1c24-230">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1c24-230">Option</span></span> | <span data-ttu-id="f1c24-231">Сведения</span><span class="sxs-lookup"><span data-stu-id="f1c24-231">Details</span></span> |  
      |:--- |:--- |  
      | **<span data-ttu-id="f1c24-232">Выбор копирования</span><span class="sxs-lookup"><span data-stu-id="f1c24-232">Copy selector</span></span>** | <span data-ttu-id="f1c24-233">Скопируйте имя текущего селектора.</span><span class="sxs-lookup"><span data-stu-id="f1c24-233">Copy the current selector name.</span></span> |  
      | **<span data-ttu-id="f1c24-234">Правило копирования</span><span class="sxs-lookup"><span data-stu-id="f1c24-234">Copy rule</span></span>** | <span data-ttu-id="f1c24-235">Скопируйте правило текущего селектора.</span><span class="sxs-lookup"><span data-stu-id="f1c24-235">Copy the rule of the current selector.</span></span> |  
      | **<span data-ttu-id="f1c24-236">Копирование всех деклараций</span><span class="sxs-lookup"><span data-stu-id="f1c24-236">Copy all declarations</span></span>** | <span data-ttu-id="f1c24-237">Скопируйте все объявления в соответствии с текущим правилом, включая не допустимые и префиксные свойства.</span><span class="sxs-lookup"><span data-stu-id="f1c24-237">Copy all declarations under the current rule, including non-valid and prefixed properties.</span></span> |  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1c24-238">Копирование параметров свойства CSS.</span><span class="sxs-lookup"><span data-stu-id="f1c24-238">Copy options for a CSS property.</span></span>  
      
      | <span data-ttu-id="f1c24-239">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1c24-239">Option</span></span> | <span data-ttu-id="f1c24-240">Сведения</span><span class="sxs-lookup"><span data-stu-id="f1c24-240">Details</span></span> |      
      |:--- |:--- |  
      | **<span data-ttu-id="f1c24-241">Декларация копирования</span><span class="sxs-lookup"><span data-stu-id="f1c24-241">Copy declaration</span></span>** | <span data-ttu-id="f1c24-242">Скопируйте объявление текущей строки.</span><span class="sxs-lookup"><span data-stu-id="f1c24-242">Copy the declaration of the current line.</span></span> |  
      | **<span data-ttu-id="f1c24-243">Скопируйте свойство</span><span class="sxs-lookup"><span data-stu-id="f1c24-243">Copy property</span></span>** | <span data-ttu-id="f1c24-244">Скопируйте свойство текущей строки.</span><span class="sxs-lookup"><span data-stu-id="f1c24-244">Copy the property of the current line.</span></span> |  
      | **<span data-ttu-id="f1c24-245">Значение copy</span><span class="sxs-lookup"><span data-stu-id="f1c24-245">Copy value</span></span>** | <span data-ttu-id="f1c24-246">Скопируйте значение текущей строки.</span><span class="sxs-lookup"><span data-stu-id="f1c24-246">Copy the value of the current line.</span></span> |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Копирование параметров класса CSS в контекстной меню" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         <span data-ttu-id="f1c24-248">Копирование параметров класса CSS в контекстной меню</span><span class="sxs-lookup"><span data-stu-id="f1c24-248">Copy options for a CSS class in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Копирование параметров свойства CSS в контекстной меню" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         <span data-ttu-id="f1c24-250">Копирование параметров свойства CSS в контекстной меню</span><span class="sxs-lookup"><span data-stu-id="f1c24-250">Copy options for a CSS property in the contextual menu</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="f1c24-251">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1152391][CR1152391].</span><span class="sxs-lookup"><span data-stu-id="f1c24-251">To review the history of this feature in the Chromium open-source project, navigate to Issue [1152391][CR1152391].</span></span>  

### <a name="cookies-updates"></a><span data-ttu-id="f1c24-252">Обновления файлов cookie</span><span class="sxs-lookup"><span data-stu-id="f1c24-252">Cookies updates</span></span>  

#### <a name="new-option-to-display-url-decoded-cookies"></a><span data-ttu-id="f1c24-253">Новый параметр отображения файлов cookie с декодом URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f1c24-253">New option to display URL-decoded cookies</span></span>  

<span data-ttu-id="f1c24-254">Теперь вы можете отобразить значение cookies с декодированием URL-адресов в **области Cookies.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-254">You may now opt to display the URL-decoded cookies value in the **Cookies** pane.</span></span>  <span data-ttu-id="f1c24-255">Чтобы отобразить расшифровку cookie, перейдите к области \*\*\*\*  >  **cookie-файлов** приложений, выберите любое cookie в списке и выберите почтовый ящик рядом с декодированием **URL-адреса.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-255">To display the decoded cookie, navigate to **Application** > **Cookies** pane, choose any cookie on the list, and choose the checkbox next to **Show URL decoded**.</span></span>  <span data-ttu-id="f1c24-256">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [997625][CR997625].</span><span class="sxs-lookup"><span data-stu-id="f1c24-256">To review the history of this feature in the Chromium open-source project, navigate to Issue [997625][CR997625].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Возможность отображения файлов cookie с декодом URL-адресов" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   <span data-ttu-id="f1c24-258">Возможность отображения файлов cookie, расшифровав URL-адрес</span><span class="sxs-lookup"><span data-stu-id="f1c24-258">Option to display URL decoded cookies</span></span>  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a><span data-ttu-id="f1c24-259">Фильтрация и очистка видимых файлов cookie</span><span class="sxs-lookup"><span data-stu-id="f1c24-259">Filter and clear visible cookies</span></span>  

<span data-ttu-id="f1c24-260">В Microsoft Edge версии 88 \*\*\*\* или более ранней версии средство приложения предоставляет только способ очистки всех файлов cookie с помощью кнопки **Clear all cookies.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-260">In Microsoft Edge version 88 or earlier, the **Application** tool only provided a way to clear all cookies with the **Clear all cookies** button.</span></span>  <span data-ttu-id="f1c24-261">В Microsoft Edge версии 89 теперь можно выбрать фильтруемое cookie **Clear,** чтобы удалить только фильтрованные файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="f1c24-261">In Microsoft Edge version 89, you may now choose **Clear filtered cookies** to delete only the filtered cookies.</span></span>  <span data-ttu-id="f1c24-262">Чтобы отфильтровать файлы cookie, перейдите **к**  >  **cookie-файлам приложений**и введите текстовое ящик **фильтра.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-262">To filter cookies, navigate to **Application** > **Cookies**, and type in the **Filter** textbox.</span></span>  <span data-ttu-id="f1c24-263">Чтобы удалить отображаемое печенье, выберите кнопку **Clear filtered cookies.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-263">To delete the displayed cookies, choose the **Clear filtered cookies** button.</span></span>  <span data-ttu-id="f1c24-264">Чтобы отобразить все остальные файлы cookie, очистить текст фильтра.</span><span class="sxs-lookup"><span data-stu-id="f1c24-264">To display all other cookies, clear the filter text.</span></span>  <span data-ttu-id="f1c24-265">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [978059][CR978059].</span><span class="sxs-lookup"><span data-stu-id="f1c24-265">To review the history of this feature in the Chromium open-source project, navigate to Issue [978059][CR978059].</span></span>  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Очистка только видимых файлов cookie" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   <span data-ttu-id="f1c24-267">Очистка только видимых файлов cookie</span><span class="sxs-lookup"><span data-stu-id="f1c24-267">Clear only visible cookies</span></span>  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a><span data-ttu-id="f1c24-268">Новый вариант очистки сторонних файлов cookie в области хранения</span><span class="sxs-lookup"><span data-stu-id="f1c24-268">New option to clear third-party cookies in the Storage pane</span></span>  

<span data-ttu-id="f1c24-269">DevTools теперь очищает только первопартийные файлы cookie по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1c24-269">DevTools now clear only first-party cookies by default.</span></span>  <span data-ttu-id="f1c24-270">Чтобы очистить данные веб-сайта и только однопартийные файлы cookie, перейдите в **хранилище**приложений, а затем выберите  >  \*\*\*\* clear **site data.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-270">To clear website data and first-party cookies only, navigate to **Application** > **Storage**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="f1c24-271">Чтобы очистить данные веб-сайта и все файлы cookie, перейдите в **хранилище**  >  **приложений.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-271">To clear website data and all cookies, navigate to **Application** > **Storage**.</span></span>  <span data-ttu-id="f1c24-272">Выберите почтовый ящик рядом с **включив**сторонние файлы cookie, а затем выберите **clear site data.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-272">Choose the checkbox next to **including third-party cookies**, and then choose **Clear site data**.</span></span>  

<span data-ttu-id="f1c24-273">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1012337][CR1012337].</span><span class="sxs-lookup"><span data-stu-id="f1c24-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1012337][CR1012337].</span></span>  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Возможность очистки сторонних файлов cookie" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   <span data-ttu-id="f1c24-275">Возможность очистки сторонних файлов cookie</span><span class="sxs-lookup"><span data-stu-id="f1c24-275">Option to clear third-party cookies</span></span>  
:::image-end:::  

### <a name="network-tool-updates"></a><span data-ttu-id="f1c24-276">Обновления сетевых инструментов</span><span class="sxs-lookup"><span data-stu-id="f1c24-276">Network tool updates</span></span>  

#### <a name="persist-record-network-log-setting"></a><span data-ttu-id="f1c24-277">Параметр сетевого журнала сохраняемой записи</span><span class="sxs-lookup"><span data-stu-id="f1c24-277">Persist Record network log setting</span></span>  

<span data-ttu-id="f1c24-278">В microsoft Edge версии 88 или более ранней версии DevTools сбрасывает параметр журнала журнала записи сети при обновлении веб-страницы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f1c24-278">In Microsoft Edge version 88 or earlier, DevTools reset the **Record network log** setting when a webpage refreshes.</span></span>  <span data-ttu-id="f1c24-279">В microsoft Edge версии 89 в DevTools теперь сохраняется параметр **журнала журнала записи** сети.</span><span class="sxs-lookup"><span data-stu-id="f1c24-279">In Microsoft Edge version 89, DevTools now persist the **Record network log** setting.</span></span>  <span data-ttu-id="f1c24-280">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1122580][CR1122580].</span><span class="sxs-lookup"><span data-stu-id="f1c24-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122580][CR1122580].</span></span>  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Журнал записи сети" lightbox="../../media/2021/01/network-log.msft.png":::
   <span data-ttu-id="f1c24-282">Журнал записи сети</span><span class="sxs-lookup"><span data-stu-id="f1c24-282">Record network log</span></span>  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a><span data-ttu-id="f1c24-283">Online option is now No throttling option</span><span class="sxs-lookup"><span data-stu-id="f1c24-283">Online option is now No throttling option</span></span>  

<span data-ttu-id="f1c24-284">Параметр сетевой эмуляции **Online** теперь переименован в **No Throttling.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-284">The network emulation option **Online** is now renamed to **No Throttling**.</span></span>  <span data-ttu-id="f1c24-285">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1028078][CR1028078].</span><span class="sxs-lookup"><span data-stu-id="f1c24-285">To review the history of this feature in the Chromium open-source project, navigate to Issue [1028078][CR1028078].</span></span>  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Нет параметра регулирования" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   <span data-ttu-id="f1c24-287">**Нет параметра регулирования**</span><span class="sxs-lookup"><span data-stu-id="f1c24-287">**No throttling** option</span></span>  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a><span data-ttu-id="f1c24-288">Новые параметры копирования в средстве консоли, средстве Sources и области стилей</span><span class="sxs-lookup"><span data-stu-id="f1c24-288">New copy options in the Console tool, Sources tool, and Styles pane</span></span>

#### <a name="copy-object-in-the-console-and-sources-tool"></a><span data-ttu-id="f1c24-289">Копирование объекта в средстве консоли и источников</span><span class="sxs-lookup"><span data-stu-id="f1c24-289">Copy object in the Console and Sources tool</span></span>  

<span data-ttu-id="f1c24-290">Теперь можно скопировать значения объектов в **средствах консоли** и **источников.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-290">You may now copy object values in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="f1c24-291">Возможность копирования значений объектов полезна при работе с большими объектами.</span><span class="sxs-lookup"><span data-stu-id="f1c24-291">The ability to copy object values is useful when working with large objects.</span></span>  <span data-ttu-id="f1c24-292">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1148353][CR1148353] и [1149859][CR1149859].</span><span class="sxs-lookup"><span data-stu-id="f1c24-292">To review the history of this feature in the Chromium open-source project, navigate to Issues [1148353][CR1148353] and [1149859][CR1149859].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1c24-293">В **средстве Консоли** наведите курсор на объект, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите **объект Copy**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-293">In the **Console** tool, hover on an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1c24-294">В \*\*\*\* средстве Источники на точке останова наведите \*\*\*\* курсор на объект, в окне всплывающее окно Объекта выделяем объект, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите объект **Copy**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-294">In the **Sources** tool, on a breakpoint, hover on an object, in the **Object** popup window, highlight an object, open the contextual menu \(right-click\), and then choose **Copy object**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Копирование объекта в консоли" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         <span data-ttu-id="f1c24-296">Копирование объекта в **консоли**</span><span class="sxs-lookup"><span data-stu-id="f1c24-296">Copy object in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Копирование объекта в источниках" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         <span data-ttu-id="f1c24-298">Копирование объекта в **источниках**</span><span class="sxs-lookup"><span data-stu-id="f1c24-298">Copy object in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a><span data-ttu-id="f1c24-299">Скопируйте имя файла в инструменте Sources и области стилей</span><span class="sxs-lookup"><span data-stu-id="f1c24-299">Copy file name in the Sources tool and Styles pane</span></span>  

<span data-ttu-id="f1c24-300">Теперь можно скопировать имя файла с помощью контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="f1c24-300">You may now copy a file name using the contextual menu.</span></span>  <span data-ttu-id="f1c24-301">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1155120][CR1155120].</span><span class="sxs-lookup"><span data-stu-id="f1c24-301">To review the history of this feature in the Chromium open-source project, navigate to Issues [1155120][CR1155120].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1c24-302">В **средстве Источники** введите имя файла, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите **имя файла Copy**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-302">In the **Sources** tool, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1c24-303">В **инструменте Elements** > **стилей** наведите курсор на имя файла, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите имя файла **Copy**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-303">In the **Elements** tool > **Styles** pane, hover on a file name, open the contextual menu \(right-click\), and then choose **Copy file name**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Скопируйте имя файла в Источниках" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         <span data-ttu-id="f1c24-305">Скопируйте имя файла в **Источниках**</span><span class="sxs-lookup"><span data-stu-id="f1c24-305">Copy file name in **Sources**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Скопируйте имя файла в области Стилей" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         <span data-ttu-id="f1c24-307">Скопируйте имя файла в **области Стилей**</span><span class="sxs-lookup"><span data-stu-id="f1c24-307">Copy file name in **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a><span data-ttu-id="f1c24-308">Сведения об обновлениях в Frame</span><span class="sxs-lookup"><span data-stu-id="f1c24-308">Updates to Frame details</span></span>  

#### <a name="service-workers-information-in-frame-details"></a><span data-ttu-id="f1c24-309">Сведения о работниках служб в подробностях Frame</span><span class="sxs-lookup"><span data-stu-id="f1c24-309">Service Workers information in Frame details</span></span>  

<span data-ttu-id="f1c24-310">В DevTools теперь перечислены выделенные работники службы в родительском кадре.</span><span class="sxs-lookup"><span data-stu-id="f1c24-310">DevTools now lists a dedicated service worker under the parent frame.</span></span>  <span data-ttu-id="f1c24-311">На следующем рисунке отображаются сведения о сотрудниках службы.</span><span class="sxs-lookup"><span data-stu-id="f1c24-311">In the following figure, service worker details are displayed.</span></span>  <span data-ttu-id="f1c24-312">Чтобы отобразить сведения об сотруднике службы, перейдите к **сотрудникам службы кадров**приложений и  >  \*\*\*\*  >  `top`  >  \*\*\*\* выберите сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="f1c24-312">To display the service worker details, navigate to **Application** > **Frames** > `top` > **Service Workers** and then choose a service worker.</span></span>  <span data-ttu-id="f1c24-313">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1122507][CR1122507].</span><span class="sxs-lookup"><span data-stu-id="f1c24-313">To review the history of this feature in the Chromium open-source project, navigate to Issue [1122507][CR1122507].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Сведения о работниках служб в подробностях Frames" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   <span data-ttu-id="f1c24-315">**Сведения о работниках** служб в **подробностях Frames**</span><span class="sxs-lookup"><span data-stu-id="f1c24-315">**Service Workers** information in the **Frames** details</span></span>  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a><span data-ttu-id="f1c24-316">Измерение сведений о памяти в подробностях Frame</span><span class="sxs-lookup"><span data-stu-id="f1c24-316">Measure Memory information in Frame details</span></span>  

<span data-ttu-id="f1c24-317">Теперь состояние API отображается `performance.measureMemory()` в разделе доступность **API.**</span><span class="sxs-lookup"><span data-stu-id="f1c24-317">The `performance.measureMemory()` API status is now displayed under the **API availability** section.</span></span>  <span data-ttu-id="f1c24-318">Новый `performance.measureMemory()` API оценивает использование памяти всей веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="f1c24-318">The new `performance.measureMemory()` API estimates the memory usage of the entire webpage.</span></span>  <span data-ttu-id="f1c24-319">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="f1c24-319">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Измерение памяти" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   <span data-ttu-id="f1c24-321">Измерение памяти</span><span class="sxs-lookup"><span data-stu-id="f1c24-321">Measure Memory</span></span>  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a><span data-ttu-id="f1c24-322">Отброшенные кадры в средстве Performance</span><span class="sxs-lookup"><span data-stu-id="f1c24-322">Dropped frames in the Performance tool</span></span>  

<span data-ttu-id="f1c24-323">При [анализе производительности нагрузки][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]в средстве Performance раздел **Frames** теперь отмечает отброшенные кадры как красные.</span><span class="sxs-lookup"><span data-stu-id="f1c24-323">When you [analyze load performance in the Performance tool][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], the **Frames** section now marks dropped frames as red.</span></span>  <span data-ttu-id="f1c24-324">Чтобы отобразить частоту кадров, наведите курс на отброшенный кадр.</span><span class="sxs-lookup"><span data-stu-id="f1c24-324">To display the frame rate, hover on a dropped frame.</span></span>  <span data-ttu-id="f1c24-325">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1075865][CR1075865].</span><span class="sxs-lookup"><span data-stu-id="f1c24-325">To review the history of this feature in the Chromium open-source project, navigate to Issue [1075865][CR1075865].</span></span>  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Отброшенные кадры" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   <span data-ttu-id="f1c24-327">Отброшенные кадры</span><span class="sxs-lookup"><span data-stu-id="f1c24-327">Dropped frames</span></span>  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a><span data-ttu-id="f1c24-328">Новый расчет контрастности цвета — расширенный перцептивный контрастный алгоритм (APCA)</span><span class="sxs-lookup"><span data-stu-id="f1c24-328">New color contrast calculation - Advanced Perceptual Contrast Algorithm (APCA)</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="f1c24-329">Расширенный перцептивный контрастный алгоритм [(APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] заменяет коэффициент контраста руководящих принципов [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] в [цветопоискатель][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span><span class="sxs-lookup"><span data-stu-id="f1c24-329">The [Advanced Perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] replaces the [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] guidelines contrast ratio in the [Color Picker][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].</span></span>  <span data-ttu-id="f1c24-330">APCA — это новый способ вычисления контраста.</span><span class="sxs-lookup"><span data-stu-id="f1c24-330">APCA is a new way to compute contrast.</span></span>  <span data-ttu-id="f1c24-331">Он основан на современных исследованиях по восприятию цвета.</span><span class="sxs-lookup"><span data-stu-id="f1c24-331">It is based on modern research on color perception.</span></span>  <span data-ttu-id="f1c24-332">По сравнению с рекомендациями AA/AAA APCA больше зависит от контекста.</span><span class="sxs-lookup"><span data-stu-id="f1c24-332">Compared to AA/AAA guidelines, APCA is more context-dependent.</span></span>  <span data-ttu-id="f1c24-333">Контраст рассчитывается на основе следующих пространственных свойств текста, цвета и контекста.</span><span class="sxs-lookup"><span data-stu-id="f1c24-333">The contrast is calculated based on the following spatial properties of the text, color, and context.</span></span>  

*   <span data-ttu-id="f1c24-334">Пространственные свойства текста, которые включают вес шрифта и размер.</span><span class="sxs-lookup"><span data-stu-id="f1c24-334">Spatial properties of text that include font weight and size.</span></span>  
*   <span data-ttu-id="f1c24-335">Пространственные свойства цвета, которые включают предполагаемый контраст между текстом и фоном.</span><span class="sxs-lookup"><span data-stu-id="f1c24-335">Spatial properties of color that include perceived contrast between text and background.</span></span>  
*   <span data-ttu-id="f1c24-336">Пространственные свойства контекста, которые включают окружающий свет, окружение и предназначенную цель.</span><span class="sxs-lookup"><span data-stu-id="f1c24-336">Spatial properties of context that include ambient light, surroundings, and intended purpose.</span></span>  
    
<span data-ttu-id="f1c24-337">Чтобы включить этот эксперимент, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новый расширенный перцептивный контрастный алгоритм (APCA), заменив предыдущее отношение контраста и рекомендации  >  \*\*\*\* **AA/AAA**.</span><span class="sxs-lookup"><span data-stu-id="f1c24-337">To turn on this experiment, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable new Advanced Perceptual Contrast Algorithm (APCA) replacing previous contrast ratio and AA/AAA guidelines**.</span></span>  <span data-ttu-id="f1c24-338">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1121900][CR1121900].</span><span class="sxs-lookup"><span data-stu-id="f1c24-338">To review the history of this feature in the Chromium open-source project, navigate to Issue [1121900][CR1121900].</span></span>  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA в выборке цвета" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   <span data-ttu-id="f1c24-340">APCA в выборке цвета</span><span class="sxs-lookup"><span data-stu-id="f1c24-340">APCA in the Color Picker</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="f1c24-341">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="f1c24-341">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="f1c24-342">Если вы находитесь на Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1c24-342">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f1c24-343">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="f1c24-343">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="f1c24-344">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1c24-344">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Новые возможности в DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Просмотр соотношения контрастности текстового элемента в справочном справочнике Color Picker - Accessibility | Документы Майкрософт"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Изменение CSS — справочные | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — эмулировать двухэкранные и складные устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — эмулировать мобильные устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Производительность записи нагрузки — справочные | Документы Майкрософт"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Обзор средств разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Раздел 1 . CSS :целевая демонстрация для нового в DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229. Реализация выпадающих параметров для изменения тем | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: в том числе отладка для Microsoft Edge в качестве зависимостей | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Обновление версии Edge DevTools до 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248. Добавьте кнопки одного закрытия в панель экземпляров | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Выберите характеристики шрифта и фоновые цвета, чтобы обеспечить достаточный контраст для чтения | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Доверенные типы | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — расширение marketplace | Visual Studio Код"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR978059]: https://crbug.com/978059 "Выпуск 978059. Удаление файлов cookie при их фильтрации удалите все файлы cookie, а не только фильтрующие файлы | Ошибки Chromium"  
[CR997625]: https://crbug.com/997625 "Выпуск 997625: новая функция req | Необходимо выбрать, чтобы увидеть значение url-декодирования в файлах cookie | Ошибки Chromium"  
[CR1003629]: https://crbug.com/1003629 "Выпуск 1003629. Узел захвата больше не снимет снимок экрана узла ниже складки. | Ошибки Chromium"  
[CR1012337]: https://crbug.com/1012337 "Выпуск 1012337: Clear Site Data уничтожает сеанс Google на сайтах, не в google, | Ошибки Chromium"  
[CR1028078]: https://crbug.com/1028078 "Выпуск 1028078: в списке | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Выпуск 1054281: запрос на функции: Устройства DevTools должны подражать складным и двухэкранным устройствам | Ошибки Chromium"  
[CR1075865]: https://crbug.com/1075865 "Выпуск 1075865. Показать отброшенные кадры в графике devtools | Ошибки Chromium"  
[CR1093229]: https://crbug.com/1093229 "Выпуск 1093229: DevTools: предложение специализированного пользовательского интерфейса редактора шрифтов | Ошибки Chromium"  
[CR1121900]: https://crbug.com/1121900 "Выпуск 1121900: DevTools: обновление логики вычислений контрастности в новых спецификациях | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1122580]: https://crbug.com/1122580 "Выпуск 1122580: невозможно отключить запись сети при перезагрузке | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139949]: https://crbug.com/1139949 "Выпуск 1139949: наложение на Flexbox | Ошибки Chromium"  
[CR1147016]: https://crbug.com/1147016 "Выпуск 1147016. Выбор цвета не отображается в функции var(). | Ошибки Chromium"  
[CR1148353]: https://crbug.com/1148353 "Выпуск 1148353: запрос на функции: скопируйте объект с консоли devtools | Ошибки Chromium"  
[CR1149859]: https://crbug.com/1149859 "Выпуск 1149859: [запрос на функции][Консоль] добавьте объект копирования в элемент буфера обмена в контекстное меню | Ошибки Chromium"  
[CR1150797]: https://crbug.com/1150797 "Выпуск 1150797. Добавление меню контекста дубликатов элементов в панель Element | Ошибки Chromium"  
[CR1152391]: https://crbug.com/1152391 "Выпуск 1152391: поддержка копирования контекстного меню CSS в панели стилей | Ошибки Chromium"  
[CR1155120]: https://crbug.com/1155120 "Выпуск 1155120: [FR]Поддержка имени и номера строки | Ошибки Chromium"  
[CR1156628]: https://crbug.com/1156628 "Выпуск 1156628: DevTools: добавьте поддержку :target in force element state feature | Ошибки Chromium"  
[CR1157329]: https://crbug.com/1157329 "Выпуск 1157329: Доступность — рассказчик: Диктор не объявляет количество и положение для предложений, доступных для кода в вкладке Стили | Ошибки Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contrast (Enhanced) — способ удовлетворения WCAG (быстрая ссылка) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contrast (Minimum) — как соответствовать требованиям WCAG (быстрая ссылка) | W3C"  

> [!NOTE]
> <span data-ttu-id="f1c24-399">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1c24-399">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f1c24-400">Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/01/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="f1c24-400">The original page is found [here](https://developers.google.com/web/updates/2021/01/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f1c24-402">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1c24-402">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Местообладатель spanning"  
