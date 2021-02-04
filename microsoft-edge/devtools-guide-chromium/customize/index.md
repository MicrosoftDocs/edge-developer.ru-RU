---
description: Список способов настройки Microsoft Edge DevTools
title: Настройка Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/22/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5822fa087244fdfafdefe040709058411040ea45
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313025"
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

# Настройка Microsoft Edge DevTools  

На этой странице перечислены способы настройки Microsoft Edge DevTools.  

## Параметры  

**Параметры**  >  **Параметры** содержат множество параметров для настройки DevTools.  

Чтобы открыть "Параметры", выполните одно из следующих действий.  

*   Выберите, `F1` пока DevTools находится в фокусе.  
*   Откройте главное **меню и** выберите пункт **"Параметры".**  
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Параметры" lightbox="../media/customize-settings-preferences.msft.png":::
   **Параметры**  
:::image-end:::  

## Drawer  

Drawer **—** это вторая панель, на которой отображаются инструменты по вашему выбору.  

Чтобы открыть \(или закрыть\) **drawer**, выберите `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="The Drawer" lightbox="../media/customize-drawer-open.msft.png":::
   **Drawer**  
:::image-end:::  

По умолчанию некоторые средства открываются на главной панели, а другие отображаются в **средстве "Drawer".**  Choose **More** \( `...` \) to open a tool in the **Drawer**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="Кнопка для открытия drawer" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   Кнопка для открытия **drawer**  
:::image-end:::  

Можно перемещать инструменты между главной панелью и ящиком.  

*   Чтобы переместить средство из ящика на главную панель, наведите курсор на средство, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт "Переместить в **верхнюю"**.  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Перемещение средства из обоймы в основную панель" lightbox="../media/move-from-drawer.msft.png":::
       Перемещение средства из **обоймы в** основную панель  
    :::image-end:::  
    
*   Чтобы переместить средство с главной панели в ящик, наведите курсор на средство, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт "Переместить в **нижнюю часть".**  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Перемещение средства с главной панели на ящик" lightbox="../media/move-to-drawer.msft.png":::
       Перемещение средства с главной панели на **ящик**
    :::image-end:::  
    

## Переусортовка панелей  

Выберите и перетащите средство, чтобы изменить порядок.  Пользовательский порядок инструментов сохраняется в сеансах DevTools.  

> [!NOTE]
> По умолчанию средство **"Сеть"** обычно является четвертым слева.  На следующем рисунке панель **"Сеть"** является первой слева.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Настраиваемый порядок разработки на панели" lightbox="../media/customize-network-first-position.msft.png":::
   Настраиваемый порядок разработки на панели  
:::image-end:::  

## Изменение размещения DevTools  

См. ["Размещение Microsoft Edge DevTools".][DevToolsPlacement]  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="Undocked DevTools" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   Undocked DevTools  
:::image-end:::  

## Темная тема  

См. ["Включить темную тему".][DarkTheme]  

:::image type="complex" source="../media/customize-settings-appearance-theme.msft.png" alt-text="Темная тема" lightbox="../media/customize-settings-appearance-theme.msft.png":::
   Темная тема  
:::image-end:::  

## Эксперименты  

Чтобы включить эксперименты DevTools, выполните следующие действия.  

1.  Перейдите к `edge://flags/#enable-devtools-experiments` .  
1.  Choose **Enable**.  
1.  Choose **Relaunch Now**, at the bottom of the page.  

В следующий раз, когда вы откроете DevTools, в параметрах отобразится новая страница с именем ["Эксперименты".](#settings) ****  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DarkTheme]: ./dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/customize/index) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
