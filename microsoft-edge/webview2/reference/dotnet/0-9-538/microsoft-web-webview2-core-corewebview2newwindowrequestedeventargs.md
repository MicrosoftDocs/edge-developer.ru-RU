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
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699135"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события NewWindowRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Handled](#handled) | Обрабатываются ли NewWindowRequestedEvent с помощью Host.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.
[NewWindow](#newwindow) | Получает новое окно.
[Универсальный код ресурса (URI)](#uri) | Целевой URI для NewWindowRequest.
[WindowFeatures](#windowfeatures) | Функциональные возможности, заданные в окне вызова Window. Open.
[GetDeferral](#getdeferral) | Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).

## Участников

#### Handled 

Обрабатываются ли NewWindowRequestedEvent с помощью Host.

> общедоступный логический том [обработан](#handled)

Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy. Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет. Значение по умолчанию — false.

#### IsUserInitiated 

IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.

> Открытый логический [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Получает новое окно.

> общедоступная CoreWebView2 [NewWindow](#newwindow)

#### Универсальный код ресурса (URI) 

Целевой URI для NewWindowRequest.

> [URI](#uri) общедоступной строки

Не следует перемещаться по целевому WebView. Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.

#### WindowFeatures 

> [!NOTE]
> Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).

Функциональные возможности, заданные в окне вызова Window. Open.

> общедоступная CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)

Эти функции можно учитывать при размещении и изменении размера новых окон WebView.

#### GetDeferral 

Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

> общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()

Вы можете использовать объект CoreWebView2Deferral, чтобы завершить запрос на открытие окна позже. Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.
