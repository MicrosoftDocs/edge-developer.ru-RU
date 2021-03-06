---
description: Проверка и изменение анимации с помощью инспектора анимации Microsoft Edge DevTools.
title: Проверка эффектов анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 742096f13179de2ad1a95dc9fa62d2bbf3d7c226
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397736"
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

# <a name="inspect-animations"></a>Проверка эффектов анимации  

Проверка и изменение анимации с помощью инспектора анимации Microsoft Edge DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   инспектор анимации  
:::image-end:::  

### <a name="summary"></a>Сводка  

*   Захват анимации, открыв инспектор анимации.  Инспектор анимации автоматически обнаруживает и сортируется анимации в группы.  
*   Проверьте анимации, замедляя каждую из них, повторив каждую из них или просматривая исходный код.  
*   Изменение анимации путем изменения времени, задержки, продолжительности или смещения ключей.  

## <a name="overview"></a>Обзор  

Инспектор анимации Microsoft Edge DevTools имеет две основные цели.  

*   Проверка анимации.  Необходимо замедлить, повторить или проверить исходный код группы анимации.  
*   Изменение анимации.  Необходимо изменить смещение времени, задержки, продолжительности или смещения ключей группы анимации.  Редактирование Безье и редактирование ключей в настоящее время не поддерживаются.  

Инспектор анимации поддерживает CSS-анимации, переходы CSS и веб-анимации.  `requestAnimationFrame` анимации в настоящее время не поддерживаются.  

### <a name="what-is-an-animation-group"></a>Что такое группа анимации?  

Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.  В настоящее время в Интернете нет реальной концепции групповой анимации, поэтому дизайнеры и разработчики движения должны составлять и время отдельных анимаций, чтобы анимации отобразить как один согласованный визуальный эффект.  Инспектор анимации предсказывает, какие анимации связаны в зависимости от времени начала \(за исключением задержек и так далее\).  Инспектор анимации также группит анимации бок о бок.  
Другими словами, набор анимаций, которые запускаются в одном блоке скриптов, сгруппирован вместе.  Если анимация асинхронна, она помещается в отдельную группу.  

## <a name="get-started"></a>Начало работы  

Существует два способа открыть инспектор анимации:  

*   Откройте меню **Customize and Control DevTools**  
    1.  Перейдите в **подмену Дополнительные** средства.  
    1.  Выбор **анимаций:**  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Анимации с помощью основного меню" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Анимации** с помощью основного меню  
    :::image-end:::  
        
*   Откройте **меню команд**  
    1.  Введите `Drawer: Show Animations`.  

Инспектор анимации открывается рядом с **консольным средством.**  Так как инспектор анимации является средством ящика, вы можете использовать инспектор анимации из любой панели DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Инспектор пустой анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Инспектор пустой анимации  
:::image-end:::  

Инспектор анимации сгруппируется в четыре основных раздела \(или panes\).  Это руководство ссылается на каждую области следующим образом:  

| Индекс | Панель | Описание |  
|:--- |:--- |:--- |  
| 1 | **Элементы управления** | Отсюда можно очистить все захваченные в настоящее время группы анимации или изменить скорость выбранной в настоящее время группы анимации. |  
| 2 | **Обзор** | Выберите группу анимации здесь, чтобы проверить и изменить ее в области **Подробности.** |  
| 3 | **Информация о сроках** | Приостановка и запуск анимации отсюда или переход к определенной точке анимации. |  
| 4 | **Сведения** | Проверка и изменение выбранной в настоящее время группы анимации. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Аннотированный инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Аннотированный инспектор анимации  
:::image-end:::  

Чтобы захватить анимацию, просто выполните взаимодействие, которое запускает анимацию, пока инспектор анимации открыт.  Если анимация запускается на странице, обновите страницу с помощью инспектора анимации, открываемой для обнаружения анимации.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a>Проверка эффектов анимации  

После захвата анимации существует несколько способов ее воспроизведения:  

*   Наведите курсор на эскиз в области **Обзор,** чтобы просмотреть его предварительный просмотр.  
*   Выберите группу анимации из области **Обзор** \(так, **** чтобы она отображалась в области Details\) и выберите значок **повтора** \( значок ![ воспроизведения ][ImageReplayButtonIcon] \).  Анимация повторяется в представлении.  Выберите **значки** скорости анимации \( значки скорости анимации\) для изменения скорости предварительного просмотра выбранной в настоящее время ![ ][ImageAnimationSpeedButtonsIcon] группы анимации.  Для изменения текущего положения можно использовать красную вертикальную планку.  
*   Выберите и перетащите красную вертикальную планку для очистки анимации представления.  
    
### <a name="view-animation-details"></a>Просмотр сведений о анимации  

После захвата группы анимации выберите на ней из области **Обзор,** чтобы просмотреть сведения.  В области **Details** каждой отдельной анимации назначена строка.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Сведения о группе анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Сведения о группе анимации  
:::image-end:::  

Наведите курсор анимации, чтобы выделить ее в представлении.  Выберите анимацию, чтобы выбрать ее в **инструменте Elements.**  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Наведите курсор анимации, чтобы выделить ее в представлении" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Наведите курсор анимации, чтобы выделить ее в представлении  
:::image-end:::  

Левый, более темный раздел анимации — это определение.  Правый, более увядаемый раздел представляет итерации.  Например, на следующем рисунке разделы 2 и 3 представляют итерации раздела 1.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Схема итерации анимации" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Схема итерации анимации  
:::image-end:::  

Если в двух элементах применена та же анимация, инспектор анимации назначает элементам один и тот же цвет.  Цвет случайный и не имеет значения.  Например, на следующей фигуре применяются два элемента с одинаковой анимацией `div.cwccw.earlier` `div.cwccw.later` `spinrightleft` \( \) как и `div.ccwcw.earlier` `div.ccwcw.later` элементы.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Цветные анимации" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Цветные анимации  
:::image-end:::  

## <a name="modify-animations"></a>Изменение анимации  

Существует три способа изменения анимации с помощью инспектора анимации.  

*   Продолжительность анимации.  
*   Сроки keyframe.  
*   Задержка во времени начала.  
    
На следующем рисунке представлена оригинальная анимация.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Оригинальная анимация перед изменением" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Оригинальная анимация перед изменением  
:::image-end:::  

Чтобы изменить продолжительность анимации, выберите и перетащите первый или последний круг.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Измененная продолжительность" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Измененная продолжительность  
:::image-end:::  

Если анимация определяет какие-либо правила keyframe, то они представляются белыми внутренними кругами.  Выберите и перетащите один из них, чтобы изменить сроки ключевых рамок.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Измененный keyframe" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Измененный keyframe  
:::image-end:::  

Чтобы добавить задержку в анимацию, выберите и перетащите ее в любом месте, кроме кругов.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Измененная задержка" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Измененная задержка  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
