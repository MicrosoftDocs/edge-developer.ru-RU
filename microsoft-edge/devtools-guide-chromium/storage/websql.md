---
description: Просмотр данных веб-SQL с панели приложений Microsoft Edge DevTools.
title: Просмотр данных веб-SQL с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 802f21cb4cadfa3ee08ddd8feeea8b8132551740
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231176"
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

# Просмотр данных веб-SQL с помощью Microsoft Edge DevTools  

> [!WARNING]
> Спецификация веб-SQL не [поддерживается.][W3CWebSQLStatus]  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных веб-SQL.  

## Просмотр данных веб-SQL  

1.  Выберите **вкладку "Источники",** чтобы открыть **средство "Источники".**  Обычно **по** умолчанию открывается окно манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       The **Manifest** pane  
    :::image-end:::  
    
1.  **Разоберись с SQL** веб-страниц, чтобы просмотреть базы данных и таблицы.  На следующем рисунке под **html5meetup** находится база данных, а **комнаты** — таблица.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Веб-SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       **Веб-SQL**  
    :::image-end:::  
    
1.  Выберите таблицу, чтобы просмотреть данные для этой таблицы.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Просмотр данных таблицы веб-SQL" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Просмотр данных таблицы веб-SQL  
    :::image-end:::  
    
## Изменение данных веб-SQL  

При просмотре таблицы веб-SQL нельзя редактировать данные веб-SQL, как по сравнению с предыдущими.  Но вы можете запускать в консоли web SQL утверждения, которые редактирует или удаляет таблицы.  См. [запросы SQL веб-сайтов.](#run-web-sql-queries)  

## Выполнение запросов SQL веб-сайтов  

1.  Выберите базу данных, чтобы открыть консоль для этой базы данных.  
1.  Введите SQL Web SQL и выберите `Enter` его запуск.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Использование консоли web SQL для удаления строки из таблицы" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Использование консоли web SQL для удаления строки из таблицы  
    :::image-end:::  
    
## Обновление таблицы веб-SQL  

DevTools не обновляет таблицы в режиме реального времени.  Чтобы обновить данные в таблице, выполните следующие действия.  

1.  [Просмотр данных в таблице веб-SQL.](#view-web-sql-data)  
1.  Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).  
    
## Фильтрация столбцов в таблице веб-SQL  

1.  [Просмотр данных в таблице веб-SQL.](#view-web-sql-data)  
1.  Используйте **текстовое поле "Видимые столбцы",** чтобы указать, какие столбцы нужно отметить.  Предо в качестве CSV-списка имена столбцов.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Использование текстового окна Видимые столбцы для уменьшения числа столбцов" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Использование **текстового окна "Видимые столбцы"** для уменьшения числа столбцов  
    :::image-end:::  
    
## Удаление всех данных SQL веб-сайтов  

1.  Откройте области **"Очистить** хранилище".  
1.  Убедитесь, **что** SQL веб-страницы включен.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="The Web SQL checkbox" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       The **Web SQL** checkbox  
    :::image-end:::  
    
1.  Выберите **"Очистить данные сайта".**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Кнопка очистки данных сайта" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Кнопка **очистки данных** сайта  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "База данных веб SQL | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/websql) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
