---
description: Узнайте, как изменить стили и параметры шрифтов CSS с помощью области стилей в Microsoft Edge DevTools.
title: Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439495"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a><span data-ttu-id="a9154-104">Изменение стилей и параметров шрифтов CSS в области Стилей</span><span class="sxs-lookup"><span data-stu-id="a9154-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="a9154-105">Типография в Интернете является важной частью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a9154-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="a9154-106">Необходимо убедиться, что вы соответствуете корпоративным рекомендациям по бренду, а содержимое отображается как ожидалось на различных устройствах.</span><span class="sxs-lookup"><span data-stu-id="a9154-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="a9154-107">Текст должен быть простым для чтения с помощью размера и высоты строки.</span><span class="sxs-lookup"><span data-stu-id="a9154-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="a9154-108">Пользователи могут повторно размеры шрифтов для удовлетворения индивидуальных потребностей.</span><span class="sxs-lookup"><span data-stu-id="a9154-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="a9154-109">В ситуациях, когда конкретные шрифты недоступны на устройстве пользователя, необходимо предоставить параметры откатных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a9154-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="a9154-110">CSS обеспечивает лучшую поддержку типографии в последние годы.</span><span class="sxs-lookup"><span data-stu-id="a9154-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="a9154-111">Для определения размера текста доступны десятки различных подразделений CSS.</span><span class="sxs-lookup"><span data-stu-id="a9154-111">Dozens of different CSS units are available to define the size of text.</span></span>  <span data-ttu-id="a9154-112">Кроме того, у вас есть несколько свойств CSS, которые влияют на размер шрифта, интервалы, высоту строки и другие типографические функции.</span><span class="sxs-lookup"><span data-stu-id="a9154-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="a9154-113">Чтобы упростить работу с типографией, визуальный \*\*\*\* редактор шрифтов теперь находится в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a9154-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="a9154-114">Вы можете изменить параметры шрифта, и изменения будут немедленно отрисовки в браузере.</span><span class="sxs-lookup"><span data-stu-id="a9154-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="a9154-115">Все без глубоких знаний о CSS.</span><span class="sxs-lookup"><span data-stu-id="a9154-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="a9154-116">В настоящее время эта функция является экспериментальной, и ее необходимо **Enable new font editor tool within the Styles pane** включить для Microsoft Edge Developer [Tools.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="a9154-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="a9154-117">Любой CSS в области **Стилей,** определения шрифтов или стили в линию, автоматически отображает значок, открываю визуальный **редактор шрифта.**</span><span class="sxs-lookup"><span data-stu-id="a9154-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="a9154-118">Чтобы открыть визуальный **редактор шрифта,** выберите **значок Редактор шрифта.**</span><span class="sxs-lookup"><span data-stu-id="a9154-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Значок в области Стилей для редактирования параметров шрифта" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="a9154-120">Значок в области **Стилей** для редактирования параметров шрифта</span><span class="sxs-lookup"><span data-stu-id="a9154-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей" lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="a9154-122">Редактор **шрифта,** открытый поверх области **Стилей**</span><span class="sxs-lookup"><span data-stu-id="a9154-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a9154-123">Все поля в редакторе **визуальных шрифтов** заполняются из значений в CSS в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a9154-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="a9154-124">Например, определение установлено в области Стилей, поэтому текстовое поле высоты строки отображает и отобразит отсев `line-height` `160%` \*\*\*\* `160` `%` единицы.</span><span class="sxs-lookup"><span data-stu-id="a9154-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="a9154-125">Кроме того, ползунок автоматически устанавливается в соответствие со значениями текстового поля.</span><span class="sxs-lookup"><span data-stu-id="a9154-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="a9154-126">Редактор **шрифта** состоит из двух частей: селектора семейства шрифтов и редактора свойств CSS.</span><span class="sxs-lookup"><span data-stu-id="a9154-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <a name="the-font-family-selector"></a><span data-ttu-id="a9154-127">Селектор семейства шрифтов</span><span class="sxs-lookup"><span data-stu-id="a9154-127">The Font Family selector</span></span>  

<span data-ttu-id="a9154-128">Селектор семейства шрифтов — верхняя часть визуального **редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="a9154-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="a9154-129">Чтобы выбрать шрифты правила CSS, в редакторе CSS используйте селектор **семейства** шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a9154-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="a9154-130">Для каждого правила CSS можно выбрать основные и откатные шрифты.</span><span class="sxs-lookup"><span data-stu-id="a9154-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенным селектором семейства шрифтов" lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="a9154-132">Редактор **шрифта,** открытый поверх области **Стилей** с выделенным селектором **семейства** шрифтов</span><span class="sxs-lookup"><span data-stu-id="a9154-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="a9154-133">Используйте **отсев семейства** шрифтов, чтобы выбрать из списка шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a9154-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="a9154-134">Шрифты организованы в четыре группы.</span><span class="sxs-lookup"><span data-stu-id="a9154-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="a9154-135">Вычислительные шрифты, которые являются шрифтами, доступными в таблице стилей в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a9154-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="a9154-136">Системные шрифты, которые являются шрифтами, доступными в текущей операционной системе.</span><span class="sxs-lookup"><span data-stu-id="a9154-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="a9154-137">Общие семейства шрифтов, например `serif` или `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="a9154-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="a9154-138">Глобальные значения, такие как `inherit` `initial` , и `unset` .</span><span class="sxs-lookup"><span data-stu-id="a9154-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенным селектором семейства шрифтов" lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="a9154-140">Редактор **шрифта,** открытый поверх области **Стилей** с выделенным селектором **семейства** шрифтов</span><span class="sxs-lookup"><span data-stu-id="a9154-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="a9154-141">После выбора шрифта отображается еще одно выпадение меню для выбора откатных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a9154-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="a9154-142">Вы можете выбрать до восьми откатных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a9154-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="a9154-143">Чтобы удалить шрифт, выберите **значок Delete Font Family.**</span><span class="sxs-lookup"><span data-stu-id="a9154-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="a9154-144">Если вы выбираете глобальное значение для семейства шрифтов, вы не получите еще одного отката, так как в CSS нет отката для него.</span><span class="sxs-lookup"><span data-stu-id="a9154-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <a name="the-css-properties-editor"></a><span data-ttu-id="a9154-145">Редактор CSS Properties</span><span class="sxs-lookup"><span data-stu-id="a9154-145">The CSS Properties editor</span></span>  

<span data-ttu-id="a9154-146">Свойства шрифта CSS можно изменить в нижней части визуального **редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="a9154-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="a9154-147">Можно изменить размер шрифта, высоту строки, вес шрифта и интервал между буквами с помощью любого из элементов управления пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="a9154-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="a9154-148">Изменения применяются немедленно в браузере.</span><span class="sxs-lookup"><span data-stu-id="a9154-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенными свойствами CSS" lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="a9154-150">Редактор **шрифта,** открытый поверх области **Стилей** с выделенными свойствами CSS</span><span class="sxs-lookup"><span data-stu-id="a9154-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="a9154-151">Кроме того, можно преобразовать подразделения CSS с помощью визуального **редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="a9154-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="a9154-152">Например, вы можете использовать средство в правиле CSS, в котором изначально установлен ползунок **размер** шрифта `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="a9154-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="a9154-153">Теперь используйте выпадаемую единицу и выберите значение `em` .</span><span class="sxs-lookup"><span data-stu-id="a9154-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="a9154-154">`1 em`Отображаемая равна `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="a9154-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Изменение размера шрифта до 16 пикселей" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="a9154-156">Изменение размера шрифта на</span><span class="sxs-lookup"><span data-stu-id="a9154-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Откройте выпадаемую единицу для преобразования в em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="a9154-158">Откройте выпадаемую единицу для преобразования в</span><span class="sxs-lookup"><span data-stu-id="a9154-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a9154-159">В отсеве единицы доступны все доступные числимые единицы CSS.</span><span class="sxs-lookup"><span data-stu-id="a9154-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="a9154-160">Размер шрифта, высота строки, вес шрифта и интервалы использования различных единиц.</span><span class="sxs-lookup"><span data-stu-id="a9154-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="a9154-161">Если в текстовых полях фокусируется, можно выбрать клавиши и клавиши для настройки `arrow up` `arrow down` параметров.</span><span class="sxs-lookup"><span data-stu-id="a9154-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="a9154-162">Чтобы использовать ползунки с клавиатурой, выберите `arrow left` клавиши и `arrow down` клавиши.</span><span class="sxs-lookup"><span data-stu-id="a9154-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="a9154-163">Редактор CSS Properties также содержит заранее.</span><span class="sxs-lookup"><span data-stu-id="a9154-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="a9154-164">Чтобы использовать заранее задатки ключевых слов, справа выберите `Toggle Input Type` значок.</span><span class="sxs-lookup"><span data-stu-id="a9154-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="a9154-165">Отображаются изменения пользовательского интерфейса и отсев предустановленных ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="a9154-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="a9154-166">Чтобы вернуться к пользовательскому интерфейсу с помощью ползунок и других элементов управления пользовательским интерфейсом, выберите `Toggle Input Type` значок снова.</span><span class="sxs-lookup"><span data-stu-id="a9154-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Откройте предустановленный интерфейс ключевого слова" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="a9154-168">Откройте предустановленный интерфейс ключевого слова</span><span class="sxs-lookup"><span data-stu-id="a9154-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a9154-169">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a9154-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
