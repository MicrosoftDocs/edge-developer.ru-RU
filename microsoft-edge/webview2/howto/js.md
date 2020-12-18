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
# Использование JavaScript в WebView для расширенных сценариев  

Использование JavaScript в элементе управления WebView2 позволяет настраивать собственный приложения в удовлетворении ваших требований.  В этой статье рассматриваются использование JavaScript в WebView2 и разработка с использованием расширенных функций и функций WebView2.  

## Перед началом работы  

В этой статье предполагается, что у вас уже есть рабочий проект.  Если у вас нет проекта и вы хотите следовать за ним, перейдите в руководство по началу [работы WebView2.][Webview2GettingstartedWpf]  

## Базовые функции WebView2  

Используйте следующие функции, чтобы начать встраить JavaScript в приложение WebView.  

| API  | Описание  |
|:--- |:--- |  
| [ExecuteScriptAsync][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | Запустите JavaScript в control WebView. Дополнительные сведения можно найти в учебнике по началу работы. |
| [OnDocumentCreatedAsync][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | Выполняется при запуске объектной модели документа \(DOM\). |
      
## Сценарий: запуск выделенного файла сценария  

В этом разделе можно получить доступ к выделенного файла JavaScript из вашего управления WebView2.  

> [!NOTE]
> Хотя написание строки JavaScript может быть эффективным для быстрых команд JavaScript, вы теряете цветовые темы JavaScript и форматирование строк, что затрудняет написание больших разделов кода в Visual Studio.  

Чтобы решить проблему, создайте отдельный файл JavaScript с кодом, а затем передайте ссылку на этот файл с помощью `ExecuteScriptAsync` параметров.  

1.  Создайте `.js` файл в проекте и добавьте код JavaScript, который вы хотите запустить.  Например, создайте файл под названием `script.js` .  
1.  Преобразуем файл JavaScript в строку, которая передается `ExecuteScriptAsync` в .  
    1.  Чтобы преобразовать файл JavaScript в строку, скопируйте следующий фрагмент кода.  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  В paste the code into `MainWindow.xaml.cs` .  
1.  Передайте текстовую переменную с помощью `ExecuteScriptAsync` .  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## Сценарий: удаление функции перетаскивания  

В этом разделе используйте JavaScript для удаления функции перетаскивания из вашего управления WebView2.  

Для начала изучите текущие функции перетаскивания.  

1.  Создайте `.txt` файл для перетаскивания.  Например, создайте файл с именем `contoso.txt` и добавьте в него текст.  
1.  Запустите проект.  
1.  Перетащите файл `contoso.txt` в управление WebView.  Откроется новое окно, которое является результатом кода в примере проекта.  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Результат перетаскивание и перетаскивание contoso.txt" lightbox="./media/dragtext.png":::
       Результат перетаскивание и перетаскивание contoso.txt  
    :::image-end:::  

Теперь добавьте код для удаления функции перетаскивания из управления WebView2.  

1.  Скопируйте и в paste следующий фрагмент кода в `InitializeAsync()` `MainWindow.xaml.cs` .   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  Запустите проект.  
1.  Попробуйте `contoso.txt` перетащить.  Подтвердите, что перетаскивать не удастся.  

## Сценарий: удаление контекстного меню  

В этом разделе удалите контекстное меню по умолчанию из вашего управления WebView2.  

Для начала изучите текущие функции контекстного меню.  

1.  Запустите проект.  
1.  Наведите курсор на любой пункт управления WebView2 и откройте контекстное меню \(щелкните правой кнопкой мыши\).  Контекстное меню отображает варианты по умолчанию.  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Контекстное меню с вариантами по умолчанию" lightbox="./media/contextmenu.png":::
       Контекстное меню с вариантами по умолчанию  
    :::image-end:::  
    
Теперь добавьте код для удаления функции контекстного меню из управления WebView2.  

1.  Скопируйте и в paste следующий фрагмент кода в `InitializeAsync()` `MainWindow.xaml.cs` .    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  Запустите код еще раз.  Подтвердим, что вы не можете открыть контекстное меню \(щелкните правой кнопкой мыши\).  
   
## См. также  

*   Дополнительные сведения о том, как начать работу с WebView2, можно найти в руководствах по началу работы [с WebView2.][Webview2MainGettingStarted]  
*   Чтобы получить полный пример возможностей WebView2, перейдите к репозиту [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.  
*   Подробные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ApiReference]  
*   Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2][Webview2MainNextSteps].  

## Знакомство с командой Microsoft Edge WebView  

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
