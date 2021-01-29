---
description: Упорядодрять ресурсы по кадру, домену, типу или другим критериям.
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 353c36a9d98dac287c3fdaaa3feed2fe3b17cd07
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230777"
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

# Просмотр ресурсов страниц с помощью Microsoft Edge DevTools  

  

В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.  Ресурсы — это файлы, необходимые странице для правильного отображения.  Примеры ресурсов: CSS, JavaScript и HTML-файлы, а также изображения.  

В этом руководстве предполагается, что [][MDNLearnWebDevelopment] вы знакомы с основами веб-разработки и [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

## Открытие ресурсов  

Если вы знаете имя ресурса, который нужно **** проверить, меню команд обеспечивает быстрый способ открытия ресурса.  

1.  Выберите `Control` + `P` \(Windows, Linux\) или `Command` + `P` \(macOS\).  Откроется **диалоговое окно** "Открыть файл".  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно Открыть файл" lightbox="../media/resources-command-menu-empty.msft.png":::
       Диалоговое **окно "Открыть** файл"  
    :::image-end:::  
    
1.  Выберите файл в выпадаемом окне или начните вводить имя файла и выберите его после выделения нужного файла в поле `Enter` автозаполнеия.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Введите имя файла в диалоговом окке Открыть файл" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Введите имя файла в диалоговом окке **"Открыть** файл"  
    :::image-end:::  
    
### Открытие ресурсов на панели "Сеть"  

Перейдите [к просмотру сведений о ресурсе.][DevtoolsNetworkInspectDetailsResource]  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Проверка ресурса на панели Сеть" lightbox="../media/resources-network-response.msft.png":::
   Проверка ресурса на панели **"Сеть"**  
:::image-end:::  

### Ресурсы раскрытия на панели "Сеть" с других панелей  

В [разделе "Обзор](#browse-resources) ресурсов" ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.  Если вы когда-либо хотите **** проверить ресурс на панели "Сеть", щелкните правой кнопкой мыши ресурс и выберите "Показать" **на панели "Сеть".**  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Показать на панели Сеть" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Показать на панели "Сеть"**  
:::image-end:::  

## Просмотр ресурсов  

### Просмотр ресурсов на панели "Сеть"  

Перейдите в [журнал сетевой активности.][DevtoolsNetworkLogActivity]  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ресурсы страницы в сетевом журнале" lightbox="../media/resources-network-resources.msft.png":::
   Ресурсы страницы в **сетевом журнале**  
:::image-end:::  

### Обзор по каталогу  

Чтобы просмотреть ресурсы страницы, организованной по каталогу:  

1.  Щелкните **вкладку "Источники",** чтобы открыть панель **источников.**  
1.  Щелкните **вкладку** "Страница", чтобы отдемонстрировать ресурсы страницы.  **Откроется** страница страницы.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="The Page pane" lightbox="../media/resources-sources-page-empty.msft.png":::
       The **Page** pane  
    :::image-end:::  
    
    Вот разбивка неявных элементов на предыдущем рисунке.  
    
    | Элемент страницы | Описание |  
    |:--- |:--- |  
    | `top` | Контекст просмотра [основного документа.][MDNInlineFrame] |  
    | `airhorner.com` | Домен.  Все вложенные в него ресурсы приходят из этого домена.  Например, полный URL-адрес `comlink.global.j` файла, вероятно, будет `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Каталог. |  
    | `(index)` | Основной HTML-документ. |  
    | `sw.js` | Контекст рабочего времени службы. |  
    
1.  Щелкните ресурс, чтобы просмотреть его в **редакторе.**  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Просмотр файла в редакторе" lightbox="../media/resources-sources-page-resource.msft.png":::
       Просмотр файла в **редакторе**  
    :::image-end:::  
    
### Обзор по имени файла  

По умолчанию в **области** страниц ресурсы группироваться по каталогу.  Чтобы отключить эту группу и просмотреть ресурсы для каждого домена в качестве плоского списка:  

1.  Откройте **страницу.**  Перейдите в ["Обзор по каталогу".](#browse-by-directory)  
1.  Choose **More Options** and `...` disable Group By **Folder**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Параметр Группировка по папке" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Параметр **"Группировка по папке"**  
    :::image-end:::  
    
    Ресурсы организованы по типу файла.  В каждом типе файлов ресурсы организованы в алфавитном порядке.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="The Page pane after disabling Group By Folder" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       The **Page** pane after disabling **Group By Folder**  
    :::image-end:::  
    
### Обзор по типу файла  

Группировка ресурсов в зависимости от типа файла:  

1.  Перейдите на **вкладку "Приложение".**  Откроется **панель** "Приложение".  По умолчанию **сначала открывается** окно манифеста.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Панель Приложение" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Панель **"Приложение"**  
    :::image-end:::  
    
1.  Прокрутите вниз до области **"Кадры".**  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="The Frames pane" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       The **Frames** pane  
    :::image-end:::  
    
1.  Разорите разделы, в которых вас интересует.  
1.  Щелкните ресурс, чтобы просмотреть его.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Просмотр ресурса на панели приложения" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Просмотр ресурса на панели **приложения**  
    :::image-end:::  
    
#### Просмотр файлов по типу на панели "Сеть"  

Перейдите к [фильтру по типу ресурса.][DevtoolsNetworkFilterByResourceType]  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Фильтр CSS в сетевом журнале" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Фильтр CSS в **сетевом журнале**  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтрация по типу ресурса — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Проверка сведений о ресурсе — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Запись сетевой активности — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Изучите веб-разработку | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/resources/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
