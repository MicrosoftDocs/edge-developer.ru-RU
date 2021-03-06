---
description: В этом руководстве представлен обзор компонентов и стандартов разработчика, включенных в EdgeHTML 16.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399199"
---
# <a name="whats-new-in-edgehtml-16"></a>Новые возможности в EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот список новых и обновленных функций, отправляемых на веб-платформе [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) в рамках обновления Создатели падения [Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Сборка 16299\).  Изменения в определенных сборках предварительного просмотра предварительной версии Windows см. в [веб-сайте Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](../whats-new.md)  

Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## <a name="new-and-updated-features"></a>Новые и обновленные функции  

### <a name="css-grid-layout"></a>Макет сетки CSS  

Microsoft Edge теперь поддерживает неоконченную реализацию [макета сетки CSS.](https://www.w3.org/TR/css-grid-1)  [Схема сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двухмерную систему макета на основе сетки, которая обеспечивает больше плавности макета, чем это возможно, при расположении с помощью поплавков или скриптов.  В приведенной ниже примере используется схема сетки CSS для создания структуры базовой веб-страницы.  

<iframe height='303' scrolling='no' title='Макет сетки CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. макет <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетки Pen CSS </a> от MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> CodePen </a> .</iframe>  

### <a name="css-object-fit-and-object-position"></a>Объектная и объектная позиция CSS  

EdgeHTML 16 представляет поддержку свойств CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) и [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Эти свойства контролируют положение и размер замененного контента в поле контента.  

### <a name="developer-tools"></a>Средства разработчика  

В этом выпуске мы начали основные усилия по рефакторингу Microsoft Edge DevTools для повышения надежности и производительности, а также добавили кучу новых функций, которые можно начать использовать сегодня в сборках [Windows Insider.](https://insider.windows.com)  Дополнительные новости о том, что изменилось, ознакомьтесь с руководством Microsoft [Edge DevTools!](../whats-new.md)  

### <a name="javascript"></a>JavaScript  

[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) строится на оптимизации производительности Javascript предыдущих выпусков, расширяя возможности двигателя Chakra для отсрочки или повторного отодвигания функций, использования многоморфных кэшей и оптимизации функций с помощью `try` / `finally` блоков.  

Кроме того, функции, которые впервые были предварительно предварительно представлены в EdgeHTML 15, теперь стабильны и включены по умолчанию:  

#### <a name="new-features"></a>Новые возможности  

Включено по умолчанию  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([демонстрация](https://webassembly.org/demo)\)  
*   [Общая память и атомы](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a>API запроса оплаты  

API [запроса](../windows-integration/payment-request-api.md) платежей — это открытый меж браузерный стандарт, который позволяет браузерам выступать в качестве посредника между продавцами, потребителями и методами оплаты \(например, кредитными картами\), которые потребители хранят в облаке.  API в EdgeHTML 16 был обновлен в соответствии с последней спецификацией API запроса [платежей](https://w3c.github.io/payment-request) W3C.  К ним относятся:  

*   Поддержка `canMakePayment()` метода  
*   Поддержка `requestId` свойства  
*   Поддержка `id` свойства  
*   Значение по умолчанию для `complete()` параметра `result` метода изменено с "" на "неизвестный"  

### <a name="service-workers"></a>Служебные сценарии  

[Сотрудники служб](https://www.w3.org/TR/service-workers-1) — это сценарии, управляемые событиями, которые работают на фоне веб-страницы.  Сотрудники службы обеспечивают функции, ранее доступные только с помощью локальных приложений, таких как перехват и обработка запросов из сети, управление и обработка фоновой синхронизации, локальное хранилище и push-уведомления.  Поддержка для сотрудника службы по-прежнему находится в разработке, но вы можете проверить свою PWA в Microsoft Edge с помощью нашей экспериментальной поддержки сотрудника службы, включив функцию работника службы `about:flags` в .  

### <a name="webvr"></a>WebVR  

WebVR для Microsoft Edge добавил поддержку [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Эти контроллеры имеют точное положение в пространстве, позволяя тонко взаимодействовать с цифровыми объектами в виртуальной реальности.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры движения" lightbox="../media/MotionControllers.jpg":::
   Контроллеры движения  
:::image-end:::  

Веб-видеорегистратор также оптимизирован для поддержки двух различных типов работы.  

**Компьютеры смешанной реальности** Windows — настольные компьютеры и ноутбуки с интегрированной графикой.  При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со 60 кадрами в секунду.  
**Windows Mixed Reality Ultra PCs** — настольные компьютеры и ноутбуки с дискретной графикой.  При подключении к этим устройствам наши иммерсивные гарнитуры будут работать со 90 кадрами в секунду.  

Обе установки будут поддерживать один и тот же захватывающий видео и игровой опыт.  

Дополнительные сведения о предстоящих обновлениях смешанной реальности Windows вы можете узнать в блоге блога [обновления windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Для руководств и демонстраций перенахлопайся в Руководство по разработчику [Веб-видеорегистратора.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Так как спецификация WebVR еще находится в разработке, реализация Microsoft Edge может измениться позже.  

## <a name="new-apis-in-edgehtml-16"></a>Новые API в EdgeHTML 16  

Полный список новых API в EdgeHTML 16.  Они перечислены в формате `[interface name].[api name]` .

> [!NOTE] 
> Несмотря на то, что следующие API выставлены в DOM, поведение некоторых из них по-прежнему находится в разработке.  Обратитесь [к статусу платформы Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) для официального слова о поддержке функций.  

---  

<iframe height='559' scrolling='no' title='Новые API в EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>См. новые <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> API pen в EdgeHTML 16 </a> msEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## <a name="previous-edgehtml-releases"></a>Предыдущие выпуски EdgeHTML  

[EdgeHTML 12 / Windows build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Windows build 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Сборка Windows 15063 (4/2017)](./edgehtml-15.md)  
