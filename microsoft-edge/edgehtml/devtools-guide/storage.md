---
description: Используйте панель хранения для проверки веб-хранилища, IndexedDB, файлов cookie и кэшей запроса и ответа
title: Хранение | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, web storage, local storage, session storage, indexeddb, cookies, service worker, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398898"
---
# <a name="storage"></a><span data-ttu-id="89725-104">Storage</span><span class="sxs-lookup"><span data-stu-id="89725-104">Storage</span></span>

<span data-ttu-id="89725-105">Используйте панель **хранения** для проверки и управления различными локально кэшными данными, в том числе:</span><span class="sxs-lookup"><span data-stu-id="89725-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>  

*   <span data-ttu-id="89725-106">[Пары ключей](#local-and-session-storage-managers) и значений для веб-хранилища \(Локальное и сеансное хранилище\)</span><span class="sxs-lookup"><span data-stu-id="89725-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span></span>  
*   <span data-ttu-id="89725-107">[Индексные структурированные](#indexeddb-manager) данные DB</span><span class="sxs-lookup"><span data-stu-id="89725-107">[Indexed DB](#indexeddb-manager) structured data</span></span>  
*   <span data-ttu-id="89725-108">[Cookies](#cookies-list) для домена</span><span class="sxs-lookup"><span data-stu-id="89725-108">[Cookies](#cookies-list) for the domain</span></span>  
*   <span data-ttu-id="89725-109">[Кэш](#cache-manager) \(пары запросов и ответов\) для отладки сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="89725-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span></span>  

<span data-ttu-id="89725-110">Расширь любую из этих категорий и нажмите на детскую запись, чтобы открыть вкладку диспетчер ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89725-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>  

## <a name="local-and-session-storage-managers"></a><span data-ttu-id="89725-111">Локальные и сеансные диспетчеры хранения</span><span class="sxs-lookup"><span data-stu-id="89725-111">Local and Session storage managers</span></span>  

<span data-ttu-id="89725-112">Для проверки и управления веб-хранилищем для вашей страницы используйте диспетчер локального хранения и диспетчер хранения сеансов.</span><span class="sxs-lookup"><span data-stu-id="89725-112">Use the Local Storage manager and Session Storage manager to inspect and manage the web storage for your page.</span></span>  

<span data-ttu-id="89725-113">Папки **локального** хранения и хранения сеансов [](./debugger.md#resource-picker) в выборке ресурсов панели хранения отображают список истоков страницы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="89725-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [Resource picker](./debugger.md#resource-picker) display a list of origins for the page.</span></span>  <span data-ttu-id="89725-114">Выбор одного из этих кадров открывает редактируемую таблицу текущих пар ключей и значений, задаваемых через [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) или [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage)соответственно \(и/или задаваемые непосредственно из списка хранения DevTools [](#storage-list)\).</span><span class="sxs-lookup"><span data-stu-id="89725-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively \(and/or set directly from the  DevTools [Storage list](#storage-list)\).</span></span>  

![Диспетчер хранилища DevTools](./media/storage_web_storage.png)  

<span data-ttu-id="89725-116">Из вкладок локального хранения и хранения сеансов можно:</span><span class="sxs-lookup"><span data-stu-id="89725-116">From the Local Storage and Session Storage tabs you can:</span></span>  

*   <span data-ttu-id="89725-117">**Обновление** \. Список хранилища, чтобы увидеть текущий набор пар ключей и значений `Ctrl+F5` для данного [](#cookies-list) домена.</span><span class="sxs-lookup"><span data-stu-id="89725-117">**Refresh** \(`Ctrl+F5`\) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span>  <span data-ttu-id="89725-118">\(Список не обновляется автоматически при обновлении скрипта.\)</span><span class="sxs-lookup"><span data-stu-id="89725-118">\(The list does not auto-refresh upon script updates.\)</span></span>  
*   <span data-ttu-id="89725-119">**Имитация достижения предельного срока хранения**  для веб-хранилища Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89725-119">**Simulate reaching the storage limit**  for Microsoft Edge web storage.</span></span>  <span data-ttu-id="89725-120">У каждого домена и поддомена есть собственная область хранения, однако существует совместное ограничение:</span><span class="sxs-lookup"><span data-stu-id="89725-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>  
    *   <span data-ttu-id="89725-121">**Subdomains:** до 5 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="89725-121">**Subdomains**:  up to 5 MBs of space</span></span>  
    *   <span data-ttu-id="89725-122">**Домены:** до 10 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="89725-122">**Domains**:  up to 10 MBs of space</span></span>  
    *   <span data-ttu-id="89725-123">**Итого для всех доменов:** до 50 МБ пространства</span><span class="sxs-lookup"><span data-stu-id="89725-123">**Total for all domains**:  up to 50 MBs of space</span></span>  

   <span data-ttu-id="89725-124">Хранилище сеансов очищается, как только закрывается последняя вкладка браузера, ссылаясь на ее происхождение.</span><span class="sxs-lookup"><span data-stu-id="89725-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span>  <span data-ttu-id="89725-125">Локальные записи хранения сохраняются бесконечно до тех пор, пока пользователь не расчистит страницу или вручную:</span><span class="sxs-lookup"><span data-stu-id="89725-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>  

   <span data-ttu-id="89725-126">**Параметры**  >  **Очистка данных просмотра**  >  **Файлы cookie и сохраненные данные веб-сайта**</span><span class="sxs-lookup"><span data-stu-id="89725-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

![Очистка данных просмотра с панели параметров Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a><span data-ttu-id="89725-128">Список хранения</span><span class="sxs-lookup"><span data-stu-id="89725-128">Storage list</span></span>  

<span data-ttu-id="89725-129">Из таблицы список хранения можно:</span><span class="sxs-lookup"><span data-stu-id="89725-129">From the Storage list table you can:</span></span>  

*   <span data-ttu-id="89725-130">**Проверьте и сортировать** пары, нажав на имя `key/value` столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="89725-130">**Inspect and sort** your `key/value` pairs by clicking on either column name in the table.</span></span>  
*   <span data-ttu-id="89725-131">**Изменение** `Key` `Value` существующей записи и ее изменения, щелкнув в ячейке.</span><span class="sxs-lookup"><span data-stu-id="89725-131">**Edit** the `Key` and `Value` of an existing entry by clicking in the cell.</span></span>  
*   <span data-ttu-id="89725-132">**Удаление** \( \) записи из параметра контекстного меню правой `Del` кнопкой мыши, **Удалить элемент**.</span><span class="sxs-lookup"><span data-stu-id="89725-132">**Delete** \(`Del`\) an entry from the right-click context menu option, **Delete item**.</span></span>  
*   <span data-ttu-id="89725-133">**Добавьте** новую `key/value` пару, щелкнув пустую строку в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="89725-133">**Add** a new `key/value` pair by clicking on the empty row at the bottom of the table.</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="89725-134">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="89725-134">Shortcuts</span></span>

| <span data-ttu-id="89725-135">Действие</span><span class="sxs-lookup"><span data-stu-id="89725-135">Action</span></span> | <span data-ttu-id="89725-136">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="89725-136">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="89725-137">Обновить</span><span class="sxs-lookup"><span data-stu-id="89725-137">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="89725-138">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="89725-138">Delete item</span></span> | `Del` |  
| <span data-ttu-id="89725-139">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="89725-139">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="89725-140">Выделить все</span><span class="sxs-lookup"><span data-stu-id="89725-140">Select all</span></span> | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a><span data-ttu-id="89725-141">Диспетчер IndexedDB</span><span class="sxs-lookup"><span data-stu-id="89725-141">IndexedDB manager</span></span>  

<span data-ttu-id="89725-142">Используйте **вкладку IndexedDB** для проверки и управления структурированными данными, хранимыми локально на клиентской машине.</span><span class="sxs-lookup"><span data-stu-id="89725-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span>  <span data-ttu-id="89725-143">В частности, вы можете проверять/сортировать и обновлять хранилища и индексы объектов, а также удалять отдельные записи с ключевым значением.</span><span class="sxs-lookup"><span data-stu-id="89725-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>  

> [!TIP]
> <span data-ttu-id="89725-144">Вы можете использовать нашу [демо-версию](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) аудиомеханик для тест-драйва руководителя *IndexedDB* в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="89725-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="89725-145">Чтобы удалить все данные IndexedDB, хранимые для текущего пользователя в Microsoft Edge, используйте меню Microsoft Edge **Settings:**</span><span class="sxs-lookup"><span data-stu-id="89725-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge **Settings** menu:</span></span>  

<span data-ttu-id="89725-146">**...** >  **Параметры**  >  **Очистка данных просмотра**  >  **Файлы cookie и сохраненные данные веб-сайта**</span><span class="sxs-lookup"><span data-stu-id="89725-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

<span data-ttu-id="89725-147">Папка в средстве выборщика ресурсов Отладщика отображает список источников из ресурсов, `IndexedDB` загруженных на [](./debugger.md#resource-picker) страницу.</span><span class="sxs-lookup"><span data-stu-id="89725-147">The `IndexedDB` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="89725-148">Все базы данных IndexedDB \(IDB\) будут указаны в начале, а также в их хранилищах объектов.</span><span class="sxs-lookup"><span data-stu-id="89725-148">Any IndexedDB \(IDB\) databases will be listed under the origin, along with their object stores.</span></span>  

![Диспетчер индексации DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a><span data-ttu-id="89725-150">Панель инструментов IndexedDB</span><span class="sxs-lookup"><span data-stu-id="89725-150">IndexedDB Toolbar</span></span>  

<span data-ttu-id="89725-151">Из панели инструментов IndexedDB можно:</span><span class="sxs-lookup"><span data-stu-id="89725-151">From the IndexedDB toolbar you can:</span></span>  

*   <span data-ttu-id="89725-152">**Обновление** \. Чтобы увидеть текущие записи `Ctrl` + `F5` в объектном хранилище или индексе базы данных.</span><span class="sxs-lookup"><span data-stu-id="89725-152">**Refresh** \(`Ctrl`+`F5`\) to see the current entries in the object store or index of your database.</span></span>  <span data-ttu-id="89725-153">Диспетчер IndexedDB не обновляется автоматически при внесении изменений в базу данных.</span><span class="sxs-lookup"><span data-stu-id="89725-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>  

### <a name="object-store-entries-list"></a><span data-ttu-id="89725-154">Список записей в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="89725-154">Object store entries list</span></span>  

<span data-ttu-id="89725-155">Из таблицы "Объектный магазин" или "Индекс" можно:</span><span class="sxs-lookup"><span data-stu-id="89725-155">From the Object store or Index table you can:</span></span>  

*   <span data-ttu-id="89725-156">**Проверьте и сортировать** пары значений ключа, щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="89725-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="89725-157">**Обновление** \( `Ctrl` + `F5` \)</span><span class="sxs-lookup"><span data-stu-id="89725-157">**Refresh** \(`Ctrl`+`F5`\)</span></span>  
*   <span data-ttu-id="89725-158">**Удаление элемента** \( `Del` \) для удаления выбранной записи в хранилище объекта или индексе.</span><span class="sxs-lookup"><span data-stu-id="89725-158">**Delete item** \(`Del`\) to remove the selected entry in your object store or index.</span></span>  <span data-ttu-id="89725-159">Вы также можете сделать это из параметра контекстного меню правой [кнопкой](#context-menu) мыши Удалить **элемент**.</span><span class="sxs-lookup"><span data-stu-id="89725-159">You can also do this from the right-click [context menu](#context-menu) option, **Delete item**.</span></span>  
*   <span data-ttu-id="89725-160">**Скопируйте выбранные** элементы `Ctrl` + \( \) для копирования выбранного элемента `C` в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="89725-160">**Copy selected items** \(`Ctrl`+`C`\) to copy the selected item to your clipboard.</span></span>  <span data-ttu-id="89725-161">Вы также можете сделать это из параметра контекстного меню правой [кнопкой](#context-menu) мыши, **скопируйте выбранный элемент**.</span><span class="sxs-lookup"><span data-stu-id="89725-161">You can also do this from the right-click [context menu](#context-menu) option, **Copy selected item**.</span></span>  
*   <span data-ttu-id="89725-162">**Выберите все** \( \) для выбора всех `Ctrl` + `A` записей в объектном магазине или индексе.</span><span class="sxs-lookup"><span data-stu-id="89725-162">**Select all** \(`Ctrl`+`A`\) to select all the entries in your object store or index.</span></span>  <span data-ttu-id="89725-163">Вы также можете сделать это из параметра контекстного меню правой [кнопкой](#context-menu) мыши Выберите **все**.</span><span class="sxs-lookup"><span data-stu-id="89725-163">You can also do this from the right-click [context menu](#context-menu) option, **Select all**.</span></span>  

<span data-ttu-id="89725-164">Столбцы магазина объектов или таблицы Index можно сортировать:</span><span class="sxs-lookup"><span data-stu-id="89725-164">The columns of the Object store or Index table are sortable:</span></span>  

| <span data-ttu-id="89725-165">Столбец</span><span class="sxs-lookup"><span data-stu-id="89725-165">Column</span></span> | <span data-ttu-id="89725-166">Описание</span><span class="sxs-lookup"><span data-stu-id="89725-166">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="89725-167">Раздел</span><span class="sxs-lookup"><span data-stu-id="89725-167">Key</span></span> | <span data-ttu-id="89725-168">Имя пары ключ-значение \(то же самое, что **Основной**ключ \) при итерации над хранилищем объектов; Имя ключа индекса \(текущий ключ курсора\) при итерации над индексом</span><span class="sxs-lookup"><span data-stu-id="89725-168">Name of the key-value pair \(same as **Primary Key**\) when iterating over an object store; Name of the index key \(cursor's current key\) when iterating over an index</span></span> |  
| <span data-ttu-id="89725-169">Основной ключ</span><span class="sxs-lookup"><span data-stu-id="89725-169">Primary Key</span></span> | <span data-ttu-id="89725-170">Имя пары ключ-значение \(см. веб-документы **MDN** для получения дополнительных данных на клавишах [IDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span><span class="sxs-lookup"><span data-stu-id="89725-170">Name of the key-value pair \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span></span> |  
| <span data-ttu-id="89725-171">Значение</span><span class="sxs-lookup"><span data-stu-id="89725-171">Value</span></span> | <span data-ttu-id="89725-172">Значение пары ключ-значение</span><span class="sxs-lookup"><span data-stu-id="89725-172">Value of the key-value pair</span></span> |  

<span data-ttu-id="89725-173">Ознакомьтесь *с веб-docs MDN,* чтобы узнать больше о концепциях [и использовании IndexedDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)</span><span class="sxs-lookup"><span data-stu-id="89725-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>  

### <a name="context-menu"></a><span data-ttu-id="89725-174">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="89725-174">Context menu</span></span>  

<span data-ttu-id="89725-175">В дополнение к панели инструментов [ *IndexedDB* ](#indexeddb-toolbar)вы также можете управлять своими данными в хранилищах объектов или индексах из меню **контекста** правой кнопкой мыши и/или ярлыков [клавиатуры.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="89725-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="89725-176">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="89725-176">Shortcuts</span></span>

| <span data-ttu-id="89725-177">Действие</span><span class="sxs-lookup"><span data-stu-id="89725-177">Action</span></span> | <span data-ttu-id="89725-178">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="89725-178">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="89725-179">Обновить</span><span class="sxs-lookup"><span data-stu-id="89725-179">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="89725-180">Удаление пары значений ключа</span><span class="sxs-lookup"><span data-stu-id="89725-180">Delete key-value pair</span></span> | `Del` |  
| <span data-ttu-id="89725-181">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="89725-181">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="89725-182">Выделить все</span><span class="sxs-lookup"><span data-stu-id="89725-182">Select all</span></span> | `Ctrl +`<span data-ttu-id="89725-183">A'</span><span class="sxs-lookup"><span data-stu-id="89725-183">A\`</span></span> |  

## <a name="cookies-manager"></a><span data-ttu-id="89725-184">Менеджер cookies</span><span class="sxs-lookup"><span data-stu-id="89725-184">Cookies manager</span></span>  

<span data-ttu-id="89725-185">Используйте диспетчер cookies для проверки и управления файлами cookie для данного домена.</span><span class="sxs-lookup"><span data-stu-id="89725-185">Use the Cookies manager to inspect and manage the cookies for the given domain.</span></span>  

<span data-ttu-id="89725-186">Папка в средстве выборщика ресурсов Отладщика отображает список источников из ресурсов, `Cookies` загруженных на [](./debugger.md#resource-picker) страницу.</span><span class="sxs-lookup"><span data-stu-id="89725-186">The `Cookies` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="89725-187">Выбор одного из этих кадров открывает таблицу, представляющую [](https://developer.mozilla.org/docs/Web/HTTP/Cookies) текущие файлы cookie, установленные либо http-загонами, либо по сценарию [с Document.cookie.](https://developer.mozilla.org/docs/Web/API/Document/cookie)</span><span class="sxs-lookup"><span data-stu-id="89725-187">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>  

![Менеджер cookies DevTools](./media/storage_cookies.png)  

<span data-ttu-id="89725-189">На панели инструментов вкладки Cookie можно:</span><span class="sxs-lookup"><span data-stu-id="89725-189">From the Cookies tab toolbar you can:</span></span>  

*   <span data-ttu-id="89725-190">**Обновление** \. `Ctrl` + `F5` Список [cookies,](#cookies-list) чтобы увидеть текущий набор файлов cookie для данного домена.</span><span class="sxs-lookup"><span data-stu-id="89725-190">**Refresh** \(`Ctrl`+`F5`\) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span>  <span data-ttu-id="89725-191">\(Список не обновляется автоматически.\)</span><span class="sxs-lookup"><span data-stu-id="89725-191">\(The list does not auto-refresh.\)</span></span>  
*   <span data-ttu-id="89725-192">**Удалите все** файлы cookie \( `Ctrl` + `Shift` + `Del` \) \(сеанс и постоянный\) для пути текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="89725-192">**Delete all cookies** \(`Ctrl`+`Shift`+`Del`\) \(session and permanent\) for the path of the current page.</span></span>  
*   <span data-ttu-id="89725-193">**Удалите все файлы cookie сеанса** `Ctrl` + `Del` \( \) для пути текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="89725-193">**Delete all session cookies** \(`Ctrl`+`Del`\) for the path of the current page.</span></span>  

<span data-ttu-id="89725-194">Чтобы полностью очистить список cookies, может потребоваться очистить все **файлы cookie** для домена из панели инструментов [панели](./network.md#toolbar) Сети.</span><span class="sxs-lookup"><span data-stu-id="89725-194">To completely clear your Cookies list, you might need to **Clear all cookies for the domain** from the [Network](./network.md#toolbar) panel toolbar.</span></span>  

### <a name="cookies-list"></a><span data-ttu-id="89725-195">Список файлов cookie</span><span class="sxs-lookup"><span data-stu-id="89725-195">Cookies list</span></span>  

<span data-ttu-id="89725-196">Из таблицы списков Cookie можно:</span><span class="sxs-lookup"><span data-stu-id="89725-196">From the Cookies list table you can:</span></span>  

*   <span data-ttu-id="89725-197">**Проверьте и сортировать** файлы cookie, щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="89725-197">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="89725-198">**Изменение** `Name` `Value` существующего файла cookie и его редактирования, щелкнув в ячейке.</span><span class="sxs-lookup"><span data-stu-id="89725-198">**Edit** the `Name` and `Value` of an existing cookie by clicking in the cell.</span></span>  
*   <span data-ttu-id="89725-199">**Удаление** \( \) cookie из параметра контекстного меню правой `Del` кнопкой [](#context-menu) `Delete cookie` мыши.</span><span class="sxs-lookup"><span data-stu-id="89725-199">**Delete** \(`Del`\) a cookie from the right-click [context menu](#context-menu) option, `Delete cookie`.</span></span>  
*   <span data-ttu-id="89725-200">**Добавьте** новое cookie сеанса для данного, щелкнув пустую строку `Domain/Path` в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="89725-200">**Add** a new session cookie for the given `Domain/Path` by clicking on the empty row at the bottom of the table.</span></span>  <span data-ttu-id="89725-201">Это работает только для файлов cookie сеанса; постоянные файлы cookie \(с определенными датами истечения\) должны быть установлены традиционными методами.</span><span class="sxs-lookup"><span data-stu-id="89725-201">This only works for session cookies; permanent cookies \(with specific expiry dates\) must be set with traditional methods.</span></span>  <span data-ttu-id="89725-202">Значения `Domain` `Path` и значения автоматически заполняются в зависимости от расположения страницы.</span><span class="sxs-lookup"><span data-stu-id="89725-202">The `Domain` and `Path` values are auto-filled according to the location of the page.</span></span>  

<span data-ttu-id="89725-203">Столбцы списка Cookie можно сортировать:</span><span class="sxs-lookup"><span data-stu-id="89725-203">The columns of the Cookies list are sortable:</span></span>

| <span data-ttu-id="89725-204">Столбец</span><span class="sxs-lookup"><span data-stu-id="89725-204">Column</span></span> | <span data-ttu-id="89725-205">Описание</span><span class="sxs-lookup"><span data-stu-id="89725-205">Description</span></span> |  
| :--- | :--- |  
| <span data-ttu-id="89725-206">Name</span><span class="sxs-lookup"><span data-stu-id="89725-206">Name</span></span> | <span data-ttu-id="89725-207">Имя файла cookie</span><span class="sxs-lookup"><span data-stu-id="89725-207">Name of the cookie</span></span> |  
| <span data-ttu-id="89725-208">Значение</span><span class="sxs-lookup"><span data-stu-id="89725-208">Value</span></span> | <span data-ttu-id="89725-209">Значение файла cookie</span><span class="sxs-lookup"><span data-stu-id="89725-209">Value of the cookie</span></span> |  
| <span data-ttu-id="89725-210">Домен</span><span class="sxs-lookup"><span data-stu-id="89725-210">Domain</span></span> | <span data-ttu-id="89725-211">Имя хост-файла cookie \(может быть пустым\)</span><span class="sxs-lookup"><span data-stu-id="89725-211">Host name of the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="89725-212">Путь</span><span class="sxs-lookup"><span data-stu-id="89725-212">Path</span></span> | <span data-ttu-id="89725-213">ПУТЬ URL-адреса для cookie \(может быть пустым\)</span><span class="sxs-lookup"><span data-stu-id="89725-213">URL path for the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="89725-214">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="89725-214">Expires</span></span> | <span data-ttu-id="89725-215">Максимальный срок службы cookie в качестве даты http-даты.</span><span class="sxs-lookup"><span data-stu-id="89725-215">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span>  <span data-ttu-id="89725-216">Если нет `Expires` `Max-Age` или установлено, запись считается cookie session.</span><span class="sxs-lookup"><span data-stu-id="89725-216">If no `Expires` or `Max-Age` was set, the entry is considered a Session cookie.</span></span>  |  
| <span data-ttu-id="89725-217">ТОЛЬКО HTTP</span><span class="sxs-lookup"><span data-stu-id="89725-217">HTTP only</span></span> | <span data-ttu-id="89725-218">Указывает, было ли установлено cookie с директивой, указывающее, что он недоступен `HttpOnly` для JavaScript</span><span class="sxs-lookup"><span data-stu-id="89725-218">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span> |  
| <span data-ttu-id="89725-219">Защита</span><span class="sxs-lookup"><span data-stu-id="89725-219">Secure</span></span> | <span data-ttu-id="89725-220">Указывает, было ли установлено cookie с директивой, указав, что оно будет отправлено на сервер только из запроса с помощью `Secure` SSL и протокола HTTPS.</span><span class="sxs-lookup"><span data-stu-id="89725-220">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>  |  

<span data-ttu-id="89725-221">Дополнительные сведения о свойствах cookie см. в справке по [веб-docs Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) **MDN.**</span><span class="sxs-lookup"><span data-stu-id="89725-221">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>  

### <a name="context-menu"></a><span data-ttu-id="89725-222">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="89725-222">Context menu</span></span>  

<span data-ttu-id="89725-223">В дополнение к панели инструментов вкладки Cookies, вы также можете \*\*\*\* управлять своими куки из меню контекста правой кнопкой мыши и/или ярлыков [клавиатуры.](#shortcuts) [](#cookies-manager)</span><span class="sxs-lookup"><span data-stu-id="89725-223">In addition to the Cookies tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="89725-224">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="89725-224">Shortcuts</span></span>  

| <span data-ttu-id="89725-225">Действие</span><span class="sxs-lookup"><span data-stu-id="89725-225">Action</span></span> | <span data-ttu-id="89725-226">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="89725-226">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="89725-227">Обновить</span><span class="sxs-lookup"><span data-stu-id="89725-227">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="89725-228">Удаление cookie</span><span class="sxs-lookup"><span data-stu-id="89725-228">Delete cookie</span></span> | `Del` |  
| <span data-ttu-id="89725-229">Удаление всех файлов cookie</span><span class="sxs-lookup"><span data-stu-id="89725-229">Delete all cookies</span></span> | `Ctrl`+`Shift`+`Del` |  
| <span data-ttu-id="89725-230">Удаление всех файлов cookie сеанса</span><span class="sxs-lookup"><span data-stu-id="89725-230">Delete all session cookies</span></span> | `Ctrl`+`Del` |  
| <span data-ttu-id="89725-231">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="89725-231">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="89725-232">Выделить все</span><span class="sxs-lookup"><span data-stu-id="89725-232">Select all</span></span> | `Ctrl`+`A` |  

### <a name="cache-manager"></a><span data-ttu-id="89725-233">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="89725-233">Cache manager</span></span>  

<span data-ttu-id="89725-234">Нажав на определенную запись кэша, \*\*\*\* откроется диспетчер кэша сотрудника службы, где можно проверять и необязательно удалять записи кэша \( и пары ключей и `Request` значений\): `Response`</span><span class="sxs-lookup"><span data-stu-id="89725-234">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries \(`Request` and `Response` key/value pairs\):</span></span>  

![Диспетчер кэша](./media/storage_cache.png)  

### <a name="shortcuts"></a><span data-ttu-id="89725-236">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="89725-236">Shortcuts</span></span>  

#### <a name="cache-manager"></a><span data-ttu-id="89725-237">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="89725-237">Cache manager</span></span>  

| <span data-ttu-id="89725-238">Действие</span><span class="sxs-lookup"><span data-stu-id="89725-238">Action</span></span> | <span data-ttu-id="89725-239">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="89725-239">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="89725-240">Обновить</span><span class="sxs-lookup"><span data-stu-id="89725-240">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="89725-241">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="89725-241">Delete item</span></span> | `Del` |  
| <span data-ttu-id="89725-242">Копирование выбранных элементов</span><span class="sxs-lookup"><span data-stu-id="89725-242">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="89725-243">Выделить все</span><span class="sxs-lookup"><span data-stu-id="89725-243">Select all</span></span> | `Ctrl`+`A` |  
