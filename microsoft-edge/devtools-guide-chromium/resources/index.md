---
description: Организация ресурсов по кадру, домену, типу или другим критериям.
title: Просмотр ресурсов страниц с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 75063b23f23c25ff4fe2e7f6e044a2de9a7b1ccd
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398226"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a>Просмотр ресурсов страниц с помощью Microsoft Edge DevTools  

В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.  Ресурсы — это файлы, необходимые странице для правильного отображения.  Примеры ресурсов: CSS, JavaScript и HTML-файлы, а также изображения.  

В этом руководстве предполагается, что [][MDNLearnWebDevelopment] вы знакомы с основами веб-разработки и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## <a name="open-resources"></a>Открытые ресурсы  

Когда вы знаете имя ресурса, который необходимо проверить, меню **команд** обеспечивает быстрый способ открытия ресурса.  

1.  Выберите `Control` + `P` \(Windows, Linux\) `Command` + `P` или \(macOS\).  Открывается диалоговое окно **Open File.**  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно Open File" lightbox="../media/resources-command-menu-empty.msft.png":::
       Диалоговое **окно Open File**  
    :::image-end:::  
    
1.  Выберите файл из выпадаемой папки или начните вводить имя файла и выберите, как только правильный файл будет выделен в поле `Enter` автокомплетов.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Введите имя файла в диалоговом окте "Открытый файл"" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Введите имя файла в **диалоговом окте "Открытый** файл"  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a>Откройте ресурсы в средстве Network  

Перейдите [для проверки сведений о ресурсе.][DevtoolsNetworkInspectDetailsResource]  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Проверка ресурса в средстве Network" lightbox="../media/resources-network-response.msft.png":::
   Проверка ресурса в **средстве Network**  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a>Выявление ресурсов в средстве Network с других панелей  

В [разделе Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.  Если вы когда-либо хотите **** проверить ресурс в средстве Network, наведите курсор на ресурс, откройте контекстное меню \(правой кнопкой мыши\) и выберите Показать в **панели Сети**.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Reveal in Network panel" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Reveal in Network panel**  
:::image-end:::  

## <a name="browse-resources"></a>Просмотр ресурсов  

### <a name="browse-resources-in-the-network-panel"></a>Просмотр ресурсов в панели Network  

Перейдите к [сетевой активности журнала][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ресурсы страницы в сетевом журнале" lightbox="../media/resources-network-resources.msft.png":::
   Ресурсы страницы в **сетевом журнале**  
:::image-end:::  

### <a name="browse-by-directory"></a>Просмотр каталога  

Просмотр ресурсов страницы, организованной каталогом:  

1.  Выберите средство **Источники** для открытия панели **Источники.**  
1.  Выберите **панель Page,** чтобы показать ресурсы страницы.  **Откроется** области Страницы.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Области Страницы" lightbox="../media/resources-sources-page-empty.msft.png":::
       Панель **Page**  
    :::image-end:::  
    
    Вот разбивка неявных элементов на предыдущем рисунке.  
    
    | Элемент Page | Описание |  
    |:--- |:--- |  
    | `top` | Основной контекст просмотра [документов][MDNInlineFrame]. |  
    | `airhorner.com` | Домен.  Все ресурсы, вложенные в него, приходят из этого домена.  Например, полный URL-адрес `comlink.global.j` файла, `https://airhorner.com/scripts/comlink.global.js` вероятно, . |  
    | `scripts` | Каталог. |  
    | `(index)` | Основной HTML-документ. |  
    | `sw.js` | Контекст времени работы сотрудника службы. |  
    
1.  Выберите ресурс, чтобы просмотреть его в **редакторе**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Просмотр файла в редакторе" lightbox="../media/resources-sources-page-resource.msft.png":::
       Просмотр файла в **редакторе**  
    :::image-end:::  
    
### <a name="browse-by-filename"></a>Просмотр по имени файла  

По умолчанию **ресурсы групп групп** страниц по каталогу.  Чтобы отключить эту группу и просмотреть ресурсы для каждого домена в качестве плоского списка:  

1.  Откройте **панель Page.**  Перейдите [к просмотру по каталогу](#browse-by-directory).  
1.  Выберите **дополнительные параметры** `...` и **отключим группу по папке**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Параметр Group By Folder" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       Параметр **Group By Folder**  
    :::image-end:::  
    
    Ресурсы организованы по типу файла.  В каждом типе файла ресурсы организованы в алфавитном порядке.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Панель Page после отключения группы по папке" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       Панель **Page** после отключения **группы по папке**  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a>Просмотр по типу файла  

Сгруппить ресурсы в зависимости от типа файла:  

1.  Выберите **вкладку Application.**  Откроется **средство** Приложения.  По умолчанию **области Манифест** обычно открывается первым.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Средство приложения" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Средство **приложения**  
    :::image-end:::  
    
1.  Прокрутите вниз **до области Frames.**  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Рамки" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       **Рамки**  
    :::image-end:::  
    
1.  Расширь разделы, в которых вас интересует.  
1.  Выберите ресурс для просмотра.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Просмотр ресурса в панели приложений" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Просмотр ресурса в панели **приложений**  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a>Просмотр файлов по типу в панели Network  

Перейдите [к фильтру по типу ресурса.][DevtoolsNetworkFilterByResourceType]  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Фильтр CSS в сетевом журнале" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Фильтр CSS в **сетевом журнале**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтр по типу ресурса — проверьте активность сети в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Проверка сведений о ресурсе — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Сетевое действие журнала — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Узнайте, как | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/resources/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
