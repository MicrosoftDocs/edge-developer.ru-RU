---
description: Фрагменты кода — это небольшие скрипты, которые можно раздать и запускать в средстве Sources Microsoft Edge DevTools.  Вы можете получать доступ к ресурсам и запускать их с любой веб-страницы.  При запуске фрагмента он запускается из контекста открытой веб-страницы.
title: Запуск фрагментов Кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230959"
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

# <span data-ttu-id="1c709-106">Запуск фрагментов Кода JavaScript на любой веб-странице с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c709-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="1c709-107">Если один и тот же [][DevtoolsConsoleIndex] код в консоли повторяется, рассмотрите возможность сохранения кода в качестве фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="1c709-108">Фрагменты кода — это сценарии, которые вы пишете в средстве ["Источники".][DevToolsSourcesTool]</span><span class="sxs-lookup"><span data-stu-id="1c709-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="1c709-109">Фрагменты кода имеют доступ к контексту JavaScript веб-страницы, и вы можете запускать фрагменты на любой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="1c709-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="1c709-110">Параметры безопасности большинства веб-страниц блокируют загрузку других сценариев в фрагментах кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="1c709-111">По этой причине необходимо включить весь код в один файл.</span><span class="sxs-lookup"><span data-stu-id="1c709-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="1c709-112">Фрагменты кода — это [][WikiBookmarklet] альтернатива закладки с разницей в том, что фрагменты кода запускаются только в DevTools и не ограничиваются допустимой длиной URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1c709-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="1c709-113">Использование фрагментов кода — отличный способ изменить некоторые моменты на стороне веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="1c709-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="1c709-114">Изменения кода в фрагментах кода добавляются на текущую веб-страницу и запускаются в том же контексте.</span><span class="sxs-lookup"><span data-stu-id="1c709-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="1c709-115">Дополнительные сведения об изменении существующего кода веб-страницы можно найти в [переопределениях.][DevtoolsJavascriptOverrides]</span><span class="sxs-lookup"><span data-stu-id="1c709-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1c709-116">Например, на следующем рисунке показана домашняя страницы DevTools слева и некоторый исходный код фрагмента справа.</span><span class="sxs-lookup"><span data-stu-id="1c709-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Перед запуском фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="1c709-118">Веб-страницы перед запуском фрагмента</span><span class="sxs-lookup"><span data-stu-id="1c709-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1c709-119">Исходный код фрагмента кода из веб-страницы перед запуском фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="1c709-120">На следующем рисунке после запуска фрагмента отображается веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="1c709-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="1c709-121">В **окне "Консольный ящик"** отображается сообщение о том, что фрагмент кода занося в журнал, а содержимое веб-страницы `Hello, Snippets!` полностью меняется.</span><span class="sxs-lookup"><span data-stu-id="1c709-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Веб-страницу после запуска фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="1c709-123">Веб-страницу после запуска фрагмента</span><span class="sxs-lookup"><span data-stu-id="1c709-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="1c709-124">Открытие области фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-124">Open the Snippets pane</span></span>  

<span data-ttu-id="1c709-125">В **области фрагментов кода** перечислены фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="1c709-126">Если вы хотите изменить фрагмент кода, его необходимо \*\*\*\* открыть в области фрагментов кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="The Snippets pane" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="1c709-128">The **Snippets** pane</span><span class="sxs-lookup"><span data-stu-id="1c709-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="1c709-129">Открытие области фрагментов кода с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="1c709-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="1c709-130">Откройте средство **"Источники"** на вкладке **"Источники".**</span><span class="sxs-lookup"><span data-stu-id="1c709-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="1c709-131">Обычно **по** умолчанию открывается страница.</span><span class="sxs-lookup"><span data-stu-id="1c709-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Средство "Источники" с открытой в левой области страницы" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="1c709-133">Средство **"Источники"** с **открытой** в левой области страницы</span><span class="sxs-lookup"><span data-stu-id="1c709-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c709-134">Откройте **вкладку "Фрагменты** кода", чтобы открыть **ее.**</span><span class="sxs-lookup"><span data-stu-id="1c709-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="1c709-135">Может потребоваться выбрать **дополнительные** вкладки \( Дополнительные вкладки \), чтобы получить доступ ![ к ][ImageMoreTabsIcon] **параметру фрагментов** кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="1c709-136">Открытие области фрагментов кода с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="1c709-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="1c709-137">Наберите курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c709-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="1c709-138">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="1c709-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="1c709-139">`Snippets`Введите, **выберите "Показать фрагменты кода"** и выберите `Enter` команду.</span><span class="sxs-lookup"><span data-stu-id="1c709-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда "Показать фрагменты кода"" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="1c709-141">Команда **"Показать фрагменты кода"**</span><span class="sxs-lookup"><span data-stu-id="1c709-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c709-142">Создание фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-142">Create Snippets</span></span>  

### <span data-ttu-id="1c709-143">Создание фрагмента кода на панели источников</span><span class="sxs-lookup"><span data-stu-id="1c709-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="1c709-144">[Откройте области **фрагментов** ](#open-the-snippets-pane)кода .</span><span class="sxs-lookup"><span data-stu-id="1c709-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="1c709-145">Choose **New snippet**.</span><span class="sxs-lookup"><span data-stu-id="1c709-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="1c709-146">Введите имя фрагмента кода, а затем выберите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="1c709-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Имя фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="1c709-148">Имя фрагмента</span><span class="sxs-lookup"><span data-stu-id="1c709-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="1c709-149">Создание фрагмента кода в меню команд</span><span class="sxs-lookup"><span data-stu-id="1c709-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="1c709-150">Наберите курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c709-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="1c709-151">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="1c709-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="1c709-152">Введите `Snippet` , **выберите "Создать новый фрагмент",** а затем `Enter` выберите команду.</span><span class="sxs-lookup"><span data-stu-id="1c709-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="1c709-154">Команда для создания нового фрагмента</span><span class="sxs-lookup"><span data-stu-id="1c709-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1c709-155">Чтобы переименовать новый фрагмент с пользовательским именем, перейдите к переименовывать [фрагменты](#rename-snippets)кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="1c709-156">Изменение фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="1c709-157">[Откройте области **фрагментов** ](#open-the-snippets-pane)кода .</span><span class="sxs-lookup"><span data-stu-id="1c709-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="1c709-158">В области **фрагментов кода** выберите имя фрагмента, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="1c709-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="1c709-159">Он откроется в **редакторе кода.**</span><span class="sxs-lookup"><span data-stu-id="1c709-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="1c709-161">Редактор **кода**</span><span class="sxs-lookup"><span data-stu-id="1c709-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c709-162">Используйте редактор **кода,** чтобы добавить JavaScript в фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="1c709-163">Если рядом с именем фрагмента появляется звездочка, это означает, что у вас есть несмеченный код.</span><span class="sxs-lookup"><span data-stu-id="1c709-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="1c709-164">Выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\) для сохранения.</span><span class="sxs-lookup"><span data-stu-id="1c709-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента указывает несмесяный код" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="1c709-166">Звездочка рядом с именем фрагмента указывает несмесяный код</span><span class="sxs-lookup"><span data-stu-id="1c709-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c709-167">Запуск фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-167">Run Snippets</span></span>  

### <span data-ttu-id="1c709-168">Запуск фрагмента кода на панели источников</span><span class="sxs-lookup"><span data-stu-id="1c709-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="1c709-169">[Откройте области **фрагментов** ](#open-the-snippets-pane)кода .</span><span class="sxs-lookup"><span data-stu-id="1c709-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="1c709-170">Выберите имя фрагмента кода, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="1c709-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="1c709-171">Фрагмент кода откроется в **редакторе кода.**</span><span class="sxs-lookup"><span data-stu-id="1c709-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="1c709-172">Choose **Run Snippet** \( ![ Run Snippet ][ImageRunSnippetIcon] \) or select `Control` + `Enter` \(Windows, Linux\) or `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="1c709-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="1c709-173">Запуск фрагмента с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="1c709-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="1c709-174">Наберите курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c709-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="1c709-175">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.</span><span class="sxs-lookup"><span data-stu-id="1c709-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="1c709-176">Удалите символ и введите символ, за которым следует имя фрагмента кода, `>` `!` который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="1c709-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Запуск фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="1c709-178">Запуск фрагмента из меню **команд**</span><span class="sxs-lookup"><span data-stu-id="1c709-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c709-179">Выберите `Enter` запуск фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="1c709-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="1c709-180">Переименование фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="1c709-181">[Откройте области **фрагментов** ](#open-the-snippets-pane)кода .</span><span class="sxs-lookup"><span data-stu-id="1c709-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="1c709-182">Наведите курсор на имя фрагмента кода, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Переименовать".**</span><span class="sxs-lookup"><span data-stu-id="1c709-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="1c709-183">Удаление фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="1c709-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="1c709-184">[Откройте области **фрагментов** ](#open-the-snippets-pane)кода .</span><span class="sxs-lookup"><span data-stu-id="1c709-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="1c709-185">Наведите курсор на имя фрагмента кода, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Удалить".**</span><span class="sxs-lookup"><span data-stu-id="1c709-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="1c709-186">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1c709-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Майкрософт"  
[DevToolsSourcesTool]: ../sources/index.md "Обзор средства "Источники" | Документы Майкрософт"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Переопределения | Документы Майкрософт"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Википедия"  

> [!NOTE]
> <span data-ttu-id="1c709-192">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c709-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c709-193">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1c709-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c709-195">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c709-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
