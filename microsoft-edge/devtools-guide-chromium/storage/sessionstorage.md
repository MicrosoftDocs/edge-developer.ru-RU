---
description: Просмотр и редактирование сеансовStorage с помощью области хранения сеансов и консоли.
title: Просмотр и редактирование хранилища сеансов с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0168b01fd01071ebd19bd211c6d947ae006d778c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439663"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a>Просмотр и редактирование хранилища сеансов с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, редактирования и удаления пар ключей-значений [sessionStorage.][MDNSessionStorage]  

## <a name="view-sessionstorage-keys-and-values"></a>Просмотр клавиш и значений sessionStorage  

1.  Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.  Панель **Manifest** отображается по умолчанию.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       Области **Манифест**  
    :::image-end:::  
    
1.  Расширь **меню хранилища сеансов.**  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Меню хранения сеансов" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Меню **хранения сеансов**  
    :::image-end:::  
    
1.  Выберите домен для просмотра пар с ключевым значением.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Пары ключ-значение sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Пары `sessionStorage` значений ключа  
    :::image-end:::  
    
1.  Выберите строку таблицы, чтобы просмотреть значение в представлении ниже таблицы.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Просмотр значения ключа x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Просмотр значения `x-sid` ключа  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a>Создание пары ключ-значение sessionStorage  

1.  [Просмотр пар значений для ключей sessionStorage домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и фокусирует курсор в **столбце Ключ.**  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a>Изменение клавиш и значений sessionStorage  

1.  [Просмотр пар значений для ключей sessionStorage домена](#view-sessionstorage-keys-and-values).  
1.  Дважды щелкните ячейку в столбце **Ключ** или **Значение,** чтобы изменить этот ключ или значение.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Изменение ключа sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Изменение `sessionStorage` ключа  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a>Удаление пар ключ-значения sessionStorage  

1.  [Просмотр `sessionStorage` пар значений ключа домена](#view-sessionstorage-keys-and-values).  
1.  Выберите пару с значением ключа, которую необходимо удалить.  DevTools выделяет его синим цветом, чтобы указать, что он выбран.  
1.  Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a>Удаление всех пар ключей sessionStorage для домена  

1.  [Просмотр `sessionStorage` пар значений ключа домена](#view-sessionstorage-keys-and-values).  
1.  Выберите **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-sessionstorage-from-the-console"></a>Взаимодействие с sessionStorage из консоли  

Так как вы можете запустить JavaScript **** в **консоли,** и так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `sessionStorage` консоли . ****  

1.  Используйте **меню контекстов JavaScript,** чтобы изменить **** контекст JavaScript консоли, если вы хотите получить доступ к парам с ключевым значением домена, кроме страницы, на котором `sessionStorage` вы находитесь.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-domain-selection.msft.png":::
       Изменение контекста JavaScript **консоли**  
    :::image-end:::  
    
1.  Запустите `sessionStorage` выражения в **консоли**, так же, как и javaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Взаимодействие с sessionStorage из консоли" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Взаимодействие с `sessionStorage` **консолью**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
