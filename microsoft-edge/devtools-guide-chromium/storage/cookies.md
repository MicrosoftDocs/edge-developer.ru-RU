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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a>Просмотр, редактирование и удаление файлов cookie с помощью Microsoft Edge DevTools  

[Файлы cookie http][MDNHTTPCookies] используются в основном для управления сеансами пользователей, хранения предпочтений по персонализации пользователей и отслеживания поведения пользователей.  Файлы cookie также являются причиной всех раздражающих на этой странице форм согласия **cookies,** которые находятся в Интернете.  В следующем руководстве рассказывается о просмотре, редактировании и удалении файлов cookie http для веб-страницы с [помощью Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

## <a name="open-the-cookies-pane"></a>Откройте области cookies  

1.  [Откройте DevTools][DevToolsOpen].  
1.  Выберите **вкладку Application** для открытия панели **приложения.**  Должна **открыться** области Манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Рис. 1. Области манифеста  
    :::image-end:::  

1.  В **статье Хранилище** **расширяют файлы Cookie,** а затем выберите источник.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="Области cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Рис. 2. Области cookies  
    :::image-end:::  

## <a name="fields"></a>Поля  

Таблица **Cookies** содержит следующие поля.  

*   **Имя**.  Имя файла cookie.  
*   **Значение**.  Значение файла cookie.  
*   **Домен**.  Хосты, которые могут получать файлы cookie.  Перейдите [к области cookie.][MDNHTTPCookiesScope]  
*   **Путь**.  URL-адрес, который должен существовать в запрашиваемом URL-адресе для отправки `Cookie` загона.  Перейдите [к области cookie.][MDNHTTPCookiesScope]  
*   **Истекает / Max-Age**.  Срок действия или максимальный возраст файла cookie.  Перейдите к [постоянным файлам cookie.][MDNHTTPCookiesPermanent]  Для [файлов cookie сеанса][MDNHTTPCookiesSession] это значение всегда `Session` .  
*   **Размер**.  Размер файла cookie в bytes.  
*   **HTTP**.  Если это поле верно, это поле указывает на то, что файлы cookie должны использоваться только для http и javaScript.  Перейдите к [файлам cookie HttpOnly][MDNHTTPCookiesSecure].  
*   **Secure**.  Если это поле верно, это поле указывает на то, что файл cookie должен быть отправлен на сервер только по безопасному подключению HTTPS.  Перейдите к [безопасному файлу cookie.][MDNHTTPCookiesSecure]  
*   **SameSite**.  Содержит `strict` или если cookie использует `lax` экспериментальный атрибут [Samesite.][MDNHTTPCookiesSamesite]  
*   **Приоритет**.  Содержит `low` , `medium` \(по умолчанию\), или если cookie использует атрибут `high` [приоритета cookie.][ChromiumIssue232693]

## <a name="filter-cookies"></a>Фильтрация файлов cookie  

Используйте **текстовое** поле Filter для фильтрации файлов cookie по **имени** или **значению**.  Фильтрация другими полями не поддерживается.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Фильтрация файлов cookie, не содержащих текстовый ID" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Рис. 3. Фильтрация файлов cookie, не содержащих текст `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a>Изменение файла cookie  

**Имена,** **значение,** **домен,** **путь**и **истекает / Max-Age** поля являются редактируемыми.  
Дважды щелкните поле, чтобы изменить его.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Настройка имени cookie в DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Рис. 4. Настройка имени файла cookie `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a>Удаление файлов cookie  

Выберите файл cookie и выберите **Delete Selected** \( ![ Delete Selected \) для удаления ](../media/delete-icon.msft.png) определенного файла cookie.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Удаление определенного файла cookie" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Рис. 5. Удаление определенного файла cookie  
:::image-end:::  

Выберите **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \) для удаления всех файлов cookie.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Очистка всех файлов cookie" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Рис. 6. Очистка всех файлов cookie  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
