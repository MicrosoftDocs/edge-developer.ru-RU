---
description: Отображение и редактирование файлов, создание фрагментов, отладка JavaScript и настройка рабочих пространств в панели Источников Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7ce7ae32b4bf91419512ec9e387cdf75549552a5
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439607"
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

# <a name="sources-panel-overview"></a><span data-ttu-id="ed9ae-104">Обзор панели источников</span><span class="sxs-lookup"><span data-stu-id="ed9ae-104">Sources panel overview</span></span>  

<span data-ttu-id="ed9ae-105">Для выполнения следующих действий используйте панель Microsoft Edge DevTools **Sources.**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="ed9ae-106">[Отображение файлов.](#display-files)</span><span class="sxs-lookup"><span data-stu-id="ed9ae-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="ed9ae-107">[Изменение CSS и JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="ed9ae-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="ed9ae-108">[Создание и сохранение **фрагментов** JavaScript,](#create-save-and-run-snippets)которые можно запустить на любой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="ed9ae-109">**Фрагменты похожи** на закладки.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="ed9ae-110">[Отламывка JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="ed9ae-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="ed9ae-111">[Настройка рабочего пространства,](#set-up-a-workspace)чтобы изменения, внесенные в DevTools, были сохранены в коде файловой системы.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <a name="display-files"></a><span data-ttu-id="ed9ae-112">Отображение файлов</span><span class="sxs-lookup"><span data-stu-id="ed9ae-112">Display files</span></span>  

<span data-ttu-id="ed9ae-113">Используйте **панель Page;** отображение всех ресурсов, загруженных на странице.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-113">Use the **Page** panel; to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Панель Page" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="ed9ae-115">Панель **Page**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-115">The **Page** panel</span></span>  
:::image-end:::  

<span data-ttu-id="ed9ae-116">Порядок \*\*\*\* организации области Страницы:</span><span class="sxs-lookup"><span data-stu-id="ed9ae-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="ed9ae-117">Верхний уровень, например `top` на предыдущем рисунке, представляет [htmL-кадр.][W3CHtml4Frames]</span><span class="sxs-lookup"><span data-stu-id="ed9ae-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="ed9ae-118">Найдите `top` на каждой странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="ed9ae-119">представляет основную рамку документа.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="ed9ae-120">Второй уровень, например `docs.microsoft.com` на предыдущем рисунке, представляет [происхождение][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="ed9ae-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="ed9ae-121">На третьем, четвертом уровнях и так далее представлены каталоги и ресурсы, загруженные из этого происхождения.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="ed9ae-122">Например, на предыдущем рисунке полный путь к `devtools-guide-chromium` ресурсу</span><span class="sxs-lookup"><span data-stu-id="ed9ae-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="ed9ae-123">Выберите файл на панели **Страницы,** чтобы отобразить содержимое в **области редактора.**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-123">Choose a file in the **Page** panel to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="ed9ae-124">Вы можете отображать любой тип файла.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-124">You may display any type of file.</span></span>  <span data-ttu-id="ed9ae-125">Для изображений отображается предварительный просмотр изображения.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Отображение содержимого a4d10f71.index-docs.js в области редактора" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="ed9ae-127">Отображение содержимого `a4d10f71.index-docs.js` панели **редактора**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** panel</span></span>  
:::image-end:::  

## <a name="edit-css-and-javascript"></a><span data-ttu-id="ed9ae-128">Изменение CSS и JavaScript</span><span class="sxs-lookup"><span data-stu-id="ed9ae-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="ed9ae-129">Используйте области **редактора** для редактирования CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="ed9ae-130">DevTools обновляет страницу для запуска нового кода.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="ed9ae-131">Например, если изменить CSS-файл, добавив правило стиля ниже:</span><span class="sxs-lookup"><span data-stu-id="ed9ae-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="ed9ae-132">Это изменение должно вступает в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Изменение CSS в области редактора, чтобы изменить текстовый цвет субтитра на красный" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="ed9ae-134">Изменение CSS в **области редактора,** чтобы изменить текстовый цвет субтитра на красный</span><span class="sxs-lookup"><span data-stu-id="ed9ae-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="ed9ae-135">Изменения CSS вступает в силу немедленно, без сохранения.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="ed9ae-136">Чтобы изменения JavaScript вступили в силу, выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ed9ae-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="ed9ae-137">DevTools не выполняет повторного запуска скрипта, поэтому только изменения JavaScript, которые вступает в силу, это те, которые вы делаете внутри функций.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="ed9ae-138">Например, на следующем рисунке обратите внимание, как `console.log('A')` не запустить, в то время как `console.log('B')` делает.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="ed9ae-139">Если DevTools повторно запускает весь скрипт после внося изменения, то текст регистрируется `A` в **консоли**.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-139">If DevTools re-runs the entire script after making the change, then the text `A` is logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Редактирование JavaScript в области редактора" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="ed9ae-141">Редактирование JavaScript в **панели редактора**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-141">Editing JavaScript in the **Editor** panel</span></span>  
:::image-end:::  

<span data-ttu-id="ed9ae-142">DevTools стирает изменения CSS и JavaScript при обновлении страницы.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-142">DevTools erases your CSS and JavaScript changes when you refresh the page.</span></span>  <span data-ttu-id="ed9ae-143">Перейдите [к настройкам рабочего пространства,](#set-up-a-workspace) чтобы узнать, как сохранить изменения в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <a name="create-save-and-run-snippets"></a><span data-ttu-id="ed9ae-144">Создание, сохранение и запуск фрагментов</span><span class="sxs-lookup"><span data-stu-id="ed9ae-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="ed9ae-145">Фрагменты — это скрипты, которые можно выполнить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="ed9ae-146">Представьте, что вы несколько раз введите следующий код в **консоли,** чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли.**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="ed9ae-147">Вместо этого вы можете сохранить \*\*\*\* этот код в фрагменте и запустить его с помощью нескольких нажатий кнопки в любое время.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="ed9ae-148">DevTools сохраняет **фрагмент файла** в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Фрагмент, который вставляет библиотеку jQuery на страницу" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="ed9ae-150">Фрагмент, **который** вставляет библиотеку jQuery на страницу</span><span class="sxs-lookup"><span data-stu-id="ed9ae-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="ed9ae-151">Для запуска **фрагмента:**</span><span class="sxs-lookup"><span data-stu-id="ed9ae-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="ed9ae-152">Откройте файл с помощью **панели фрагментов** и выберите **Выполнить** \. ![ Кнопка Запуск ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="ed9ae-152">Open the file using the **Snippets** panel, and choose **Run** \(![The Run button](../media/run-snippet-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="ed9ae-153">Откройте [командное меню,][DevtoolsGuideChromiumCommandMenuIndex]удалите символ, введите, введите имя `>` фрагмента, а затем выберите `!` \*\*\*\* `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ed9ae-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="ed9ae-154">Перейдите [к запуску фрагментов кода с любой страницы,][DevtoolsGuideChromiumJavascriptSnippets] чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <a name="debug-javascript"></a><span data-ttu-id="ed9ae-155">Отламывка JavaScript</span><span class="sxs-lookup"><span data-stu-id="ed9ae-155">Debug JavaScript</span></span>  

<span data-ttu-id="ed9ae-156">Вместо того, чтобы использовать для того, чтобы сделать вывод о неправильном использовании JavaScript, следует использовать средства отладки `console.log()` Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="ed9ae-157">Общая идея состоит в том, чтобы установить точку остановки, которая является преднамеренным местом остановки в коде, а затем выполнить время работы кода по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="ed9ae-158">При прошаговке кода можно отобразить и изменить значения всех задаваемых в настоящее время свойств и переменных, запустить JavaScript в консоли **и**другие.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="ed9ae-159">Перейдите [к началу отладки JavaScript,][DevtoolsGuideChromiumJavascriptIndex] чтобы узнать основы отладки в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Отламывка JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="ed9ae-161">Отламывка JavaScript</span><span class="sxs-lookup"><span data-stu-id="ed9ae-161">Debug JavaScript</span></span>  
:::image-end:::  

## <a name="set-up-a-workspace"></a><span data-ttu-id="ed9ae-162">Настройка рабочего пространства</span><span class="sxs-lookup"><span data-stu-id="ed9ae-162">Set up a Workspace</span></span>  

<span data-ttu-id="ed9ae-163">По умолчанию при редактировании файла в средстве **Sources** эти изменения теряются при обновлении страницы.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you refresh the page.</span></span>  <span data-ttu-id="ed9ae-164">**Рабочей области позволяют** сохранять изменения, внесенные в DevTools, в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="ed9ae-165">По сути, DevTools может использоваться в качестве редактора кода.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="ed9ae-166">Перейдите [к редактированию файлов с помощью рабочей области,][DevtoolsGuideChromiumWorkspacesIndex] чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="ed9ae-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ed9ae-167">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed9ae-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Запустите фрагменты JavaScript на любой странице с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Изменение файлов с помощью рабочей области | Документы Майкрософт"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin | СТАНДАРТ HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | W3C"  

> [!NOTE]
> <span data-ttu-id="ed9ae-174">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ed9ae-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ed9ae-175">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/sources) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="ed9ae-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ed9ae-177">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ed9ae-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
