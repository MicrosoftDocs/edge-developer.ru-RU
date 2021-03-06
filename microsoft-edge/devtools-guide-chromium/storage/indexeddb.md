---
description: Просмотр и изменение данных IndexedDB с помощью панели приложений и фрагментов.
title: Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6062cb6b574b2295441bc98616f600cbf00cee8e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398982"
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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a>Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [данных IndexedDB.][MDNIndexedDBAPI]  Предполагается, что вы знакомы с DevTools.  Кроме того, предполагается, что вы знакомы с IndexedDB.  Если нет, перейдите к [Using IndexedDB][MDNUsingIndexedDB].  

## <a name="view-indexeddb-data"></a>Просмотр данных IndexedDB  

1.  Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.  Обычно **области Манифеста** открываются по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Области **Манифест**  
    :::image-end:::  
    
1.  **Расширь меню IndexedDB,** чтобы просмотреть доступные базы данных.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Меню IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Меню **IndexedDB**  
    :::image-end:::  
    
    *   \. Значок базы данных \) представляет базу данных, где находится имя базы данных и происхождение, которое ![ имеет доступ к базе ][ImageDatabaseIcon] `notes - https://mdn.github.io` `notes` `https://mdn.github.io` данных.  
    *   \. ![ Значок Object Store ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.  
    *   **название** и **тело** [индексы][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Известные ограничения**  Сторонние базы данных не видны.  Например, если вы используете для встраивки на своей странице ad, а в вашей сети используется IndexedDB, данные IndexedDB для вашей сети не `<iframe>` видны.  Перейдите [к проблеме #943770][ChromiumIssue943770].  
    
1.  Выберите базу данных, чтобы просмотреть происхождение и номер версии.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="База данных примечаний" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       База **данных примечаний**  
    :::image-end:::  
    
1.  Выберите хранилище объектов, чтобы просмотреть пары значений ключей.  
    
    > [!NOTE]
    > Данные IndexedDB не обновляются в режиме реального времени.  Перейдите [к данным Об обновлении IndexedDB.](#refresh-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Хранилище объектов notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Хранилище **объектов notes**  
    :::image-end:::  
    
    *   **Общее число записей** — это общее число пар с ключевым значением в хранилище объектов.  
    *   **Значение генератора ключей** — это следующий доступный ключ.  Поле отображается только при использовании [генераторов ключей.][MDNBasicConceptsKeyGenerator]  
    
1.  Чтобы расширить значение, выберите ячейку в столбце **Значение.**  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Просмотр значения IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Просмотр значения **IndexedDB**  
    :::image-end:::  
    
1.  Выберите индекс, например **название** или тело на следующем рисунке, чтобы сортировать хранилище объектов в соответствии со значениями этого индекса. ****  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Сортировка объекта хранения по индексу" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Сортировка объекта хранения по индексу  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a>Обновление данных IndexedDB  

Значения IndexedDB в **средстве приложения** не обновляются в режиме реального времени.  Выберите **Обновление** \. Обновление \) при просмотре объекта хранения для обновления данных или просмотра базы данных и обновления базы данных ![ для обновления всех ][ImageRefreshIcon] данных. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Просмотр базы данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Просмотр базы данных  
:::image-end:::  

## <a name="edit-indexeddb-data"></a>Изменение данных IndexedDB  

Клавиши и значения IndexedDB не редактироваться из **средства Приложения.**  Так как у DevTools есть доступ к контексту страниц, вы можете запустить код JavaScript в DevTools для редактирования данных IndexedDB.  

### <a name="edit-indexeddb-data-with-snippets"></a>Изменение данных IndexedDB с помощью фрагментов  

[Фрагменты —][DevtoolsJavascriptSnippets] это способ хранения и запуска блоков кода JavaScript в DevTools.  При запуске фрагмента результат регистрируется в **консоли.**  Для редактирования базы данных IndexedDB можно использовать фрагмент кода JavaScript.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Использование фрагмента для взаимодействия с IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Использование фрагмента для взаимодействия с IndexedDB  
:::image-end:::  

## <a name="delete-indexeddb-data"></a>Удаление данных IndexedDB  

### <a name="delete-an-indexeddb-key-value-pair"></a>Удаление пары ключ-значение IndexedDB  

1.  [Просмотр магазина объектов IndexedDB](#view-indexeddb-data).  
1.  Выберите пару с значением ключа, которую необходимо удалить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Выберите пару с значением ключа, чтобы удалить ее" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Выберите пару с значением ключа, чтобы удалить ее  
    :::image-end:::  
    
1.  Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Как хранится объект после удаления пары значения ключа" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Как хранится объект после удаления пары значения ключа  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a>Удаление всех пар значений ключа в хранилище объектов  

1.  [Просмотр магазина объектов IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Просмотр объекта" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Просмотр объекта  
    :::image-end:::  
    
1.  Выберите **Хранилище объектов Clear** \. Хранилище ![ четких объектов ][ImageClearIcon] \).  
    
### <a name="delete-an-indexeddb-database"></a>Удаление базы данных IndexedDB  

1.  [Просмотр базы данных IndexedDB,](#view-indexeddb-data) которую необходимо удалить.  
1.  Выберите **удаление базы данных**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Кнопка Удалить базу данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Кнопка **Удалить базу** данных  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a>Удаление всего хранилища IndexedDB  

1.  Откройте области **хранения Clear.**  
1.  Убедитесь, что **включен почтовый ящик IndexedDB.**  
1.  Выберите **четкие данные сайта**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Пространство clear storage" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Пространство **clear storage**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Запустите фрагменты JavaScript на любой странице с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: Показать базы данных индексации iframeDB - хром - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Генератор ключей — основные | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Индексация API | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование indexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Использование индекса — использование индекса | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
