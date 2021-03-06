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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a><span data-ttu-id="f3777-104">Просмотр и изменение данных IndexedDB с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f3777-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f3777-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [данных IndexedDB.][MDNIndexedDBAPI]</span><span class="sxs-lookup"><span data-stu-id="f3777-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="f3777-106">Предполагается, что вы знакомы с DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3777-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="f3777-107">Кроме того, предполагается, что вы знакомы с IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="f3777-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="f3777-108">Если нет, перейдите к [Using IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="f3777-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <a name="view-indexeddb-data"></a><span data-ttu-id="f3777-109">Просмотр данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="f3777-110">Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.</span><span class="sxs-lookup"><span data-stu-id="f3777-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="f3777-111">Обычно **области Манифеста** открываются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3777-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="f3777-113">Области **Манифест**</span><span class="sxs-lookup"><span data-stu-id="f3777-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f3777-114">**Расширь меню IndexedDB,** чтобы просмотреть доступные базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3777-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Меню IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="f3777-116">Меню **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="f3777-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="f3777-117">\. Значок базы данных \) представляет базу данных, где находится имя базы данных и происхождение, которое ![ имеет доступ к базе ][ImageDatabaseIcon] `notes - https://mdn.github.io` `notes` `https://mdn.github.io` данных.</span><span class="sxs-lookup"><span data-stu-id="f3777-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="f3777-118">\. ![ Значок Object Store ][ImageObjectStoreIcon] \) `notes` — это хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f3777-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="f3777-119">**название** и **тело** [индексы][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="f3777-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f3777-120">**Известные ограничения**  Сторонние базы данных не видны.</span><span class="sxs-lookup"><span data-stu-id="f3777-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="f3777-121">Например, если вы используете для встраивки на своей странице ad, а в вашей сети используется IndexedDB, данные IndexedDB для вашей сети не `<iframe>` видны.</span><span class="sxs-lookup"><span data-stu-id="f3777-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="f3777-122">Перейдите [к проблеме #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="f3777-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="f3777-123">Выберите базу данных, чтобы просмотреть происхождение и номер версии.</span><span class="sxs-lookup"><span data-stu-id="f3777-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="База данных примечаний" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="f3777-125">База **данных примечаний**</span><span class="sxs-lookup"><span data-stu-id="f3777-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f3777-126">Выберите хранилище объектов, чтобы просмотреть пары значений ключей.</span><span class="sxs-lookup"><span data-stu-id="f3777-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f3777-127">Данные IndexedDB не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f3777-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="f3777-128">Перейдите [к данным Об обновлении IndexedDB.](#refresh-indexeddb-data)</span><span class="sxs-lookup"><span data-stu-id="f3777-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Хранилище объектов notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="f3777-130">Хранилище **объектов notes**</span><span class="sxs-lookup"><span data-stu-id="f3777-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="f3777-131">**Общее число записей** — это общее число пар с ключевым значением в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f3777-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="f3777-132">**Значение генератора ключей** — это следующий доступный ключ.</span><span class="sxs-lookup"><span data-stu-id="f3777-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="f3777-133">Поле отображается только при использовании [генераторов ключей.][MDNBasicConceptsKeyGenerator]</span><span class="sxs-lookup"><span data-stu-id="f3777-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="f3777-134">Чтобы расширить значение, выберите ячейку в столбце **Значение.**</span><span class="sxs-lookup"><span data-stu-id="f3777-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Просмотр значения IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="f3777-136">Просмотр значения **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="f3777-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f3777-137">Выберите индекс, например **название** или тело на следующем рисунке, чтобы сортировать хранилище объектов в соответствии со значениями этого индекса. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f3777-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Сортировка объекта хранения по индексу" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="f3777-139">Сортировка объекта хранения по индексу</span><span class="sxs-lookup"><span data-stu-id="f3777-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a><span data-ttu-id="f3777-140">Обновление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="f3777-141">Значения IndexedDB в **средстве приложения** не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f3777-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="f3777-142">Выберите **Обновление** \. Обновление \) при просмотре объекта хранения для обновления данных или просмотра базы данных и обновления базы данных ![ для обновления всех ][ImageRefreshIcon] данных. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f3777-142">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Просмотр базы данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="f3777-144">Просмотр базы данных</span><span class="sxs-lookup"><span data-stu-id="f3777-144">View a database</span></span>  
:::image-end:::  

## <a name="edit-indexeddb-data"></a><span data-ttu-id="f3777-145">Изменение данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="f3777-146">Клавиши и значения IndexedDB не редактироваться из **средства Приложения.**</span><span class="sxs-lookup"><span data-stu-id="f3777-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="f3777-147">Так как у DevTools есть доступ к контексту страниц, вы можете запустить код JavaScript в DevTools для редактирования данных IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="f3777-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <a name="edit-indexeddb-data-with-snippets"></a><span data-ttu-id="f3777-148">Изменение данных IndexedDB с помощью фрагментов</span><span class="sxs-lookup"><span data-stu-id="f3777-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="f3777-149">[Фрагменты —][DevtoolsJavascriptSnippets] это способ хранения и запуска блоков кода JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f3777-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="f3777-150">При запуске фрагмента результат регистрируется в **консоли.**</span><span class="sxs-lookup"><span data-stu-id="f3777-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="f3777-151">Для редактирования базы данных IndexedDB можно использовать фрагмент кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3777-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Использование фрагмента для взаимодействия с IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="f3777-153">Использование фрагмента для взаимодействия с IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <a name="delete-indexeddb-data"></a><span data-ttu-id="f3777-154">Удаление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-154">Delete IndexedDB data</span></span>  

### <a name="delete-an-indexeddb-key-value-pair"></a><span data-ttu-id="f3777-155">Удаление пары ключ-значение IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="f3777-156">[Просмотр магазина объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f3777-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="f3777-157">Выберите пару с значением ключа, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f3777-157">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="f3777-158">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="f3777-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Выберите пару с значением ключа, чтобы удалить ее" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="f3777-160">Выберите пару с значением ключа, чтобы удалить ее</span><span class="sxs-lookup"><span data-stu-id="f3777-160">Choose a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f3777-161">Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f3777-161">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Как хранится объект после удаления пары значения ключа" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="f3777-163">Как хранится объект после удаления пары значения ключа</span><span class="sxs-lookup"><span data-stu-id="f3777-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a><span data-ttu-id="f3777-164">Удаление всех пар значений ключа в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="f3777-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="f3777-165">[Просмотр магазина объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f3777-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Просмотр объекта" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="f3777-167">Просмотр объекта</span><span class="sxs-lookup"><span data-stu-id="f3777-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f3777-168">Выберите **Хранилище объектов Clear** \. Хранилище ![ четких объектов ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f3777-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <a name="delete-an-indexeddb-database"></a><span data-ttu-id="f3777-169">Удаление базы данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="f3777-170">[Просмотр базы данных IndexedDB,](#view-indexeddb-data) которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="f3777-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="f3777-171">Выберите **удаление базы данных**.</span><span class="sxs-lookup"><span data-stu-id="f3777-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Кнопка Удалить базу данных" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="f3777-173">Кнопка **Удалить базу** данных</span><span class="sxs-lookup"><span data-stu-id="f3777-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a><span data-ttu-id="f3777-174">Удаление всего хранилища IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f3777-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="f3777-175">Откройте области **хранения Clear.**</span><span class="sxs-lookup"><span data-stu-id="f3777-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="f3777-176">Убедитесь, что **включен почтовый ящик IndexedDB.**</span><span class="sxs-lookup"><span data-stu-id="f3777-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="f3777-177">Выберите **четкие данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="f3777-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Пространство clear storage" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="f3777-179">Пространство **clear storage**</span><span class="sxs-lookup"><span data-stu-id="f3777-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f3777-180">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f3777-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="f3777-188">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3777-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f3777-189">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="f3777-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f3777-191">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f3777-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
