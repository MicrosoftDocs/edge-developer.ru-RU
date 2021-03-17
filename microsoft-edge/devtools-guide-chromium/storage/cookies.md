---
description: Узнайте, как просматривать, изменять и удалять файлы cookie http для страницы с помощью Microsoft Edge DevTools.
title: Просмотр, редактирование и удаление файлов cookie с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439684"
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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a><span data-ttu-id="677de-104">Просмотр, редактирование и удаление файлов cookie с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="677de-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="677de-105">[Файлы cookie http][MDNHTTPCookies] используются в основном для управления сеансами пользователей, хранения предпочтений по персонализации пользователей и отслеживания поведения пользователей.</span><span class="sxs-lookup"><span data-stu-id="677de-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="677de-106">Файлы cookie также являются причиной всех раздражающих на этой странице форм согласия **cookies,** которые находятся в Интернете.</span><span class="sxs-lookup"><span data-stu-id="677de-106">Cookies are also the cause of all of the annoying **this page uses cookies** consent forms that are found across the web.</span></span>  <span data-ttu-id="677de-107">В следующем руководстве рассказывается о просмотре, редактировании и удалении файлов cookie http для веб-страницы с [помощью Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="677de-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a webpage with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-the-cookies-pane"></a><span data-ttu-id="677de-108">Откройте области cookies</span><span class="sxs-lookup"><span data-stu-id="677de-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="677de-109">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="677de-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="677de-110">Выберите **вкладку Application** для открытия панели **приложения.**</span><span class="sxs-lookup"><span data-stu-id="677de-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="677de-111">Должна **открыться** области Манифеста.</span><span class="sxs-lookup"><span data-stu-id="677de-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="677de-113">Рис. 1. Области манифеста</span><span class="sxs-lookup"><span data-stu-id="677de-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="677de-114">В **статье Хранилище** **расширяют файлы Cookie,** а затем выберите источник.</span><span class="sxs-lookup"><span data-stu-id="677de-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Области cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="677de-116">Рис. 2. Области cookies</span><span class="sxs-lookup"><span data-stu-id="677de-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <a name="fields"></a><span data-ttu-id="677de-117">Поля</span><span class="sxs-lookup"><span data-stu-id="677de-117">Fields</span></span>  

<span data-ttu-id="677de-118">Таблица **Cookies** содержит следующие поля.</span><span class="sxs-lookup"><span data-stu-id="677de-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="677de-119">**Имя**.</span><span class="sxs-lookup"><span data-stu-id="677de-119">**Name**.</span></span>  <span data-ttu-id="677de-120">Имя файла cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="677de-121">**Значение**.</span><span class="sxs-lookup"><span data-stu-id="677de-121">**Value**.</span></span>  <span data-ttu-id="677de-122">Значение файла cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="677de-123">**Домен**.</span><span class="sxs-lookup"><span data-stu-id="677de-123">**Domain**.</span></span>  <span data-ttu-id="677de-124">Хосты, которые могут получать файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="677de-125">Перейдите [к области cookie.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="677de-125">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="677de-126">**Путь**.</span><span class="sxs-lookup"><span data-stu-id="677de-126">**Path**.</span></span>  <span data-ttu-id="677de-127">URL-адрес, который должен существовать в запрашиваемом URL-адресе для отправки `Cookie` загона.</span><span class="sxs-lookup"><span data-stu-id="677de-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="677de-128">Перейдите [к области cookie.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="677de-128">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="677de-129">**Истекает / Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="677de-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="677de-130">Срок действия или максимальный возраст файла cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="677de-131">Перейдите к [постоянным файлам cookie.][MDNHTTPCookiesPermanent]</span><span class="sxs-lookup"><span data-stu-id="677de-131">Navigate to [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="677de-132">Для [файлов cookie сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .</span><span class="sxs-lookup"><span data-stu-id="677de-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="677de-133">**Размер**.</span><span class="sxs-lookup"><span data-stu-id="677de-133">**Size**.</span></span>  <span data-ttu-id="677de-134">Размер файла cookie в bytes.</span><span class="sxs-lookup"><span data-stu-id="677de-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="677de-135">**HTTP**.</span><span class="sxs-lookup"><span data-stu-id="677de-135">**HTTP**.</span></span>  <span data-ttu-id="677de-136">Если это поле верно, это поле указывает на то, что файлы cookie должны использоваться только для http и javaScript.</span><span class="sxs-lookup"><span data-stu-id="677de-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="677de-137">Перейдите к [файлам cookie HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="677de-137">Navigate to [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="677de-138">**Secure**.</span><span class="sxs-lookup"><span data-stu-id="677de-138">**Secure**.</span></span>  <span data-ttu-id="677de-139">Если это поле верно, это поле указывает на то, что файл cookie должен быть отправлен на сервер только по безопасному подключению HTTPS.</span><span class="sxs-lookup"><span data-stu-id="677de-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="677de-140">Перейдите к [безопасному файлу cookie.][MDNHTTPCookiesSecure]</span><span class="sxs-lookup"><span data-stu-id="677de-140">Navigate to [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="677de-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="677de-141">**SameSite**.</span></span>  <span data-ttu-id="677de-142">Содержит `strict` или если cookie использует `lax` экспериментальный атрибут [Samesite.][MDNHTTPCookiesSamesite]</span><span class="sxs-lookup"><span data-stu-id="677de-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="677de-143">**Приоритет**.</span><span class="sxs-lookup"><span data-stu-id="677de-143">**Priority**.</span></span>  <span data-ttu-id="677de-144">Содержит `low` , `medium` \(по умолчанию\), или если cookie использует атрибут `high` [приоритета cookie.][ChromiumIssue232693]</span><span class="sxs-lookup"><span data-stu-id="677de-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <a name="filter-cookies"></a><span data-ttu-id="677de-145">Фильтрация файлов cookie</span><span class="sxs-lookup"><span data-stu-id="677de-145">Filter cookies</span></span>  

<span data-ttu-id="677de-146">Используйте **текстовое** поле Filter для фильтрации файлов cookie по **имени** или **значению**.</span><span class="sxs-lookup"><span data-stu-id="677de-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="677de-147">Фильтрация другими полями не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="677de-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Фильтрация файлов cookie, не содержащих текстовый ID" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="677de-149">Рис. 3. Фильтрация файлов cookie, не содержащих текст</span><span class="sxs-lookup"><span data-stu-id="677de-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a><span data-ttu-id="677de-150">Изменение файла cookie</span><span class="sxs-lookup"><span data-stu-id="677de-150">Edit a cookie</span></span>  

<span data-ttu-id="677de-151">**Имена,** **значение,** **домен,** **путь**и **истекает / Max-Age** поля являются редактируемыми.</span><span class="sxs-lookup"><span data-stu-id="677de-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="677de-152">Дважды щелкните поле, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="677de-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Настройка имени cookie в DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="677de-154">Рис. 4. Настройка имени файла cookie</span><span class="sxs-lookup"><span data-stu-id="677de-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a><span data-ttu-id="677de-155">Удаление файлов cookie</span><span class="sxs-lookup"><span data-stu-id="677de-155">Delete cookies</span></span>  

<span data-ttu-id="677de-156">Выберите файл cookie и выберите **Delete Selected** \( ![ Delete Selected \) для удаления ](../media/delete-icon.msft.png) определенного файла cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-156">Choose a cookie and choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\) to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Удаление определенного файла cookie" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="677de-158">Рис. 5. Удаление определенного файла cookie</span><span class="sxs-lookup"><span data-stu-id="677de-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="677de-159">Выберите **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \) для удаления всех файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="677de-159">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\) to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Очистка всех файлов cookie" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="677de-161">Рис. 6. Очистка всех файлов cookie</span><span class="sxs-lookup"><span data-stu-id="677de-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="677de-162">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="677de-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Откройте Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Выпуск Chromium 232693: реализация поля приоритетов для файлов cookie | Chromium Bugs"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Файлы cookie http | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Файлы cookie HTTP — постоянные файлы cookie | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Файлы cookie HTTP — файлы cookie sameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Файлы cookie HTTP — область файлов cookie | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP - Безопасные и httpOnly cookies | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Файлы cookie HTTP — файлы cookie сеанса | MDN"  

> [!NOTE]
> <span data-ttu-id="677de-172">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="677de-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="677de-173">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="677de-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="677de-175">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="677de-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
