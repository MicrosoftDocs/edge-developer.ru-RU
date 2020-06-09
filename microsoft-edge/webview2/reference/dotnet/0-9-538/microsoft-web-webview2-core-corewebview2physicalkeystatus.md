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
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699133"
---
# Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Указывает на то, является ли ключ дополнительным ключом.
[IsKeyReleased](#iskeyreleased) | Состояние перехода.
[IsMenuKeyDown](#ismenukeydown) | Код контекста.
[RepeatCount](#repeatcount) | Число повторов для текущего сообщения.
[ScanCode](#scancode) | Код сканирования.
[WasKeyDown](#waskeydown) | Предыдущее состояние ключа.

Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Участников

#### IsExtendedKey 

Указывает на то, является ли ключ дополнительным ключом.

> public int [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

Состояние перехода.

> public int [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

Код контекста.

> public int [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

Число повторов для текущего сообщения.

> Открытый uint [repeatCount](#repeatcount)

#### ScanCode 

Код сканирования.

> Открытый uint [ScanCode](#scancode)

#### WasKeyDown 

Предыдущее состояние ключа.

> public int [WasKeyDown](#waskeydown)
