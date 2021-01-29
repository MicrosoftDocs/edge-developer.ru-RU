---
description: Все способы открытия Microsoft Edge DevTools.
title: Открытие Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d21ebbf0b84be757c1b7a69d36b3bd3cc8403c6d
ms.sourcegitcommit: 77c8f42cc84600c2b853b15aaaecf0749b74bb01
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2020
ms.locfileid: "11238229"
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
*   Выберите `Control` + `Shift` + `C` \(Windows, Linux\) или `Command` + `Option` + `C` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Параметр Проверить" lightbox="../media/bing-right-click-inspect.msft.png":::
   Параметр **"Проверить"**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Открытие панели консоли  

Каждая из следующих задач позволяет [][DevtoolsConsoleIndex] открыть панель консоли для просмотра зарегистрированных сообщений или запуска JavaScript.  

*   Чтобы открыть панель консоли, с помощью [следующих][DevtoolsConsoleIndex] действий.  
    
    1.  [Откройте DevTools.](#open-microsoft-edge-devtools)  
    1.  Выберите [панель][DevtoolsConsoleIndex] консоли.  

*   Чтобы перейти непосредственно в [панель][DevtoolsConsoleIndex] консоли, выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevtoolsShortcutsIndex].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Открытие предыдущей панели  

Чтобы перейти к предыдущей открытой панели, выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevtoolsShortcutsIndex].  

## Открытие Microsoft Edge DevTools  

Чтобы открыть DevTools, используйте один из следующих параметров.  

*   Используйте пользовательский интерфейс Microsoft Edge.  
    
    1.  Выберите **значок "Параметры" и другие** параметры \( `...` \).  
    1.  Choose **More Tools**.  
    1.  Choose **Developer Tools**.  
    
*   Используйте клавиатуру.  
    *   Выберите `F12` или `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  

Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Откройте DevTools из главного меню Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Откройте DevTools из главного меню Microsoft Edge  
:::image-end:::  

## Автоматическое открытие DevTools на каждой новой вкладке  

Чтобы автоматически открыть DevTools на каждой новой вкладке, откройте Microsoft Edge из командной строки и передав `--auto-open-devtools-for-tabs` флаг.  

### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Включите или выключите клавишу F12  

Чтобы изменить параметр `F12` сочетания клавиш, который открывает DevTools, выполните следующие действия.  

1.  Выберите значок **"Параметры" и другие** параметры `...` \( \) > **"Параметры".**  
1.  В **параметрах поиска введите** `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="Параметр Открыть DevTools при нажатии клавиши F12" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       Параметр **"Открыть DevTools"** при нажатии клавиши F12  
    :::image-end:::  
    
1.  Нажмите **кнопку "Открыть DevTools"** при нажатии клавиши F12, чтобы отключить параметр \(или on\).  Отключите параметр, чтобы не открывать DevTools с помощью сочетания `F12` клавиш.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="Параметр Открыть DevTools при нажатии клавиши F12 отключен" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       Параметр **"Открыть DevTools"** при нажатии клавиши F12 отключен  
    :::image-end:::  
    
1.  После отключения этого переключа выберите, чтобы подтвердить, что `F12` DevTools больше не открывается.  
    
    > [!NOTE]
    > После отключения параметра **Open the DevTools** при нажатии клавиши F12, чтобы открыть DevTools, выполните одно из следующих действий.  
    > 
    > *   Выберите `Ctrl` + `Shift` + `I` .  
    > *   Откройте контекстное меню \(щелкните правой кнопкой мыши\) > **проверить.**  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документация Майкрософт"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Сочетания клавиш Microsoft Edge DevTools | Документы Майкрософт"  

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
