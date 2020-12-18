---
description: Просмотр данных кэша с панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 770001beb9b7eebd4dae76355a1f3e41a8021ecb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230805"
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

# Просмотр данных кэша с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки [данных кэша.][MDNCache]  

Если вы пытаетесь проверить [данные кэша HTTP,][MDNHTTPCaching] это руководство вам не нужно.  Найдите сведения в столбце **"Размер"** **сетевого журнала.**  Перейдите в [журнал сетевой активности.][DevtoolsNetworkLogActivity]  

## Просмотр данных кэша  

1.  Выберите **вкладку "Приложение",** чтобы открыть **панель** приложений.  Обычно **по** умолчанию открывается окно манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       The **Manifest** pane  
    :::image-end:::  
    
1.  Раз развернуть раздел **"Хранилище кэша",** чтобы просмотреть доступные кэши.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Доступные кэши" lightbox="../media/storage-application-cache-storage.msft.png":::
       Доступные кэши  
    :::image-end:::  
    
1.  Выберите кэш для просмотра содержимого.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Просмотр содержимого кэша" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Просмотр содержимого кэша  
    :::image-end:::  
    
1.  Выберите ресурс, чтобы просмотреть http-заготки в разделе под таблицей.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Просмотр HTTP-загодеров ресурса" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Просмотр HTTP-загодеров ресурса  
    :::image-end:::  
    
1.  Выберите **"Предварительный** просмотр", чтобы просмотреть содержимое ресурса.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Просмотр содержимого ресурса" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Просмотр содержимого ресурса  
    :::image-end:::  
    
## Обновление ресурса  

1.  [Просмотр данных для кэша.](#view-cache-data)  
1.  Выберите ресурс, который нужно обновить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Выбор ресурса для обновления" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Выбор ресурса для обновления  
    :::image-end:::  
    
1.  Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).  
    
## Фильтрация ресурсов  

1.  [Просмотр данных для кэша.](#view-cache-data)  
1.  Используйте **текстовое поле "Фильтр** по пути", чтобы отфильтровать все ресурсы, которые не соответствуют предоставляемой вами пути.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Фильтрация ресурсов, которые не соответствуют указанному пути" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Фильтрация ресурсов, которые не соответствуют указанному пути  
    :::image-end:::  
    
## Удаление ресурса  

1.  [Просмотр данных для кэша.](#view-cache-data)  
1.  Выберите ресурс, который нужно удалить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Выбор ресурса для удаления" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Выбор ресурса для удаления  
    :::image-end:::  
    
1.  Choose **Delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).  
    
## Удаление всех данных кэша  

1.  Откройте **приложение**  >  **"Очистить хранилище".**  
1.  Убедитесь, что включен **контрольный** ящик хранилища кэша.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="The Cache Storage checkbox" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       The **Cache Storage checkbox**  
    :::image-end:::  
    
1.  Выберите **"Очистить данные сайта".**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Кнопка очистки данных сайта" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Кнопка **очистки данных** сайта  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Запись сетевой активности | Документы Майкрософт"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэшинг HTTP | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cache) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
