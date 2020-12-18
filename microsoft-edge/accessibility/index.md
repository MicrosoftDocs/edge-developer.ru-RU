---
description: Узнайте, как создавать, проектировать и тестировать доступные веб-сайты в Microsoft Edge.
title: Специальные возможности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: accessibility, accessibility for developers, accessible websites, edge, web development, ARIA, developer, UIA, UI Automation
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235278"
---
# Обзор специальных возможностей  

> "\[T\], влияние ограниченных возможностей значительно изменилось в Интернете, так как Интернет устраняет барьеры на пути к взаимодействию и взаимодействию, с которых сталкиваются многие люди в физическом мире". [(Accessibility | W3C)][W3CAccessibility]  

В [Всемирной организации здравоохранения][WHODisabilities] ограниченные возможности определяются как "несоответствие во взаимодействии между функциями тела человека и функциями среды, в которой он содержится".  Ограниченные возможности могут варьироваться от сиюмитных ограничений, таких как ограниченная мобильность при удержании детей или яркого света на телефоне, до других физических, аудиторных, визуальных или возрастных нарушений.  

Разработка веб-сайтов и других технологий для включения создает у каждого человека простое впечатление.  Инклюзивное проектирование и доступность веб-возможностей расширяют возможности и помогают всем использовать Интернет.  

Вот несколько лучших методик, примеров кода и дополнительных ресурсов, которые [][AccessibilityBuild]вы можете [][AccessibilityTest] получить, чтобы узнать больше о проектировании, [][AccessibilityDesign]создании и тестировании доступных веб-сайтов в Microsoft Edge.  

## Доступность в Microsoft Edge  

В Microsoft Edge мы представили современный [API автоматизации][WindowsWin32AutoEntryui] пользовательского интерфейса \(API UIA\).  Изменение UIA стало главной инвестицией в доступность браузера и лежит в основе более инклюзивного веб-приложения для пользователей, которые зависят от вспомогательных возможностей в Windows 10.  Пользователи также получают преимущества из-за постоянной природы поддвижки Chromium.  

Система доступности в Microsoft Edge изначально поддерживает современные веб-стандарты, включая ARIA, HTML5 и CSS3.  На следующей схеме упрощенного конвейера браузера содержимое веб-страниц передается на доступный уровень презентации.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Содержимое, преобразованное в модель обдвижки, проецируется в визуальные представления и представления с специальными специальными возможностей, представленные в качестве визуальной или доступной презентации":::
   Содержимое, преобразованное в модель обдвижки, проецируется в визуальные представления и представления с доступом, которые представлены как визуальные или доступные презентации  
:::image-end:::  

Команда Microsoft Edge постоянно работает с W3C и другими поставщиками браузеров, чтобы убедиться, что новые функции веб-платформы имеют достаточные встроенные возможности доступа.  

Сведения о том, какие новые функции HTML5 доступны в Microsoft Edge, можно найти в [htmL5Accessibility.][HTML5Accessibility]  

## Ресурсы  

#### Блог по автоматизации пользовательского интерфейса Microsoft Windows  

Блог ["Автоматизация пользовательского][ArchiveBlogsWinuiautomation] интерфейса Microsoft Windows" охватывает темы, связанные с API автоматизации Windows.  

#### Web Accessibility Initiative (WAI)  

The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.  Сайт предоставляет множество ресурсов [][W3CWaiGettingstartedOverview]для начала работы со специальными веб-ресурсами, проектирования для [включения,][W3CWaiFundamentals]учебников и [презентаций][W3CWaiTeachAdvocate]и многого другого.  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Создание доступных веб-сайтов | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Разработка доступных веб-сайтов | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Тестирование доступности | Документы Майкрософт"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Автоматизация пользовательского интерфейса | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Блог по автоматизации пользовательского интерфейса Microsoft Windows | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Доступность HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accessibility | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Введение в веб-доступность | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Начало работы: обеспечение доступности веб-сайта | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Общие сведения об обучения и адвокате | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Ограниченные возможности | WHO"  

