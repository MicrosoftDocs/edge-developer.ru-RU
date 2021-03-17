---
description: Просмотр веб-SQL с панели приложений Microsoft Edge DevTools.
title: Просмотр веб-SQL с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9f684aabf3592220079e6a8595d91cfea6785769
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439600"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a><span data-ttu-id="ffe40-104">Просмотр веб-SQL с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ffe40-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="ffe40-105">Спецификация веб SQL [не поддерживается.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="ffe40-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="ffe40-106">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки веб-SQL данных.</span><span class="sxs-lookup"><span data-stu-id="ffe40-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <a name="view-web-sql-data"></a><span data-ttu-id="ffe40-107">Просмотр веб-SQL данных</span><span class="sxs-lookup"><span data-stu-id="ffe40-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="ffe40-108">Выберите средство **Источники** для открытия **средства Источники.**</span><span class="sxs-lookup"><span data-stu-id="ffe40-108">Choose the **Sources** tool to open the **Sources** tool.</span></span>  <span data-ttu-id="ffe40-109">Обычно **области Манифеста** открываются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ffe40-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="ffe40-111">Области **Манифест**</span><span class="sxs-lookup"><span data-stu-id="ffe40-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ffe40-112">**Расширь раздел веб SQL,** чтобы просмотреть базы данных и таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffe40-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="ffe40-113">На следующем рисунке ниже **html5meetup** находится база данных, а в **комнатах** — таблица.</span><span class="sxs-lookup"><span data-stu-id="ffe40-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Области веб-SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="ffe40-115">Области **веб-SQL**</span><span class="sxs-lookup"><span data-stu-id="ffe40-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ffe40-116">Выберите таблицу для просмотра данных для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffe40-116">Choose a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Просмотр данных таблицы веб-SQL" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="ffe40-118">Просмотр данных таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ffe40-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a><span data-ttu-id="ffe40-119">Редактирование SQL веб-данных</span><span class="sxs-lookup"><span data-stu-id="ffe40-119">Edit Web SQL data</span></span>  

<span data-ttu-id="ffe40-120">При просмотре таблицы веб SQL веб-SQL, например в предыдущей таблице, изменить веб-SQL не удастся.</span><span class="sxs-lookup"><span data-stu-id="ffe40-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="ffe40-121">Но вы можете запускать заявления из консоли SQL, которые редактировать или удалять таблицы.</span><span class="sxs-lookup"><span data-stu-id="ffe40-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="ffe40-122">Перейдите [для запуска веб SQL запросов.](#run-web-sql-queries)</span><span class="sxs-lookup"><span data-stu-id="ffe40-122">Navigate to [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <a name="run-web-sql-queries"></a><span data-ttu-id="ffe40-123">Запуск веб SQL запросов</span><span class="sxs-lookup"><span data-stu-id="ffe40-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="ffe40-124">Выберите базу данных, чтобы открыть консоль для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ffe40-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="ffe40-125">Введите веб-SQL, а затем `Enter` выберите, чтобы запустить его.</span><span class="sxs-lookup"><span data-stu-id="ffe40-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Консоль веб SQL для удаления строки из таблицы" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="ffe40-127">Консоль веб SQL для удаления строки из таблицы</span><span class="sxs-lookup"><span data-stu-id="ffe40-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a><span data-ttu-id="ffe40-128">Обновление таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ffe40-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="ffe40-129">DevTools не обновляет таблицы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ffe40-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="ffe40-130">Чтобы обновить данные в таблице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ffe40-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="ffe40-131">[Просмотр данных в таблице веб-SQL.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="ffe40-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="ffe40-132">Выберите **обновление** \. ![ Обновление ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="ffe40-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a><span data-ttu-id="ffe40-133">Фильтрация столбцов в таблице веб-SQL</span><span class="sxs-lookup"><span data-stu-id="ffe40-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="ffe40-134">[Просмотр данных в таблице веб-SQL.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="ffe40-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="ffe40-135">Используйте **текстовое поле Видимые столбцы,** чтобы указать, какие столбцы нужно показывать.</span><span class="sxs-lookup"><span data-stu-id="ffe40-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="ffe40-136">Предоставление имен столбцов в качестве списка CSV.</span><span class="sxs-lookup"><span data-stu-id="ffe40-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Используйте текстовое поле Видимые столбцы, чтобы уменьшить число показанных столбцов" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="ffe40-138">Используйте **текстовое поле Видимые столбцы,** чтобы уменьшить число показанных столбцов</span><span class="sxs-lookup"><span data-stu-id="ffe40-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a><span data-ttu-id="ffe40-139">Удаление всех SQL веб SQL</span><span class="sxs-lookup"><span data-stu-id="ffe40-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="ffe40-140">Откройте пространство **Clear Storage.**</span><span class="sxs-lookup"><span data-stu-id="ffe40-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="ffe40-141">Убедитесь, что **SQL** веб-SQL включен.</span><span class="sxs-lookup"><span data-stu-id="ffe40-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Веб-SQL почтовый ящик" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="ffe40-143">**Веб-SQL** почтовый ящик</span><span class="sxs-lookup"><span data-stu-id="ffe40-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ffe40-144">Выберите **четкие данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="ffe40-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Кнопка Clear Site Data" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="ffe40-146">Кнопка **Clear Site Data**</span><span class="sxs-lookup"><span data-stu-id="ffe40-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ffe40-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ffe40-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Веб-SQL базы данных | W3C"  

> [!NOTE]
> <span data-ttu-id="ffe40-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ffe40-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ffe40-151">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/websql) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="ffe40-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ffe40-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ffe40-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
