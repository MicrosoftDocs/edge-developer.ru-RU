---
description: Все способы открытия Microsoft Edge DevTools.
title: Откройте Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 770a9d3e7a0eaaecf322d2ca847d971d1ad11b9a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398268"
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

# <a name="open-microsoft-edge-devtools"></a>Откройте Microsoft Edge DevTools  

Существует множество способов открытия Microsoft Edge DevTools, так как разным пользователям нужен быстрый доступ к различным частям пользовательского интерфейса DevTools.  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Откройте панель Elements для проверки DOM или CSS  

Каждая из следующих задач позволяет проверять стили или атрибуты узла DOM.

*   Наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Инспектировать**.  
*   Выберите `Control` + `Shift` + `C` \(Windows, Linux\) `Command` + `Option` + `C` или \(macOS\).  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="Параметр Inspect" lightbox="../media/bing-right-click-inspect.msft.png":::
   Параметр **Inspect**  
:::image-end:::  

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Откройте панель Консоли  

Каждая из следующих задач позволяет [][DevtoolsConsoleIndex] открыть консольную панель для просмотра зарегистрированных сообщений или запуска JavaScript.  

*   Чтобы открыть консоль, используйте [следующие][DevtoolsConsoleIndex] действия.  
    
    1.  [Откройте DevTools](#open-microsoft-edge-devtools).  
    1.  Выберите [консольную][DevtoolsConsoleIndex] панель.  

*   Чтобы перейти прямо [в][DevtoolsConsoleIndex] консольную панель, выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Откройте предыдущую панель  

Чтобы перейти к предыдущей панели, которую вы открыли, выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  

## <a name="open-microsoft-edge-devtools"></a>Откройте Microsoft Edge DevTools  

Чтобы открыть DevTools, используйте любой из следующих параметров.  

*   Используйте пользовательский интерфейс Microsoft Edge.  
    
    1.  Выберите **значок Параметры и другие** `...` \( \) > **дополнительные**средства  >   **разработки инструментов.**  
    
*   Используйте клавиатуру.  
    *   Выберите `F12` `Control` + `Shift` + `I` или \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).  

Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Откройте DevTools из основного меню Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Откройте DevTools из основного меню Microsoft Edge  
:::image-end:::  

## <a name="auto-open-devtools-on-every-new-tab"></a>Автоматическое открытие DevTools на каждой новой вкладке  

Чтобы автоматически открыть DevTools на каждой новой вкладке, откройте Microsoft Edge из командной строки и передай `--auto-open-devtools-for-tabs` флаг.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>Bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>Bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Toggle the F12 keyboard shortcut on or off  

Чтобы изменить параметр `F12` ярлыка клавиатуры, открываемой в DevTools, выполните следующие действия.  

1.  Выберите значок **Параметры и больше** \( `...` \) значок > **параметры**.  
1.  В **параметрах поиска**введите `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="Откройте параметр DevTools при нажатии клавиши F12" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       Откройте **параметр DevTools при** нажатии клавиши F12  
    :::image-end:::  
    
1.  Откройте **devTools,** когда клавиша F12 прижата, чтобы переключить параметр для отключения \(или on\).  Переключите параметр, чтобы остановить путь к клавиатуре `F12` от открытия DevTools.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="Откройте параметр DevTools при нажатии клавиши F12" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       Откройте **параметр DevTools при** нажатии клавиши F12  
    :::image-end:::  
    
1.  После того, как вы установите отключение очки, выберите, чтобы подтвердить, что `F12` DevTools больше не открыт.  
    
    > [!NOTE]
    > После отключения **параметра Open the DevTools** при нажатии клавиши F12 для открытия DevTools выполните одно из следующих действий.  
    > 
    > *   Выберите `Ctrl` + `Shift` + `I` .  
    > *   Откройте контекстное меню \(правой кнопкой мыши\) **>.**  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документация Майкрософт"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/open) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
