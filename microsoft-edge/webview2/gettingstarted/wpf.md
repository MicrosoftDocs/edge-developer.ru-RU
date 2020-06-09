---
description: Размещение веб-содержимого в приложении WPF с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WPF, WPF, EDGE, CoreWebView2, управление браузером, пограничный HTML, Приступая к работе, начало работы, .NET
ms.openlocfilehash: a38af67e4ac9f7d70c698231882a6b479994fbfd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697975"
---
# Начало работы с WebView2 в WPF (Предварительная версия)  

В этой статье приступите к созданию первого приложения WebView2 и ознакомьтесь с основными возможностями [WebView2 (Предварительная версия)](/microsoft-edge/hosting/webview2/index).  Дополнительные сведения об отдельных API можно найти в [справочнике API](../reference/dotnet/0-9-515-reference-webview2.md).  

## Предварительные условия  

Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:  

* [Канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) , установленный в Windows 10, Windows 8,1 или Windows 7. 
* [Visual Studio](https://visualstudio.microsoft.com/) 2017 или более поздней версии.  

## Шаг 1: создание одного оконного приложения

Начните с базового классического проекта, содержащего одно главное окно.  

1. Откройте **Visual Studio.**
2. Выберите приложение **WPF .NET Core App** или **WPF .NET Framework**и нажмите кнопку **Далее**.  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Ядро WPF":::
             Ядро WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Платформа WPF":::
             Платформа WPF :::image-end:::
       :::column-end:::
    :::row-end:::

3. Введите значения для **имени проекта** и его **местоположения**.  Выберите .NET Framework 4.6.2 или более поздней версии или .NET Core 3,0 или более поздней версии.  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Создание основы":::
             Создание основы :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Создание платформы":::
             Создание платформы :::image-end:::
       :::column-end:::
    :::row-end:::

4. Нажмите кнопку **создать** , чтобы создать проект.  

## Шаг 2. Установка WebView2 SDK  

Затем добавьте в проект пакет SDK для WebView2.  Для предварительного просмотра установите пакет SDK WebView2 с помощью NuGet.  

1. Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       NuGet :::image-end:::

2. Введите `Microsoft.Web.WebView2` строку поиска.  В результатах поиска выберите **Microsoft. Web. WebView2** .  Установите **предварительную**версию пакета и нажмите кнопку **установить**.  

     ![NuGet](./media/installnuget.PNG)

Все готово для начала разработки приложений с помощью API WebView2.  Нажмите кнопку `F5` , чтобы создать и запустить проект.  Запущенный проект отобразит пустое окно.  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Пустое приложение":::
   Пустое приложение
:::image-end:::

## Шаг 3: создание отдельного WebView в файле MainWindow. XAML  

Далее добавьте WebView в приложение.  

1. Open (открыть) `MainWindow.xaml` .  Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    Убедитесь, что код `MainWindow.xaml` выглядит так, как показано в следующем фрагменте кода.  

    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. Добавьте элемент управления WebView2, заменив `<Grid>` теги, с помощью следующего фрагмента кода.  `Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. Нажмите `F5` , чтобы создать и запустить проект.  Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com :::image-end:::

## Шаг 4 — Навигация  

Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.

1. В файле **MainWindow. XAML**Добавьте адресную строку, скопировав и вставив следующий фрагмент кода в DockPanel, который включает WebView.  

```xml
<DockPanel DockPanel.Dock="Top">
    <Button x:Name="ButtonGo"
            DockPanel.Dock="Right"
            Click="ButtonGo_Click"
            Content="Go"
    />
    <TextBox Name="addressBar"/>
</DockPanel>
```  

Убедитесь, что `DockPanel` раздел `MainWindow.xaml` выглядит так, как показано в следующем фрагменте кода.  

```xml
<DockPanel>
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
        <TextBox Name = "addressBar"/>
    </DockPanel>
    <wv2:WebView2 Name = "webView"
                  Source = "https://www.microsoft.com"
    />
</DockPanel>
```  

2. Откройте `MainWindow.xaml.cs` в Visual Studio.  Добавьте `CoreWebView2` пространство имен, вставив следующий фрагмент кода вверху `MainWindow.xaml.cs` .  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. В **MainWindow.XAML.CS**Скопируйте приведенный ниже фрагмент кода, чтобы создать `ButtonGo_Click` метод, который будет перемещаться по WebView на URL-адрес, введенный в адресной строке.  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Нажмите `F5` , чтобы создать и запустить проект.  Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.  Например, введите `https://www.bing.com` .  Убедитесь, что элемент управления WebView2 переходит по URL-адресу.  

> [!NOTE]
> Убедитесь в том, что в адресной строке введен полный URL-адрес. `ArgumentException`Если URL-адрес не начинается с `http://` или `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   Bing
:::image-end:::

## Шаг 5 — события навигации  

Приложение, содержащее элементы управления WebView2, прослушивает следующие события, возникающие при переходе на веб-страницы с помощью элемента управления WebView2.  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

Дополнительные сведения можно найти в разделе [события навигации](../reference/win32/0-9-488/icorewebview2.md#navigation-events).  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   События навигации
:::image-end:::

При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

При перенаправлении HTTP есть несколько `NavigationStarting` событий.  

Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, которые не используют HTTPS.  

`MainWindow.xaml.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.  

```csharp
public MainWindow()
{
    InitializeComponent();
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

Нажмите `F5` , чтобы создать и запустить проект. Убедитесь, что при переходе на веб-сайт HTTP WebView не **меняется**. Однако WebView будет переходить на сайты HTTPS.

## Шаг 6-Создание сценариев  

Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.  Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.  Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.  

Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.  Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .  

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

Нажмите `F5` , чтобы создать и запустить проект.  Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::

## Шаг 7: связь между узлом и веб-контентом  

Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:  

* Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .  Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.  
* Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .  Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .  

Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.  

Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.  

1. В **MainWindow.XAML.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.  `InitializeAsync`Функция ожидает [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) , так как инициализация `CoreWebView2` является асинхронной.  

    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

2. После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .  В **MainWindow.XAML.CS** Update `InitializeAsync` и Add `UpdateAddressBar` с помощью следующего фрагмента кода.  

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

3. Чтобы WebView отсылать и отвечать на веб-сообщение, после `CoreWebView2` инициализации, узел:  

    1. Встраивает в веб-содержимое сценарий, регистрирующий обработчик для печати сообщения с узла.  
    2. Вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.  

В `MainWindow.xaml.cs` . Обновите `InitializeAsync` следующим образом:  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Нажмите `F5` для сборки и запуска приложения.  Теперь в адресной строке отображается URI-адрес в WebView и при успешном переходе на новый URI WebView предупреждает пользователя о URI, показанном в WebView.  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   addressBar
:::image-end:::

Поздравляем! вы создали первое приложение WebView2!  

## Дальнейшие действия  

* Провлеките [WebView2Samplesный репозиторий](https://github.com/MicrosoftEdge/WebView2Samples) с подробным примером возможностей WebView2's
* Дополнительные сведения об интерфейсах API для извлечения [справочных](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md) данных
* Извлечение списка [ресурсов WebView2](../index.md#next-steps) для получения дополнительных сведений о WebView2

## Знакомство с командой Microsoft Edge WebView  

Помогите вам создать более широкие возможности WebView2, отправив свой отзыв.  Посетите центр [отзывов и предложений](https://aka.ms/webviewfeedback) Microsoft Edge WebView, чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.  
