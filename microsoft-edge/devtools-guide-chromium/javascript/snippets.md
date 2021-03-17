---
description: Фрагменты — это небольшие скрипты, которые можно авторить и запускать в средстве Источники Microsoft Edge DevTools.  Вы можете получать доступ к ресурсам и запускать их с любой веб-страницы.  При запуске фрагмента выполняется из контекста открытой веб-страницы.
title: Запуск фрагментов JavaScript на любой странице с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439425"
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
   limitations under the License.  -->  

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a>Запуск фрагментов JavaScript на любой веб-странице с помощью Microsoft Edge DevTools  

Если вы несколько раз запускаете один и тот же код в консоли, сберегайте код в качестве фрагмента. [][DevtoolsConsoleIndex]  Фрагменты — это скрипты, которые вы пишете в [средстве Sources.][DevToolsSourcesTool]  Фрагменты имеют доступ к контексту JavaScript веб-страницы, и вы можете запускать фрагменты на любой веб-странице.  Параметры безопасности большинства веб-страниц блокируют загрузку других скриптов в фрагментах.  По этой причине необходимо включить весь код в один файл.  

Фрагменты являются альтернативой [][WikiBookmarklet] закладки с разницей, что фрагменты работают только в DevTools и не ограничиваются разрешенной длиной URL-адреса.  

Использование фрагментов является отличным способом изменить некоторые вещи на сторонних веб-странице.  Изменения кода в фрагментах добавляются на текущую веб-страницу и запускаются в том же контексте.  Дополнительные сведения об изменении существующего кода веб-страницы перейдите к [переопределениям.][DevtoolsJavascriptOverrides]  

:::row:::
   :::column span="":::
      Например, на следующем рисунке показана домашняя страницы DevTools слева и некоторый исходный код фрагмента справа.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Перед запуском фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Веб-страницу перед запуском фрагмента  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Исходный код фрагмента из веб-страницы перед запуском фрагмента.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

На следующем рисунке веб-страницу отображается после запуска фрагмента.  В **ящике** консоли всплывет сообщение о том, что фрагмент журнала и содержимое веб-страницы полностью `Hello, Snippets!` меняется.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Веб-страницу после запуска фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Веб-страницу после запуска фрагмента  
:::image-end:::  

## <a name="open-the-snippets-pane"></a>Откройте области фрагментов  

В **области фрагментов** перечислены фрагменты.  При редактировании фрагмента необходимо открыть его из области **фрагментов.**  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Области фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Области **фрагментов**  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a>Откройте области фрагментов с помощью мыши  

1.  Выберите **вкладку Источники,** чтобы открыть **средство Источники.**  Обычно **области Страницы** открываются по умолчанию.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Средство Sources с открываемой слева области Страницы" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Средство **Sources** с **открываемой** слева области Страницы  
    :::image-end:::  
    
1.  Выберите **вкладку Фрагменты, чтобы** открыть области **фрагментов.**  Возможно, вам потребуется выбрать **дополнительные вкладки** \. Дополнительные вкладки \) для доступа ![ к ](../media/more-tabs-icon.msft.png) **параметру Фрагменты.**  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a>Откройте области фрагментов с командным меню  

1.  Сосредоточь курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.  
1.  `Snippets`Введите, **выберите показать фрагменты,** а затем выберите `Enter` для запуска команды.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда фрагментов show" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Команда **фрагментов** show  
    :::image-end:::  
    
## <a name="create-snippets"></a>Создание фрагментов  

### <a name="create-a-snippet-through-the-sources-panel"></a>Создание фрагмента через панель Источники  

1.  [Откройте **области фрагментов** ](#open-the-snippets-pane).  
1.  Выберите **новый фрагмент**.  
1.  Введите имя фрагмента фрагмента, а затем выберите `Enter` для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Имя фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Имя фрагмента  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a>Создание фрагмента в командном меню  

1.  Сосредоточь курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.  
1.  `Snippet`Введите, выберите Создание нового **фрагмента,** а затем `Enter` выберите для запуска команды.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда создания нового фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Команда создания нового фрагмента  
    :::image-end:::  
    
Чтобы переименовать новый фрагмент с настраиваемой именем, перейдите к [фрагментам переименования.](#rename-snippets)  

## <a name="edit-snippets"></a>Изменение фрагментов  

1.  [Откройте **области фрагментов** ](#open-the-snippets-pane).  
1.  В области **фрагментов** выберите имя фрагмента, который необходимо изменить.  Он открывается в **редакторе кода**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Редактор **кода**  
    :::image-end:::  
    
1.  Используйте редактор **кода,** чтобы добавить JavaScript в фрагмент.  
1.  Если звездочка появится рядом с именем фрагмента, это означает, что у вас есть незасвеченный код.  Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента указывает неавтокопимый код" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Звездочка рядом с именем фрагмента указывает неавтокопимый код  
    :::image-end:::  
    
## <a name="run-snippets"></a>Запуск фрагментов  

### <a name="run-a-snippet-from-the-sources-panel"></a>Запуск фрагмента из панели Источники  

1.  [Откройте **области фрагментов** ](#open-the-snippets-pane).  
1.  Выберите имя фрагмента, который необходимо выполнить.  Фрагмент кода открывается в **редакторе кода**.  
1.  Выберите **фрагмент run** \( Run ![ Snippet \) или выберите ](../media/run-snippet-icon.msft.png) `Control` + `Enter` \(Windows, Linux\) или `Command` + `Enter` \(macOS\).  
    
### <a name="run-a-snippet-with-the-command-menu"></a>Запуск фрагмента с командным меню  

1.  Сосредоточь курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия командного меню.  
1.  Удалите символ и введите символ с именем фрагмента, который необходимо `>` `!` выполнить.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Запуск фрагмента из меню команды" lightbox="../media/javascript-search-run-command.msft.png":::
       Запуск фрагмента из меню **команды**  
    :::image-end:::  
    
1.  Выберите `Enter` для запуска фрагмента.  

## <a name="rename-snippets"></a>Переименовать фрагменты  

1.  [Откройте **области фрагментов** ](#open-the-snippets-pane).  
1.  Наведите курсор на имя фрагмента, откройте контекстное меню \(правой кнопкой мыши\) и выберите **переименование**.  
    
## <a name="delete-snippets"></a>Удаление фрагментов  

1.  [Откройте **области фрагментов** ](#open-the-snippets-pane).  
1.  Наведите курсор на имя фрагмента, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Удалить**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Майкрософт"  
[DevToolsSourcesTool]: ../sources/index.md "Обзор инструментов источников | Документы Майкрософт"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Переопределения | Документы Майкрософт"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
