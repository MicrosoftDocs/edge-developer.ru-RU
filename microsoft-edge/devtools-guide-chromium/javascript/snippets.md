---
description: Фрагменты — это небольшие скрипты, которые можно авторить и запускать в средстве Источники Microsoft Edge DevTools.  Вы можете получать доступ к ресурсам и запускать их с любой веб-страницы.  При запуске фрагмента выполняется из контекста открытой веб-страницы.
title: Запуск фрагментов JavaScript на любой странице с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439425"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="07dff-106">Запуск фрагментов JavaScript на любой веб-странице с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="07dff-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="07dff-107">Если вы несколько раз запускаете один и тот же код в консоли, сберегайте код в качестве фрагмента. [][DevtoolsConsoleIndex]</span><span class="sxs-lookup"><span data-stu-id="07dff-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="07dff-108">Фрагменты — это скрипты, которые вы пишете в [средстве Sources.][DevToolsSourcesTool]</span><span class="sxs-lookup"><span data-stu-id="07dff-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="07dff-109">Фрагменты имеют доступ к контексту JavaScript веб-страницы, и вы можете запускать фрагменты на любой веб-странице.</span><span class="sxs-lookup"><span data-stu-id="07dff-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="07dff-110">Параметры безопасности большинства веб-страниц блокируют загрузку других скриптов в фрагментах.</span><span class="sxs-lookup"><span data-stu-id="07dff-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="07dff-111">По этой причине необходимо включить весь код в один файл.</span><span class="sxs-lookup"><span data-stu-id="07dff-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="07dff-112">Фрагменты являются альтернативой [][WikiBookmarklet] закладки с разницей, что фрагменты работают только в DevTools и не ограничиваются разрешенной длиной URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="07dff-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="07dff-113">Использование фрагментов является отличным способом изменить некоторые вещи на сторонних веб-странице.</span><span class="sxs-lookup"><span data-stu-id="07dff-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="07dff-114">Изменения кода в фрагментах добавляются на текущую веб-страницу и запускаются в том же контексте.</span><span class="sxs-lookup"><span data-stu-id="07dff-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="07dff-115">Дополнительные сведения об изменении существующего кода веб-страницы перейдите к [переопределениям.][DevtoolsJavascriptOverrides]</span><span class="sxs-lookup"><span data-stu-id="07dff-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="07dff-116">Например, на следующем рисунке показана домашняя страницы DevTools слева и некоторый исходный код фрагмента справа.</span><span class="sxs-lookup"><span data-stu-id="07dff-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Перед запуском фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="07dff-118">Веб-страницу перед запуском фрагмента</span><span class="sxs-lookup"><span data-stu-id="07dff-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="07dff-119">Исходный код фрагмента из веб-страницы перед запуском фрагмента.</span><span class="sxs-lookup"><span data-stu-id="07dff-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="07dff-120">На следующем рисунке веб-страницу отображается после запуска фрагмента.</span><span class="sxs-lookup"><span data-stu-id="07dff-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="07dff-121">В **ящике** консоли всплывет сообщение о том, что фрагмент журнала и содержимое веб-страницы полностью `Hello, Snippets!` меняется.</span><span class="sxs-lookup"><span data-stu-id="07dff-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Веб-страницу после запуска фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="07dff-123">Веб-страницу после запуска фрагмента</span><span class="sxs-lookup"><span data-stu-id="07dff-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-pane"></a><span data-ttu-id="07dff-124">Откройте области фрагментов</span><span class="sxs-lookup"><span data-stu-id="07dff-124">Open the Snippets pane</span></span>  

<span data-ttu-id="07dff-125">В **области фрагментов** перечислены фрагменты.</span><span class="sxs-lookup"><span data-stu-id="07dff-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="07dff-126">При редактировании фрагмента необходимо открыть его из области **фрагментов.**</span><span class="sxs-lookup"><span data-stu-id="07dff-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Области фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="07dff-128">Области **фрагментов**</span><span class="sxs-lookup"><span data-stu-id="07dff-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a><span data-ttu-id="07dff-129">Откройте области фрагментов с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="07dff-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="07dff-130">Выберите **вкладку Источники,** чтобы открыть **средство Источники.**</span><span class="sxs-lookup"><span data-stu-id="07dff-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="07dff-131">Обычно **области Страницы** открываются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07dff-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Средство Sources с открываемой слева области Страницы" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="07dff-133">Средство **Sources** с **открываемой** слева области Страницы</span><span class="sxs-lookup"><span data-stu-id="07dff-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07dff-134">Выберите **вкладку Фрагменты, чтобы** открыть области **фрагментов.**</span><span class="sxs-lookup"><span data-stu-id="07dff-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="07dff-135">Возможно, вам потребуется выбрать **дополнительные вкладки** \. Дополнительные вкладки \) для доступа ![ к ](../media/more-tabs-icon.msft.png) **параметру Фрагменты.**</span><span class="sxs-lookup"><span data-stu-id="07dff-135">You may need to choose **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) to access the **Snippets** option.</span></span>  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a><span data-ttu-id="07dff-136">Откройте области фрагментов с командным меню</span><span class="sxs-lookup"><span data-stu-id="07dff-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="07dff-137">Сосредоточь курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="07dff-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="07dff-138">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.</span><span class="sxs-lookup"><span data-stu-id="07dff-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="07dff-139">`Snippets`Введите, **выберите показать фрагменты,** а затем выберите `Enter` для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="07dff-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда фрагментов show" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="07dff-141">Команда **фрагментов** show</span><span class="sxs-lookup"><span data-stu-id="07dff-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="07dff-142">Создание фрагментов</span><span class="sxs-lookup"><span data-stu-id="07dff-142">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-panel"></a><span data-ttu-id="07dff-143">Создание фрагмента через панель Источники</span><span class="sxs-lookup"><span data-stu-id="07dff-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="07dff-144">[Откройте **области фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="07dff-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="07dff-145">Выберите **новый фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="07dff-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="07dff-146">Введите имя фрагмента фрагмента, а затем выберите `Enter` для сохранения.</span><span class="sxs-lookup"><span data-stu-id="07dff-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Имя фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="07dff-148">Имя фрагмента</span><span class="sxs-lookup"><span data-stu-id="07dff-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="07dff-149">Создание фрагмента в командном меню</span><span class="sxs-lookup"><span data-stu-id="07dff-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="07dff-150">Сосредоточь курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="07dff-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="07dff-151">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.</span><span class="sxs-lookup"><span data-stu-id="07dff-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="07dff-152">`Snippet`Введите, выберите Создание нового **фрагмента,** а затем `Enter` выберите для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="07dff-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда создания нового фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="07dff-154">Команда создания нового фрагмента</span><span class="sxs-lookup"><span data-stu-id="07dff-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="07dff-155">Чтобы переименовать новый фрагмент с настраиваемой именем, перейдите к [фрагментам переименования.](#rename-snippets)</span><span class="sxs-lookup"><span data-stu-id="07dff-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="07dff-156">Изменение фрагментов</span><span class="sxs-lookup"><span data-stu-id="07dff-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="07dff-157">[Откройте **области фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="07dff-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="07dff-158">В области **фрагментов** выберите имя фрагмента, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="07dff-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="07dff-159">Он открывается в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="07dff-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="07dff-161">Редактор **кода**</span><span class="sxs-lookup"><span data-stu-id="07dff-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07dff-162">Используйте редактор **кода,** чтобы добавить JavaScript в фрагмент.</span><span class="sxs-lookup"><span data-stu-id="07dff-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="07dff-163">Если звездочка появится рядом с именем фрагмента, это означает, что у вас есть незасвеченный код.</span><span class="sxs-lookup"><span data-stu-id="07dff-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="07dff-164">Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения.</span><span class="sxs-lookup"><span data-stu-id="07dff-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента указывает неавтокопимый код" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="07dff-166">Звездочка рядом с именем фрагмента указывает неавтокопимый код</span><span class="sxs-lookup"><span data-stu-id="07dff-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="07dff-167">Запуск фрагментов</span><span class="sxs-lookup"><span data-stu-id="07dff-167">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-panel"></a><span data-ttu-id="07dff-168">Запуск фрагмента из панели Источники</span><span class="sxs-lookup"><span data-stu-id="07dff-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="07dff-169">[Откройте **области фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="07dff-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="07dff-170">Выберите имя фрагмента, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="07dff-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="07dff-171">Фрагмент кода открывается в **редакторе кода**.</span><span class="sxs-lookup"><span data-stu-id="07dff-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="07dff-172">Выберите **фрагмент run** \( Run ![ Snippet \) или выберите ](../media/run-snippet-icon.msft.png) `Control` + `Enter` \(Windows, Linux\) или `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="07dff-172">Choose **Run Snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="07dff-173">Запуск фрагмента с командным меню</span><span class="sxs-lookup"><span data-stu-id="07dff-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="07dff-174">Сосредоточь курсор где-нибудь в DevTools.</span><span class="sxs-lookup"><span data-stu-id="07dff-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="07dff-175">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.</span><span class="sxs-lookup"><span data-stu-id="07dff-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="07dff-176">Удалите символ и введите символ с именем фрагмента, который необходимо `>` `!` выполнить.</span><span class="sxs-lookup"><span data-stu-id="07dff-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Запуск фрагмента из меню команды" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="07dff-178">Запуск фрагмента из меню **команды**</span><span class="sxs-lookup"><span data-stu-id="07dff-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="07dff-179">Выберите `Enter` для запуска фрагмента.</span><span class="sxs-lookup"><span data-stu-id="07dff-179">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="07dff-180">Переименовать фрагменты</span><span class="sxs-lookup"><span data-stu-id="07dff-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="07dff-181">[Откройте **области фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="07dff-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="07dff-182">Наведите курсор на имя фрагмента, откройте контекстное меню \(правой кнопкой мыши\) и выберите **переименование**.</span><span class="sxs-lookup"><span data-stu-id="07dff-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="07dff-183">Удаление фрагментов</span><span class="sxs-lookup"><span data-stu-id="07dff-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="07dff-184">[Откройте **области фрагментов** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="07dff-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="07dff-185">Наведите курсор на имя фрагмента, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="07dff-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="07dff-186">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="07dff-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Майкрософт"  
[DevToolsSourcesTool]: ../sources/index.md "Обзор инструментов источников | Документы Майкрософт"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Переопределения | Документы Майкрософт"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Википедия"  

> [!NOTE]
> <span data-ttu-id="07dff-192">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07dff-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="07dff-193">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="07dff-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="07dff-195">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07dff-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
