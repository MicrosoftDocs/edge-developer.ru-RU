---
description: Узнайте, как сохранить изменения, внесенные в DevTools на диск.
title: Редактирование файлов с помощью рабочей области
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 17f9ced15dbacd62c9ffe40e4af889925a8155fb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399248"
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

# <a name="edit-files-with-workspaces"></a><span data-ttu-id="24fae-104">Редактирование файлов с помощью рабочей области</span><span class="sxs-lookup"><span data-stu-id="24fae-104">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="24fae-105">Цель этого руководства состоит в предоставлении практической практики по настройке и использованию workspaces, чтобы вы могли использовать workspaces в собственных проектах.</span><span class="sxs-lookup"><span data-stu-id="24fae-105">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="24fae-106">Вы можете сохранить изменения в исходный код на локальном компьютере, внесенные в DevTools после того, как вы включаете workspaces.</span><span class="sxs-lookup"><span data-stu-id="24fae-106">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="24fae-107">**Необходимые условия.** Перед началом этого руководства необходимо знать, как выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="24fae-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="24fae-108">Использование html, CSS и JavaScript для создания веб-страницы</span><span class="sxs-lookup"><span data-stu-id="24fae-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="24fae-109">Использование DevTools для внесения основных изменений в CSS</span><span class="sxs-lookup"><span data-stu-id="24fae-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="24fae-110">Запуск локального веб-сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="24fae-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="24fae-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="24fae-111">Overview</span></span>  

<span data-ttu-id="24fae-112">Рабочее пространство позволяет сохранить изменение, которое вы делаете в Devtools, на локализованную копию того же файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="24fae-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="24fae-113">В этом руководстве на компьютере должны быть следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="24fae-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="24fae-114">У вас есть исходный код для сайта на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="24fae-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="24fae-115">Вы работаете на локальном веб-сервере из каталога исходных кодов, чтобы сайт был доступен по `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="24fae-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="24fae-116">Вы открылись в Microsoft Edge и используете DevTools для изменения `localhost:8080` CSS сайта.</span><span class="sxs-lookup"><span data-stu-id="24fae-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="24fae-117">С включенной рабочей областью изменения CSS, внесенные в DevTools, сохраняются в исходный код на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="24fae-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="24fae-118">Ограничения</span><span class="sxs-lookup"><span data-stu-id="24fae-118">Limitations</span></span>  

<span data-ttu-id="24fae-119">Если вы используете современную структуру, она, вероятно, преобразует исходный код из формата, который легко поддерживать, в формат, оптимизированный для максимально быстрого запуска.</span><span class="sxs-lookup"><span data-stu-id="24fae-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="24fae-120">Workspaces обычно может с помощью исходных карт составить оптимизированный код обратно в [исходный код.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="24fae-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="24fae-121">Но существует много различий между фреймворками в том, как каждая из них использует исходные карты.</span><span class="sxs-lookup"><span data-stu-id="24fae-121">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="24fae-122">Devtools просто поддерживает все варианты.</span><span class="sxs-lookup"><span data-stu-id="24fae-122">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="24fae-123">Известно, что рабочей области не работают со следующими рамками.</span><span class="sxs-lookup"><span data-stu-id="24fae-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="24fae-124">Создание приложения React</span><span class="sxs-lookup"><span data-stu-id="24fae-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="24fae-125">Связанная функция: локальные переопределения</span><span class="sxs-lookup"><span data-stu-id="24fae-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="24fae-126">**Локальные переопределения** — это еще одна функция DevTools, аналогичная рабочей области.</span><span class="sxs-lookup"><span data-stu-id="24fae-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="24fae-127">Используйте локальные переопределения, когда вы хотите экспериментировать с изменениями на веб-странице, и вам необходимо отображать изменения на веб-странице нагрузки, но вам не важно сопоставление изменений в исходный код веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="24fae-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="24fae-128">Шаг 1. Настройка</span><span class="sxs-lookup"><span data-stu-id="24fae-128">Step 1: Set up</span></span>  

<span data-ttu-id="24fae-129">Выполните следующие действия, чтобы получить практический опыт работы с workspaces.</span><span class="sxs-lookup"><span data-stu-id="24fae-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="24fae-130">Настройка демонстрации</span><span class="sxs-lookup"><span data-stu-id="24fae-130">Set up the demo</span></span>  

1.  <span data-ttu-id="24fae-131">[Откройте демо.][GlitchWorkspacesDemo]</span><span class="sxs-lookup"><span data-stu-id="24fae-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Проект Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="24fae-133">Проект Glitch</span><span class="sxs-lookup"><span data-stu-id="24fae-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="24fae-134">Создание `app` каталога на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="24fae-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="24fae-135">Сохранение копий файлов из `workspaces-demo` каталога в `app` каталог.</span><span class="sxs-lookup"><span data-stu-id="24fae-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="24fae-136">В остальной части учебника каталог называется `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="24fae-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="24fae-137">Запустите локальный веб-сервер `~/Desktop/app` в .</span><span class="sxs-lookup"><span data-stu-id="24fae-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="24fae-138">Ниже приведен пример кода для `SimpleHTTPServer` запуска, но вы можете использовать любой сервер, который вы предпочитаете.</span><span class="sxs-lookup"><span data-stu-id="24fae-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="24fae-139">Откройте вкладку в Microsoft Edge и перейдите к локальной версии сайта.</span><span class="sxs-lookup"><span data-stu-id="24fae-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="24fae-140">Вы должны иметь доступ к нему с помощью URL-адреса, как `localhost:8080` или `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="24fae-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="24fae-141">Точный [номер порта может][WikiPortURLs] быть другим.</span><span class="sxs-lookup"><span data-stu-id="24fae-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Демонстрация" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="24fae-143">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="24fae-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="24fae-144">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="24fae-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="24fae-145">Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\) \*\*\*\* для открытия консоли панели DevTools.</span><span class="sxs-lookup"><span data-stu-id="24fae-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Панель Консоли" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="24fae-147">Панель **Консоли**</span><span class="sxs-lookup"><span data-stu-id="24fae-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-148">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="24fae-148">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="24fae-149">Выберите панель **Filesystem.**</span><span class="sxs-lookup"><span data-stu-id="24fae-149">Choose the **Filesystem** panel.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Панель Filesystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="24fae-151">Панель **Filesystem**</span><span class="sxs-lookup"><span data-stu-id="24fae-151">The **Filesystem** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-152">Выберите **добавить папку в рабочее пространство.**</span><span class="sxs-lookup"><span data-stu-id="24fae-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="24fae-153">Введите `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="24fae-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="24fae-154">Выберите **Разрешить** предоставить DevTools разрешение на чтение и записи в каталог.</span><span class="sxs-lookup"><span data-stu-id="24fae-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="24fae-155">В панели **Filesystem** теперь есть зеленая точка рядом `index.html` с , и `script.js` `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="24fae-155">In the **Filesystem** panel, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="24fae-156">Эти зеленые точки означают, что DevTools установил сопоставление между сетевыми ресурсами страницы и файлами в `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="24fae-156">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="На панели Filesystem теперь показано сопоставление между локальными и сетевыми файлами" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="24fae-158">На **панели Filesystem** теперь показано сопоставление между локальными и сетевыми файлами</span><span class="sxs-lookup"><span data-stu-id="24fae-158">The **Filesystem** panel now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="24fae-159">Шаг 2. Сохранение изменения CSS на диск</span><span class="sxs-lookup"><span data-stu-id="24fae-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="24fae-160">Откройте `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="24fae-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="24fae-161">Свойство `color` `h1` элементов установлено `fuchsia` для .</span><span class="sxs-lookup"><span data-stu-id="24fae-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Просмотр styles.css в текстовом редакторе" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="24fae-163">Просмотр `styles.css` в текстовом редакторе</span><span class="sxs-lookup"><span data-stu-id="24fae-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-164">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="24fae-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="24fae-165">Измените значение `color` свойства элемента на `<h1>` ваш любимый цвет.</span><span class="sxs-lookup"><span data-stu-id="24fae-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="24fae-166">Помните, что для отображения правил CSS, примененных к ней в области Стилей, необходимо выбрать `<h1>` элемент **dom Tree.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="24fae-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="24fae-167">Зеленая точка рядом с означает, что любое изменение, которое вы `styles.css:1` делаете, соо- `~/Desktop/app/styles.css`</span><span class="sxs-lookup"><span data-stu-id="24fae-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Зеленый индикатор, связанный с файлом" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="24fae-169">Зеленый индикатор, связанный с файлом</span><span class="sxs-lookup"><span data-stu-id="24fae-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-170">Откройте `styles.css` в текстовом редакторе снова.</span><span class="sxs-lookup"><span data-stu-id="24fae-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="24fae-171">Свойство `color` теперь настроено на ваш любимый цвет.</span><span class="sxs-lookup"><span data-stu-id="24fae-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="24fae-172">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="24fae-172">Refresh the page.</span></span>  <span data-ttu-id="24fae-173">Цвет элемента `<h1>` по-прежнему за набором вашего любимого цвета.</span><span class="sxs-lookup"><span data-stu-id="24fae-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="24fae-174">Изменение остается через обновление, так как при внося изменения DevTools сохранил изменение на диск.</span><span class="sxs-lookup"><span data-stu-id="24fae-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="24fae-175">Затем при обновлении страницы локальный сервер обслуживал измененную копию файла с диска.</span><span class="sxs-lookup"><span data-stu-id="24fae-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="24fae-176">Шаг 3. Сохранение HTML-изменения на диске</span><span class="sxs-lookup"><span data-stu-id="24fae-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="24fae-177">Изменение HTML-кодов из панели Elements</span><span class="sxs-lookup"><span data-stu-id="24fae-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="24fae-178">Вы можете внести изменения в html из панели элементов, но изменения дерева DOM не сохраняются на диске и влияют только на текущую сессию браузера.</span><span class="sxs-lookup"><span data-stu-id="24fae-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="24fae-179">Дерево DOM не html.</span><span class="sxs-lookup"><span data-stu-id="24fae-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-panel"></a><span data-ttu-id="24fae-180">Изменение HTML-кодов с панели Источники</span><span class="sxs-lookup"><span data-stu-id="24fae-180">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="24fae-181">Если вы хотите сохранить изменение html страницы, сделайте это с помощью **панели Источники.**</span><span class="sxs-lookup"><span data-stu-id="24fae-181">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="24fae-182">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="24fae-182">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="24fae-183">Выберите **панель Page.**</span><span class="sxs-lookup"><span data-stu-id="24fae-183">Choose the **Page** panel.</span></span>  
1.  <span data-ttu-id="24fae-184">Выберите **(индекс).**</span><span class="sxs-lookup"><span data-stu-id="24fae-184">Choose **(index)**.</span></span>  <span data-ttu-id="24fae-185">Открывается HTML-код страницы.</span><span class="sxs-lookup"><span data-stu-id="24fae-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="24fae-186">Замените `<h1>Workspaces Demo</h1>` `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="24fae-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="24fae-187">Просмотрите следующую цифру.</span><span class="sxs-lookup"><span data-stu-id="24fae-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="24fae-188">Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="24fae-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="24fae-189">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="24fae-189">Refresh the page.</span></span>  <span data-ttu-id="24fae-190">Элемент `<h1>` по-прежнему отображает новый текст.</span><span class="sxs-lookup"><span data-stu-id="24fae-190">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Изменение HTML-кодов с панели Источники" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="24fae-192">Изменение HTML-кодов с **панели Источники**</span><span class="sxs-lookup"><span data-stu-id="24fae-192">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-193">Откройте `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="24fae-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="24fae-194">Элемент `<h1>` содержит новый текст.</span><span class="sxs-lookup"><span data-stu-id="24fae-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="24fae-195">Шаг 4. Сохранение изменения JavaScript на диск</span><span class="sxs-lookup"><span data-stu-id="24fae-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="24fae-196">Панель **Источники** также является местом для внесения изменений в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24fae-196">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="24fae-197">Но иногда вам необходимо получить доступ к другим панелям, например к средству **Elements** или панели **консоли,** при внесении изменений на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="24fae-197">But sometimes you need to access other panels, such as the **Elements** tool or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="24fae-198">Существует способ открыть панель **Источников** вместе с другими панелями.</span><span class="sxs-lookup"><span data-stu-id="24fae-198">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="24fae-199">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="24fae-199">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="24fae-200">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="24fae-200">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="24fae-201">Откроется **командное** меню.</span><span class="sxs-lookup"><span data-stu-id="24fae-201">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="24fae-202">`QS`Введите, а затем выберите показать быстрый **источник**.</span><span class="sxs-lookup"><span data-stu-id="24fae-202">Type `QS`, then choose **Show Quick Source**.</span></span>  <span data-ttu-id="24fae-203">В нижней части окна DevTools теперь имеется панель **быстрого** источника.</span><span class="sxs-lookup"><span data-stu-id="24fae-203">At the bottom of your DevTools window there is now a **Quick Source** panel.</span></span>  <span data-ttu-id="24fae-204">Панель отображает содержимое последнего файла, отредактируемого в `index.html` панели **Источники.**</span><span class="sxs-lookup"><span data-stu-id="24fae-204">The panel is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="24fae-205">Панель **Быстрого источника** предоставляет редактор из панели **Источники,** чтобы вы могли редактировать файлы при открытых других панелях.</span><span class="sxs-lookup"><span data-stu-id="24fae-205">The **Quick Source** panel gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Откройте панель быстрого источника с помощью командного меню" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="24fae-207">Откройте панель **быстрого источника** с помощью **командного меню**</span><span class="sxs-lookup"><span data-stu-id="24fae-207">Open the **Quick Source** panel using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="24fae-208">Чтобы `Control` + `P` открыть диалоговое окно Open File, выберите \(Windows, Linux\) или `Command` + `P` \(macOS\). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="24fae-208">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="24fae-209">Просмотрите следующую цифру.</span><span class="sxs-lookup"><span data-stu-id="24fae-209">Review the following figure.</span></span>  
1.  <span data-ttu-id="24fae-210">`script`Введите, а затем выберите **app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="24fae-210">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Откройте script.js диалоговое окно Open File" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="24fae-212">Откройте `script.js` диалоговое окно **Open File**</span><span class="sxs-lookup"><span data-stu-id="24fae-212">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="24fae-213">Ссылка `Save Changes To Disk With Workspaces` в демо регулярно стилизуется.</span><span class="sxs-lookup"><span data-stu-id="24fae-213">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="24fae-214">Добавьте следующий код в нижнюю часть **script.js** панели **быстрого** источника.</span><span class="sxs-lookup"><span data-stu-id="24fae-214">Add the following code to the bottom of **script.js** using the **Quick Source** panel.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="24fae-215">Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="24fae-215">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="24fae-216">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="24fae-216">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="24fae-217">Ссылка на странице теперь является italicized.</span><span class="sxs-lookup"><span data-stu-id="24fae-217">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Ссылка на странице теперь является итальяно-" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="24fae-219">Ссылка на странице теперь является итальяно-</span><span class="sxs-lookup"><span data-stu-id="24fae-219">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="24fae-220">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="24fae-220">Next steps</span></span>  

<span data-ttu-id="24fae-221">Используйте то, что вы узнали в этом руководстве, чтобы настроить workspaces в собственном проекте.</span><span class="sxs-lookup"><span data-stu-id="24fae-221">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="24fae-222">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="24fae-222">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Демо-файлы workspaces | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Содержимое - CSS: каскадные листы стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с веб-| MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Запуск простого локального http-сервера | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в DOM - веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Введение в исходные | Блог Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(компьютерная сеть\) — Википедия"  

> [!NOTE]
> <span data-ttu-id="24fae-231">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24fae-231">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="24fae-232">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="24fae-232">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="24fae-234">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24fae-234">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
