---
description: Узнайте, как статически связать библиотеку загрузщика WebView2.
title: Как статически связать библиотеку загрузчик WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузером, edge html
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230931"
---
# Статически связывать библиотеку загрузок WebView2  

Возможно, вы захотите распространять приложение с одним исполняемым файлом, а не с пакетом из множества файлов. Чтобы создать один исполняемый файл или уменьшить размер пакета, необходимо статически связать файлы WebView2Loader. SDK WebView2 содержит файл загона `WebView2Loader.dll` и `IDL` файл. `WebView2Loader.dll` — это небольшой компонент, который помогает приложениям находить на устройстве компоненты времени работы WebView2 или не стабильные каналы Microsoft Edge.  

Для приложений, которые не хотят погрузки, `WebView2Loader.dll` выполните следующие действия.  

1.  Откройте файл `.vcxproj` проекта приложения в текстовом редакторе, например Visual Studio Code.  
    
    > [!NOTE]
    > Файл проекта может быть скрытым, то есть он не отображается `.vcproj` в Visual Studio.  Используйте командную строку для поиска скрытых файлов.  
    
1.  Найдите раздел в коде, где вы включаете файлы целевого пакета NuGet WebView2.  Расположение в коде выделено на следующем рисунке.  

    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода project Files" lightbox="./media/inserthere.png":::
       Фрагмент кода project Files   
    :::image-end:::  
  
1.  Скопируйте следующий фрагмент кода и включаем его там, `Microsoft.Web.WebView2.targets` где он включен.  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Вставленный фрагмент кода" lightbox="./media/staticlib.png":::
       Вставленный фрагмент кода  
    :::image-end:::  
    
1.  Изменение дополнительных зависимостей конфигурации сборки для вашего приложения.  Для начала найдите все `<AdditionalDependencies>` теги. Для каждой из них `version.lib` добавьте дополнительную зависимость для каждой конфигурации сборки в `.vcxproj` файле.  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Добавление version.lib в ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       Добавление `version.lib` в `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > Команда WebView2 стремится автоматизировать добавление дополнительной зависимости в будущих выпусках.  
    
1. Скомпилировать и запустить приложение.

### Знакомство с командой WebView2  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### См. также  

*   Чтобы начать работу с WebView2, перейдите к руководствам по началу работы [WebView2.][Webview2MainGettingStarted]  
*   Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.
*   Дополнительные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ApiReference]
*   Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2MainNextSteps]

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности - Отладатель JavaScript для Visual Studio Code — microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Приложения Microsoft Edge (Chromium) WebView — Visual Studio Code — отладка для Microsoft Edge — microsoft/vscode-edge-debug2 | GitHub"  
