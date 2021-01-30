---
description: Руководство по началу работы с WebView2 для приложений WinForms
title: Начало работы с WebView2 для приложений WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, веб-просмотр, приложения winforms, winforms, edge, CoreWebView2, элемент управления браузером, edge html, начало работы, начало работы, .NET, формы Windows
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306168"
---
# Начало работы с WebView2 в Windows Forms

В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Дополнительные сведения об отдельных API можно найти в [справочнике по API.][DotnetApiMicrosoftWebWebview2Winforms]  

## Предварительные условия  

Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).  
    
    > [!NOTE]
    > Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 или более поздней.  
    
> [!NOTE]
> В настоящее время WebView2 не поддерживает конструкторы .NET 5 и .NET Core.

## Шаг 1. Создание одноокнего приложения

Начните с базового проекта настольного компьютера, который содержит одно главное окно.  

1.  В Visual Studio выберите **приложение Windows Forms .NET Framework**  >  **App Next.**
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Новый проект" lightbox="./media/winforms-newproject.png":::
       Новый проект  
    :::image-end:::
    
1.  Введите значения для **имени и расположения** **проекта.**  Выберите **.NET Framework 4.6.2 или более** поздней.  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Запуск проекта" lightbox="./media/winforms-startproj.png":::
       Запуск проекта  
    :::image-end:::
    
1.  Чтобы создать проект, выберите **"Создать".**
    
## Шаг 2. Установка SDK WebView2

Добавьте в проект SDK WebView2 с помощью NuGet.  

1.  Наведите курсор на проект, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Управление пакетами **NuGet"...**  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       Управление пакетами NuGet
    :::image-end:::
    
1.  В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Начните разработку приложений с помощью API WebView2.  Чтобы построить и запустить проект, выберите `F5` .  Запущенный проект отображает пустое окно.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Пустое приложение" lightbox="./media/winforms-emptyapp.png":::
       Пустое приложение  
    :::image-end:::
    
## Шаг 3. Создание одного webView  

Добавьте WebView в приложение.  

1.  Откройте **конструктор форм Windows.**  
1.  Поиск **WebView2** на панели **инструментов.**  
    
    > [!NOTE]
    > Если вы используете Visual Studio 2017, по умолчанию **WebView2** может не отображаться на **панели инструментов.**  Чтобы включить поведение, **выберите**"Параметры инструментов" > для параметра "Автоматическое заполнение  >  ****  >  **** **панели инструментов".** `True`  
    
    Перетащите управление **WebView2** в приложение Windows Forms.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Панели инструментов, отображающие WebView2":::
       Панели инструментов, отображающие WebView2
    :::image-end:::  

1.  За установите `(Name)` для свойства свойство `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Свойства управления WebView2":::
       Свойства управления WebView2
    :::image-end:::

1.  Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.  За установите `Source` для свойства свойство `https://www.microsoft.com` .  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Свойство Source для управления WebView2":::
       Свойство **Source** для управления WebView2
    :::image-end:::  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что отображается ваш контроль [https://www.microsoft.com][|::ref1::|Main] WebView2.

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   hello webview  
:::image-end:::  

> [!NOTE]
> Если вы работаете с монитором с высоким DPI, может потребоваться настроить приложение Windows Forms для [поддержки высокого DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## Шаг 4. Обработка событий window Resize

Добавьте в формы Windows Forms еще несколько элементов управления с панели элементов, а затем обработать события, соответствующие окну.

1.  В **конструкторе форм Windows**откройте панели **инструментов**
1.  Перетащите **TextBox в** приложение Windows Forms.  На **вкладке "Свойства"** назовем **TextBox.** `addressBar`
1.  Перетащите **кнопку в** приложение Windows Forms.  Измените текст кнопки на **кнопку** и `Go!` назовем **ее** на `goButton` **вкладке "Свойства".**

    Приложение должно выглядеть следующим образом в конструкторе.
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="designer" lightbox="./media/winforms-designer.png":::
       designer  
    :::image-end:::  

1.  В `Form1.cs` файле определите, что элементы управления должны быть на месте при повторном размере окна `Form_Resize` приложения.

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что приложение отображается примерно так, как по снимку экрана ниже.

:::image type="complex" source="./media/winforms-app.png" alt-text="приложение" lightbox="./media/winforms-app.png":::
   Приложение  
:::image-end:::

## Шаг 5. Навигация

Добавьте возможность разрешить пользователям изменять URL-адрес, отображаемый в веб-функции Управления WebView2, добавив адресную стойку в приложение.

1.  Чтобы добавить пространство имен, вставьте в файл следующий фрагмент кода `Form1.cs` `CoreWebView2` в верхней части файла.  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  В **конструкторе форм Windows**дважды щелкните кнопку, чтобы `Go!` создать метод в `goButton_Click` `Form1.cs` файле.  Скопируйте и в paste следующий фрагмент кода внутри функции.  Теперь функция переходит в WebView по `goButton_Click` URL-адресу, введенного в адресной панели.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Чтобы построить и запустить проект, выберите `F5` .  Введите новый URL-адрес в адресной панели и выберите **"Перейти".**  Например, введите `https://www.bing.com` .  Убедитесь, что с помощью управления WebView2 можно перейти по URL-адресу.  

> [!NOTE]
> Убедитесь, что в адресной панели введен полный URL-адрес.  Если URL-адрес не начинается с `ArgumentException` или `http://` `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::

## Шаг 6. События навигации  

Во время навигации на веб-странице с помощью управления WebView2 вызываются события.  Приложение, в котором размещены элементы управления WebView2, прослушивает следующие события.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Дополнительные сведения можно найти в [меню "События навигации".][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   События навигации
:::image-end:::

При ошибке возникают следующие события, которые могут зависеть от навигации на веб-страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.  

Чтобы продемонстрировать, как использовать эти события, сначала зарегистрируйте обработок, который отменит все запросы, которые не `NavigationStarting` используют ПРОТОКОЛ HTTPS.  

В файле обновим конструктор в соответствии со следующим фрагментом кода и `Form1.cs` добавьте `EnsureHttps` функцию.  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```

В конструкторе EnsureHttps регистрируется как обработчик событий в событии `NavigationStarting` в control WebView2.  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что при переходе к http-сайту Веб-просмотр остается без изменений.  Однако WebView будет переходить на сайты HTTPS.

## Шаг 7. Сценарии  

Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.  Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.  Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.  Введенный JavaScript работает с определенными сроками.  

*   Запустите его после создания глобального объекта.  
*   Запустите его перед запуском любого другого сценария, включенного в HTML-документ.  

В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.  Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее метод ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что приложение отображает оповещение при переходе на веб-сайт, который не использует ПРОТОКОЛ HTTPS.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::

## Шаг 8. Взаимодействие между хост-контентом и веб-контентом  

Содержимое хоста и веб-сайта может использовать для `postMessage` связи друг с другом следующим образом:  

*   Веб-содержимое в control WebView2 может использовать `window.chrome.webview.postMessage` для публикации сообщения на хост-сервере.  The host handles the message using any registered `WebMessageReceived` on the host.  
*   Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .  Эти сообщения перехвачены обработчиками, добавленными в `window.chrome.webview.addEventListener` .  

Механизм связи передает сообщения из веб-содержимого на хост с использованием своих возможностей.  

В проекте при переходе по URL-адресу с помощью управления WebView2 он отображает URL-адрес в адресной панели и оповещает пользователя об URL-адресе, отображаемом в веб-интерфейсе2.  

1.  В файле обновите конструктор и создайте функцию, которая `Form1.cs` `InitializeAsync` будет соответствовать следующему фрагменту кода.  Функция `InitializeAsync` ожидает [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] так как инициализация `CoreWebView2` является асинхронной.  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1.  После `CoreWebView2` инициализации зарегистрируйте обработок событий, чтобы ответить `WebMessageReceived` на него.  В `Form1.cs` файле `InitializeAsync` обновим и добавьте его, используя следующий `UpdateAddressBar` фрагмент кода.  

    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }

    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  

1.  Чтобы webView отправил веб-сообщение и ответил на него, после инициализации хост введет скрипт в `CoreWebView2` веб-содержимое, чтобы:  

    1.  Отправьте URL-адрес на хост с помощью `postMessage` .
    1.  Зарегистрируйте обработок событий, чтобы распечатать сообщение, отправленное с хоста.  

В `Form1.cs` файле `InitializeAsync` обновим, чтобы он совпадал со следующим фрагментом кода.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Чтобы выполнить сборку и запустить приложение, выберите `F5` .  Теперь в адресной панели отображается URI в control WebView2.  Кроме того, при успешном переходе к новому URL-адресу WebView оповещает пользователя об URL-адресе, отображаемом в WebView.  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Окончательное приложение" lightbox="./media/winforms-finalapp.png":::
   Окончательное приложение  
:::image-end:::

Поздравляем, вы создали свое первое приложение WebView2.  

## Дальнейшие действия  

Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.  

### См. также  

*   Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2IndexNextSteps]  
*   Подробные сведения об API WebView2 можно найти в справочнике [по API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия: введение в Microsoft Edge WebView2 (предварительная | Документы Майкрософт"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft.Web.WebView2.WinForms | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Класс WebView2 | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Метод WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Документы Майкрософт"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Настройка приложения Windows Forms для поддержки высокого DPI — поддержка высокого DPI в Windows Forms | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Разработчик Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Майкрософт"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  