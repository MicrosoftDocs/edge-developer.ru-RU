---
description: Руководство по началу работы с WebView2 для приложений Win32
title: Начало работы с WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, элемент управления браузером, edge html
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306161"
---
# Начало работы с WebView2  

В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Дополнительные сведения об отдельных API WebView2 можно найти в справочнике [по API.][Webview2ReferenceWin32]  

## Предварительные условия  

Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.  

*   [WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).  
    
    > [!NOTE]
    > Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 или более поздней с установленной поддержкой C++.  
    
## Шаг 1. Создание одноокнего приложения  

Начните с базового проекта настольного компьютера, который содержит одно главное окно.  

> [!IMPORTANT]
> Чтобы лучше сосредоточиться на этом пономерии, используйте измененный пример кода из [walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.  Чтобы скачать измененный пример и начать работу, перейдите к [примеру WebView2.][GithubMicrosoftedgeWebview2samplesGettingStartedGuide]  

1.  В Visual Studio откройте `WebView2GettingStarted.sln` .  
    Если вы используете более старую версию Visual Studio, наведите курсор на проект **WebView2GettingStarted,** откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Свойства".**  В **области "Общие**свойства конфигурации" измените версию Windows SDK и инструменты платформы, чтобы использовать доступный вам Visual Studio  >  **** Win10 SDK. **** ****  

:::image type="complex" source="../media/tool-version.png" alt-text="Версия средства" lightbox="../media/tool-version.png":::
   Версия средства  
:::image-end:::  

Visual Studio могут отображаться ошибки, так как в проекте отсутствует файл загона WebView2.  Ошибки должны быть исправлены [после шага 2.](#step-2---install-webview2-sdk)  

## Шаг 2. Установка SDK WebView2  

Добавьте в проект SDK WebView2.  Установка win32 SDK с помощью NuGet.  

1.  Наведите курсор на проект, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Управление пакетами NuGet".**  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Управление пакетами NuGet" lightbox="../media/manage-nuget-packages.png":::
       Управление пакетами NuGet  
    :::image-end:::  
    
1.  Установите библиотеку реализации Windows.  
    1.  В панели поиска введите > `Microsoft.Windows.ImplementationLibrary` **Microsoft.Windows.ImplementationLibrary.**  
    1.  В правом окне выберите **"Установить".**  NuGet скачивает библиотеку на компьютер.  
        
        > [!NOTE]
        > Библиотека [реализации Windows][GithubMicrosoftWilMain] и библиотека шаблонов [C++][CppCxWrlTemplateLibraryVS2019] для времени выполнения Windows являются необязательными и упрощают работу с COM в этом примере.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Библиотека реализации Windows" lightbox="../media/wil.png":::
           Библиотека реализации Windows  
        :::image-end:::  
        
1.  Установите SDK WebView2.  
    1.  В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**  
    1.  В правом окне выберите **"Установить".**  NuGet скачивает SDK на компьютер.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet диспетчер пакетов" lightbox="../media/nuget.png":::
           NuGet диспетчер пакетов
        :::image-end:::  
        
1.  Добавьте в проект загон WebView2.  
    :::row:::
       :::column span="1":::
          В файле скопируйте следующий фрагмент кода и в `HelloWebView.cpp` paste его после последней `#include` строки.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          Раздел "Включить" должен выглядеть примерно так, как в следующем фрагменте кода.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Готово к использованию и построению с использованием API WebView2.  

### Создание пустого примера приложения  

Чтобы создать и запустить пример приложения, выберите `F5` .  Приложение отображает пустое окно.  

:::image type="complex" source="../media/empty-app.png" alt-text="Пустое приложение" lightbox="../media/empty-app.png":::
   Пустое приложение  
:::image-end:::  

## Шаг 3. Создание одного веб-приложения в родительском окне  

Добавьте WebView в главное окно.  

 Используйте этот метод, чтобы настроить среду и найти браузер Microsoft Edge \(Chromium\), в которой установлено `CreateCoreWebView2Environment` управление.  Этот метод также можно использовать, если нужно указать расположение браузера, папку пользователя, флаги браузера и так далее, а не параметр `CreateCoreWebView2EnvironmentWithOptions` по умолчанию.  По завершении работы метода запустите метод в callback и запустите метод, чтобы получить `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` связанный WebView.  

В вызываемом окне установите еще несколько параметров, избавите webView на 100 % от родительского окна и перейдите к Bing.  

Скопируйте следующий фрагмент кода и в конце комментария и `HelloWebView.cpp` `// <-- WebView2 sample code starts here -->` перед `// <-- WebView2 sample code ends here -->` комментарием.  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### Создание примера приложения Bing  

Чтобы выполнить сборку и запустить приложение, выберите `F5` .  Теперь у вас есть окно WebView со страницей Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Окно Bing" lightbox="../media/bing-window.png":::
   Окно Bing  
:::image-end:::  

## Шаг 4. События навигации  

Команда WebView уже освещала переход на URL-адрес с помощью `ICoreWebView2::Navigate` метода на последнем шаге.  Во время навигации WebView сожмет последовательность событий, которые может прослушивать хост.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Для получения дополнительных сведений перейдите к [событиям навигации.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации" lightbox="../media/navigation-events.png":::
   События навигации  
:::image-end:::  

В случае ошибок может произойти одно или несколько из следующих событий в зависимости от того, продолжается ли навигация до веб-страницы ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.  

В качестве примера использования событий зарегистрируйте обработок для события, чтобы отменить все запросы, не `NavigationStarting` относя такие как https.  Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

Теперь приложение не переходит на сайты без https.  Аналогичный механизм можно использовать для выполнения других задач, например ограничения навигации в пределах собственного домена.  

## Шаг 5. Сценарии  

Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.  Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.  Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.  Введенный JavaScript работает с определенными сроками.  

*   Запустите его после создания глобального объекта.  
*   Запустите его перед запуском любого другого сценария, включенного в HTML-документ.  

Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

Теперь WebView всегда должен зависать объект и `Object` возвращать документ страницы один раз.  

> [!NOTE] 
> API-коды для впрыска скриптов \(и некоторые другие API WebView2\) являются асинхронными, следует использовать функции вызова, если код должен запускаться в определенном порядке.  

## Шаг 6. Взаимодействие между хост-контентом и веб-контентом  

С помощью этого метода хост и веб-контент также могут взаимодействовать друг с `postMessage` другом.  Веб-содержимое, запущенное в WebView, может размещаться на хост-сервере с помощью метода, а сообщение обрабатывается любым зарегистрированным обработом событий на `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` хост-сервере.  Аналогичным образом, хост может отправить сообщение веб-содержимому через или метод, который будет перехвачен обработчиками, добавленными `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` из `window.chrome.webview.addEventListener` прослушивателей.  Механизм связи позволяет веб-содержимому использовать свои возможности, передавая сообщения с запросом на запуск нативных API на хост-сервере.  

В качестве примера для понимания механизма при попытке вывода URL-адреса документа в WebView происходят следующие действия.  

1.  Хост регистрирует обработок для возврата полученного сообщения в веб-содержимое  
1.  Хост внедряет сценарий в веб-содержимое, которое регистрирует обработок для печати сообщения с хоста  
1.  Хост внедряет сценарий в веб-содержимое, которое публикует URL-адрес на хост-сайте.  
1.  Запускается обработок хоста, который возвращает сообщение \(URL\) в веб-содержимое  
1.  Запускается обработок веб-содержимого, который печатает сообщение с хоста \(URL\)  

Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### Создание примера приложения с URL-адресом для отображения  

Чтобы выполнить сборку и запустить приложение, выберите `F5` .  URL-адрес отображается во всплывающее окно перед переходом на веб-страницу.  

:::image type="complex" source="../media/show-url.png" alt-text="Url-адрес отображения" lightbox="../media/show-url.png":::
   Url-адрес отображения  
:::image-end:::  

Поздравляем, вы создали свое первое приложение WebView2.  

## Дальнейшие действия  

Многие функции WebView2 не освещаются в этой статье. В следующем разделе предоставляется больше ресурсов.  

### См. также  

*   Полный пример возможностей WebView2 можно найти в примере [API WebView2.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Для примера приложения, построенного с помощью WebView2, перейдите к [WebView2Browser.][GithubMicrosoftedgeWebview2browser]  
*   Подробные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ReferenceWin32]  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Разработчик Microsoft Edge"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Майкрософт"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Библиотека шаблонов C++ (WRL) в | Документы Майкрософт"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser — MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Пример API WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Библиотеки реализации Windows (WIL) — microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2"  
