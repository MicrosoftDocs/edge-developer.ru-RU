---
description: Фрагменты кода — это небольшие скрипты, которые можно раздать и запускать в средстве Sources Microsoft Edge DevTools.  Вы можете получать доступ к ресурсам и запускать их с любой веб-страницы.  При запуске фрагмента он запускается из контекста открытой веб-страницы.
title: Запуск фрагментов Кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230959"
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

# Запуск фрагментов Кода JavaScript на любой веб-странице с помощью Microsoft Edge DevTools  

Если один и тот же [][DevtoolsConsoleIndex] код в консоли повторяется, рассмотрите возможность сохранения кода в качестве фрагмента кода.  Фрагменты кода — это сценарии, которые вы пишете в средстве ["Источники".][DevToolsSourcesTool]  Фрагменты кода имеют доступ к контексту JavaScript веб-страницы, и вы можете запускать фрагменты на любой веб-странице.  Параметры безопасности большинства веб-страниц блокируют загрузку других сценариев в фрагментах кода.  По этой причине необходимо включить весь код в один файл.  

Фрагменты кода — это [][WikiBookmarklet] альтернатива закладки с разницей в том, что фрагменты кода запускаются только в DevTools и не ограничиваются допустимой длиной URL-адреса.  

Использование фрагментов кода — отличный способ изменить некоторые моменты на стороне веб-страницы.  Изменения кода в фрагментах кода добавляются на текущую веб-страницу и запускаются в том же контексте.  Дополнительные сведения об изменении существующего кода веб-страницы можно найти в [переопределениях.][DevtoolsJavascriptOverrides]  

:::row:::
   :::column span="":::
      Например, на следующем рисунке показана домашняя страницы DevTools слева и некоторый исходный код фрагмента справа.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Перед запуском фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         Веб-страницы перед запуском фрагмента  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Исходный код фрагмента кода из веб-страницы перед запуском фрагмента кода.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

На следующем рисунке после запуска фрагмента отображается веб-страницу.  В **окне "Консольный ящик"** отображается сообщение о том, что фрагмент кода занося в журнал, а содержимое веб-страницы `Hello, Snippets!` полностью меняется.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Веб-страницу после запуска фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Веб-страницу после запуска фрагмента  
:::image-end:::  

## Открытие области фрагментов кода  

В **области фрагментов кода** перечислены фрагменты кода.  Если вы хотите изменить фрагмент кода, его необходимо **** открыть в области фрагментов кода.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="The Snippets pane" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   The **Snippets** pane  
:::image-end:::  

### Открытие области фрагментов кода с помощью мыши  

1.  Откройте средство **"Источники"** на вкладке **"Источники".**  Обычно **по** умолчанию открывается страница.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Средство Источники с открытой в левой области страницы" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Средство **"Источники"** с **открытой** в левой области страницы  
    :::image-end:::  
    
1.  Откройте **вкладку "Фрагменты** кода", чтобы открыть **ее.**  Может потребоваться выбрать **дополнительные** вкладки \( Дополнительные вкладки \), чтобы получить доступ ![ к ][ImageMoreTabsIcon] **параметру фрагментов** кода.  
    
### Открытие области фрагментов кода с помощью меню команд  

1.  Наберите курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.  
1.  `Snippets`Введите, **выберите "Показать фрагменты кода"** и выберите `Enter` команду.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда Показать фрагменты кода" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Команда **"Показать фрагменты кода"**  
    :::image-end:::  
    
## Создание фрагментов кода  

### Создание фрагмента кода на панели источников  

1.  [Откройте области **фрагментов** ](#open-the-snippets-pane)кода .  
1.  Choose **New snippet**.  
1.  Введите имя фрагмента кода, а затем выберите `Enter` для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Имя фрагмента" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Имя фрагмента  
    :::image-end:::  
    
### Создание фрагмента кода в меню команд  

1.  Наберите курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.  
1.  Введите `Snippet` , **выберите "Создать новый фрагмент",** а затем `Enter` выберите команду.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Команда для создания нового фрагмента  
    :::image-end:::  
    
Чтобы переименовать новый фрагмент с пользовательским именем, перейдите к переименовывать [фрагменты](#rename-snippets)кода.  

## Изменение фрагментов кода  

1.  [Откройте области **фрагментов** ](#open-the-snippets-pane)кода .  
1.  В области **фрагментов кода** выберите имя фрагмента, который необходимо изменить.  Он откроется в **редакторе кода.**  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Редактор **кода**  
    :::image-end:::  
    
1.  Используйте редактор **кода,** чтобы добавить JavaScript в фрагмент кода.  
1.  Если рядом с именем фрагмента появляется звездочка, это означает, что у вас есть несмеченный код.  Выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\) для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента указывает несмесяный код" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Звездочка рядом с именем фрагмента указывает несмесяный код  
    :::image-end:::  
    
## Запуск фрагментов кода  

### Запуск фрагмента кода на панели источников  

1.  [Откройте области **фрагментов** ](#open-the-snippets-pane)кода .  
1.  Выберите имя фрагмента кода, который нужно выполнить.  Фрагмент кода откроется в **редакторе кода.**  
1.  Choose **Run Snippet** \( ![ Run Snippet ][ImageRunSnippetIcon] \) or select `Control` + `Enter` \(Windows, Linux\) or `Command` + `Enter` \(macOS\).  
    
### Запуск фрагмента с помощью меню команд  

1.  Наберите курсор где-нибудь в DevTools.  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню команд.  
1.  Удалите символ и введите символ, за которым следует имя фрагмента кода, `>` `!` который необходимо выполнить.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Запуск фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       Запуск фрагмента из меню **команд**  
    :::image-end:::  
    
1.  Выберите `Enter` запуск фрагмента кода.  

## Переименование фрагментов кода  

1.  [Откройте области **фрагментов** ](#open-the-snippets-pane)кода .  
1.  Наведите курсор на имя фрагмента кода, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Переименовать".**  
    
## Удаление фрагментов кода  

1.  [Откройте области **фрагментов** ](#open-the-snippets-pane)кода .  
1.  Наведите курсор на имя фрагмента кода, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Удалить".**  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Майкрософт"  
[DevToolsSourcesTool]: ../sources/index.md "Обзор средства "Источники" | Документы Майкрософт"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Переопределения | Документы Майкрософт"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
