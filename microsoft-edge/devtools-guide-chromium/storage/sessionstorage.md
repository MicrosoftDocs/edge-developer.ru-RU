---
description: Просмотр и изменение sessionStorage с помощью области хранилища сеансов и консоли.
title: Просмотр и изменение хранилища сеансов с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e31e45abc5eac26d297cd9bc9fca43778dd74300
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231197"
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

# Просмотр и изменение хранилища сеансов с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления пар ["ключ-значение" sessionStorage.][MDNSessionStorage]  

## Просмотр ключей и значений sessionStorage  

1.  Откройте средство **"Приложение"** на вкладке **"Приложение".**  По **умолчанию** отображается области манифеста.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       The **Manifest** pane  
    :::image-end:::  
    
1.  Разорите **меню "Хранилище** сеансов".  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Меню хранилища сеансов" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Меню **хранилища сеансов**  
    :::image-end:::  
    
1.  Выберите домен для просмотра пар "ключ-значение".  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Пары ключ-значение sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Пары `sessionStorage` "ключ-значение"  
    :::image-end:::  
    
1.  Выберите строку таблицы, чтобы просмотреть значение в представлении под таблицей.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Просмотр значения ключа X-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Просмотр значения `x-sid` ключа  
    :::image-end:::  
    
## Создание новой пары "ключ-значение" sessionStorage  

1.  [Просмотр пар "ключ-значение" sessionStorage домена.](#view-sessionstorage-keys-and-values)  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и фокусирует курсор в **столбце "Ключ".**  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Пустая часть таблицы, которая дважды щелкает, чтобы создать новую пару ключ-значение." lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Пустая часть таблицы, которая дважды щелкает, чтобы создать новую пару "ключ-значение".  
    :::image-end:::  
    
## Изменение ключей или значений sessionStorage  

1.  [Просмотр пар "ключ-значение" sessionStorage домена.](#view-sessionstorage-keys-and-values)  
1.  Дважды щелкните ячейку в столбце **"Ключ"** или **"Значение",** чтобы изменить этот ключ или значение.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Изменение ключа sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Изменение `sessionStorage` ключа  
    :::image-end:::  
    
## Удаление пар "ключ-значение" sessionStorage  

1.  [Просмотр пар `sessionStorage` "ключ-значение" домена.](#view-sessionstorage-keys-and-values)  
1.  Выберите пару "ключ-значение", которую нужно удалить.  DevTools выделяет его синим цветом, чтобы показать, что он выбран.  
1.  Select the `Delete` key or choose Delete **Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).  
    
## Удаление всех пар "ключ-значение sessionStorage" для домена  

1.  [Просмотр пар `sessionStorage` "ключ-значение" домена.](#view-sessionstorage-keys-and-values)  
1.  Choose **Clear All** \( Clear All ![ ][ImageClearIcon] \).  
    
## Взаимодействие с sessionStorage из консоли  

Так как вы можете запустить JavaScript **** в **консоли,** а так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `sessionStorage` **консолью.**  

1.  Используйте **контекстное меню JavaScript,** чтобы изменить **** контекст JavaScript консоли, если вы хотите получить доступ к парам "ключ-значение" домена, кроме страницы, на котором вы `sessionStorage` находитесь.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-domain-selection.msft.png":::
       Изменение контекста JavaScript **консоли**  
    :::image-end:::  
    
1.  Запустите выражения в консоли так же, как и в `sessionStorage` JavaScript. ****  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Взаимодействие с sessionStorage из консоли" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Взаимодействие с `sessionStorage` **консолью**  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
