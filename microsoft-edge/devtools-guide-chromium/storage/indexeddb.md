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

# <span data-ttu-id="ba8e9-104">Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ba8e9-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ba8e9-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [данных IndexedDB.][MDNIndexedDBAPI]</span><span class="sxs-lookup"><span data-stu-id="ba8e9-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="ba8e9-106">Предполагается, что вы знакомы с DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="ba8e9-107">Также предполагается, что вы знакомы с IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="ba8e9-108">Если нет, перейдите к [сайту Using IndexedDB.][MDNUsingIndexedDB]</span><span class="sxs-lookup"><span data-stu-id="ba8e9-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="ba8e9-109">Просмотр данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="ba8e9-110">Откройте средство **"Приложение"** на вкладке **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="ba8e9-111">Обычно **по** умолчанию открывается окно манифеста.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="ba8e9-113">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="ba8e9-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba8e9-114">**Разорите меню IndexedDB,** чтобы просмотреть доступные базы данных.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Меню IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="ba8e9-116">Меню **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="ba8e9-117">\( Значок базы данных \) представляет базу данных, где это имя базы данных и источник, который имеет доступ к ![ ][ImageDatabaseIcon] базе `notes - https://mdn.github.io` `notes` `https://mdn.github.io` данных.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="ba8e9-118">\( ![ Значок магазина объектов ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="ba8e9-119">**заголовок** **и тело** являются [индексами.][MDNUsingIndexedDBUsingIndex]</span><span class="sxs-lookup"><span data-stu-id="ba8e9-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ba8e9-120">**Известное ограничение**  Сторонние базы данных не видны.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="ba8e9-121">Например, если вы используете an для встраив в свою страницу, а ваша сеть использует IndexedDB, данные IndexedDB для вашей сети не будут `<iframe>` видны.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="ba8e9-122">Перейдите к [проблеме #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="ba8e9-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="ba8e9-123">Выберите базу данных, чтобы просмотреть источник и номер версии.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="База данных заметок" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="ba8e9-125">База **данных заметок**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba8e9-126">Выберите хранилище объектов, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ba8e9-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ba8e9-127">Данные IndexedDB не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="ba8e9-128">Перейдите [к данным Refresh IndexedDB.](#refresh-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="ba8e9-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Хранилище объектов notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="ba8e9-130">Хранилище **объектов notes**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="ba8e9-131">**Общее количество записей** — это общее число пар "ключ-значение" в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="ba8e9-132">**Значение генератора ключей** — следующий доступный ключ.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="ba8e9-133">Поле отображается только при использовании [генераторов ключей.][MDNBasicConceptsKeyGenerator]</span><span class="sxs-lookup"><span data-stu-id="ba8e9-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="ba8e9-134">Выберите ячейку в столбце **"Значение",** чтобы развернуть значение.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Просмотр значения IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="ba8e9-136">Просмотр значения **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba8e9-137">Выберите индекс, например **заголовок** или тело на следующем рисунке, чтобы отсортировать хранилище объектов в соответствии со значениями этого индекса. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ba8e9-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Сортировка хранения объектов по индексу" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="ba8e9-139">Сортировка хранения объектов по индексу</span><span class="sxs-lookup"><span data-stu-id="ba8e9-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ba8e9-140">Обновление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="ba8e9-141">Значения IndexedDB в **средстве "Приложение"** не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="ba8e9-142">При **просмотре** объекта для обновления данных выберите "Обновить" или "Обновить" или "Обновить базу данных", чтобы ![ обновить все ][ImageReloadIcon] данные. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ba8e9-142">Choose **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Просмотр базы данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="ba8e9-144">Просмотр базы данных</span><span class="sxs-lookup"><span data-stu-id="ba8e9-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="ba8e9-145">Изменение данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="ba8e9-146">Ключи и значения IndexedDB нельзя редактировать в **средстве приложения.**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="ba8e9-147">Так как DevTools имеет доступ к контексту страницы, вы можете запустить код JavaScript в DevTools для редактирования данных IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="ba8e9-148">Изменение данных IndexedDB с помощью фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="ba8e9-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="ba8e9-149">[Фрагменты кода —][DevtoolsJavascriptSnippets] это способ хранения и запуска блоков кода JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="ba8e9-150">При запуске фрагмента в консоли регистрируется **результат.**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="ba8e9-151">Фрагмент кода можно использовать для запуска кода JavaScript для изменения базы данных IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Использование фрагмента кода для взаимодействия с IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="ba8e9-153">Использование фрагмента кода для взаимодействия с IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="ba8e9-154">Удаление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-154">Delete IndexedDB data</span></span>  

### <span data-ttu-id="ba8e9-155">Удаление пары "ключ-значение" IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="ba8e9-156">[Просмотреть хранилище объектов IndexedDB.](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="ba8e9-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="ba8e9-157">Выберите пару "ключ-значение", которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="ba8e9-158">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Выберите пару "ключ-значение", чтобы удалить ее" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="ba8e9-160">Выберите пару "ключ-значение", чтобы удалить ее</span><span class="sxs-lookup"><span data-stu-id="ba8e9-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba8e9-161">Нажмите `Delete` клавишу или выберите **delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ba8e9-161">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Как выглядит хранилище объектов после удаления пары "ключ-значение"" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="ba8e9-163">Как выглядит хранилище объектов после удаления пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="ba8e9-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ba8e9-164">Удаление всех пар "ключ-значение" в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="ba8e9-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="ba8e9-165">[Просмотреть хранилище объектов IndexedDB.](#view-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="ba8e9-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Просмотр объекта" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="ba8e9-167">Просмотр объекта</span><span class="sxs-lookup"><span data-stu-id="ba8e9-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ba8e9-168">Choose **Clear object store** \( Clear object store ![ ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ba8e9-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="ba8e9-169">Удаление базы данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="ba8e9-170">[Просмотр базы данных IndexedDB,](#view-indexeddb-data) которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="ba8e9-171">Choose **Delete database**.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Кнопка "Удалить базу данных"" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="ba8e9-173">Кнопка **"Удалить базу данных"**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ba8e9-174">Удаление всего хранилища IndexedDB</span><span class="sxs-lookup"><span data-stu-id="ba8e9-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="ba8e9-175">Откройте **открытую области** хранения.</span><span class="sxs-lookup"><span data-stu-id="ba8e9-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="ba8e9-176">Убедитесь, что включен **контрольный ящик IndexedDB.**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="ba8e9-177">Выберите **"Очистить данные сайта".**</span><span class="sxs-lookup"><span data-stu-id="ba8e9-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Очистка области хранения" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="ba8e9-179">Очистка **области** хранения</span><span class="sxs-lookup"><span data-stu-id="ba8e9-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ba8e9-180">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba8e9-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="ba8e9-188">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba8e9-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba8e9-189">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ba8e9-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba8e9-191">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba8e9-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
