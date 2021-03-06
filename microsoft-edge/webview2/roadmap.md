---
description: Узнайте, что будет дальше для WebView2
title: Дорожная карта для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398415"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Дорожная карта Microsoft Edge WebView2  

> [!NOTE]
> Последнее обновление: ноябрь 2020 г.  

Управление WebView2 позволяет разработчикам встраить веб-технологии в свои собственные приложения.  На следующей странице описывается перспективная дорожная карта для WebView2.  

> [!NOTE]
> WebView2 находится в активной разработке, и дорожная карта продолжает развиваться с учетом изменений рынка и отзывов клиентов, поэтому обратите внимание, что описанные здесь планы не являются исчерпывающими и подлежат изменениям.  

Если у вас есть проблемы или вопросы о дорожной карте, предоподавайте свои отзывы в [репо обратной связи.][GithubMicrosoftedgeWebviewfeedbackMain]  

Команда WebView2 планирует следующие основные усилия для будущих обновлений.  

:::row:::
   :::column span="1":::
      Установщик времени работы WebView2  
   :::column-end:::
   :::column span="2":::
      *   Q4 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Фиксированная версия  
   :::column-end:::
   :::column span="2":::
      *   Q4 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Общая доступность  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \(Q4 2020\)  
      *   .NET \(Q4 2020\)  
      *   [WinUI3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a>Время запуска и установки WebView2  

[Модель распространения Evergreen][ConceptDistributionEvergreenModel] позволяет нацелить или установить на компьютер пользователя время запуска WebView2.  Время запуска и установки Evergreen WebView2 достигло общего уровня доступности \(GA\).  

## <a name="fixed-version"></a>Исправленная версия  

[Модель распространения фиксированной][ConceptsDistributionFixedVersionModel] версии позволяет упаковывать двухфайли Microsoft Edge внутри вашего родного приложения.  Исправленная версия достигла общей доступности \(GA\).  

## <a name="general-availability"></a>Общая доступность  

### <a name="win32-cc"></a>Win32 C/C++  

SDK Win32 C/C++ достиг ga.  

### <a name="net"></a>.NET  

SDK .NET достиг ga. 

### <a name="winui-30"></a>WinUI3.0  

Вы можете получить доступ к WebView2 в приложениях UWP с помощью [win UI 3.0,][UwpToolkitsWinui3Index]в настоящее время в альфа-версии.  Дополнительные сведения о том, как быть в курсе, перейдите к дорожной карте [библиотеки пользовательского интерфейса Windows.][GithubMicrosoftUiXamlRoadmap]  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Модель распространения Evergreen — распространение приложений с помощью webView2 | Документы Майкрософт"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Модель распространения фиксированной версии — распространение приложений с помощью webView2 | Документы Майкрософт"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3.0 Preview 1 (май 2020 г.) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Отзывы веб-просмотров — MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Дорожная карта библиотеки пользовательского интерфейса Windows — microsoft/microsoft-ui-xaml | GitHub"  
