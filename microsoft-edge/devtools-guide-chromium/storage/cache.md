---
description: Просмотр данных кэша из панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0ce4dbbf2456579abe84fca48bca8106384995dd
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439319"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a>Просмотр данных кэша с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки [данных кэша.][MDNCache]  

Если вы пытаетесь проверить [данные кэша HTTP,][MDNHTTPCaching] это не нужное руководство.  Сведения в столбце **Размер** сетевого журнала **.**  Перейдите к [сетевой активности журнала][DevtoolsNetworkLogActivity].  

## <a name="view-cache-data"></a>Просмотр данных кэша  

1.  Выберите **вкладку Application** для открытия панели **приложения.**  Обычно **области Манифеста** открываются по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       Области **Манифест**  
    :::image-end:::  
    
1.  **Расширь раздел Хранилища кэша,** чтобы просмотреть доступные кэши.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Доступные кэши" lightbox="../media/storage-application-cache-storage.msft.png":::
       Доступные кэши  
    :::image-end:::  
    
1.  Выберите кэш для просмотра содержимого.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Просмотр содержимого кэша" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Просмотр содержимого кэша  
    :::image-end:::  
    
1.  Выберите ресурс для просмотра заглавных таблиц HTTP в разделе под таблицей.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Просмотр http-заглавных окей ресурса" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Просмотр http-заглавных окей ресурса  
    :::image-end:::  
    
1.  Выберите **Предварительный** просмотр, чтобы просмотреть содержимое ресурса.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Просмотр содержимого ресурса" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Просмотр содержимого ресурса  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a>Обновление ресурса  

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который необходимо обновить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Выберите ресурс для обновления" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Выберите ресурс для обновления  
    :::image-end:::  
    
1.  Выберите **обновление** \. ![ Обновление ](../media/refresh-icon.msft.png) \).  
    
## <a name="filter-resources"></a>Фильтрация ресурсов  

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Используйте **текстовое поле Filter by Path,** чтобы отфильтровать все ресурсы, которые не соответствуют пути, который вы предоставляете.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Фильтрация ресурсов, не совпадает с указанным путем" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Фильтрация ресурсов, не совпадает с указанным путем  
    :::image-end:::  
    
## <a name="delete-a-resource"></a>Удаление ресурса  

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который необходимо удалить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Выбор ресурса для удаления" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Выбор ресурса для удаления  
    :::image-end:::  
    
1.  Выберите **Удалить выбранный** \. ![ Удалить выбранный ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-cache-data"></a>Удаление всех данных кэша  

1.  Open **Application**  >  **Clear Storage**.  
1.  Убедитесь, что включен **почтовый ящик хранения** кэша.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Почтовый ящик хранения кэша" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Почтовый **ящик хранения кэша**  
    :::image-end:::  
    
1.  Выберите **четкие данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Кнопка Clear Site Data" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Кнопка **Clear Site Data**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Журнал сетевой активности | Документы Майкрософт"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Http кэш | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cache) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
