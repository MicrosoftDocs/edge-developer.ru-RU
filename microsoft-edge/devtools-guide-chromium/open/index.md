---
description: Все способы открытия Microsoft Edge DevTools.
title: Открытие Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ce46f08be176fb58161355d67167c3e39043e83b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235150"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# Открытие Microsoft Edge DevTools  

Существует множество способов открыть Microsoft Edge DevTools, так как разным пользователям нужен быстрый доступ к различным частям пользовательского интерфейса DevTools.  

## Откройте панель "Элементы" для проверки DOM или CSS  

Каждая из следующих задач позволяет проверить стили или атрибуты узла DOM.

*   Наведите курсор на элемент, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Проверить".**  
*   Выберите `Control` + `Shift` + `C` \(Windows, Linux\) или `Command` + `Option` + `C` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Параметр "Проверить"" lightbox="../media/bing-right-click-inspect.msft.png":::
   Параметр **"Проверить"**  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Открытие панели консоли  

Каждая из следующих задач позволяет [][DevToolsConsoleIndex] открыть панель консоли для просмотра зарегистрированных сообщений или запуска JavaScript.  

*   Чтобы открыть панель консоли, с помощью [следующих][DevToolsConsoleIndex] действий.  
    
    1.  [Откройте DevTools.](#open-microsoft-edge-devtools)  
    1.  Выберите [панель][DevToolsConsoleIndex] консоли.  

*   Чтобы перейти непосредственно в панель [консоли,][DevToolsConsoleIndex] выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).  Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Открытие предыдущей панели  

Чтобы перейти к предыдущей открытой панели, выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  

## Открытие Microsoft Edge DevTools  

Каждая из следующих задач позволяет открыть DevTools.  

*   Чтобы открыть Microsoft Edge DevTools, с помощью следующих действий.  
    
    1.  Выберите  `...` значок \(Параметры **и еще** значок\).  
    1.  Choose **More Tools**.  
    1.  Choose **Developer Tools**.  
    
*   Чтобы открыть Microsoft Edge DevTools, выберите `F12` `Control` + `Shift` + `I` или \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Откройте DevTools из главного меню Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Откройте DevTools из главного меню Microsoft Edge  
:::image-end:::  

## Автоматическое открытие DevTools на каждой новой вкладке  

Чтобы автоматически открыть DevTools на каждой новой вкладке, откройте Microsoft Edge из командной строки и передав `--auto-open-devtools-for-tabs` флаг.  

#### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

#### [bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleIndex]: ../console/index.md "Обзор консоли | Документация Майкрософт"  
[DevtoolsShortcuts]: ../shortcuts/index.md "Сочетания клавиш Microsoft Edge DevTools — Microsoft Docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/open) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
