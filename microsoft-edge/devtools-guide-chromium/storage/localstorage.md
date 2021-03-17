---
description: Просмотр и редактирование localStorage с помощью области локального хранения и консоли.
title: Просмотр и редактирование локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439677"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="50fd6-104">Просмотр и редактирование локального хранилища с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="50fd6-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="50fd6-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, редактирования и удаления пар [ключей localStorage.][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="50fd6-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <a name="view-localstorage-keys-and-values"></a><span data-ttu-id="50fd6-106">Просмотр ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="50fd6-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="50fd6-107">Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.</span><span class="sxs-lookup"><span data-stu-id="50fd6-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="50fd6-108">По умолчанию отображается области **Манифеста.**</span><span class="sxs-lookup"><span data-stu-id="50fd6-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="50fd6-110">Области **Манифест**</span><span class="sxs-lookup"><span data-stu-id="50fd6-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50fd6-111">**Расширь меню локального** хранения.</span><span class="sxs-lookup"><span data-stu-id="50fd6-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Меню локального хранения" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="50fd6-113">Меню **локального** хранения</span><span class="sxs-lookup"><span data-stu-id="50fd6-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50fd6-114">Выберите домен для просмотра пар с ключевым значением.</span><span class="sxs-lookup"><span data-stu-id="50fd6-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Пары ключей localStorage для https://www.bing.com домена" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="50fd6-116">Пары `localStorage` значений ключа для `https://www.bing.com` домена</span><span class="sxs-lookup"><span data-stu-id="50fd6-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50fd6-117">Выберите строку таблицы, чтобы просмотреть значение в представлении ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="50fd6-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Просмотр значения клавиши eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="50fd6-119">Просмотр значения `eventLogQueue_Online` ключа</span><span class="sxs-lookup"><span data-stu-id="50fd6-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a><span data-ttu-id="50fd6-120">Создание новой пары ключ-значение localStorage</span><span class="sxs-lookup"><span data-stu-id="50fd6-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="50fd6-121">[Просмотр пар ключ-значения localStorage домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="50fd6-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="50fd6-122">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="50fd6-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="50fd6-123">DevTools создает новую строку и фокусирует курсор в **столбце Ключ.**</span><span class="sxs-lookup"><span data-stu-id="50fd6-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="50fd6-125">Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа</span><span class="sxs-lookup"><span data-stu-id="50fd6-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a><span data-ttu-id="50fd6-126">Изменение ключей или значений localStorage</span><span class="sxs-lookup"><span data-stu-id="50fd6-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="50fd6-127">[Просмотр пар ключ-значения localStorage домена.](#view-localstorage-keys-and-values)</span><span class="sxs-lookup"><span data-stu-id="50fd6-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="50fd6-128">Дважды щелкните ячейку в столбце **Ключ** или **Значение,** чтобы изменить этот ключ или значение.</span><span class="sxs-lookup"><span data-stu-id="50fd6-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Изменение ключа localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="50fd6-130">Изменение `localStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="50fd6-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a><span data-ttu-id="50fd6-131">Удаление пар ключ-значения localStorage</span><span class="sxs-lookup"><span data-stu-id="50fd6-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="50fd6-132">[Просмотр `localStorage` пар значений ключа домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="50fd6-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="50fd6-133">Выберите пару с значением ключа, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="50fd6-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="50fd6-134">DevTools выделяет его синим цветом, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="50fd6-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="50fd6-135">Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="50fd6-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="50fd6-136">Удаление всех `localStorage` пар значений ключа для домена</span><span class="sxs-lookup"><span data-stu-id="50fd6-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="50fd6-137">[Просмотр `localStorage` пар значений ключа домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="50fd6-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="50fd6-138">Выберите **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="50fd6-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-localstorage-from-the-console"></a><span data-ttu-id="50fd6-139">Взаимодействие с localStorage из консоли</span><span class="sxs-lookup"><span data-stu-id="50fd6-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="50fd6-140">Так как вы можете запустить JavaScript в \*\*\*\* **консоли,** и так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `localStorage` консоли . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="50fd6-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="50fd6-141">Используйте **меню контекстов JavaScript** для изменения контекста JavaScript консоли, если вы хотите получить доступ к парам с ключевым значением домена, кроме отображаемой \*\*\*\* `localStorage` страницы.</span><span class="sxs-lookup"><span data-stu-id="50fd6-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="50fd6-143">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="50fd6-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="50fd6-144">Запустите выражения в консоли, как и `localStorage` в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="50fd6-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Взаимодействие с localStorage из консоли" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="50fd6-146">Взаимодействие с `localStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="50fd6-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="50fd6-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="50fd6-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="50fd6-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50fd6-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="50fd6-151">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="50fd6-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="50fd6-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="50fd6-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
