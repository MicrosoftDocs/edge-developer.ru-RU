---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c82c37d7127d69700f35fbf9e2a69f85159a7109
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699158"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события NavigationCompleted.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Удачи](#issuccess) | Значение true, если навигация выполнена успешно.
[NavigationId](#navigationid) | Идентификатор навигации.
[WebErrorStatus](#weberrorstatus) | Код ошибки, если навигация завершилась сбоем.

## Участников

#### Удачи 

Значение true, если навигация выполнена успешно.

> общедоступный bool ( [успешно](#issuccess) )

Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.

#### NavigationId 

Идентификатор навигации.

> общедоступный ulong [NavigationId](#navigationid)

#### WebErrorStatus 

Код ошибки, если навигация завершилась сбоем.

> общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)
