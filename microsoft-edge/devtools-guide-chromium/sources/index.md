---
description: Отображение и редактирование файлов, создание фрагментов кода, отладка JavaScript и настройка рабочих пространств в панели источников Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235272"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="34308-104">Обзор панели источников</span><span class="sxs-lookup"><span data-stu-id="34308-104">Sources panel overview</span></span>  

<span data-ttu-id="34308-105">Используйте панель источников Microsoft \*\*\*\* Edge DevTools для выполнения следующих действий.</span><span class="sxs-lookup"><span data-stu-id="34308-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="34308-106">[Отображение файлов.](#display-files)</span><span class="sxs-lookup"><span data-stu-id="34308-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="34308-107">[Редактирование CSS и JavaScript.](#edit-css-and-javascript)</span><span class="sxs-lookup"><span data-stu-id="34308-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="34308-108">[Создайте и **сохраните фрагменты** Кода JavaScript,](#create-save-and-run-snippets)которые можно запустить на любой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="34308-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="34308-109">**Фрагменты кода похожи** на закладки.</span><span class="sxs-lookup"><span data-stu-id="34308-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="34308-110">[Отлаговка JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="34308-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="34308-111">[Настройка рабочей области, чтобы](#set-up-a-workspace)изменения, внесенные в DevTools, были сохранены в код в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="34308-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="34308-112">Отображение файлов</span><span class="sxs-lookup"><span data-stu-id="34308-112">Display files</span></span>  

<span data-ttu-id="34308-113">Используйте **страницу** для отображения всех ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="34308-113">Use the **Page** pane to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="The Page pane" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="34308-115">The **Page** pane</span><span class="sxs-lookup"><span data-stu-id="34308-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="34308-116">Как **организована** страница:</span><span class="sxs-lookup"><span data-stu-id="34308-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="34308-117">Верхний уровень, как на `top` предыдущем рисунке, представляет [HTML-кадр.][W3CHtml4Frames]</span><span class="sxs-lookup"><span data-stu-id="34308-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="34308-118">Найдите `top` на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="34308-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="34308-119">представляет основной кадр документа.</span><span class="sxs-lookup"><span data-stu-id="34308-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="34308-120">Второй уровень, как на предыдущем `docs.microsoft.com` рисунке, представляет [собой источник.][HtmlstandardOrigin]</span><span class="sxs-lookup"><span data-stu-id="34308-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="34308-121">Третий уровень, четвертый уровень и так далее представляют каталоги и ресурсы, загруженные из этого источника.</span><span class="sxs-lookup"><span data-stu-id="34308-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="34308-122">Например, на предыдущем рисунке полный путь к `devtools-guide-chromium` ресурсу:</span><span class="sxs-lookup"><span data-stu-id="34308-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="34308-123">Выберите файл в **области** страниц, чтобы отобразить содержимое в области **редактора.**</span><span class="sxs-lookup"><span data-stu-id="34308-123">Choose a file in the **Page** pane to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="34308-124">Вы можете отобразить любой тип файла.</span><span class="sxs-lookup"><span data-stu-id="34308-124">You may display any type of file.</span></span>  <span data-ttu-id="34308-125">Для изображений отображается предварительный просмотр изображения.</span><span class="sxs-lookup"><span data-stu-id="34308-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Отображение содержимого a4d10f71.index-docs.js в области редактора" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="34308-127">Отображение содержимого в `a4d10f71.index-docs.js` области **редактора**</span><span class="sxs-lookup"><span data-stu-id="34308-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="34308-128">Редактирование CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="34308-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="34308-129">С помощью **области редактора** можно редактировать CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="34308-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="34308-130">DevTools обновляет страницу для запуска нового кода.</span><span class="sxs-lookup"><span data-stu-id="34308-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="34308-131">Например, если изменить CSS-файл, добавив правило стиля ниже:</span><span class="sxs-lookup"><span data-stu-id="34308-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="34308-132">Это изменение вступает в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="34308-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Измените CSS в области редактора, чтобы изменить цвет текста субтитра на красный" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="34308-134">Измените CSS в **области** редактора, чтобы изменить цвет текста субтитра на красный</span><span class="sxs-lookup"><span data-stu-id="34308-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="34308-135">Изменения CSS вступает в силу немедленно, сохранение не требуется.</span><span class="sxs-lookup"><span data-stu-id="34308-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="34308-136">Чтобы изменения JavaScript вступили в силу, выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="34308-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="34308-137">DevTools не выполняет скрипт повторно, поэтому единственными изменениями JavaScript, которые вступает в силу, являются изменения, внесенные в функции.</span><span class="sxs-lookup"><span data-stu-id="34308-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="34308-138">Например, на следующем рисунке обратите внимание, что это не `console.log('A')` `console.log('B')` так.</span><span class="sxs-lookup"><span data-stu-id="34308-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="34308-139">Если DevTools повторно запускает весь сценарий после вставки изменения, то текст был бы зарегистрирован в `A` консоли. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="34308-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Редактирование JavaScript в области редактора" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="34308-141">Редактирование JavaScript в **области редактора**</span><span class="sxs-lookup"><span data-stu-id="34308-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="34308-142">DevTools стирает изменения CSS и JavaScript при перезагрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="34308-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="34308-143">Перейдите [в папку "Настройка рабочей области",](#set-up-a-workspace) чтобы узнать, как сохранить изменения в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="34308-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="34308-144">Создание, сохранение и запуск фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="34308-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="34308-145">Фрагменты кода — это сценарии, которые можно запускать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="34308-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="34308-146">Предположим, что вы многократно вводите следующий код в **консоли,** чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли.**</span><span class="sxs-lookup"><span data-stu-id="34308-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="34308-147">Вместо этого вы можете сохранить \*\*\*\* этот код в фрагменте кода и запустить его с помощью нескольких нажатий кнопки в любое время.</span><span class="sxs-lookup"><span data-stu-id="34308-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="34308-148">DevTools сохраняет **фрагмент** в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="34308-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Фрагмент кода, который вставляет библиотеку jQuery на страницу" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="34308-150">Фрагмент **кода,** который вставляет библиотеку jQuery на страницу</span><span class="sxs-lookup"><span data-stu-id="34308-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="34308-151">Чтобы запустить **фрагмент:**</span><span class="sxs-lookup"><span data-stu-id="34308-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="34308-152">Откройте файл с помощью области **фрагментов** кода и выберите **"Выполнить"** \( ![ Кнопка "Выполнить" ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="34308-152">Open the file using the **Snippets** pane, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="34308-153">Откройте меню [команд,][DevtoolsGuideChromiumCommandMenuIndex]удалите символ, введите , введите имя фрагмента кода, а `>` `!` затем выберите \*\*\*\* `Enter` .</span><span class="sxs-lookup"><span data-stu-id="34308-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="34308-154">Чтобы узнать [больше,][DevtoolsGuideChromiumJavascriptSnippets] перейдите к фрагментам кода на любой странице.</span><span class="sxs-lookup"><span data-stu-id="34308-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="34308-155">Отлаговка JavaScript</span><span class="sxs-lookup"><span data-stu-id="34308-155">Debug JavaScript</span></span>  

<span data-ttu-id="34308-156">Вместо того чтобы использовать для того, чтобы выявить, где происходит ошибка JavaScript, рассмотрите возможность использования средств отладки `console.log()` Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="34308-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="34308-157">Общая идея состоит в том, чтобы установить точку останова, которая является преднамеренным местом остановки в коде, а затем пошаговая пошаговая часть времени работы кода по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="34308-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="34308-158">Пошаговая пошаговая часть кода может отображать и изменять значения всех текущих свойств \*\*\*\* и переменных, запускать JavaScript в консоли и многого другое.</span><span class="sxs-lookup"><span data-stu-id="34308-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="34308-159">Перейдите [к началу отладки JavaScript,][DevtoolsGuideChromiumJavascriptIndex] чтобы изучить основы отладки в DevTools.</span><span class="sxs-lookup"><span data-stu-id="34308-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Отлаговка JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="34308-161">Отлаговка JavaScript</span><span class="sxs-lookup"><span data-stu-id="34308-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="34308-162">Настройка рабочей области</span><span class="sxs-lookup"><span data-stu-id="34308-162">Set up a Workspace</span></span>  

<span data-ttu-id="34308-163">По умолчанию при редактировании файла в средстве **"Источники"** эти изменения теряются при перезагрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="34308-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="34308-164">**Workspaces** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="34308-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="34308-165">По сути, DevTools можно использовать в качестве редактора кода.</span><span class="sxs-lookup"><span data-stu-id="34308-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="34308-166">Перейдите [к редактированию файлов с помощью workspaces,][DevtoolsGuideChromiumWorkspacesIndex] чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="34308-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <span data-ttu-id="34308-167">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34308-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Запуск фрагментов Кода JavaScript на любой странице с Помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Редактирование файлов с помощью workspaces | Документы Майкрософт"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin | HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> <span data-ttu-id="34308-174">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="34308-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="34308-175">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/sources) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="34308-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="34308-177">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="34308-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
