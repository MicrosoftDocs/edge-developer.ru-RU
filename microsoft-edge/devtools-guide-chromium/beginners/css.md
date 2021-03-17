---
description: Начало работы с CSS
title: 'DevTools для начинающих: начало работы с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools
ms.openlocfilehash: 6a7135e144123917535e7c43e6a3cd608ec0c8a7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439439"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-css"></a><span data-ttu-id="56ff8-104">DevTools для начинающих: начало работы с CSS</span><span class="sxs-lookup"><span data-stu-id="56ff8-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="56ff8-105">В этом руководстве вы узнаете, как использовать CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="56ff8-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="56ff8-106">Вы также узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.</span><span class="sxs-lookup"><span data-stu-id="56ff8-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="56ff8-107">Следующая статья — это второй учебник из серии учебников, который учит вас основам веб-разработки и Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="56ff8-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="56ff8-108">Вы получаете практический опыт, фактически построив собственный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="56ff8-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="56ff8-109">Вам не нужно завершить первый учебник, прежде чем следовать второму.</span><span class="sxs-lookup"><span data-stu-id="56ff8-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="56ff8-110">[Настройка кода показывает,](#set-up-your-code) как настроиться.</span><span class="sxs-lookup"><span data-stu-id="56ff8-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="56ff8-111">Этот учебник предназначен для абсолютных новичков \*\*\*\* и посвящен основам веб-разработки и основам использования DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="56ff8-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="56ff8-112">Если вы хотите учебник, который фокусируется только на DevTools, перейдите к началу просмотра и [изменения CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="56ff8-112">If you want a tutorial that only focuses on DevTools, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="56ff8-113">В начале учебника ваш сайт должен выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="56ff8-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Как выглядит ваш сайт в настоящее время" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="56ff8-115">Как выглядит ваш сайт в настоящее время</span><span class="sxs-lookup"><span data-stu-id="56ff8-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="56ff8-116">После завершения руководства сайт должен выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="56ff8-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Как должен выглядеть ваш сайт в конце учебника" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="56ff8-118">Как должен выглядеть ваш сайт в конце учебника</span><span class="sxs-lookup"><span data-stu-id="56ff8-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <a name="goals"></a><span data-ttu-id="56ff8-119">Цели</span><span class="sxs-lookup"><span data-stu-id="56ff8-119">Goals</span></span>  

<span data-ttu-id="56ff8-120">Следуйте этому учебнику, чтобы лучше понять следующие понятия и задачи.</span><span class="sxs-lookup"><span data-stu-id="56ff8-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="56ff8-121">Использование CSS для стиля веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="56ff8-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="56ff8-122">Использование Microsoft Edge DevTools для экспериментов с CSS.</span><span class="sxs-lookup"><span data-stu-id="56ff8-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="56ff8-123">Разница между CSS и CSS frameworks.</span><span class="sxs-lookup"><span data-stu-id="56ff8-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="56ff8-124">Вы строите реальный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="56ff8-124">You are building a real website.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="56ff8-125">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="56ff8-125">Prerequisites</span></span>  

<span data-ttu-id="56ff8-126">Перед попыткой этого руководства выполните следующие необходимые условия.</span><span class="sxs-lookup"><span data-stu-id="56ff8-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="56ff8-127">Полное начало работы с HTML и [DOM][DevtoolsBeginnersHtml] или убедитесь, что у вас есть понимание HTML и DOM аналогично тому, что преподается в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="56ff8-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="56ff8-128">Скачайте [веб-браузер Microsoft Edge.][MicrosoftEdgeInsider]</span><span class="sxs-lookup"><span data-stu-id="56ff8-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="56ff8-129">В следующем руководстве используется набор средств веб-разработки, называемых Microsoft Edge DevTools, встроенных в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="56ff8-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="56ff8-130">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="56ff8-130">Set up your code</span></span>  

<span data-ttu-id="56ff8-131">Чтобы создать свой сайт, сначала необходимо выполнить следующие действия, чтобы настроить код.</span><span class="sxs-lookup"><span data-stu-id="56ff8-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="56ff8-132">Если вы уже завершили первый учебник в этой серии, переехав в следующий раздел.</span><span class="sxs-lookup"><span data-stu-id="56ff8-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="56ff8-133">Продолжить использование кода из последнего учебника, [начало работы с HTML и DOM][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="56ff8-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="56ff8-134">Откройте [исходный код.][GlitchCookedAmphibianIndex]</span><span class="sxs-lookup"><span data-stu-id="56ff8-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="56ff8-135">Вкладка в фокусе браузера ссылается на вкладку **редактирования.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Вкладка редактирования" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="56ff8-137">Вкладка **редактирования**</span><span class="sxs-lookup"><span data-stu-id="56ff8-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-138">Выберите **вареную амфибию.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="56ff8-139">Всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="56ff8-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Меню Параметры проекта" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="56ff8-141">Меню Параметры проекта</span><span class="sxs-lookup"><span data-stu-id="56ff8-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="56ff8-142">Выберите **Проект Remix**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="56ff8-143">Сбой создает копию проекта, которую можно изменить.</span><span class="sxs-lookup"><span data-stu-id="56ff8-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="56ff8-144">Сбой создает случайное имя для нового проекта.</span><span class="sxs-lookup"><span data-stu-id="56ff8-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="56ff8-145">Выберите **Показать** и **выбрать в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-145">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="56ff8-146">Откроется еще одна вкладка с живым представлением сайта.</span><span class="sxs-lookup"><span data-stu-id="56ff8-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="56ff8-147">Вкладка в фокусе браузера ссылается на вкладку **live.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Вкладка live" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="56ff8-149">Вкладка **live**</span><span class="sxs-lookup"><span data-stu-id="56ff8-149">The **live tab**</span></span>  
    :::image-end:::  

## <a name="understand-css"></a><span data-ttu-id="56ff8-150">Понимание CSS</span><span class="sxs-lookup"><span data-stu-id="56ff8-150">Understand CSS</span></span>  

<span data-ttu-id="56ff8-151">**CSS** — это компьютерный язык, который определяет макет и стиль веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="56ff8-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="56ff8-152">Следующая фигура — абзац с границей.</span><span class="sxs-lookup"><span data-stu-id="56ff8-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Текст стилизовылся с помощью CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="56ff8-154">Текст стилизовылся с помощью CSS</span><span class="sxs-lookup"><span data-stu-id="56ff8-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="56ff8-155">Следующий фрагмент кода — код HTML и CSS, используемый для создания абзаца на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="56ff8-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="56ff8-156">вероятно, выглядит новым для вас.</span><span class="sxs-lookup"><span data-stu-id="56ff8-156">probably looks new to you.</span></span>  <span data-ttu-id="56ff8-157">Остальные должны выглядеть знакомыми.</span><span class="sxs-lookup"><span data-stu-id="56ff8-157">The rest should look familiar.</span></span>  <span data-ttu-id="56ff8-158">Если нет, выполните начало работы с HTML и [DOM,][DevtoolsBeginnersHtml] прежде чем пытаться выполнить следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="56ff8-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <a name="add-inline-styles"></a><span data-ttu-id="56ff8-159">Добавление встройных стилей</span><span class="sxs-lookup"><span data-stu-id="56ff8-159">Add inline styles</span></span>  

<span data-ttu-id="56ff8-160">Выполните следующие действия, чтобы использовать стили **для** применения стилей к одному элементу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="56ff8-161">Вернуться на вкладку редактирования и открыть `index.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="56ff8-163">Откройте `index.html` на вкладке редактирования</span><span class="sxs-lookup"><span data-stu-id="56ff8-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-164">Добавьте `style="background-color: aliceblue;"` к вашему `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="56ff8-165">В блоке кода ниже четвертая строка кода — это строка, которая должна измениться.</span><span class="sxs-lookup"><span data-stu-id="56ff8-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="56ff8-166">Остальное только там, поэтому вы можете убедиться, что вы ставите новый код в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="56ff8-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="56ff8-167">Чтобы отобразить изменения, перейдите на **вкладку live.**  Фон раздела `<nav>` теперь синий.</span><span class="sxs-lookup"><span data-stu-id="56ff8-167">To display the changes, navigate to the **live tab**.  The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Фоновый цвет ссылок дома и контактов теперь синий" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="56ff8-169">Фоновый цвет ссылок **дома** и **контактов** теперь синий</span><span class="sxs-lookup"><span data-stu-id="56ff8-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a><span data-ttu-id="56ff8-170">Повторное использование стилей на одной странице с внутренними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="56ff8-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="56ff8-171">В предыдущем фрагменте кода вложенный стиль применял стиль к одному `<p>` тегу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="56ff8-172">Что делать, если вы хотите, чтобы все элементы на вашей веб-странице были одинаково `<p>` стили.</span><span class="sxs-lookup"><span data-stu-id="56ff8-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="56ff8-173">Код необходимо скопировать и вклеить в каждый `<p>` тег на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="56ff8-173">You have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="56ff8-174">Это много времени и усилий.</span><span class="sxs-lookup"><span data-stu-id="56ff8-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="56ff8-175">И, если вам нужно сделать изменение, вам придется изменить каждый тег снова.</span><span class="sxs-lookup"><span data-stu-id="56ff8-175">And, if you needed to make an edit, you have to change every tag again.</span></span>  <span data-ttu-id="56ff8-176">Выполните следующие действия, чтобы использовать **таблицу внутренних** стилей для записи CSS один раз, чтобы она применяла к нескольким элементам.</span><span class="sxs-lookup"><span data-stu-id="56ff8-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="56ff8-177">На вкладке в прямом эфире **выберите Контакт,** чтобы перейти на контактную страницу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-177">In the live tab, choose **Contact** to navigate to the contact page.</span></span>  <span data-ttu-id="56ff8-178">Обратите внимание на шрифт **Дома и** **Контакта.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Страница Контакт" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="56ff8-180">Страница Контакт</span><span class="sxs-lookup"><span data-stu-id="56ff8-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-181">На **вкладке редактор откройте** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-181">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="56ff8-182">Добавьте следующий код в `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="56ff8-183">Помните, что строки, начиная с и `<style>` `</style>` заканчивая, это то, что нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="56ff8-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="56ff8-184">Другой код только там, чтобы вы знали, куда поместить новый код.</span><span class="sxs-lookup"><span data-stu-id="56ff8-184">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="56ff8-185">Возвращайся к **вкладке live.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="56ff8-186">Выберите **Контакт,** чтобы вернуться на контактную страницу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="56ff8-187">Изменен шрифт **Дома и** **Контакта.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Изменен шрифт ссылок дома и контактов" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="56ff8-189">Изменен шрифт ссылок **дома** и **контактов**</span><span class="sxs-lookup"><span data-stu-id="56ff8-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a><span data-ttu-id="56ff8-190">Понимание внутренних таблиц стилей</span><span class="sxs-lookup"><span data-stu-id="56ff8-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="56ff8-191">Внутренние таблицы стилей применяют стили с помощью **селекторов.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="56ff8-192">Селекторы — это шаблоны, которые могут применяться к одному или более элементам HTML.</span><span class="sxs-lookup"><span data-stu-id="56ff8-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="56ff8-193">Предыдущий фрагмент кода добавил следующий стиль.</span><span class="sxs-lookup"><span data-stu-id="56ff8-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="56ff8-194">является селектором, который переводится как "любой `<li>` элемент, содержащий `<a>` элемент".</span><span class="sxs-lookup"><span data-stu-id="56ff8-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="56ff8-195">Браузер меняет шрифт ссылок **"Дома"** и **"Контакт",** так как каждая из групп тегов соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="56ff8-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="56ff8-196">является **объявлением**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-196">is a **declaration**.</span></span>  <span data-ttu-id="56ff8-197">Объявление состоит из следующих двух частей.</span><span class="sxs-lookup"><span data-stu-id="56ff8-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="56ff8-198">свойство</span><span class="sxs-lookup"><span data-stu-id="56ff8-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="56ff8-199">Свойство описывает общий способ изменения стиля элемента.</span><span class="sxs-lookup"><span data-stu-id="56ff8-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="56ff8-200">value</span><span class="sxs-lookup"><span data-stu-id="56ff8-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="56ff8-201">В значении описывается, как именно должен меняться стиль элемента.</span><span class="sxs-lookup"><span data-stu-id="56ff8-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="56ff8-202">Например, `font-family: 'Courier New', Courier, serif` дает браузеру следующую инструкцию: "Установите шрифт элементов, которые соответствуют `li a` шаблону `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="56ff8-203">Если этот шрифт не доступен, используйте `Courier` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="56ff8-204">Если это не доступно, используйте `serif` ."</span><span class="sxs-lookup"><span data-stu-id="56ff8-204">If that is not available, use `serif`."</span></span>  

### <a name="add-multiple-selectors-to-a-ruleset"></a><span data-ttu-id="56ff8-205">Добавление нескольких селекторов в правило</span><span class="sxs-lookup"><span data-stu-id="56ff8-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="56ff8-206">Блок кода CSS, как и следующий фрагмент кода, называется **правилом.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-206">A block of CSS code like the following code snippet is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="56ff8-207">Выполните следующие действия, чтобы использовать запятые для добавления нескольких селекторов в список правил.</span><span class="sxs-lookup"><span data-stu-id="56ff8-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="56ff8-208">На **вкладке редактор откройте** `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="56ff8-209">После `li a` введите `, h1` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="56ff8-210">Предыдущий фрагмент кода сообщает браузеру о стиле элементов так же, как он стили `<h1>` элементов, которые соответствуют шаблону `li a` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="56ff8-211">Перейдите на **вкладку в прямом эфире.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-211">Navigate to the **live tab**.</span></span>  
1.  <span data-ttu-id="56ff8-212">Выберите **контактную** ссылку, чтобы вернуться на контактную страницу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="56ff8-213">Теперь **свяжитесь со мной!**</span><span class="sxs-lookup"><span data-stu-id="56ff8-213">Now, **Contact Me!**</span></span> <span data-ttu-id="56ff8-214">имеет тот же шрифт, что и ссылки на навигацию.</span><span class="sxs-lookup"><span data-stu-id="56ff8-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Текст Свяжитесь со мной!  теперь имеет тот же шрифт, что и ссылки Home и Contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="56ff8-217">Текст **Свяжитесь со мной!**</span><span class="sxs-lookup"><span data-stu-id="56ff8-217">The text **Contact Me!**</span></span> <span data-ttu-id="56ff8-218">теперь имеет тот же шрифт, что и **ссылки Home** и **Contact**</span><span class="sxs-lookup"><span data-stu-id="56ff8-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a><span data-ttu-id="56ff8-219">Эксперимент с DevTools</span><span class="sxs-lookup"><span data-stu-id="56ff8-219">Experiment with DevTools</span></span>  

<span data-ttu-id="56ff8-220">По мере того как вы продолжите свое путешествие, чтобы стать экспертом в веб-разработке, вы можете обнаружить, что CSS является сложной.</span><span class="sxs-lookup"><span data-stu-id="56ff8-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="56ff8-221">Вы можете написать некоторые CSS и ожидать его отображения в одну сторону, но браузер делает что-то совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="56ff8-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="56ff8-222">Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно отображает влияние изменений на страницу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately display how the changes affect the page.</span></span>  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a><span data-ttu-id="56ff8-223">Добавление объявления к существующему правилу в DevTools</span><span class="sxs-lookup"><span data-stu-id="56ff8-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="56ff8-224">Выполните следующие действия, чтобы итерировать стиль существующего элемента, добавьте объявление в существующий список правил.</span><span class="sxs-lookup"><span data-stu-id="56ff8-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="56ff8-225">Наведите курсор на **ссылку Главная,** откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-225">Hover on the **Home** link, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Проверка домашней ссылки" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="56ff8-227">Проверка домашней ссылки</span><span class="sxs-lookup"><span data-stu-id="56ff8-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="56ff8-228">DevTools открывается рядом со своей страницей.</span><span class="sxs-lookup"><span data-stu-id="56ff8-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="56ff8-229">Код, который представляет ссылку Главная, выделен синим `<a href="/">Home</a>` цветом в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="56ff8-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="56ff8-230">Фрагмент кода и предварительный просмотр должны быть знакомы в [get Started с HTML и DOM.][DevtoolsBeginnersHtml]</span><span class="sxs-lookup"><span data-stu-id="56ff8-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="56ff8-231">На следующем рисунке объявление, к которое вы ранее добавили, отображается на вкладке `font-family: 'Courier New', Courier, serif` `contact.html` **Стили** ниже дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="56ff8-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is displayed in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Вкладка Стили находится ниже дерева DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="56ff8-233">Вкладка **Стили** находится ниже дерева DOM</span><span class="sxs-lookup"><span data-stu-id="56ff8-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="56ff8-234">Если окно DevTools широкое, вкладка Styles находится справа от дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="56ff8-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Вкладка Styles находится справа от дерева DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="56ff8-236">Вкладка **Styles** находится справа от дерева DOM</span><span class="sxs-lookup"><span data-stu-id="56ff8-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="56ff8-237">Выберите пустую строку `font-family: 'Courier New', Courier, Serif` ниже, чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="56ff8-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Добавление нового объявления" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="56ff8-239">Добавление нового объявления</span><span class="sxs-lookup"><span data-stu-id="56ff8-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-240">Введите `color` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="56ff8-241">Пользовательский интерфейс автокомплекта предлагает варианты при введите.</span><span class="sxs-lookup"><span data-stu-id="56ff8-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Цвет типа" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="56ff8-243">Тип</span><span class="sxs-lookup"><span data-stu-id="56ff8-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-244">Введите `magenta` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="56ff8-245">Весь текст на странице контакта теперь пурпурный.</span><span class="sxs-lookup"><span data-stu-id="56ff8-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Тип magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="56ff8-247">Тип</span><span class="sxs-lookup"><span data-stu-id="56ff8-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a><span data-ttu-id="56ff8-248">Изменение объявления в DevTools</span><span class="sxs-lookup"><span data-stu-id="56ff8-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="56ff8-249">Выполните следующие действия по редактированию существующих деклараций в DevTools.</span><span class="sxs-lookup"><span data-stu-id="56ff8-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="56ff8-250">Выберите квадрат magenta рядом `magenta` с .</span><span class="sxs-lookup"><span data-stu-id="56ff8-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="56ff8-251">Всплывет подбиратель цветов.</span><span class="sxs-lookup"><span data-stu-id="56ff8-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Выбор цвета" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="56ff8-253">Выбор цвета</span><span class="sxs-lookup"><span data-stu-id="56ff8-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-254">Используйте выборщик цвета, чтобы изменить текст шрифта на цвет, который вам нравится.</span><span class="sxs-lookup"><span data-stu-id="56ff8-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Измените цвет шрифта на фиолетовый с помощью цвета Picker" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="56ff8-256">Измените цвет шрифта на фиолетовый с помощью цвета Picker</span><span class="sxs-lookup"><span data-stu-id="56ff8-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a><span data-ttu-id="56ff8-257">Добавление нового правила в DevTools</span><span class="sxs-lookup"><span data-stu-id="56ff8-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="56ff8-258">Выполните следующие действия, чтобы добавить новые правила в DevTools.</span><span class="sxs-lookup"><span data-stu-id="56ff8-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="56ff8-259">Выберите **новое правило** стиля \( Новое правило стиля ![ ](../media/new-style-rule-icon.msft.png) \), которое находится рядом с **.cls**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-259">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) which is next to **.cls**.</span></span>  <span data-ttu-id="56ff8-260">Пустой регламент отображается в `a` качестве селектора.</span><span class="sxs-lookup"><span data-stu-id="56ff8-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Добавление нового правила" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="56ff8-262">Добавление нового правила</span><span class="sxs-lookup"><span data-stu-id="56ff8-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-263">Замените `a` `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Замените a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="56ff8-265">Замените `a` на</span><span class="sxs-lookup"><span data-stu-id="56ff8-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="56ff8-266">является **псевдоклассом.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="56ff8-267">Используйте псевдо-классы для элементов стиля, которые могут вводить особые состояния.</span><span class="sxs-lookup"><span data-stu-id="56ff8-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="56ff8-268">Например, стиль вступает в силу только при наведении над `a:hover` `<a>` элементом.</span><span class="sxs-lookup"><span data-stu-id="56ff8-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="56ff8-269">Выберите между скобками, чтобы добавить новое объявление.</span><span class="sxs-lookup"><span data-stu-id="56ff8-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="56ff8-270">Введите `background-color` имя объявления и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Тип фонового цвета" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="56ff8-272">Тип</span><span class="sxs-lookup"><span data-stu-id="56ff8-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-273">Введите `green` значение объявления и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Введите зеленый цвет" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="56ff8-275">Тип</span><span class="sxs-lookup"><span data-stu-id="56ff8-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-276">Наведите курсор мыши по **ссылке Главная.**</span><span class="sxs-lookup"><span data-stu-id="56ff8-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="56ff8-277">Фон ссылки становится зеленым.</span><span class="sxs-lookup"><span data-stu-id="56ff8-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Наведите курсор на ссылку Главная, чтобы показать ее зеленый фон" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="56ff8-279">Наведите курсор на ссылку Главная, чтобы показать ее зеленый фон</span><span class="sxs-lookup"><span data-stu-id="56ff8-279">Hover on the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a><span data-ttu-id="56ff8-280">Повторное использование стилей на страницах с внешними таблицами стилей</span><span class="sxs-lookup"><span data-stu-id="56ff8-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="56ff8-281">На предыдущем этапе в таблицу внутренних стилей добавлен следующий фрагмент `contact.html` кода.</span><span class="sxs-lookup"><span data-stu-id="56ff8-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="56ff8-282">Что делать, если вы хотите стиль `index.html` таким же образом?</span><span class="sxs-lookup"><span data-stu-id="56ff8-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="56ff8-283">Что делать, если у вас есть большое количество страниц, на которые вы хотите применить стили?</span><span class="sxs-lookup"><span data-stu-id="56ff8-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="56ff8-284">Необходимо скопировать и вклеить таблицу внутренних стилей на каждую веб-страницу на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="56ff8-284">You have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="56ff8-285">Выполните следующие действия, чтобы добавить таблицу **внешних** стилей, чтобы позволить вам написать CSS один раз и применить его к нескольким страницам.</span><span class="sxs-lookup"><span data-stu-id="56ff8-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="56ff8-286">Сначала обновите вкладку в прямом эфире, чтобы удалить изменения, внесенные в DevTools.</span><span class="sxs-lookup"><span data-stu-id="56ff8-286">First, refresh the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" После обновления страницы изменения, внесенные в DevTools, исчезли" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="56ff8-288">После обновления страницы изменения, внесенные в DevTools, исчезли</span><span class="sxs-lookup"><span data-stu-id="56ff8-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-289">Возвращайся на **вкладку редактора и** открывай `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="56ff8-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="56ff8-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-292">Удаление всего `<style>` между и , в том числе и `</style>` `<style>` `</style>` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Тег стиля удален" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="56ff8-294">Тег стиля удален</span><span class="sxs-lookup"><span data-stu-id="56ff8-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-295">Откройте `index.html` и `style="background-color: aliceblue;"` удалите из `<nav>` тега.</span><span class="sxs-lookup"><span data-stu-id="56ff8-295">Open `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="56ff8-296">Теперь вы удалили все CSS, которые вы ранее добавили на свой сайт.</span><span class="sxs-lookup"><span data-stu-id="56ff8-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Стиль inline был удален из элемента nav" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="56ff8-298">Стиль inline был удален из элемента nav</span><span class="sxs-lookup"><span data-stu-id="56ff8-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-299">Выберите **новый файл**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Новый диалоговое окно файла" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="56ff8-301">Новый диалоговое окно файла</span><span class="sxs-lookup"><span data-stu-id="56ff8-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-302">Замените `cool-file.js` и выберите Add `style.css` **File**.</span><span class="sxs-lookup"><span data-stu-id="56ff8-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Тип style.css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="56ff8-304">Тип</span><span class="sxs-lookup"><span data-stu-id="56ff8-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-305">Добавьте в файл следующий фрагмент `style.css` кода.</span><span class="sxs-lookup"><span data-stu-id="56ff8-305">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Добавление кода в style.css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="56ff8-307">Добавление кода в</span><span class="sxs-lookup"><span data-stu-id="56ff8-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="56ff8-308">Убедитесь, что вы создали таблицу внешних стилей.</span><span class="sxs-lookup"><span data-stu-id="56ff8-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="56ff8-309">Ваш HTML не знает, что он существует.</span><span class="sxs-lookup"><span data-stu-id="56ff8-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="56ff8-310">Откройте `index.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="56ff8-311">Добавьте `<link rel="stylesheet" href="style.css">` в HTML.</span><span class="sxs-lookup"><span data-stu-id="56ff8-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Ссылка на style.css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="56ff8-313">Ссылка на</span><span class="sxs-lookup"><span data-stu-id="56ff8-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-314">Откройте файл `contact.html` и добавьте ссылку.</span><span class="sxs-lookup"><span data-stu-id="56ff8-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Ссылка на style.css в contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="56ff8-316">Ссылка на `style.css` в</span><span class="sxs-lookup"><span data-stu-id="56ff8-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-317">Перейдите на **вкладку в прямом эфире.**  На домашней странице теперь есть тот же шрифт из последнего раздела и синий раздел навигации.</span><span class="sxs-lookup"><span data-stu-id="56ff8-317">Navigate to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Главная страница" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="56ff8-319">Главная страница</span><span class="sxs-lookup"><span data-stu-id="56ff8-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-320">Выберите **контактную** ссылку, чтобы перейти на контактную страницу.</span><span class="sxs-lookup"><span data-stu-id="56ff8-320">Choose the **Contact** link to navigate to the contact page.</span></span>  <span data-ttu-id="56ff8-321">Контактная страница имеет тот же формат, что и домашняя страница.</span><span class="sxs-lookup"><span data-stu-id="56ff8-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Страница контактов" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="56ff8-323">Страница контактов</span><span class="sxs-lookup"><span data-stu-id="56ff8-323">The contact page</span></span>  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a><span data-ttu-id="56ff8-324">Использование CSS-фреймворка</span><span class="sxs-lookup"><span data-stu-id="56ff8-324">Use a CSS framework</span></span>  

<span data-ttu-id="56ff8-325">**CSS frameworks —** это коллекции стилей, построенных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="56ff8-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="56ff8-326">Вместо того, чтобы самостоятельно определять стили, рамки предоставляют вам коллекцию стилей, которые можно использовать на элементах страницы.</span><span class="sxs-lookup"><span data-stu-id="56ff8-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="56ff8-327">Скопируйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="56ff8-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="56ff8-328">Откройте вкладку редактирования и вклеите код в `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-328">Open the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Ссылка на рамки в contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="56ff8-330">Ссылка на фреймворк в</span><span class="sxs-lookup"><span data-stu-id="56ff8-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-331">Откройте файл `index.html` и добавьте код.</span><span class="sxs-lookup"><span data-stu-id="56ff8-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Ссылка на рамки в index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="56ff8-333">Ссылка на фреймворк в</span><span class="sxs-lookup"><span data-stu-id="56ff8-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-334">Возвращайся на вкладку в прямом эфире, чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="56ff8-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="56ff8-335">Несмотря на то, что фоновый цвет элемента и шрифта и элементов одинаковы, шрифт других элементов `<nav>` `<li>` `<a>` изменился.</span><span class="sxs-lookup"><span data-stu-id="56ff8-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Некоторые шрифты на домашней странице изменились из-за рамок" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="56ff8-337">Некоторые шрифты на домашней странице изменились из-за рамок</span><span class="sxs-lookup"><span data-stu-id="56ff8-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <a name="use-a-class"></a><span data-ttu-id="56ff8-338">Использование класса</span><span class="sxs-lookup"><span data-stu-id="56ff8-338">Use a class</span></span>  

<span data-ttu-id="56ff8-339">В последнем разделе вы добавили Bootstrap на свои веб-страницы, которые изменили шрифты некоторых элементов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="56ff8-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="56ff8-340">CSS-фреймворки помогают вносить существенные изменения на страницу с очень небольшим кодом.</span><span class="sxs-lookup"><span data-stu-id="56ff8-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="56ff8-341">Выполните следующие действия по изменению загона.</span><span class="sxs-lookup"><span data-stu-id="56ff8-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="56ff8-342">Скопируйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="56ff8-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="56ff8-343">Добавьте предыдущий фрагмент кода в тег `<header>` `index.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Добавление классов в index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="56ff8-345">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="56ff8-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-346">Добавьте код в тег `<header>` `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Добавление классов в contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="56ff8-348">Добавление классов в</span><span class="sxs-lookup"><span data-stu-id="56ff8-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-349">Просмотр изменений на вкладке в прямом эфире.  Вокруг загона есть большая серая коробка.</span><span class="sxs-lookup"><span data-stu-id="56ff8-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="В загоне теперь есть большой серый поле вокруг него" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="56ff8-351">В загоне теперь есть большой серый поле вокруг него</span><span class="sxs-lookup"><span data-stu-id="56ff8-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <a name="understand-classes"></a><span data-ttu-id="56ff8-352">Понимание классов</span><span class="sxs-lookup"><span data-stu-id="56ff8-352">Understand classes</span></span>  

<span data-ttu-id="56ff8-353">Классы могут назначать коллекции стилей произвольным элементам.</span><span class="sxs-lookup"><span data-stu-id="56ff8-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="56ff8-354">Используйте следующий фрагмент кода, чтобы применить несколько стилей к элементу после того, как `<header>` задаете `class` атрибут `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="56ff8-355">Одним из преимуществ класса является то, что он позволяет применять стили к любым элементам, которые вы хотите.</span><span class="sxs-lookup"><span data-stu-id="56ff8-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="56ff8-356">Например, предположим, что необходимо установить фоновый цвет некоторых элементов на фиолетовый, но `<p>` не все `<p>` элементы.</span><span class="sxs-lookup"><span data-stu-id="56ff8-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="56ff8-357">Чтобы определить стиль в классе, используйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="56ff8-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="56ff8-358">Далее применим класс только `<p>` к элементам, которые необходимо в стиле.</span><span class="sxs-lookup"><span data-stu-id="56ff8-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a><span data-ttu-id="56ff8-359">Выравнивание элементов</span><span class="sxs-lookup"><span data-stu-id="56ff8-359">Align elements</span></span>  

<span data-ttu-id="56ff8-360">Выполните следующие действия, чтобы выполнить загрузку и предоставить классы для выравнивания элементов.</span><span class="sxs-lookup"><span data-stu-id="56ff8-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="56ff8-361">Возвращайся на вкладку редактора и открывай `index.html` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="56ff8-362">Добавьте `class="container-fluid"` в `<body>` тег.</span><span class="sxs-lookup"><span data-stu-id="56ff8-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Добавление класса контейнерной жидкости" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="56ff8-364">Добавление `container-fluid` класса</span><span class="sxs-lookup"><span data-stu-id="56ff8-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="56ff8-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="56ff8-366">Чтобы правильно закрыть новый тег, убедитесь, что нужно поставить `</div>` `</main>` после.</span><span class="sxs-lookup"><span data-stu-id="56ff8-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Добавление строки" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="56ff8-368">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="56ff8-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-369">Добавьте `class="col-3"` в тег и в `<nav>` `class="col-9"` `<main>` тег.</span><span class="sxs-lookup"><span data-stu-id="56ff8-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Добавление классов col-3 и col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="56ff8-371">Добавление `col-3` классов `col-9` и классов</span><span class="sxs-lookup"><span data-stu-id="56ff8-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="56ff8-372">Просмотр изменений на вкладке в прямом эфире.</span><span class="sxs-lookup"><span data-stu-id="56ff8-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Содержимое nav теперь находится слева от основного контента" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="56ff8-374">Содержимое nav теперь находится слева от основного контента</span><span class="sxs-lookup"><span data-stu-id="56ff8-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="56ff8-375">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="56ff8-375">Next steps</span></span>  

<span data-ttu-id="56ff8-376">Поздравляем, вы закончили.</span><span class="sxs-lookup"><span data-stu-id="56ff8-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="56ff8-377">Лучший способ улучшить веб-разработку — создать больше сайтов.</span><span class="sxs-lookup"><span data-stu-id="56ff8-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="56ff8-378">Не беспокойтесь о взломе вещей.</span><span class="sxs-lookup"><span data-stu-id="56ff8-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="56ff8-379">Просто повеселиться и узнать как можно больше по пути.</span><span class="sxs-lookup"><span data-stu-id="56ff8-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="56ff8-380">Чтобы узнать больше о стиле веб-страниц, перейдите к [вводу в CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="56ff8-380">To learn more about styling web pages, navigate to [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="56ff8-381">Чтобы узнать больше о том, как использовать DevTools для экспериментов с CSS страницы, перейдите к началу просмотра и изменения [CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="56ff8-381">To learn more about how to use DevTools to experiment with the CSS of a page, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="56ff8-382">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="56ff8-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools для начинающих: начало работы с HTML и doM | Документы Майкрософт"  
[DevtoolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html — приготовленные амфибии | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="56ff8-388">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56ff8-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="56ff8-389">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и является автором [Кэтрин][KatherineJackson] Джексон \(Технический стажер писатель, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="56ff8-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="56ff8-391">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56ff8-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
