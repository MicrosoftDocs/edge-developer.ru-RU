---
description: Использование панели хранилища для проверки веб-хранилища, IndexedDB, файлов cookie и кэшей запросов и ответов
title: DevTools — хранилище
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, веб-хранилище, локальное хранилище, хранилище сеансов, indexeddb, файлы cookie, рабочий процесс службы, кэш
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 90a2e2fdb0f329c3d83f52beb9eba169bdd48520
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235217"
---
# <span data-ttu-id="11dca-104">Хранилище</span><span class="sxs-lookup"><span data-stu-id="11dca-104">Storage</span></span>

<span data-ttu-id="11dca-105">Панель хранения **используется** для проверки и управления различными локально кэшными данными, в том числе:</span><span class="sxs-lookup"><span data-stu-id="11dca-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="11dca-106">[Пары ключ-значение](#local-and-session-storage-managers) для веб-хранилища *(локальное* хранилище и хранилище сеансов) \*\*</span><span class="sxs-lookup"><span data-stu-id="11dca-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="11dca-107">[Индексные структурированные данные](#indexeddb-manager) баз данных</span><span class="sxs-lookup"><span data-stu-id="11dca-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="11dca-108">[Файлы cookie](#cookies-list) для домена</span><span class="sxs-lookup"><span data-stu-id="11dca-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="11dca-109">[Кэш](#cache-manager) (пары запросов и ответов) для отладки рабочих служб</span><span class="sxs-lookup"><span data-stu-id="11dca-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="11dca-110">Разйдите любую из этих категорий и щелкните ее, чтобы открыть вкладку диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11dca-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="11dca-111">Локальные диспетчеры хранилища и диспетчеры хранилища сеансов</span><span class="sxs-lookup"><span data-stu-id="11dca-111">Local and Session storage managers</span></span>

<span data-ttu-id="11dca-112">Используйте *локальный диспетчер хранилища и* *диспетчер хранилища сеансов* для проверки и управления веб-хранилищем для вашей страницы.</span><span class="sxs-lookup"><span data-stu-id="11dca-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="11dca-113">В **папках "Локальное** хранилище" и [\*\*](./debugger.md#resource-picker) "Хранилище сеансов" в панели выбора ресурсов панели хранения отображается список источника страницы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11dca-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="11dca-114">При выборе одного из этих кадров открывается редактируемая таблица текущих пар ключ-значение, задаваемых с помощью [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) или [](#storage-list) [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)соответственно (и/или задаваемых непосредственно из списка хранилища DevTools).</span><span class="sxs-lookup"><span data-stu-id="11dca-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![Диспетчер локального хранилища DevTools](./media/storage_web_storage.png)

<span data-ttu-id="11dca-116">На *вкладке "Локальное* хранилище" *и "Хранилище* сеансов" можно:</span><span class="sxs-lookup"><span data-stu-id="11dca-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="11dca-117">**Обновите** () список хранения, чтобы увидеть текущий набор пар "ключ-значение" для `Ctrl+F5` данного [](#cookies-list) домена.</span><span class="sxs-lookup"><span data-stu-id="11dca-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="11dca-118">(При обновлении скрипта список не обновляется автоматически.)</span><span class="sxs-lookup"><span data-stu-id="11dca-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="11dca-119">**Имитация достижения предельного хранилища для** веб-хранилища Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="11dca-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="11dca-120">У каждого домена и поддомена есть собственная область хранения, но существует комбинированное ограничение:</span><span class="sxs-lookup"><span data-stu-id="11dca-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="11dca-121">**Поддомены:** до 5 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="11dca-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="11dca-122">**Домены:** до 10 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="11dca-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="11dca-123">**Всего для всех доменов:** до 50 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="11dca-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="11dca-124">Хранилище сеанса очищается, как только закрывается последняя вкладка браузера, ссылаясь на источник.</span><span class="sxs-lookup"><span data-stu-id="11dca-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="11dca-125">Локальные записи хранения сохраняются неопределенное время до тех пор, пока страница не будет очищена программным путем или вручную пользователем:</span><span class="sxs-lookup"><span data-stu-id="11dca-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="11dca-126">**Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайта**</span><span class="sxs-lookup"><span data-stu-id="11dca-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Очистка данных браузера с панели параметров Microsoft Edge](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="11dca-128">Список хранилищ</span><span class="sxs-lookup"><span data-stu-id="11dca-128">Storage list</span></span>

<span data-ttu-id="11dca-129">Из *таблицы списка хранилища* вы можете:</span><span class="sxs-lookup"><span data-stu-id="11dca-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="11dca-130">**Проверьте и отсортировать** пары "ключ-значение", щелкнув имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="11dca-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="11dca-131">**Изменить** ключ *и* *значение существующей* записи, щелкнув ячейку.</span><span class="sxs-lookup"><span data-stu-id="11dca-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="11dca-132">**Delete** ( `Del` ) an entry from the right-click context menu option, Delete *item*.</span><span class="sxs-lookup"><span data-stu-id="11dca-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="11dca-133">**Добавьте** новую пару ключ-значение, щелкнув пустую строку в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="11dca-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="11dca-134">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="11dca-134">Shortcuts</span></span>

| <span data-ttu-id="11dca-135">Действие</span><span class="sxs-lookup"><span data-stu-id="11dca-135">Action</span></span>              | <span data-ttu-id="11dca-136">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="11dca-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="11dca-137">Обновить</span><span class="sxs-lookup"><span data-stu-id="11dca-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="11dca-138">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="11dca-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="11dca-139">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="11dca-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="11dca-140">Выделить все</span><span class="sxs-lookup"><span data-stu-id="11dca-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="11dca-141">Диспетчер IndexedDB</span><span class="sxs-lookup"><span data-stu-id="11dca-141">IndexedDB manager</span></span>

<span data-ttu-id="11dca-142">Вкладка **IndexedDB** используется для проверки структурированных данных, которые хранятся локально на клиентских компьютерах, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="11dca-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="11dca-143">В частности, можно проверить, отсортировать и обновить хранилища объектов и индексы, а также удалить отдельные записи значения ключа.</span><span class="sxs-lookup"><span data-stu-id="11dca-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="11dca-144">Вы можете использовать нашу [демонстрацию Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) для тестирования диспетчера *IndexedDB* в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="11dca-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="11dca-145">Чтобы удалить все данные IndexedDB, хранимые для текущего пользователя в Microsoft Edge, используйте меню *параметров* Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="11dca-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="11dca-146">**...** >  **Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайта**</span><span class="sxs-lookup"><span data-stu-id="11dca-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="11dca-147">В **папке IndexedDB** в средстве [\*\*](./debugger.md#resource-picker) "Выбор ресурсов" отладщика отображается список источников ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="11dca-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="11dca-148">Все базы данных IndexedDB (IDB) будут указаны в источниках вместе с их хранилищами объектов.</span><span class="sxs-lookup"><span data-stu-id="11dca-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![Диспетчер IndexedDB DevTools](./media/storage_indexeddb.png)

### <span data-ttu-id="11dca-150">Панель инструментов IndexedDB</span><span class="sxs-lookup"><span data-stu-id="11dca-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="11dca-151">На панели *инструментов IndexedDB* можно:</span><span class="sxs-lookup"><span data-stu-id="11dca-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="11dca-152">**Обновить** ( `Ctrl+F5` ), чтобы увидеть текущие записи в хранилище объектов или индексе базы данных.</span><span class="sxs-lookup"><span data-stu-id="11dca-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="11dca-153">Диспетчер IndexedDB не обновляется автоматически при внесении изменений в базу данных.</span><span class="sxs-lookup"><span data-stu-id="11dca-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="11dca-154">Список записей в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="11dca-154">Object store entries list</span></span>

<span data-ttu-id="11dca-155">Из *таблицы "Хранилище объектов"* или *"Индекс"* можно:</span><span class="sxs-lookup"><span data-stu-id="11dca-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="11dca-156">**Проверьте и отсортировать** пары "ключ-значение", щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="11dca-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="11dca-157">**Refresh** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="11dca-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="11dca-158">**Удаление элемента** ( `Del` ) для удаления выбранной записи в хранилище объектов или индексе.</span><span class="sxs-lookup"><span data-stu-id="11dca-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="11dca-159">Это также можно сделать в [](#context-menu) контекстное меню правой кнопкой мыши *"Удалить элемент".*</span><span class="sxs-lookup"><span data-stu-id="11dca-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="11dca-160">**Скопируйте выбранные элементы** ( ), чтобы скопировать `Ctrl+C` выбранный элемент в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="11dca-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="11dca-161">Это также можно сделать в [](#context-menu) контекстное меню правой кнопкой мыши, *скопируйте выбранный элемент.*</span><span class="sxs-lookup"><span data-stu-id="11dca-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="11dca-162">**Выберите все** `Ctrl+A` () для выбора всех записей в хранилище объектов или индексе.</span><span class="sxs-lookup"><span data-stu-id="11dca-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="11dca-163">Это также можно сделать в [](#context-menu) контекстное меню правой кнопкой мыши, *выберите все.*</span><span class="sxs-lookup"><span data-stu-id="11dca-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="11dca-164">Столбцы в хранилище *объектов или* таблице *индекса* можно сортировать:</span><span class="sxs-lookup"><span data-stu-id="11dca-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="11dca-165">Столбец</span><span class="sxs-lookup"><span data-stu-id="11dca-165">Column</span></span> | <span data-ttu-id="11dca-166">Описание</span><span class="sxs-lookup"><span data-stu-id="11dca-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="11dca-167">Раздел</span><span class="sxs-lookup"><span data-stu-id="11dca-167">Key</span></span> | <span data-ttu-id="11dca-168">Имя пары "ключ-значение" (то же, что *и первичный*ключ) при итерации над хранилищем объектов; Имя ключа индекса (текущий ключ курсора) при итерации по индексу</span><span class="sxs-lookup"><span data-stu-id="11dca-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="11dca-169">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="11dca-169">Primary Key</span></span> | <span data-ttu-id="11dca-170">Имя пары "ключ-значение" (подробнее о ключах [IDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)см. в веб-документы *MDN)*</span><span class="sxs-lookup"><span data-stu-id="11dca-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="11dca-171">Значение</span><span class="sxs-lookup"><span data-stu-id="11dca-171">Value</span></span> | <span data-ttu-id="11dca-172">Значение пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="11dca-172">Value of the key-value pair</span></span>

<span data-ttu-id="11dca-173">Ознакомьтесь *с веб-документы MDN,* чтобы узнать больше о понятиях [и использовании IndexedDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)</span><span class="sxs-lookup"><span data-stu-id="11dca-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="11dca-174">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="11dca-174">Context menu</span></span>

<span data-ttu-id="11dca-175">Помимо панели инструментов [ *IndexedDB,* ](#indexeddb-toolbar)вы также можете управлять своими данными в хранилищах объектов или индексах с помощью контекстного меню правой кнопки мыши и/или сочетания [клавиш.](#shortcuts) \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11dca-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="11dca-176">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="11dca-176">Shortcuts</span></span>

<span data-ttu-id="11dca-177">Действие</span><span class="sxs-lookup"><span data-stu-id="11dca-177">Action</span></span> | <span data-ttu-id="11dca-178">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="11dca-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="11dca-179">Обновить</span><span class="sxs-lookup"><span data-stu-id="11dca-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="11dca-180">Удаление пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="11dca-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="11dca-181">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="11dca-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="11dca-182">Выделить все</span><span class="sxs-lookup"><span data-stu-id="11dca-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="11dca-183">Диспетчер файлов cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-183">Cookies manager</span></span>

<span data-ttu-id="11dca-184">Используйте диспетчер *файлов cookie для* проверки файлов cookie для данного домена и управления ими.</span><span class="sxs-lookup"><span data-stu-id="11dca-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="11dca-185">В **папке cookie** в средстве [\*\*](./debugger.md#resource-picker) "Выбор ресурсов" отладщика отображается список источников ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="11dca-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="11dca-186">При выборе одного из этих кадров открывается таблица, представляющая текущие файлы cookie, установленные либо с помощью HTTP-загона, либо с помощью скрипта [Document.cookie.](https://developer.mozilla.org/docs/Web/API/Document/cookie) [](https://developer.mozilla.org/docs/Web/HTTP/Cookies)</span><span class="sxs-lookup"><span data-stu-id="11dca-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![Диспетчер файлов cookie DevTools](./media/storage_cookies.png)

<span data-ttu-id="11dca-188">На панели *инструментов вкладки "Файлы* cookie" можно:</span><span class="sxs-lookup"><span data-stu-id="11dca-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="11dca-189">**Обновите** () список файлов cookie, чтобы увидеть текущий набор `Ctrl+F5` файлов cookie для данного домена. [](#cookies-list)</span><span class="sxs-lookup"><span data-stu-id="11dca-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="11dca-190">(Список не обновляется автоматически.)</span><span class="sxs-lookup"><span data-stu-id="11dca-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="11dca-191">**Удалите все файлы cookie** ( `Ctrl+Shift+Del` ) (сеанс и постоянный) для пути к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="11dca-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="11dca-192">**Удалите все файлы cookie сеанса** `Ctrl+Del` () для пути к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="11dca-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="11dca-193">Чтобы полностью очистить список *файлов cookie,* может потребоваться очистить все файлы **cookie** для домена с панели инструментов [**панели**](./network.md#toolbar) "Сеть".</span><span class="sxs-lookup"><span data-stu-id="11dca-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="11dca-194">Список файлов cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-194">Cookies list</span></span>

<span data-ttu-id="11dca-195">Из *таблицы списка cookie можно:*</span><span class="sxs-lookup"><span data-stu-id="11dca-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="11dca-196">**Проверьте и отсортировать** файлы cookie, щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="11dca-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="11dca-197">**Изменить** имя *и* *значение существующего* файла cookie, щелкнув ячейку.</span><span class="sxs-lookup"><span data-stu-id="11dca-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="11dca-198">**Delete** ( `Del` ) a cookie from the right-click context [menu](#context-menu) option, *Delete cookie*.</span><span class="sxs-lookup"><span data-stu-id="11dca-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="11dca-199">**Добавьте** новый файл cookie сеанса для данного *домена или* пути, щелкнув пустую строку в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="11dca-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="11dca-200">Это работает только для файлов cookie сеанса; постоянные файлы cookie (с определенными датами истечения срока действия) должны устанавливаться с помощью традиционных методов.</span><span class="sxs-lookup"><span data-stu-id="11dca-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="11dca-201">Значения *Domain* и *Path* заполняются автоматически в соответствии с расположением страницы.</span><span class="sxs-lookup"><span data-stu-id="11dca-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="11dca-202">Столбцы списка *cookie можно сортировать:*</span><span class="sxs-lookup"><span data-stu-id="11dca-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="11dca-203">Столбец</span><span class="sxs-lookup"><span data-stu-id="11dca-203">Column</span></span> | <span data-ttu-id="11dca-204">Описание</span><span class="sxs-lookup"><span data-stu-id="11dca-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="11dca-205">Name</span><span class="sxs-lookup"><span data-stu-id="11dca-205">Name</span></span> | <span data-ttu-id="11dca-206">Имя файла cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-206">Name of the cookie</span></span>
<span data-ttu-id="11dca-207">Значение</span><span class="sxs-lookup"><span data-stu-id="11dca-207">Value</span></span> | <span data-ttu-id="11dca-208">Значение файла cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-208">Value of the cookie</span></span>
<span data-ttu-id="11dca-209">Домен</span><span class="sxs-lookup"><span data-stu-id="11dca-209">Domain</span></span> | <span data-ttu-id="11dca-210">Имя хоста файла cookie (может быть пустым)</span><span class="sxs-lookup"><span data-stu-id="11dca-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="11dca-211">Путь</span><span class="sxs-lookup"><span data-stu-id="11dca-211">Path</span></span> | <span data-ttu-id="11dca-212">URL-путь для файла cookie (может быть пустым)</span><span class="sxs-lookup"><span data-stu-id="11dca-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="11dca-213">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="11dca-213">Expires</span></span> | <span data-ttu-id="11dca-214">Максимальное время существования файла cookie в качестве даты и времени HTTP.</span><span class="sxs-lookup"><span data-stu-id="11dca-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="11dca-215">Если нет `Expires` или `Max-Age` не было установлено, запись считается файлом cookie *сеанса.*</span><span class="sxs-lookup"><span data-stu-id="11dca-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="11dca-216">Только HTTP</span><span class="sxs-lookup"><span data-stu-id="11dca-216">HTTP only</span></span> | <span data-ttu-id="11dca-217">Указывает, установлен ли файл cookie с директивой, указывая, что он `HttpOnly` недоступен из JavaScript</span><span class="sxs-lookup"><span data-stu-id="11dca-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="11dca-218">Защита</span><span class="sxs-lookup"><span data-stu-id="11dca-218">Secure</span></span> | <span data-ttu-id="11dca-219">Указывает, был ли файл cookie установлен с помощью директивы, указывая, что он будет отправлен на сервер только из запроса с использованием `Secure` протокола SSL и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="11dca-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="11dca-220">Дополнительные сведения о свойствах файлов cookie см. в справочнике [по set-cookie веб-документы](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) **MDN.**</span><span class="sxs-lookup"><span data-stu-id="11dca-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="11dca-221">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="11dca-221">Context menu</span></span>

<span data-ttu-id="11dca-222">Помимо панели инструментов вкладок *"Файлы* cookie", [](#cookies-manager)вы также можете \*\*\*\* управлять своими файлами cookie из контекстного меню правой кнопкой мыши и/или с помощью сочетания [клавиш.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="11dca-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="11dca-223">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="11dca-223">Shortcuts</span></span>

| <span data-ttu-id="11dca-224">Действие</span><span class="sxs-lookup"><span data-stu-id="11dca-224">Action</span></span>                     | <span data-ttu-id="11dca-225">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="11dca-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="11dca-226">Обновить</span><span class="sxs-lookup"><span data-stu-id="11dca-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="11dca-227">Удаление файла cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="11dca-228">Удаление всех файлов cookie</span><span class="sxs-lookup"><span data-stu-id="11dca-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="11dca-229">Удаление всех файлов cookie сеанса</span><span class="sxs-lookup"><span data-stu-id="11dca-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="11dca-230">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="11dca-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="11dca-231">Выделить все</span><span class="sxs-lookup"><span data-stu-id="11dca-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="11dca-232">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="11dca-232">Cache manager</span></span>

<span data-ttu-id="11dca-233">Если щелкнуть определенную запись кэша, \*\*\*\* откроется диспетчер кэша рабочих служб, где можно \*\* проверить и при желании удалить записи кэша *(пары* ключ-значение запроса и ответа):</span><span class="sxs-lookup"><span data-stu-id="11dca-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Диспетчер кэша](./media/storage_cache.png)

### <span data-ttu-id="11dca-235">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="11dca-235">Shortcuts</span></span>

#### <span data-ttu-id="11dca-236">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="11dca-236">Cache manager</span></span>

| <span data-ttu-id="11dca-237">Действие</span><span class="sxs-lookup"><span data-stu-id="11dca-237">Action</span></span>              | <span data-ttu-id="11dca-238">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="11dca-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="11dca-239">Обновить</span><span class="sxs-lookup"><span data-stu-id="11dca-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="11dca-240">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="11dca-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="11dca-241">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="11dca-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="11dca-242">Выделить все</span><span class="sxs-lookup"><span data-stu-id="11dca-242">Select all</span></span>          | `Ctrl` + `A`  |
