---
description: Просмотр веб-SQL с панели приложений Microsoft Edge DevTools.
title: Просмотр веб-SQL с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 326fe492a3436a40d81c8e31db99a26da4ea054f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397554"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a>Просмотр веб-SQL с помощью Microsoft Edge DevTools  

> [!WARNING]
> Спецификация веб SQL [не поддерживается.][W3CWebSQLStatus]  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки веб-SQL данных.  

## <a name="view-web-sql-data"></a>Просмотр веб-SQL данных  

1.  Выберите средство **Источники** для открытия **средства Источники.**  Обычно **области Манифеста** открываются по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       Области **Манифест**  
    :::image-end:::  
    
1.  **Расширь раздел веб SQL,** чтобы просмотреть базы данных и таблицы.  На следующем рисунке ниже **html5meetup** находится база данных, а в **комнатах** — таблица.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Области веб-SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Области **веб-SQL**  
    :::image-end:::  
    
1.  Выберите таблицу для просмотра данных для этой таблицы.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Просмотр данных таблицы веб-SQL" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Просмотр данных таблицы веб-SQL  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a>Редактирование SQL веб-данных  

При просмотре таблицы веб SQL веб-SQL, например в предыдущей таблице, изменить веб-SQL не удастся.  Но вы можете запускать заявления из консоли SQL, которые редактировать или удалять таблицы.  Перейдите [для запуска веб SQL запросов.](#run-web-sql-queries)  

## <a name="run-web-sql-queries"></a>Запуск веб SQL запросов  

1.  Выберите базу данных, чтобы открыть консоль для этой базы данных.  
1.  Введите веб-SQL, а затем `Enter` выберите, чтобы запустить его.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Консоль веб SQL для удаления строки из таблицы" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Консоль веб SQL для удаления строки из таблицы  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a>Обновление таблицы веб-SQL  

DevTools не обновляет таблицы в режиме реального времени.  Чтобы обновить данные в таблице, выполните следующие действия.  

1.  [Просмотр данных в таблице веб-SQL.](#view-web-sql-data)  
1.  Выберите **обновление** \. ![ Обновление ][ImageRefreshIcon] \).  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a>Фильтрация столбцов в таблице веб-SQL  

1.  [Просмотр данных в таблице веб-SQL.](#view-web-sql-data)  
1.  Используйте **текстовое поле Видимые столбцы,** чтобы указать, какие столбцы нужно показывать.  Предоставление имен столбцов в качестве списка CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Используйте текстовое поле Видимые столбцы, чтобы уменьшить число показанных столбцов" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Используйте **текстовое поле Видимые столбцы,** чтобы уменьшить число показанных столбцов  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a>Удаление всех SQL веб SQL  

1.  Откройте пространство **Clear Storage.**  
1.  Убедитесь, что **SQL** веб-SQL включен.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Веб-SQL почтовый ящик" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       **Веб-SQL** почтовый ящик  
    :::image-end:::  
    
1.  Выберите **четкие данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Кнопка Clear Site Data" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Кнопка **Clear Site Data**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Веб-SQL базы данных | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/websql) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
