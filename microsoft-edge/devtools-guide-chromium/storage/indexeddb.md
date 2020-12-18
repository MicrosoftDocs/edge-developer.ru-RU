---
description: Просмотр и изменение данных IndexedDB с помощью панели приложений и фрагментов кода.
title: Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231204"
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

# Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [данных IndexedDB.][MDNIndexedDBAPI]  Предполагается, что вы знакомы с DevTools.  Также предполагается, что вы знакомы с IndexedDB.  Если нет, перейдите к [сайту Using IndexedDB.][MDNUsingIndexedDB]  

## Просмотр данных IndexedDB  

1.  Откройте средство **"Приложение"** на вкладке **"Приложение".**  Обычно **по** умолчанию открывается окно манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest-empty.msft.png":::
       The **Manifest** pane  
    :::image-end:::  
    
1.  **Разорите меню IndexedDB,** чтобы просмотреть доступные базы данных.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Меню IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       Меню **IndexedDB**  
    :::image-end:::  
    
    *   \( Значок базы данных \) представляет базу данных, где это имя базы данных и источник, который имеет доступ к ![ ][ImageDatabaseIcon] базе `notes - https://mdn.github.io` `notes` `https://mdn.github.io` данных.  
    *   \( ![ Значок магазина объектов ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.  
    *   **заголовок** **и тело** являются [индексами.][MDNUsingIndexedDBUsingIndex]  
    
    > [!NOTE]
    > **Известное ограничение**  Сторонние базы данных не видны.  Например, если вы используете an для встраив в свою страницу, а ваша сеть использует IndexedDB, данные IndexedDB для вашей сети не будут `<iframe>` видны.  Перейдите к [проблеме #943770][ChromiumIssue943770].  
    
1.  Выберите базу данных, чтобы просмотреть источник и номер версии.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="База данных заметок" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       База **данных заметок**  
    :::image-end:::  
    
1.  Выберите хранилище объектов, чтобы просмотреть пары "ключ-значение".  
    
    > [!NOTE]
    > Данные IndexedDB не обновляются в режиме реального времени.  Перейдите [к данным Refresh IndexedDB.](#refresh-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Хранилище объектов notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       Хранилище **объектов notes**  
    :::image-end:::  
    
    *   **Общее количество записей** — это общее число пар "ключ-значение" в хранилище объектов.  
    *   **Значение генератора ключей** — следующий доступный ключ.  Поле отображается только при использовании [генераторов ключей.][MDNBasicConceptsKeyGenerator]  
    
1.  Выберите ячейку в столбце **"Значение",** чтобы развернуть значение.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Просмотр значения IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Просмотр значения **IndexedDB**  
    :::image-end:::  
    
1.  Выберите индекс, например **заголовок** или тело на следующем рисунке, чтобы отсортировать хранилище объектов в соответствии со значениями этого индекса. ****  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Сортировка хранения объектов по индексу" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Сортировка хранения объектов по индексу  
    :::image-end:::  
    
## Обновление данных IndexedDB  

Значения IndexedDB в **средстве "Приложение"** не обновляются в режиме реального времени.  При **просмотре** объекта для обновления данных выберите "Обновить" или "Обновить" или "Обновить базу данных", чтобы ![ обновить все ][ImageReloadIcon] данные. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Просмотр базы данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Просмотр базы данных  
:::image-end:::  

## Изменение данных IndexedDB  

Ключи и значения IndexedDB нельзя редактировать в **средстве приложения.**  Так как DevTools имеет доступ к контексту страницы, вы можете запустить код JavaScript в DevTools для редактирования данных IndexedDB.  

### Изменение данных IndexedDB с помощью фрагментов кода  

[Фрагменты кода —][DevtoolsJavascriptSnippets] это способ хранения и запуска блоков кода JavaScript в DevTools.  При запуске фрагмента в консоли регистрируется **результат.**  Фрагмент кода можно использовать для запуска кода JavaScript для изменения базы данных IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Использование фрагмента кода для взаимодействия с IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Использование фрагмента кода для взаимодействия с IndexedDB  
:::image-end:::  

## Удаление данных IndexedDB  

### Удаление пары "ключ-значение" IndexedDB  

1.  [Просмотреть хранилище объектов IndexedDB.](#view-indexeddb-data)  
1.  Выберите пару "ключ-значение", которую нужно удалить.  DevTools выделяет его, чтобы указать, что он выбран.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Выберите пару "ключ-значение", чтобы удалить ее" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Выберите пару "ключ-значение", чтобы удалить ее  
    :::image-end:::  
    
1.  Нажмите `Delete` клавишу или выберите **delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Как выглядит хранилище объектов после удаления пары "ключ-значение"" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Как выглядит хранилище объектов после удаления пары "ключ-значение"  
    :::image-end:::  
    
### Удаление всех пар "ключ-значение" в хранилище объектов  

1.  [Просмотреть хранилище объектов IndexedDB.](#view-indexeddb-data)  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Просмотр объекта" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Просмотр объекта  
    :::image-end:::  
    
1.  Choose **Clear object store** \( Clear object store ![ ][ImageClearIcon] \).  
    
### Удаление базы данных IndexedDB  

1.  [Просмотр базы данных IndexedDB,](#view-indexeddb-data) которую необходимо удалить.  
1.  Choose **Delete database**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Кнопка "Удалить базу данных"" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       Кнопка **"Удалить базу данных"**  
    :::image-end:::  
    
### Удаление всего хранилища IndexedDB  

1.  Откройте **открытую области** хранения.  
1.  Убедитесь, что включен **контрольный ящик IndexedDB.**  
1.  Выберите **"Очистить данные сайта".**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Очистка области хранения" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       Очистка **области** хранения  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Запуск фрагментов Кода JavaScript на любой странице с Помощью Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 — DevTools: показывать базы данных iframe IndexedDB — chromium - Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Генератор ключей — основные понятия | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Использование индекса — использование IndexedDB | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
