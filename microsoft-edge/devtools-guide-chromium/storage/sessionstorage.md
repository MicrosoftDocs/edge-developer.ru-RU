---
description: Просмотр и редактирование сеансовStorage с помощью области хранения сеансов и консоли.
title: Просмотр и редактирование хранилища сеансов с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: cf00d71302e7a1f16ba1cceaa17c9380245d12f8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398009"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="82769-104">Просмотр и редактирование хранилища сеансов с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="82769-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="82769-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, редактирования и удаления пар ключей-значений [sessionStorage.][MDNSessionStorage]</span><span class="sxs-lookup"><span data-stu-id="82769-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [sessionStorage][MDNSessionStorage] key-value pairs.</span></span>  

## <a name="view-sessionstorage-keys-and-values"></a><span data-ttu-id="82769-106">Просмотр клавиш и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="82769-106">View sessionStorage keys and values</span></span>  

1.  <span data-ttu-id="82769-107">Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.</span><span class="sxs-lookup"><span data-stu-id="82769-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="82769-108">Панель **Manifest** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82769-108">The **Manifest** panel is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="82769-110">Области **Манифест**</span><span class="sxs-lookup"><span data-stu-id="82769-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82769-111">Расширь **меню хранилища сеансов.**</span><span class="sxs-lookup"><span data-stu-id="82769-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Меню хранения сеансов" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="82769-113">Меню **хранения сеансов**</span><span class="sxs-lookup"><span data-stu-id="82769-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82769-114">Выберите домен для просмотра пар с ключевым значением.</span><span class="sxs-lookup"><span data-stu-id="82769-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Пары ключ-значение sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="82769-116">Пары `sessionStorage` значений ключа</span><span class="sxs-lookup"><span data-stu-id="82769-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82769-117">Выберите строку таблицы, чтобы просмотреть значение в представлении ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="82769-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Просмотр значения ключа x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="82769-119">Просмотр значения `x-sid` ключа</span><span class="sxs-lookup"><span data-stu-id="82769-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a><span data-ttu-id="82769-120">Создание пары ключ-значение sessionStorage</span><span class="sxs-lookup"><span data-stu-id="82769-120">Create a new sessionStorage key-value pair</span></span>  

1.  <span data-ttu-id="82769-121">[Просмотр пар значений для ключей sessionStorage домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="82769-121">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="82769-122">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="82769-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="82769-123">DevTools создает новую строку и фокусирует курсор в **столбце Ключ.**</span><span class="sxs-lookup"><span data-stu-id="82769-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="82769-125">Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа</span><span class="sxs-lookup"><span data-stu-id="82769-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a><span data-ttu-id="82769-126">Изменение клавиш и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="82769-126">Edit sessionStorage keys or values</span></span>  

1.  <span data-ttu-id="82769-127">[Просмотр пар значений для ключей sessionStorage домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="82769-127">[View the sessionStorage key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="82769-128">Дважды щелкните ячейку в столбце **Ключ** или **Значение,** чтобы изменить этот ключ или значение.</span><span class="sxs-lookup"><span data-stu-id="82769-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Изменение ключа sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="82769-130">Изменение `sessionStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="82769-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a><span data-ttu-id="82769-131">Удаление пар ключ-значения sessionStorage</span><span class="sxs-lookup"><span data-stu-id="82769-131">Delete sessionStorage key-value pairs</span></span>  

1.  <span data-ttu-id="82769-132">[Просмотр `sessionStorage` пар значений ключа домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="82769-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="82769-133">Выберите пару с значением ключа, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="82769-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="82769-134">DevTools выделяет его синим цветом, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="82769-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="82769-135">Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="82769-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="82769-136">Удаление всех пар ключей sessionStorage для домена</span><span class="sxs-lookup"><span data-stu-id="82769-136">Delete all sessionStorage key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="82769-137">[Просмотр `sessionStorage` пар значений ключа домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="82769-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="82769-138">Выберите **Clear All** \( Clear All ![ ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="82769-138">Choose **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <a name="interact-with-sessionstorage-from-the-console"></a><span data-ttu-id="82769-139">Взаимодействие с sessionStorage из консоли</span><span class="sxs-lookup"><span data-stu-id="82769-139">Interact with sessionStorage from the Console</span></span>  

<span data-ttu-id="82769-140">Так как вы можете запустить JavaScript \*\*\*\* в **консоли,** и так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `sessionStorage` консоли . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="82769-140">Since you may run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="82769-141">Используйте **меню контекстов JavaScript,** чтобы изменить \*\*\*\* контекст JavaScript консоли, если вы хотите получить доступ к парам с ключевым значением домена, кроме страницы, на котором `sessionStorage` вы находитесь.</span><span class="sxs-lookup"><span data-stu-id="82769-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="82769-143">Изменение контекста JavaScript **консоли**</span><span class="sxs-lookup"><span data-stu-id="82769-143">Change the JavaScript context of the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="82769-144">Запустите `sessionStorage` выражения в **консоли**, так же, как и javaScript.</span><span class="sxs-lookup"><span data-stu-id="82769-144">Run your `sessionStorage` expressions in the **Console**, the same as your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Взаимодействие с sessionStorage из консоли" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="82769-146">Взаимодействие с `sessionStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="82769-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="82769-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="82769-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="82769-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82769-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="82769-151">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="82769-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="82769-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="82769-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
