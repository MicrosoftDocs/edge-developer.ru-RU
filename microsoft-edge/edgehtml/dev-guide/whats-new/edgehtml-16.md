---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: В этом руководстве представлен обзор новых функций и API в EdgeHTML 16.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7697114546153555d947903eda6bf8477cca3516
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235467"
---
# Новые возможности EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот список новых и обновленных функций, которые поставляются в веб-платформе [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) в составе [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, сборка 16299\).  Изменения в конкретных сборках Windows Insider Preview см. в записях microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](../whats-new.md)  

Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## Новые и обновленные функции  

### Макет сетки CSS  

Microsoft Edge теперь поддерживает реализацию макета [сетки CSS](https://www.w3.org/TR/css-grid-1)без префикса.  [Макет сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двухмерную систему макета на основе сетки, которая обеспечивает более плавность макета, чем это возможно, при расположении с помощью с плавающей заместки или сценариев.  В примере ниже для создания структуры для базовой веб-страницы используется макет сетки CSS.  

<iframe height='303' scrolling='no' title='Макет сетки CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. макет <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетки CSS пера </a> от MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>  

### CSS object-fit and object-position  

EdgeHTML 16 поддерживает свойства CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) и [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Эти свойства контролируют положение и размер замененного содержимого в поле содержимого.  

### Средства разработчика  

В этом выпуске мы начали основные усилия по рефакторингу Microsoft Edge DevTools для повышения надежности и производительности, а также добавили ряд новых функций, которые вы можете начать использовать уже сегодня в сборках для программы [insider Для Windows.](https://insider.windows.com)  Подробнее об изменениях можно узнать в руководстве По разработке для [Microsoft Edge.](../whats-new.md)  

### JavaScript  

[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) строится на оптимизации производительности JavaScript предыдущих выпусков, расширяя возможность ядра Chakra откладывать или повторно откладывать функции, использовать многоморфные кэши и оптимизировать функции с помощью `try` / `finally` блоков.  

Кроме того, функции, которые были предварительно представлены в EdgeHTML 15, теперь стабильны и включены по умолчанию:  

#### Новые возможности  

Включено по умолчанию  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)  
*   [Общая память и атомарные](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### API запроса оплаты  

[API](../windows-integration/payment-request-api.md) запроса платежей — это открытый кросс браузерный стандарт, который позволяет браузерам действовать в качестве посредника между продавцами, потребителями и методами оплаты (например, кредитными картами),которые потребители хранили в облаке.  API в EdgeHTML 16 обновлен в соответствии с последней спецификацией [API](https://w3c.github.io/payment-request) запроса платежей W3C.  К ним относятся:  

*   Поддержка `canMakePayment()` метода  
*   Поддержка `requestId` свойства  
*   Поддержка `id` свойства  
*   Значение по умолчанию для параметра метода `complete()` `result` изменилось с " " на "unknown"  

### Служебные сценарии  

[Service Workers](https://www.w3.org/TR/service-workers-1) — это сценарии на основе событий, которые запускаются в фоновом режиме веб-страницы.  Сотрудники службы обеспечивают функции, которые ранее были доступны только в таких приложениях, как перехват и обработка запросов из сети, управление фоновой синхронизацией, локальное хранилище и push-уведомления.  Поддержка сотрудников службы еще находится на стадии разработки, но вы можете протестировать PWA в Microsoft Edge с помощью нашей экспериментальной поддержки рабочих служб, включив в нее функцию работы `about:flags` службы.  

### WebVR  

WebVR для Microsoft Edge добавлена поддержка [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Эти контроллеры имеют точное положение в пространстве, позволяя точно взаимодействовать с цифровыми объектами в виртуальной реальности.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры движения" lightbox="../media/MotionControllers.jpg":::
   Контроллеры движения  
:::image-end:::  

WebVR также был оптимизирован для поддержки двух различных типов работы.  

**Компьютеры Windows Mixed Reality** — настольные компьютеры и ноутбуки со встроенной графикой.  При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со частотой 60 кадров в секунду.  
**Компьютеры Windows Mixed Reality—** настольные компьютеры и ноутбуки с дискретной графикой.  При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со частотой 90 кадров в секунду.  

Обе программы установки поддерживают одно и то же иммерсивное видео и игровое время.  

Дополнительные сведения о предстоящих обновлениях Windows Mixed Reality можно узнать в записи блога об обновлении праздников [Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Руководства и демонстрации можно найти в руководстве разработчика [WebVR.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Так как спецификация WebVR еще находится в разработке, реализация Microsoft Edge может измениться позже.  

## Новые API в EdgeHTML 16  

Ниже полный список новых API в EdgeHTML 16.  Они перечислены в формате `[interface name].[api name]` .

> [!NOTE] 
> Несмотря на то что в модели DOM есть следующие API, все еще возможно, что некоторые из них находятся в разработке.  Официальное слово о поддержке функций можно найти в статусе платформы [Microsoft Edge.](https://developer.microsoft.com/microsoft-edge/platform/status)  

---  

<iframe height='559' scrolling='no' title='Новые API в EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. API-код для новых перьев в <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> EdgeHTML 16 от </a> MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>  

---  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 12 / Сборка Windows 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Сборка Windows 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Сборка Windows 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Сборка Windows 15063 (4/2017)](./edgehtml-15.md)  
