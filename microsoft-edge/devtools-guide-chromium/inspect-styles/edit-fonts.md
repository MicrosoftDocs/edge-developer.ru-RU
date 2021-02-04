---
description: Узнайте, как изменить стили и параметры шрифтов CSS с помощью области стилей в Microsoft Edge DevTools.
title: Изменение стилей и параметров шрифтов CSS в области стилей в DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 928f7abb0f74839708cbe5c904ad321109ae33f0
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313306"
---
# <span data-ttu-id="50d06-104">Изменение стилей и параметров шрифтов CSS в области стилей</span><span class="sxs-lookup"><span data-stu-id="50d06-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="50d06-105">Оформление в Интернете является важной частью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="50d06-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="50d06-106">Вы хотите убедиться, что вы соответствуете рекомендациям по корпоративной фирменой марке, и содержимое будет отображаться ожидаемым образом на различных устройствах.</span><span class="sxs-lookup"><span data-stu-id="50d06-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="50d06-107">Текст должен быть легко читаться с помощью размера и высоты строки.</span><span class="sxs-lookup"><span data-stu-id="50d06-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="50d06-108">Пользователи могут менять размер шрифтов в удовлетворении индивидуальных потребностей.</span><span class="sxs-lookup"><span data-stu-id="50d06-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="50d06-109">В ситуациях, когда определенные шрифты недоступны на устройстве пользователя, следует предоставить параметры отката шрифтов.</span><span class="sxs-lookup"><span data-stu-id="50d06-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="50d06-110">CSS обеспечивает лучшую поддержку оформление в последние годы.</span><span class="sxs-lookup"><span data-stu-id="50d06-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="50d06-111">Для определения размера текста доступно множество различных единиц CSS.</span><span class="sxs-lookup"><span data-stu-id="50d06-111">There are dozens of different CSS units available to define the size of text.</span></span>  <span data-ttu-id="50d06-112">Также имеется несколько свойств CSS, которые влияют на размер шрифта, интервалы, высоту строки и другие оптические функции.</span><span class="sxs-lookup"><span data-stu-id="50d06-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="50d06-113">Чтобы упростить работу с шрифтом, визуальный \*\*\*\* редактор шрифтов теперь находится в **области** стилей.</span><span class="sxs-lookup"><span data-stu-id="50d06-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="50d06-114">Вы можете изменить параметры шрифта, и изменения немедленно отрисовыются в браузере.</span><span class="sxs-lookup"><span data-stu-id="50d06-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="50d06-115">Все без подробного знания CSS.</span><span class="sxs-lookup"><span data-stu-id="50d06-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="50d06-116">В **настоящее время средство** "Включить новый редактор шрифтов" в области стилей является экспериментальным и его необходимо включить для средств разработчика [Microsoft Edge.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="50d06-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="50d06-117">Любой CSS \*\*\*\* в области стилей, определения шрифтов или стили во время работы, автоматически отображает значок, который открывает редактор **визуальных шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="50d06-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="50d06-118">Чтобы открыть редактор **визуальных шрифтов,** выберите **значок редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="50d06-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Значок в области стилей для изменения параметров шрифта" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="50d06-120">Значок в **области** стилей для изменения параметров шрифта</span><span class="sxs-lookup"><span data-stu-id="50d06-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Редактор шрифтов, открытый в верхней части области стилей" lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="50d06-122">Редактор **шрифтов,** открытый в верхней **части** области стилей</span><span class="sxs-lookup"><span data-stu-id="50d06-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="50d06-123">Все поля в редакторе **визуальных** шрифтов заполняются значениями в CSS **в** области стилей.</span><span class="sxs-lookup"><span data-stu-id="50d06-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="50d06-124">Например, определение устанавливается в области стилей, поэтому отображается текстовое поле высоты строки, а в выпадаемом поле `line-height` `160%` \*\*\*\* `160` `%` единицы.</span><span class="sxs-lookup"><span data-stu-id="50d06-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="50d06-125">Кроме того, ползунок автоматически устанавливается в соответствие со значениями текстового поля.</span><span class="sxs-lookup"><span data-stu-id="50d06-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="50d06-126">Редактор **шрифтов** состоит из двух частей: селектора семейства шрифтов и редактора свойств CSS.</span><span class="sxs-lookup"><span data-stu-id="50d06-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <span data-ttu-id="50d06-127">Выбор семейства шрифтов</span><span class="sxs-lookup"><span data-stu-id="50d06-127">The Font Family selector</span></span>  

<span data-ttu-id="50d06-128">Селектор семейства шрифтов является верхней частью визуального **редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="50d06-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="50d06-129">Чтобы выбрать шрифты правила CSS, в редакторе CSS используйте селектор **семейства** шрифтов.</span><span class="sxs-lookup"><span data-stu-id="50d06-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="50d06-130">Для каждого правила CSS можно выбрать основной и откатный шрифты.</span><span class="sxs-lookup"><span data-stu-id="50d06-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Редактор шрифтов, открытый в верхней части области стилей с выделенной селектором семейства шрифтов" lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="50d06-132">Редактор **шрифтов,** открытый в верхней части области **стилей** с **выделенной селектором** семейства шрифтов</span><span class="sxs-lookup"><span data-stu-id="50d06-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="50d06-133">Выберите **один из списков** шрифтов в выпаданом списке "Семейство шрифтов".</span><span class="sxs-lookup"><span data-stu-id="50d06-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="50d06-134">Шрифты организованы в четыре группы.</span><span class="sxs-lookup"><span data-stu-id="50d06-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="50d06-135">Вычисленные шрифты, которые являются шрифтами, доступными в таблице стилей **в** области стилей.</span><span class="sxs-lookup"><span data-stu-id="50d06-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="50d06-136">Системные шрифты, которые являются шрифтами, доступными в текущей операционной системе.</span><span class="sxs-lookup"><span data-stu-id="50d06-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="50d06-137">Универсальные семейства шрифтов, например `serif` или `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="50d06-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="50d06-138">Глобальные значения, такие как `inherit` , `initial` и `unset` .</span><span class="sxs-lookup"><span data-stu-id="50d06-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Редактор шрифтов, открытый в верхней части области стилей с выделенной селектором семейства шрифтов" lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="50d06-140">Редактор **шрифтов,** открытый в верхней части области **стилей** с **выделенной селектором** семейства шрифтов</span><span class="sxs-lookup"><span data-stu-id="50d06-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="50d06-141">После выбора шрифта отобразится еще одно меню для выбора фона.</span><span class="sxs-lookup"><span data-stu-id="50d06-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="50d06-142">Можно выбрать до восьми шрифтов для отката.</span><span class="sxs-lookup"><span data-stu-id="50d06-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="50d06-143">Чтобы удалить шрифт, выберите значок **"Удалить семейство** шрифтов".</span><span class="sxs-lookup"><span data-stu-id="50d06-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="50d06-144">Если вы выберете глобальное значение для семейства шрифтов, вы не получите еще одно dropdown, так как в CSS для него нет отката.</span><span class="sxs-lookup"><span data-stu-id="50d06-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <span data-ttu-id="50d06-145">Редактор свойств CSS</span><span class="sxs-lookup"><span data-stu-id="50d06-145">The CSS Properties editor</span></span>  

<span data-ttu-id="50d06-146">Свойства шрифта CSS можно изменить в нижней части редактора **визуальных шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="50d06-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="50d06-147">Вы можете изменить размер шрифта, высоту строки, вес шрифта и интервалы букв с помощью любого из элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="50d06-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="50d06-148">Изменения применяются непосредственно в браузере.</span><span class="sxs-lookup"><span data-stu-id="50d06-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Редактор шрифтов, открытый в верхней части области стилей с выделенными свойствами CSS" lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="50d06-150">Редактор **шрифтов,** открытый \*\*\*\* в верхней части области стилей с выделенными свойствами CSS</span><span class="sxs-lookup"><span data-stu-id="50d06-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="50d06-151">Вы также можете преобразовать единицы CSS с помощью редактора **визуальных шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="50d06-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="50d06-152">Например, вы можете использовать это средство в правиле CSS, где ползунок **"Размер** шрифта" изначально установлен в качестве `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="50d06-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="50d06-153">Теперь используйте dropdown единиц и выберите `em` значение.</span><span class="sxs-lookup"><span data-stu-id="50d06-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="50d06-154">Отображается `1 em` равным `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="50d06-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Изменение размера шрифта на 16 пикселей" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="50d06-156">Измените размер шрифта на</span><span class="sxs-lookup"><span data-stu-id="50d06-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Откройте dropdown единицы для преобразования в em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="50d06-158">Откройте dropdown единицы для преобразования в</span><span class="sxs-lookup"><span data-stu-id="50d06-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="50d06-159">В этом подразделении доступны все доступные числимые единицы CSS.</span><span class="sxs-lookup"><span data-stu-id="50d06-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="50d06-160">Размер шрифта, высота строки, вес шрифта и интервалы используются разными единицами.</span><span class="sxs-lookup"><span data-stu-id="50d06-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="50d06-161">Если в текстовых полях есть фокус, вы можете выбрать клавиши и клавиши для точной настройки `arrow up` `arrow down` параметров.</span><span class="sxs-lookup"><span data-stu-id="50d06-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="50d06-162">Чтобы использовать ползунки с клавиатурой, выберите `arrow left` клавиши и `arrow down` клавиши.</span><span class="sxs-lookup"><span data-stu-id="50d06-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="50d06-163">Редактор свойств CSS также содержит предустановленные ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="50d06-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="50d06-164">Чтобы использовать предустановленные ключевые слова, в правой части выберите `Toggle Input Type` значок.</span><span class="sxs-lookup"><span data-stu-id="50d06-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="50d06-165">Отображается изменение пользовательского интерфейса и выпадение готовых ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="50d06-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="50d06-166">Чтобы вернуться к пользовательскому интерфейсу с ползуноком и другими элементами управления пользовательского интерфейса, снова выберите `Toggle Input Type` значок.</span><span class="sxs-lookup"><span data-stu-id="50d06-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Открытие предустановленного интерфейса ключевых слов" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="50d06-168">Открытие предустановленного интерфейса ключевых слов</span><span class="sxs-lookup"><span data-stu-id="50d06-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <span data-ttu-id="50d06-169">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="50d06-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Включить экспериментальные функции — экспериментальные | Документы Майкрософт"  
