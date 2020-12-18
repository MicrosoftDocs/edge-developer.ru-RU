---
description: Узнайте, как использовать JavaScript в сложных сценариях в приложениях WebView2
title: Использование JavaScript в приложениях WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузером, edge html
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230938"
---
# <span data-ttu-id="e3f72-104">Использование JavaScript в WebView для расширенных сценариев</span><span class="sxs-lookup"><span data-stu-id="e3f72-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="e3f72-105">Использование JavaScript в элементе управления WebView2 позволяет настраивать собственный приложения в удовлетворении ваших требований.</span><span class="sxs-lookup"><span data-stu-id="e3f72-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="e3f72-106">В этой статье рассматриваются использование JavaScript в WebView2 и разработка с использованием расширенных функций и функций WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <span data-ttu-id="e3f72-107">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="e3f72-107">Before you begin</span></span>  

<span data-ttu-id="e3f72-108">В этой статье предполагается, что у вас уже есть рабочий проект.</span><span class="sxs-lookup"><span data-stu-id="e3f72-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="e3f72-109">Если у вас нет проекта и вы хотите следовать за ним, перейдите в руководство по началу [работы WebView2.][Webview2GettingstartedWpf]</span><span class="sxs-lookup"><span data-stu-id="e3f72-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <span data-ttu-id="e3f72-110">Базовые функции WebView2</span><span class="sxs-lookup"><span data-stu-id="e3f72-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="e3f72-111">Используйте следующие функции, чтобы начать встраить JavaScript в приложение WebView.</span><span class="sxs-lookup"><span data-stu-id="e3f72-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="e3f72-112">API</span><span class="sxs-lookup"><span data-stu-id="e3f72-112">API</span></span>  | <span data-ttu-id="e3f72-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e3f72-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="e3f72-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="e3f72-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="e3f72-115">Запустите JavaScript в control WebView.</span><span class="sxs-lookup"><span data-stu-id="e3f72-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="e3f72-116">Дополнительные сведения можно найти в учебнике по началу работы.</span><span class="sxs-lookup"><span data-stu-id="e3f72-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="e3f72-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="e3f72-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="e3f72-118">Выполняется при запуске объектной модели документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="e3f72-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <span data-ttu-id="e3f72-119">Сценарий: запуск выделенного файла сценария</span><span class="sxs-lookup"><span data-stu-id="e3f72-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="e3f72-120">В этом разделе можно получить доступ к выделенного файла JavaScript из вашего управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="e3f72-121">Хотя написание строки JavaScript может быть эффективным для быстрых команд JavaScript, вы теряете цветовые темы JavaScript и форматирование строк, что затрудняет написание больших разделов кода в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3f72-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="e3f72-122">Чтобы решить проблему, создайте отдельный файл JavaScript с кодом, а затем передайте ссылку на этот файл с помощью `ExecuteScriptAsync` параметров.</span><span class="sxs-lookup"><span data-stu-id="e3f72-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="e3f72-123">Создайте `.js` файл в проекте и добавьте код JavaScript, который вы хотите запустить.</span><span class="sxs-lookup"><span data-stu-id="e3f72-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="e3f72-124">Например, создайте файл под названием `script.js` .</span><span class="sxs-lookup"><span data-stu-id="e3f72-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="e3f72-125">Преобразуем файл JavaScript в строку, которая передается `ExecuteScriptAsync` в .</span><span class="sxs-lookup"><span data-stu-id="e3f72-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="e3f72-126">Чтобы преобразовать файл JavaScript в строку, скопируйте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="e3f72-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="e3f72-127">В paste the code into `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e3f72-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="e3f72-128">Передайте текстовую переменную с помощью `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="e3f72-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <span data-ttu-id="e3f72-129">Сценарий: удаление функции перетаскивания</span><span class="sxs-lookup"><span data-stu-id="e3f72-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="e3f72-130">В этом разделе используйте JavaScript для удаления функции перетаскивания из вашего управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="e3f72-131">Для начала изучите текущие функции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="e3f72-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="e3f72-132">Создайте `.txt` файл для перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="e3f72-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="e3f72-133">Например, создайте файл с именем `contoso.txt` и добавьте в него текст.</span><span class="sxs-lookup"><span data-stu-id="e3f72-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="e3f72-134">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="e3f72-134">Run your project.</span></span>  
1.  <span data-ttu-id="e3f72-135">Перетащите файл `contoso.txt` в управление WebView.</span><span class="sxs-lookup"><span data-stu-id="e3f72-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="e3f72-136">Откроется новое окно, которое является результатом кода в примере проекта.</span><span class="sxs-lookup"><span data-stu-id="e3f72-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Результат перетаскивание и перетаскивание contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="e3f72-138">Результат перетаскивание и перетаскивание contoso.txt</span><span class="sxs-lookup"><span data-stu-id="e3f72-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="e3f72-139">Теперь добавьте код для удаления функции перетаскивания из управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="e3f72-140">Скопируйте и в paste следующий фрагмент кода в `InitializeAsync()` `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e3f72-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="e3f72-141">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="e3f72-141">Run your project.</span></span>  
1.  <span data-ttu-id="e3f72-142">Попробуйте `contoso.txt` перетащить.</span><span class="sxs-lookup"><span data-stu-id="e3f72-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="e3f72-143">Подтвердите, что перетаскивать не удастся.</span><span class="sxs-lookup"><span data-stu-id="e3f72-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <span data-ttu-id="e3f72-144">Сценарий: удаление контекстного меню</span><span class="sxs-lookup"><span data-stu-id="e3f72-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="e3f72-145">В этом разделе удалите контекстное меню по умолчанию из вашего управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="e3f72-146">Для начала изучите текущие функции контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="e3f72-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="e3f72-147">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="e3f72-147">Run your project.</span></span>  
1.  <span data-ttu-id="e3f72-148">Наведите курсор на любой пункт управления WebView2 и откройте контекстное меню \(щелкните правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="e3f72-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="e3f72-149">Контекстное меню отображает варианты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3f72-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Контекстное меню с вариантами по умолчанию" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="e3f72-151">Контекстное меню с вариантами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e3f72-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e3f72-152">Теперь добавьте код для удаления функции контекстного меню из управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e3f72-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="e3f72-153">Скопируйте и в paste следующий фрагмент кода в `InitializeAsync()` `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="e3f72-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="e3f72-154">Запустите код еще раз.</span><span class="sxs-lookup"><span data-stu-id="e3f72-154">Run the code again.</span></span>  <span data-ttu-id="e3f72-155">Подтвердим, что вы не можете открыть контекстное меню \(щелкните правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="e3f72-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <span data-ttu-id="e3f72-156">См. также</span><span class="sxs-lookup"><span data-stu-id="e3f72-156">See also</span></span>  

*   <span data-ttu-id="e3f72-157">Дополнительные сведения о том, как начать работу с WebView2, можно найти в руководствах по началу работы [с WebView2.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="e3f72-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="e3f72-158">Чтобы получить полный пример возможностей WebView2, перейдите к репозиту [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="e3f72-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="e3f72-159">Подробные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="e3f72-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="e3f72-160">Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="e3f72-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <span data-ttu-id="e3f72-161">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e3f72-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Документы Майкрософт"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Начало работы с WebView2 в WPF (предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 — интерфейс ICoreWebView2 | Документы Майкрософт"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
