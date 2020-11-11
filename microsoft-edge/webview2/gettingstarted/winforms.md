---
description: Руководство по началу работы с WebView2 для приложений для WinForms
title: Начало работы с WebView2 для приложений WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WinForms, WinForms, EDGE, CoreWebView2, браузер, край HTML, Приступая к работе, Приступая к работе, .NET, Windows Forms
ms.openlocfilehash: c4092c545c24bf09667a5090251b51b96259efc2
ms.sourcegitcommit: a59464aff9e2c0bf57d172afbacdeed2c1a3ea42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11162641"
---
# Начало работы с WebView2 в Windows Forms (Предварительная версия)  

В этой статье приступите к созданию первого приложения WebView2 и ознакомьтесь с основными возможностями [WebView2 (Предварительная версия)](/microsoft-edge/webview2/index).  Дополнительные сведения об отдельных API можно найти в [справочнике API](/dotnet/api/microsoft.web.webview2.winforms).  

## Предварительные условия  

Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:  

* [Среда выполнения WebView2][Webview2Installer] или любой [нестабильный канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download) , установленный в windows 10, Windows 8,1 или Windows 7. 
* [Visual Studio](https://visualstudio.microsoft.com) 2017 или более поздней версии.

> [!NOTE]
> WebView2 в настоящее время не поддерживает базовые конструкторы .NET 5 и .NET.

## Шаг 1: создание одного оконного приложения

Начните с базового классического проекта, содержащего одно главное окно.  

1. Откройте **Visual Studio.**

1. Выберите **приложение Windows Forms .NET Framework** и нажмите кнопку **Далее**.

    ![newproject](./media/winforms-newproject.png)

1. Введите значения для **имени проекта** и его **местоположения**.  Выберите **.NET Framework 4.6.2** или более поздней версии.  

    ![startproject](./media/winforms-startproj.png)

1. Нажмите кнопку **создать** , чтобы создать проект.

## Шаг 2. Установка WebView2 SDK

Затем добавьте в проект пакет SDK для WebView2.  Для предварительного просмотра установите пакет SDK WebView2 с помощью NuGet.  

1. Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       Управление пакетами NuGet :::image-end:::

1. Введите `Microsoft.Web.WebView2` строку поиска.  В результатах поиска выберите **Microsoft. Web. WebView2** .  

    > [!IMPORTANT]
    > Убедитесь, что установлен флажок **Добавить предварительную**версию, выберите пакет предварительной версии в **версии**и нажмите кнопку **установить**.  

    ![NuGet](./media/installnuget.png)

Все готово для начала разработки приложений с помощью API WebView2.  Выберите `F5` для сборки и запуска проекта.  Запущенный проект отобразит пустое окно.  

![emptyApp](./media/winforms-emptyApp.png)

## Шаг 3: создание единого WebView  

Далее добавьте WebView в приложение.  

1. Откройте **конструктор Windows Forms**.  
1. Найдите **WebView2** на **панели элементов**. Перетащите элемент управления **WebView2** в приложение Windows Forms.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Панель элементов, в которой отображается WebView2":::
       Панель элементов, в которой отображается WebView2 :::image-end:::  

1. Измените `Name` свойство на `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Свойства элемента управления WebView2":::
       Свойства элемента управления WebView2 :::image-end:::

1. `Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2. Установите для свойства Source значение <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Свойство Source элемента управления WebView2":::
       Свойство Source элемента управления WebView2 :::image-end:::

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> Если вы работаете с монитором с высоким разрешением, может потребоваться [настроить поддержку высокого разрешения для приложения Windows Forms](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).

## Шаг 4: обработка событий изменения размера окна

Добавьте еще несколько элементов управления в формы Windows Forms с панели элементов, а затем обработайте события изменения размера окна соответствующим образом.

1. Открытие **панели элементов** в **конструкторе Windows Forms**
1. Перетащите **текстовое поле** в приложение Windows Forms. Назовите **поле TextBox** `addressBar` на **вкладке Свойства**.
1. Перетащите **кнопку** в приложение Windows Forms. Измените текст **кнопки** `Go!` и назовите **кнопку** на `goButton` **вкладке Свойства**.

    Приложение должно выглядеть так, как показано в конструкторе:
    
    ![Проектировщик](./media/winforms-designer.png)

1. В **Form1.CS** определите, `Form_Resize` нужно ли сохранять элементы управления при изменении размера окна приложения.

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

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что приложение отображается примерно так, как показано на следующем снимке экрана.

![приложение](./media/winforms-app.png)

## Шаг 5 — Навигация

Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.

1. В поле `Form1.cs` Добавить `CoreWebView2` пространство имен вставьте следующий фрагмент кода вверху `Form1.cs` .  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. В **конструкторе Windows Forms**дважды щелкните `Go!` кнопку, чтобы создать `goButton_Click` метод `Form1.cs` . Скопируйте и вставьте следующий фрагмент в функцию. Теперь `goButton_Click` функция переходит по WebView на URL-адрес, введенный в адресной строке.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.  Например, введите `https://www.bing.com` .  Убедитесь, что элемент управления WebView2 переходит по URL-адресу.  

> [!NOTE]
> Убедитесь в том, что в адресной строке введен полный URL-адрес. `ArgumentException`Если URL-адрес не начинается с `http://` или `https://`

![bing](./media/winforms-bing.png)

## Шаг 6 — события навигации  

Приложение, содержащее элементы управления WebView2, прослушивает следующие события, возникающие при переходе на веб-страницы с помощью элемента управления WebView2.  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

Дополнительные сведения можно найти в разделе [события навигации](../concepts/navigation-events.md).  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   События навигации
:::image-end:::

При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

При перенаправлении HTTP есть несколько `NavigationStarting` событий.  

Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, которые не используют HTTPS.  

`Form1.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.  

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

В конструкторе EnsureHttps регистрируется в качестве обработчика событий для `NavigationStarting` события в элементе управления WebView2.  

Выберите `F5` , чтобы выполнить сборку и запустить проект. Убедитесь, что при переходе на веб-сайт HTTP WebView не меняется. Однако WebView будет переходить на сайты HTTPS.

## Шаг 7: создание сценариев  

Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.  Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.  Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.  

Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.  Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync]() .  

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

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.  

![https](./media/winforms-https.png)

## Шаг 8-связь между узлом и веб-контентом  

Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:  

* Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .  Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.  
* Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .  Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .  

Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.  

Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.  

1. В **Form1.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.  `InitializeAsync`Функция ожидает [EnsureCoreWebView2Async]() , так как инициализация `CoreWebView2` является асинхронной.  

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

1. После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .  В разделе `Form1.cs` Update `InitializeAsync` и Add `UpdateAddressBar` (добавить с помощью следующего фрагмента кода).  

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

1. Чтобы WebView отсылать и отвечать на веб-сообщение, после его `CoreWebView2` инициализации ведущее приложение вставляет сценарий в веб-содержимое в:  

    1. Отправьте URL-адрес узлу с помощью `postMessage` .
    1. Зарегистрируйте обработчик событий, чтобы напечатать сообщение, отправленное с узла.  

В `Form1.cs` Обновите, `InitializeAsync` как показано в следующем фрагменте кода.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Выберите `F5` , чтобы выполнить сборку и запустить приложение.  Убедитесь в том, что в адресной строке отображается URL-адрес сайта, отображаемого в WebView. Кроме того, при успешном переходе к новому URL-адресу WebView предупреждает пользователя об URL-адресе, показанном в WebView.  

![finalapp](./media/winforms-finalapp.png)

Поздравляем! вы создали первое приложение WebView2!  

## Дальнейшие действия 

* Провлеките [WebView2Samplesный репозиторий](https://github.com/MicrosoftEdge/WebView2Samples) с подробным примером возможностей WebView2's
* Дополнительные сведения об интерфейсах API для извлечения [справочных](/dotnet/api/microsoft.web.webview2.winforms.webview2) данных
* Извлечение списка [ресурсов WebView2](../index.md#next-steps) для получения дополнительных сведений о WebView2


## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2" 