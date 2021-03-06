---
description: Начало работы с HTML и DOM
title: 'DevTools для начинающих: начало работы с HTML и DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools
ms.openlocfilehash: 6ca27b720a17928545712666e43495c4da2fb880
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397932"
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

# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="f29d8-104">DevTools для начинающих: начало работы с HTML и DOM</span><span class="sxs-lookup"><span data-stu-id="f29d8-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="f29d8-105">Это первый из серии учебников, которые обучат вас основам веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="f29d8-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="f29d8-106">Узнайте о наборе средств веб-разработчика с именем Microsoft Edge DevTools, которые могут повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="f29d8-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="f29d8-107">В этом руководстве вы узнаете о HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="f29d8-108">HTML — одна из основных технологий веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="f29d8-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="f29d8-109">Это язык, который управляет структурой и контентом веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="f29d8-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="f29d8-110">DoM также связан со структурой и контентом веб-страниц, подробнее об этом вы узнаете позже.</span><span class="sxs-lookup"><span data-stu-id="f29d8-110">The DOM is also related to the structure and content of webpages, learn more about that later.</span></span>  

## <a name="goals"></a><span data-ttu-id="f29d8-111">Цели</span><span class="sxs-lookup"><span data-stu-id="f29d8-111">Goals</span></span>  

<span data-ttu-id="f29d8-112">Вы собираетесь изучить веб-разработку, фактически построив собственный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="f29d8-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="f29d8-113">К завершению всех учебников в серии **DevTools для** начинающих ваш готовый сайт может выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f29d8-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="f29d8-115">Готовый сайт</span><span class="sxs-lookup"><span data-stu-id="f29d8-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="f29d8-116">К концу этого учебника вы должны понять следующие темы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-116">By the end of this tutorial, you should understand the following topics.</span></span>  

*   <span data-ttu-id="f29d8-117">Как HTML и DOM создают контент, отображаемый на веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="f29d8-117">How HTML and the DOM create the content that are displayed on webpages.</span></span>  
*   <span data-ttu-id="f29d8-118">Как Microsoft Edge DevTools может помочь вам поэкспериментировать с изменениями HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="f29d8-119">Разница между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="f29d8-120">У вас также есть реальный веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="f29d8-120">You also have a real website.</span></span>  <span data-ttu-id="f29d8-121">Вы можете использовать сайт для хозяйского резюме или блога.</span><span class="sxs-lookup"><span data-stu-id="f29d8-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="f29d8-122">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f29d8-122">Prerequisites</span></span>  

<span data-ttu-id="f29d8-123">Перед попыткой этого руководства выполните следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="f29d8-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="f29d8-124">Если вы не знакомы с HTML, [прочитайте начало работы с HTML.][MDNGettingStartedHtml]</span><span class="sxs-lookup"><span data-stu-id="f29d8-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="f29d8-125">Скачайте [веб-браузер Microsoft Edge.][MicrosoftEdgeInsider]</span><span class="sxs-lookup"><span data-stu-id="f29d8-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="f29d8-126">В этом руководстве используется набор средств веб-разработки, называемых Microsoft Edge DevTools, встроенных в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f29d8-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="f29d8-127">Настройка кода</span><span class="sxs-lookup"><span data-stu-id="f29d8-127">Set up your code</span></span>  

<span data-ttu-id="f29d8-128">Вы собираетесь создать свой сайт в редакторе кода в Интернете под названием Glitch.</span><span class="sxs-lookup"><span data-stu-id="f29d8-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="f29d8-129">Откройте [исходный код.][GlitchAlluringShockIndex]</span><span class="sxs-lookup"><span data-stu-id="f29d8-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="f29d8-130">Эта вкладка называется вкладка **редактора** во всем этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="f29d8-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Вкладка редактора" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="f29d8-132">Вкладка редактора</span><span class="sxs-lookup"><span data-stu-id="f29d8-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-133">Выберите **завихрение-шок**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="f29d8-134">Меню Параметры проекта открывается в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="f29d8-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Меню Параметры проекта" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="f29d8-136">Меню Параметры проекта</span><span class="sxs-lookup"><span data-stu-id="f29d8-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-137">Выберите **Проект Remix**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="f29d8-138">Сбой создает копию проекта, которую можно изменить и случайным образом создать новое имя для проекта.</span><span class="sxs-lookup"><span data-stu-id="f29d8-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="f29d8-139">Контент такой же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="f29d8-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Ремиксируемый проект" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="f29d8-141">Ремиксируемый проект</span><span class="sxs-lookup"><span data-stu-id="f29d8-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-142">Если вы планируете завершить следующий учебник в \*\*\*\* этой серии, выберите вход и войдя в глюк с помощью учетной записи GitHub или Facebook.</span><span class="sxs-lookup"><span data-stu-id="f29d8-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign into Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="f29d8-143">Если вы решите не войти в свою учетную запись, вы потеряете возможность изменить проект после закрытия вкладки редактирования.</span><span class="sxs-lookup"><span data-stu-id="f29d8-143">If you choose to not sign into your account, you lose the ability to edit the project after you close the editing tab.</span></span>  
1.  <span data-ttu-id="f29d8-144">Выберите **Показать** и **выбрать в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="f29d8-145">Откроется новая вкладка, показывающая живую страницу.</span><span class="sxs-lookup"><span data-stu-id="f29d8-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="f29d8-146">Эта вкладка называется вкладка **live во** всем этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="f29d8-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Вкладка live" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="f29d8-148">Вкладка live</span><span class="sxs-lookup"><span data-stu-id="f29d8-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="f29d8-149">Добавление контента</span><span class="sxs-lookup"><span data-stu-id="f29d8-149">Add content</span></span>  

<span data-ttu-id="f29d8-150">Ваш сайт довольно пуст.</span><span class="sxs-lookup"><span data-stu-id="f29d8-150">Your site is pretty empty.</span></span>  <span data-ttu-id="f29d8-151">Следуйте ниже шагам, чтобы добавить в него содержимое.</span><span class="sxs-lookup"><span data-stu-id="f29d8-151">Follow the steps below to add some content to it.</span></span>  

1.  <span data-ttu-id="f29d8-152">На **вкладке редактора** `<!-- You're "About Me" will go here.  -->` замените `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="f29d8-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Новый код выделен на вкладке редактора" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="f29d8-154">Новый код выделен на вкладке редактора</span><span class="sxs-lookup"><span data-stu-id="f29d8-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="f29d8-155">Просмотр изменений на **вкладке в прямом эфире.**  Текст `About Me` отображается на странице.</span><span class="sxs-lookup"><span data-stu-id="f29d8-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="f29d8-156">Текст больше, чем окружающий текст, так как элемент `<h1>` представляет заголовки раздела.</span><span class="sxs-lookup"><span data-stu-id="f29d8-156">The text larger than the surrounding text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="f29d8-157">Ваш веб-браузер автоматически стили заголовки в больших размерах шрифта.</span><span class="sxs-lookup"><span data-stu-id="f29d8-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Новая рубрика видна на вкладке live" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="f29d8-159">Новая рубрика видна на вкладке live</span><span class="sxs-lookup"><span data-stu-id="f29d8-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-160">Назад в **вкладке редактор**, `<p>I am learning HTML.  Recent accomplishments:</p>` вставьте на строку ниже, где вы только что `<h1>About Me</h1>` положили .</span><span class="sxs-lookup"><span data-stu-id="f29d8-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                      <p>I am learning web development.  Recent accomplishments:</p>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Обновленный код выделен на вкладке редактора" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="f29d8-162">Обновленный код выделен на вкладке редактора</span><span class="sxs-lookup"><span data-stu-id="f29d8-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="f29d8-163">Просмотр изменений в **вкладке в прямом эфире.**</span><span class="sxs-lookup"><span data-stu-id="f29d8-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="f29d8-164">Возвращаясь на **вкладку редактора,** добавьте список достижений:</span><span class="sxs-lookup"><span data-stu-id="f29d8-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <p>I am learning web development.  Recent accomplishments:</p>
                  <ul>
                      <li>Learned how to set up my code in Glitch.</li>
                      <li>Added content to my HTML.</li>
                      <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                      <li>TODO: Learn the difference between HTML and the DOM.</li>
                  </ul>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Обновленный код также выделен на вкладке редактора" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="f29d8-166">Обновленный код также выделен на вкладке редактора</span><span class="sxs-lookup"><span data-stu-id="f29d8-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f29d8-167">Снова возвращайтесь на вкладку **в прямом эфире,** чтобы убедиться, что новое содержимое отображается правильно.</span><span class="sxs-lookup"><span data-stu-id="f29d8-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Новый список отображается на вкладке live" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="f29d8-169">Новый список отображается на вкладке live</span><span class="sxs-lookup"><span data-stu-id="f29d8-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="f29d8-170">Экспериментируйте с изменениями контента в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f29d8-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f29d8-171">Если вы разрабатывали большую страницу с большим количеством HTML, то несколько утомительным было бы несколько утомительным ходить между вкладкой редактора и вкладкой live сотни раз, чтобы отобразить изменения, особенно если вы не уверены, что именно нужно поместить на странице.</span><span class="sxs-lookup"><span data-stu-id="f29d8-171">If you were developing a big page with a lot of HTML, it is somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to display your changes, especially if you are unsure what exactly to put on the page.</span></span>  <span data-ttu-id="f29d8-172">Microsoft Edge DevTools помогает вам экспериментировать с изменениями контента, не покидая **вкладку в прямом эфире.**</span><span class="sxs-lookup"><span data-stu-id="f29d8-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="f29d8-173">Узнайте разницу между HTML и DOM</span><span class="sxs-lookup"><span data-stu-id="f29d8-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="f29d8-174">Прежде чем приступить к редактированию контента из Microsoft Edge DevTools, необходимо понять разницу между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-174">Before you start editing your content from Microsoft Edge DevTools, you should understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="f29d8-175">Лучший способ узнать это на примере:</span><span class="sxs-lookup"><span data-stu-id="f29d8-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="f29d8-176">Перейдите на **вкладку в прямом эфире.**  В нижней части страницы отображается `A new element!?!` текст.</span><span class="sxs-lookup"><span data-stu-id="f29d8-176">Navigate to the **live tab**.  At the bottom of your page, the text `A new element!?!` is displayed.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="В нижней части страницы текст Новый элемент!?! отображается" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="f29d8-179">В нижней части страницы отображается `A new element!?!` текст</span><span class="sxs-lookup"><span data-stu-id="f29d8-179">At the bottom of the page the text `A new element!?!` is displayed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-180">Вернуться на вкладку **редактора** и попытаться найти текст `index.html` в .</span><span class="sxs-lookup"><span data-stu-id="f29d8-180">Go back to the **editor tab** and try to find the text in `index.html`.</span></span>  <span data-ttu-id="f29d8-181">Текст не существует.</span><span class="sxs-lookup"><span data-stu-id="f29d8-181">The text is not there.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Тайный текст Новый элемент!?! нигде не найти в index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="f29d8-184">Текст тайны `A new element!?!` нигде не найти в</span><span class="sxs-lookup"><span data-stu-id="f29d8-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-185">Возвращайся к **вкладке в прямом эфире,** наведите курсор, откройте контекстное меню \(правой кнопкой `A new element!?!` мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-185">Go back to the **live tab**, hover on `A new element!?!`, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Проверка текста" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="f29d8-187">Проверка текста</span><span class="sxs-lookup"><span data-stu-id="f29d8-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f29d8-188">DevTools открывается рядом со своей страницей.</span><span class="sxs-lookup"><span data-stu-id="f29d8-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="f29d8-189">выделено синим цветом.</span><span class="sxs-lookup"><span data-stu-id="f29d8-189">is highlighted blue.</span></span>  <span data-ttu-id="f29d8-190">Хотя эта структура в DevTools выглядит как HTML, на самом деле это **дерево DOM.**</span><span class="sxs-lookup"><span data-stu-id="f29d8-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools открыт рядом со страницей" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="f29d8-192">DevTools открыт рядом со страницей</span><span class="sxs-lookup"><span data-stu-id="f29d8-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f29d8-193">При загрузке страницы браузер принимает HTML для создания *исходного* контента страницы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="f29d8-194">DoM представляет *текущее* содержимое страницы, которое со временем может изменяться.</span><span class="sxs-lookup"><span data-stu-id="f29d8-194">The DOM represents the *current* content of the page, which may change over time.</span></span>  <span data-ttu-id="f29d8-195">Загадочное `<div>A new element!?!</div>` содержимое добавляется на страницу из-за тега `<script src="new.js"></script>` в нижней части HTML.</span><span class="sxs-lookup"><span data-stu-id="f29d8-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="f29d8-196">Этот тег вызывает запуск кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f29d8-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="f29d8-197">Дополнительные материалы о JavaScript можно узнать в более позднем руководстве, но пока думайте о нем как о языке программирования, который может изменить содержимое вашей страницы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-197">Learn more about JavaScript in a later tutorial, but for now think of it as a programming language that may change the content of your page.</span></span>  <span data-ttu-id="f29d8-198">В этом конкретном случае код JavaScript `<div>A new element!?!</div>` добавляется на страницу.</span><span class="sxs-lookup"><span data-stu-id="f29d8-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="f29d8-199">Поэтому этот таинственный текст отображается на вашей странице в прямом эфире, но не в HTML.</span><span class="sxs-lookup"><span data-stu-id="f29d8-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="f29d8-200">Изменение DOM</span><span class="sxs-lookup"><span data-stu-id="f29d8-200">Edit the DOM</span></span>  

<span data-ttu-id="f29d8-201">Если вы хотите быстро поэкспериментировать с изменениями контента, не покидая вкладку в прямом эфире, попробуйте DevTools.</span><span class="sxs-lookup"><span data-stu-id="f29d8-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="f29d8-202">В DevTools наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `Your site!` **Изменить в качестве HTML.**</span><span class="sxs-lookup"><span data-stu-id="f29d8-202">In DevTools, hover on `Your site!`, open the contextual menu \(right-click\), and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Редактирование узла в формате HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="f29d8-204">Редактирование узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="f29d8-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-205">Замените `<p>Your site!</p>` код ниже.</span><span class="sxs-lookup"><span data-stu-id="f29d8-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <header>
                      <p><b>Welcome to my site!</b></p>
                      <button>Download my resume</button>
                  </header>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Обновление узла в формате HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="f29d8-207">Обновление узла в формате HTML</span><span class="sxs-lookup"><span data-stu-id="f29d8-207">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f29d8-208">Выберите `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` или \(macOS\) для сохранения изменений или выберите вне окна.</span><span class="sxs-lookup"><span data-stu-id="f29d8-208">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or choose outside of the box.</span></span>  <span data-ttu-id="f29d8-209">Изменения автоматически показываются в режиме прямого просмотра страницы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="f29d8-210">Текст `Your site!` был заменен новым контентом.</span><span class="sxs-lookup"><span data-stu-id="f29d8-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Новое содержимое сразу же появляется на странице" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="f29d8-212">Новое содержимое сразу же появляется на странице</span><span class="sxs-lookup"><span data-stu-id="f29d8-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f29d8-213">Этот рабочий процесс хорош только для экспериментов с изменениями контента.</span><span class="sxs-lookup"><span data-stu-id="f29d8-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="f29d8-214">Если вы обновите страницу или закройте вкладку, ваши изменения будут потеряны навсегда.</span><span class="sxs-lookup"><span data-stu-id="f29d8-214">If you refresh the page or close the tab, your changes are gone forever.</span></span>  <span data-ttu-id="f29d8-215">Если вы используете этот рабочий процесс и хотите сохранить изменения, необходимо вручную скопировать эти изменения в HTML.</span><span class="sxs-lookup"><span data-stu-id="f29d8-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="f29d8-216">В следующих нескольких разделах покажут еще несколько способов изменения контента из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-216">The next couple of sections show you some more ways that you may change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="f29d8-217">Узлы реордера</span><span class="sxs-lookup"><span data-stu-id="f29d8-217">Reorder nodes</span></span>  

<span data-ttu-id="f29d8-218">Вы также можете изменить порядок узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-218">You may also change the order of DOM nodes.</span></span>  <span data-ttu-id="f29d8-219">Например, на веб-странице меню навигации находится в нижней части.</span><span class="sxs-lookup"><span data-stu-id="f29d8-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="f29d8-220">Чтобы переместить его в верхнюю часть:</span><span class="sxs-lookup"><span data-stu-id="f29d8-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="f29d8-221">Найдите `<nav>` узел в **dom Tree** of DevTools.</span><span class="sxs-lookup"><span data-stu-id="f29d8-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Узел nav выделен синим цветом в DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="f29d8-223">Узел nav выделен синим цветом в DevTools</span><span class="sxs-lookup"><span data-stu-id="f29d8-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-224">Перетащите узел в верхнюю часть, чтобы узел был первым `<nav>` ребенком `<body>` узла.</span><span class="sxs-lookup"><span data-stu-id="f29d8-224">Drag the `<nav>` node to the top, so that the node is the first child of the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Перетаскивание узла nav в верхнюю часть" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="f29d8-226">Перетаскивание узла nav в верхнюю часть</span><span class="sxs-lookup"><span data-stu-id="f29d8-226">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="f29d8-227">Узел `<nav>` отображается в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="f29d8-227">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Узел nav находится в верхней части страницы" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="f29d8-229">Узел nav находится в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="f29d8-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="f29d8-230">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="f29d8-230">Delete a node</span></span>  

<span data-ttu-id="f29d8-231">Кроме того, можно удалить узлы из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-231">You may also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="f29d8-232">В **дереве DOM выберите** `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="f29d8-232">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="f29d8-233">DevTools выделяет синий узел.</span><span class="sxs-lookup"><span data-stu-id="f29d8-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Выберите удаленный узел" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="f29d8-235">Выберите удаленный узел</span><span class="sxs-lookup"><span data-stu-id="f29d8-235">Choose the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-236">Выберите `Delete` клавишу на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="f29d8-236">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="f29d8-237">Узел `<div>A new element!?!</div>` удаляется из дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Узел удален" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="f29d8-239">Узел удален</span><span class="sxs-lookup"><span data-stu-id="f29d8-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="f29d8-240">Копирование изменений</span><span class="sxs-lookup"><span data-stu-id="f29d8-240">Copy your changes</span></span>  

<span data-ttu-id="f29d8-241">Вы почти закончили.</span><span class="sxs-lookup"><span data-stu-id="f29d8-241">You're almost done.</span></span>  <span data-ttu-id="f29d8-242">Вы сделали несколько изменений на своей странице в DevTools, но они еще не сохранены в исходный код.</span><span class="sxs-lookup"><span data-stu-id="f29d8-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="f29d8-243">Обновление **вкладки в прямом эфире.**  Изменения, внесенные в dom Tree, исчезают.</span><span class="sxs-lookup"><span data-stu-id="f29d8-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="f29d8-244">В частности, текст возвращается в верхнюю часть страницы, а текст `Your site!` `A new element!?!` возвращается в нижнюю часть.</span><span class="sxs-lookup"><span data-stu-id="f29d8-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Внесенные изменения исчезли" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="f29d8-246">Внесенные изменения исчезли</span><span class="sxs-lookup"><span data-stu-id="f29d8-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f29d8-247">Скопируйте код ниже.</span><span class="sxs-lookup"><span data-stu-id="f29d8-247">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
    
1.  <span data-ttu-id="f29d8-248">Возвращайся на **вкладку редактора** и замените содержимое файла `index.html` кодом, который вы только что скопировали.</span><span class="sxs-lookup"><span data-stu-id="f29d8-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Как должен выглядеть index.html-файл" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="f29d8-250">Внешний вид `index.html` файла</span><span class="sxs-lookup"><span data-stu-id="f29d8-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="f29d8-251">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f29d8-251">Next steps</span></span>  

*   <span data-ttu-id="f29d8-252">Выполните следующий учебник в этой серии , Начало работы с [CSS][DevToolsBeginnersCss], чтобы узнать, как стиль вашей страницы и экспериментировать с изменениями стиля в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="f29d8-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="f29d8-253">Ознакомьтесь [с введением в DOM,][MDNIntroductionDom] чтобы узнать больше о DOM.</span><span class="sxs-lookup"><span data-stu-id="f29d8-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="f29d8-254">Ознакомьтесь с курсом ["Введение в веб-разработку",][CourseraIntroductionToWebDevelopment] чтобы получить дополнительные практические веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="f29d8-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f29d8-255">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f29d8-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools для начинающих: начало работы с CSS | Документы Майкрософт"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Введение в веб-разработку | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html — | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML-| MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в dom | MDN"  

> [!NOTE]
> <span data-ttu-id="f29d8-262">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f29d8-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f29d8-263">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и является автором [Кэтрин][KatherineJackson] Джексон \(Технический стажер писатель, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="f29d8-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f29d8-265">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f29d8-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
