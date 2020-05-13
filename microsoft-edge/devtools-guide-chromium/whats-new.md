---
description: Функции, добавленные в Microsoft EDGE (Chromium) DevTools 2019 марта
title: Новые возможности Microsoft EDGE (Chromium) DevTools 2019 марта
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: bf1919b0ab46df378880d664dd4e59aee96605e5
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645324"
---
# Новые возможности Microsoft EDGE (Chromium) DevTools

Благодарим вас за пробную версию следующей версии Microsoft Edge! В этом выпуске мы решили крупную смену на базовой веб-платформе Microsoft EDGE, принимая проект Chromium Open Source. Благодаря этому изменению вы сможете легко создавать и тестировать веб-сайты в Microsoft EDGE и гарантировать, что они будут работать должным образом даже в том случае, если пользователи просматривают другие браузеры на базе Chromium, например Google Chrome, Vivaldi, Opera или Brave.

## Новый Microsoft EDGE (Chromium) DevTools

Если вы выйдете из Microsoft EDGE и вы в основном разрабатываете в Chromium-браузере, вам нужно прямо дома. Средства разработчика Microsoft EDGE (Chromium) в точности похожи на средства разработчика, которые вы уже знаете и используете.

![Microsoft EDGE (Chromium) DevTools](./media/devtools.png)

Если вы выйдете к следующей версии Microsoft EDGE, и вы в основном разрабатывались в Microsoft EDGE (EdgeHTML), у нас есть несколько новых инструментов, которые мы надеемся, чтобы облегчить и быстро создавать и тестировать веб-сайты в Microsoft Edge. Чтобы узнать больше об этих новых средствах, ознакомьтесь [со статьей руководство по DevTools Microsoft EDGE (Chromium)](../devtools-guide-chromium.md).

## Новые темные и легкие темы для DevTools

Мы разработали новые темные и легкие темы для DevTools, которые мы будем рады тебе! По умолчанию в Microsoft EDGE (Chromium) DevTools будет использоваться темная тема. Чтобы изменить тему DevTools, нажмите `Fn`  +  `F1` кнопку в правом верхнем углу окна DevTools на панели Windows или Mac или перейдите к пункту параметры с помощью `...` кнопки.

![Главное меню Microsoft EDGE (Chromium) DevTools](./media/devtools-main-menu.png)

Из параметров можно изменить тему DevTools. Если вы изменили способ, которым DevTools просмотрел в браузере на основе Chromium, вы можете сделать так, чтобы Microsoft EDGE (Chromium) DevTools точно так же, как и в случае выбора **темной темы (Chromium)** или **света (Chromium)** соответственно. 

## Отладка Microsoft EDGE (Chromium) из кода VS

С помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS вы можете отлаживать как Microsoft EDGE (EdgeHTML), так и Microsoft EDGE (Chromium) прямо из кода VS!

![Отладчик для расширения кода пограничных и других кодов](./media/vscode-debugger.png)

Чтобы запустить Microsoft EDGE (Chromium) вместо Microsoft EDGE (EdgeHTML) из кода VS, необходимо добавить `version` атрибут к существующей конфигурации **Launch. JSON** с версией Microsoft EDGE (Chromium), которую вы хотите запустить ( `dev` `beta` или `canary` ). Ниже приведен пример конфигурации **Launch. JSON** , с помощью которой Канарские версия Microsoft EDGE (Chromium) будет запущена в [Bing.com](https://www.bing.com/):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

Дополнительные сведения [об отладке Microsoft EDGE (Chromium) из кода VS можно](../visual-studio-code/debugger-for-edge.md)найти в этой процедуре.

## Обновление протокола пограничного DevTools

При смене базовой веб-платформы Microsoft Edge протокол пограничного DevTools не получит никаких обновлений. DevTools Microsoft EDGE (Chromium) будет использовать протокол DevTools или CDP для Chrome. Для получения справочной документации по доменам и методам в CDP ознакомьтесь со [средством просмотра CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).

В следующей версии Microsoft Edge все методы с префиксом `ms` не поддерживаются. Чтобы узнать больше о том, как использовать CDP в Microsoft EDGE (Chromium), обратитесь к разделу [протокол DevTools (Chromium)](../devtools-protocol-chromium.md).

## Известные проблемы

Многие ссылки с веб-сайтов Microsoft EDGE (Chromium) DevTools на содержимое, размещенное на сторонних сайтах, временно удалены. Как только мы сможем заменить эти ссылки, мы добавим их обратно в DevTools.


При отладке веб-содержимого на устройстве Android из Microsoft EDGE (Chromium) версия DevTools, которая запускается при нажатии кнопки " **проверить** **", может** не совпадать с версией браузера на устройстве с Android. В результате в DevTools могут отображаться новые возможности, которые не будут работать в браузере на устройстве с Android. Если вы столкнулись с вашим мнением, мы будем рады узнать о нем, чтобы получить [отзыв о файле](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).

Наконец, Visual Studio для Windows и Mac пока не поддерживает Microsoft EDGE (Chromium). Зарегистрируйтесь [здесь](https://visualstudio.microsoft.com/vs/preview/) , чтобы узнать, когда у нас есть ознакомительная версия Visual Studio, поддерживающая отладку JavaScript в Microsoft EDGE (Chromium) для проектов ASP.NET!  
