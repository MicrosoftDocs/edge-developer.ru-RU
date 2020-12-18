---
description: Просмотр данных кэша приложений с панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша приложений с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3d73047a8332e4d6cae5f7411f968a7dfe4c3738
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230784"
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

# Просмотр данных кэша приложений с помощью Microsoft Edge DevTools  

> [!WARNING]
> API кэша приложений удаляется [с веб-платформы.][HTMLStandardOfflineWebApplications]  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки ресурсов [кэша][MDNWebAPIsWindowApplicationCache] приложений.  

## Просмотр данных кэша приложений  

1.  Выберите **вкладку "Источники",** чтобы открыть панель **источников.**  Обычно **по** умолчанию открывается окно манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       The **Manifest** pane  
    :::image-end:::  

1.  Раз expand **the Application Cache** section and choose a cache to view the resources.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="The Application Cache pane" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       The **Application Cache** pane  
    :::image-end:::  

Каждая строка таблицы представляет кэшный ресурс.  

Столбец **"Тип"** представляет [категорию ресурса.][MDNHTMLResourcesInAnApplicationCache]  

| Категория | Сведения |  
|:--- |:--- |  
| `Explicit` | Этот ресурс был явно указан в манифесте. |  
| `Fallback` | URL-адрес является откатом для другого ресурса.  URL-адрес другого ресурса не указан в DevTools. |  
| `Master` | Атрибут ресурса указывает, что кэш `manifest` является родительским для ресурса. |  
| `Network` | Манифест указывает, что ресурс должен быть источником из сети. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

В нижней части таблицы находятся значки состояния, указывающие сетевое подключение и состояние **кэша приложений.**  Кэш **приложений может** иметь следующие состояния.  

| Состояние | Сведения |  
|:--- |:--- |  
| `CHECKING` | Манифест извлекется и проверяется на наличие обновлений. |  
| `DOWNLOADING` | Ресурсы добавляются в кэш. |  
| `IDLE` | В кэше нет новых изменений. |  
| `OBSOLETE` | Кэш удаляется. |  
| `UPDATEREADY` |  Доступна новая версия кэша. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Автономные веб-приложения — HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ресурсы в кэше приложений | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache — веб-API | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
