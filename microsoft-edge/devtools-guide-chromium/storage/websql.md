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

# <span data-ttu-id="1c40c-104">Просмотр данных веб-SQL с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c40c-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="1c40c-105">Спецификация веб-SQL не [поддерживается.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="1c40c-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="1c40c-106">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных веб-SQL.</span><span class="sxs-lookup"><span data-stu-id="1c40c-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="1c40c-107">Просмотр данных веб-SQL</span><span class="sxs-lookup"><span data-stu-id="1c40c-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="1c40c-108">Выберите **вкладку "Источники",** чтобы открыть **средство "Источники".**</span><span class="sxs-lookup"><span data-stu-id="1c40c-108">Select the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="1c40c-109">Обычно **по** умолчанию открывается окно манифеста.</span><span class="sxs-lookup"><span data-stu-id="1c40c-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="1c40c-111">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="1c40c-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c40c-112">**Разоберись с SQL** веб-страниц, чтобы просмотреть базы данных и таблицы.</span><span class="sxs-lookup"><span data-stu-id="1c40c-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="1c40c-113">На следующем рисунке под **html5meetup** находится база данных, а **комнаты** — таблица.</span><span class="sxs-lookup"><span data-stu-id="1c40c-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Веб-SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="1c40c-115">**Веб-SQL**</span><span class="sxs-lookup"><span data-stu-id="1c40c-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c40c-116">Выберите таблицу, чтобы просмотреть данные для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="1c40c-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Просмотр данных таблицы веб-SQL" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="1c40c-118">Просмотр данных таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="1c40c-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c40c-119">Изменение данных веб-SQL</span><span class="sxs-lookup"><span data-stu-id="1c40c-119">Edit Web SQL data</span></span>  

<span data-ttu-id="1c40c-120">При просмотре таблицы веб-SQL нельзя редактировать данные веб-SQL, как по сравнению с предыдущими.</span><span class="sxs-lookup"><span data-stu-id="1c40c-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="1c40c-121">Но вы можете запускать в консоли web SQL утверждения, которые редактирует или удаляет таблицы.</span><span class="sxs-lookup"><span data-stu-id="1c40c-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="1c40c-122">См. [запросы SQL веб-сайтов.](#run-web-sql-queries)</span><span class="sxs-lookup"><span data-stu-id="1c40c-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="1c40c-123">Выполнение запросов SQL веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="1c40c-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="1c40c-124">Выберите базу данных, чтобы открыть консоль для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="1c40c-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="1c40c-125">Введите SQL Web SQL и выберите `Enter` его запуск.</span><span class="sxs-lookup"><span data-stu-id="1c40c-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Использование консоли web SQL для удаления строки из таблицы" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="1c40c-127">Использование консоли web SQL для удаления строки из таблицы</span><span class="sxs-lookup"><span data-stu-id="1c40c-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c40c-128">Обновление таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="1c40c-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="1c40c-129">DevTools не обновляет таблицы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="1c40c-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="1c40c-130">Чтобы обновить данные в таблице, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c40c-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="1c40c-131">[Просмотр данных в таблице веб-SQL.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="1c40c-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="1c40c-132">Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="1c40c-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="1c40c-133">Фильтрация столбцов в таблице веб-SQL</span><span class="sxs-lookup"><span data-stu-id="1c40c-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="1c40c-134">[Просмотр данных в таблице веб-SQL.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="1c40c-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="1c40c-135">Используйте **текстовое поле "Видимые столбцы",** чтобы указать, какие столбцы нужно отметить.</span><span class="sxs-lookup"><span data-stu-id="1c40c-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="1c40c-136">Предо в качестве CSV-списка имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="1c40c-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Использование текстового окна "Видимые столбцы" для уменьшения числа столбцов" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="1c40c-138">Использование **текстового окна "Видимые столбцы"** для уменьшения числа столбцов</span><span class="sxs-lookup"><span data-stu-id="1c40c-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c40c-139">Удаление всех данных SQL веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="1c40c-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="1c40c-140">Откройте области **"Очистить** хранилище".</span><span class="sxs-lookup"><span data-stu-id="1c40c-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="1c40c-141">Убедитесь, **что** SQL веб-страницы включен.</span><span class="sxs-lookup"><span data-stu-id="1c40c-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="The Web SQL checkbox" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="1c40c-143">The **Web SQL** checkbox</span><span class="sxs-lookup"><span data-stu-id="1c40c-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1c40c-144">Выберите **"Очистить данные сайта".**</span><span class="sxs-lookup"><span data-stu-id="1c40c-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Кнопка очистки данных сайта" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="1c40c-146">Кнопка **очистки данных** сайта</span><span class="sxs-lookup"><span data-stu-id="1c40c-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1c40c-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1c40c-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "База данных веб SQL | W3C"  

> [!NOTE]
> <span data-ttu-id="1c40c-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c40c-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c40c-151">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/websql) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1c40c-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c40c-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c40c-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
