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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a>Просмотр и редактирование локального хранилища с помощью Microsoft Edge DevTools  

В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, редактирования и удаления пар [ключей localStorage.][MDNWindowsLocalStorage]  

## <a name="view-localstorage-keys-and-values"></a>Просмотр ключей и значений localStorage  

1.  Выберите **вкладку Приложение,** чтобы открыть **средство** приложения.  По умолчанию отображается области **Манифеста.**  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       Области **Манифест**  
    :::image-end:::  
    
1.  **Расширь меню локального** хранения.  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Меню локального хранения" lightbox="../media/storage-application-local-storage.msft.png":::
       Меню **локального** хранения  
    :::image-end:::  
    
1.  Выберите домен для просмотра пар с ключевым значением.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Пары ключей localStorage для https://www.bing.com домена" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Пары `localStorage` значений ключа для `https://www.bing.com` домена  
    :::image-end:::  
    
1.  Выберите строку таблицы, чтобы просмотреть значение в представлении ниже таблицы.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Просмотр значения клавиши eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Просмотр значения `eventLogQueue_Online` ключа  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a>Создание новой пары ключ-значение localStorage  

1.  [Просмотр пар ключ-значения localStorage домена.](#view-localstorage-keys-and-values)  
1.  Дважды щелкните пустую часть таблицы.  DevTools создает новую строку и фокусирует курсор в **столбце Ключ.**  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Пустая часть таблицы дважды щелкнуть, чтобы создать новую пару значений ключа  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a>Изменение ключей или значений localStorage  

1.  [Просмотр пар ключ-значения localStorage домена.](#view-localstorage-keys-and-values)  
1.  Дважды щелкните ячейку в столбце **Ключ** или **Значение,** чтобы изменить этот ключ или значение.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Изменение ключа localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Изменение `localStorage` ключа  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a>Удаление пар ключ-значения localStorage  

1.  [Просмотр `localStorage` пар значений ключа домена](#view-localstorage-keys-and-values).  
1.  Выберите пару с значением ключа, которую необходимо удалить.  DevTools выделяет его синим цветом, чтобы указать, что он выбран.  
1.  Выберите ключ `Delete` или выберите **Удалить выбранный** \. ![ Удалить выбранный ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a>Удаление всех `localStorage` пар значений ключа для домена  

1.  [Просмотр `localStorage` пар значений ключа домена](#view-localstorage-keys-and-values).  
1.  Выберите **Clear All** \( Clear All ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-localstorage-from-the-console"></a>Взаимодействие с localStorage из консоли  

Так как вы можете запустить JavaScript в **** **консоли,** и так как консоль имеет доступ к контекстам JavaScript страницы, можно взаимодействовать с `localStorage` консоли . ****  

1.  Используйте **меню контекстов JavaScript** для изменения контекста JavaScript консоли, если вы хотите получить доступ к парам с ключевым значением домена, кроме отображаемой **** `localStorage` страницы.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-local-storage.msft.png":::
       Изменение контекста JavaScript консоли  
    :::image-end:::  
    
1.  Запустите выражения в консоли, как и `localStorage` в JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Взаимодействие с localStorage из консоли" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Взаимодействие с `localStorage` **консолью**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
