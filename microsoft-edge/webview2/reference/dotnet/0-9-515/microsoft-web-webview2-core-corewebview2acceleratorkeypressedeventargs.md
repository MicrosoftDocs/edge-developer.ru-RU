---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ef2eb16f6ba0186494400e6190d316ea503f9f16
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654943"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события AcceleratorKeyPressed.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Handled](#handled) | Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.
[KeyEventKind](#keyeventkind) | Тип события key, который привел к инициированию события.
[KeyEventLParam](#keyeventlparam) | Значение LPARAM, сопровождающее сообщение в окне.
[PhysicalKeyStatus](#physicalkeystatus) | Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.
[VirtualKey](#virtualkey) | Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.

## Участников

#### Handled 

Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.

> общедоступный логический том [обработан](#handled)

Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя. В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.

#### KeyEventKind 

Тип события key, который привел к инициированию события.

> общедоступная [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)

#### KeyEventLParam 

Значение LPARAM, сопровождающее сообщение в окне.

> public int [KeyEventLParam](#keyeventlparam)

Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.

#### PhysicalKeyStatus 

Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.

> общедоступная [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)

#### VirtualKey 

Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.

> Открытый uint [VirtualKey](#virtualkey)

Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A". Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).
