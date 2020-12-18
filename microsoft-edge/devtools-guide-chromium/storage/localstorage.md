---
description: Просмотр и изменение localStorage с помощью области локального хранилища и консоли.
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c68f11b8ba2c10a0792f10acf5c5ededf2ad8e8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231190"
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

# <span data-ttu-id="eb39a-104">Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eb39a-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="eb39a-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления пар ["ключ-значение localStorage".][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="eb39a-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="eb39a-106">Просмотр ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="eb39a-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="eb39a-107">Откройте средство **"Приложение"** на вкладке **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="eb39a-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="eb39a-108">По **умолчанию** отображается области манифеста.</span><span class="sxs-lookup"><span data-stu-id="eb39a-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="eb39a-110">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="eb39a-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eb39a-111">Разорите **меню "Локальное** хранилище".</span><span class="sxs-lookup"><span data-stu-id="eb39a-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Меню "Локальное хранилище"" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="eb39a-113">Меню **"Локальное хранилище"**</span><span class="sxs-lookup"><span data-stu-id="eb39a-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eb39a-114">Выберите домен для просмотра пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="eb39a-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Пары "ключ-значение" localStorage для https://www.bing.com домена" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="eb39a-116">Пары `localStorage` "ключ-значение" для `https://www.bing.com` домена</span><span class="sxs-lookup"><span data-stu-id="eb39a-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eb39a-117">Выберите строку таблицы, чтобы просмотреть значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="eb39a-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Просмотр значения ключа eventLogQueue_Online клавиши" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="eb39a-119">Просмотр значения `eventLogQueue_Online` ключа</span><span class="sxs-lookup"><span data-stu-id="eb39a-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="eb39a-120">Создание новой пары ключ-значение localStorage</span><span class="sxs-lookup"><span data-stu-id="eb39a-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="eb39a-121">[Просмотр пар "ключ-значение localStorage" домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="eb39a-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="eb39a-122">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="eb39a-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="eb39a-123">DevTools создает новую строку и фокусирует курсор в **столбце "Ключ".**</span><span class="sxs-lookup"><span data-stu-id="eb39a-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Пустая часть таблицы, которая дважды щелкает, чтобы создать новую пару "ключ-значение"." lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="eb39a-125">Пустая часть таблицы, которая дважды щелкает, чтобы создать новую пару "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="eb39a-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="eb39a-126">Изменение ключей или значений localStorage</span><span class="sxs-lookup"><span data-stu-id="eb39a-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="eb39a-127">[Просмотр пар "ключ-значение localStorage" домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="eb39a-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="eb39a-128">Дважды щелкните ячейку в столбце **"Ключ"** или **"Значение",** чтобы изменить этот ключ или значение.</span><span class="sxs-lookup"><span data-stu-id="eb39a-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Изменение ключа localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="eb39a-130">Изменение `localStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="eb39a-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="eb39a-131">Удаление пар "ключ-значение" localStorage</span><span class="sxs-lookup"><span data-stu-id="eb39a-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="eb39a-132">[Просмотр пар `localStorage` "ключ-значение" домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="eb39a-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="eb39a-133">Выберите пару "ключ-значение", которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eb39a-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="eb39a-134">DevTools выделяет его синим цветом, чтобы показать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="eb39a-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="eb39a-135">Select the `Delete` key or choose Delete **Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="eb39a-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="eb39a-136">Удаление всех `localStorage` пар "ключ-значение" для домена</span><span class="sxs-lookup"><span data-stu-id="eb39a-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="eb39a-137">[Просмотр пар `localStorage` "ключ-значение" домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="eb39a-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="eb39a-138">Choose **Clear All** \( Clear All ![ ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="eb39a-138">Choose **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="eb39a-139">Взаимодействие с localStorage из консоли</span><span class="sxs-lookup"><span data-stu-id="eb39a-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="eb39a-140">Так как вы можете запускать JavaScript в \*\*\*\* **консоли,** а так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `localStorage` **консолью.**</span><span class="sxs-lookup"><span data-stu-id="eb39a-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="eb39a-141">Используйте **контекстное меню JavaScript,** чтобы изменить \*\*\*\* контекст JavaScript консоли, если вы хотите получить доступ к парам "ключ-значение" домена, кроме отображаемой `localStorage` страницы.</span><span class="sxs-lookup"><span data-stu-id="eb39a-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="eb39a-143">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="eb39a-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eb39a-144">Запустите выражения в консоли так же, как `localStorage` и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eb39a-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Взаимодействие с localStorage из консоли" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="eb39a-146">Взаимодействие с `localStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="eb39a-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="eb39a-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="eb39a-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="eb39a-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb39a-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eb39a-151">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="eb39a-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="eb39a-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb39a-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
