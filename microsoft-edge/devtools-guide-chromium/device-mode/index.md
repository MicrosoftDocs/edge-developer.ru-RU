---
description: Использование виртуальных устройств в Microsoft Edge для создания веб-сайтов с мобильными устройствами.
title: Эмулировать мобильные устройства в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, девтуолы, эмуляция, устройство, моделирование, мобильный телефон
ms.openlocfilehash: bb081ddd5f773e5e9ae6a1b83b5fcb13408df6cb
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439453"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a>Эмулировать мобильные устройства в Microsoft Edge DevTools  

Используйте **эмуляцию** устройства, чтобы приблизить внешний вид и ответы страницы на мобильном устройстве.  Microsoft Edge DevTools предоставляет коллекцию функций, которые помогут вам подражать мобильным устройствам.  Коллекция содержит следующие функции.  

*   [Имитация мобильного представления](#simulate-a-mobile-viewport)  
*   [Throttle сеть](#throttle-the-network-only)  
*   [Throttle the CPU](#throttle-the-cpu-only)  
*   [Имитация геолокации](#override-geolocation)  
*   [Настройка ориентации](#set-orientation)  
*   [Настройка строки агента пользователя](#set-user-agent-string)  

## <a name="limitations"></a>Ограничения  

**Эмуляция** устройства — это [аппроксимация][WikiApproximation] внешний вид вашей страницы на мобильном устройстве.  **Эмуляция устройства** фактически не запускает код на мобильном устройстве.  Вместо этого вы имитируете работу мобильных пользователей с ноутбука или рабочего стола.  

Некоторые аспекты мобильных устройств никогда не эмулированы в DevTools.  Например, архитектура мобильных процессоров отличается от архитектуры процессоров ноутбука или настольных компьютеров.  Если вы сомневаетесь, лучше всего запустить страницу на мобильном устройстве.  Используйте [Удаленное отладка][DevToolsRemoteDebugging] для взаимодействия с кодом страницы из компьютера, пока страница фактически работает на мобильном устройстве.  Вы можете просматривать, изменять, отлаговка, профиль или все четыре во время взаимодействия с кодом.  Компьютер может быть ноутбуком или настольным компьютером.  

## <a name="simulate-a-mobile-viewport"></a>Имитация мобильного представления  

Выберите эмуляцию устройства **Toggle** \. Панель инструментов устройства \) или выберите Настройка и управление эмуляцией ![ ](../media/toggle-device-toolbar-dark-icon.msft.png) **DevTools** `...` \( **** \) > устройства, чтобы открыть пользовательский интерфейс, который позволяет имитировать мобильный видпорт.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Панель инструментов устройства  
:::image-end:::  

По умолчанию панель инструментов устройства открывается в режиме Responsive Viewport.  

### <a name="responsive-viewport-mode"></a>Режим "Отзывчивый режим просмотра"  

Чтобы быстро проверить внешний вид и внешний вид страницы на нескольких размерах экрана, перетащите ручки для повторного размера представления до требуемого размера.  Вы также можете ввести определенные значения в полях ширины и высоты.  На следующем рисунке за установлена ширина, а высота `626` `516` — .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Ручки для изменения размеров представления в режиме Responsive Viewport" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Ручки для изменения размеров представления в режиме Responsive Viewport  
:::image-end:::  

#### <a name="show-media-queries"></a>Показать запросы мультимедиа  

Если вы определили запросы мультимедиа на своей странице, переперейти к измерениям viewport, где эти запросы мультимедиа вступает в силу, показывая точки разлома запроса мультимедиа над представлением.  Выберите **дополнительные**  >  **параметры Показать запросы мультимедиа**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Показать запросы мультимедиа" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Показать запросы мультимедиа**  
:::image-end:::  

Выберите точку разлома, чтобы изменить ширину представления, чтобы запрос мультимедиа был срабатываем.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Выберите точку разрыва, чтобы изменить ширину представления" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Выберите точку разрыва, чтобы изменить ширину представления  
:::image-end:::  

#### <a name="set-the-device-type"></a>Настройка типа устройства  

Используйте список **типа устройства** для имитации мобильного устройства или настольного устройства.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Список типов устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Список **типов** устройств  
:::image-end:::  

В следующей таблице описываются различия между доступными вариантами типа устройства.  В столбце метода рендеринга указывается, отрисовка страницы Microsoft Edge в качестве мобильного или настольного представления.  Столбец Cursor ссылается на тип курсора, отображаемого при наведении на странице.  В срабатывом столбце События указывается, запускается ли страница или события при взаимодействии `touch` `click` со страницей.  

| Параметр | Метод отрисовки | Значок Cursor | События, срабатыва |  
|:--- |:--- |:--- |:--- |  
| Мобильные устройства | Мобильные устройства | Круг | Сенсорный ввод |  
| Mobile \(без касания\) | Мобильные устройства | Обычный |  выберите  |  
| Desktop | Desktop | Обычный |  выберите  |  
| Desktop \(touch\) | Desktop | Круг | Сенсорный ввод |  

> [!NOTE]
> Если список **типа** устройства не отображается, выберите **Дополнительные параметры**  >  **Добавить тип устройства.**  

### <a name="mobile-device-viewport-mode"></a>Режим представления мобильных устройств  

Чтобы имитировать размеры определенного мобильного устройства, выберите устройство из **списка Устройств.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Список устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Список **устройств**  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a>Поверните представление на ориентацию ландшафта  

Проверьте веб-страницу в ландшафтной ориентации.  

*   Чтобы повернуть представление в ландшафтную ориентацию, выберите **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Страница, отображаемая в ландшафтной ориентации" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Страница, отображаемая в ландшафтной ориентации  
    :::image-end:::  
    
> [!NOTE]
> Кнопка **Вращать** исчезает, если панель **инструментов устройства** узкая.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Панель **инструментов устройства**  
:::image-end:::  

Дополнительные сведения перейдите в [set orientation](#set-orientation).  

#### <a name="show-device-frame"></a>Показать кадр устройства  

Отображение физической рамки устройства вокруг представления при имитации размеров определенного мобильного устройства, например iPhone 6.  

1.  Откройте **дополнительные параметры**.  
1.  Выберите **кадр устройства Show**.  

> [!NOTE]
> Если кадр устройства для определенного устройства не отображается, это означает, что в DevTools нет искусства для этого параметра.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Показать кадр устройства" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Показать кадр устройства  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Кадр устройства для iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Кадр устройства для iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a>Добавление настраиваемого мобильного устройства  

Если необходимый параметр мобильного устройства не включен в список по умолчанию, можно добавить настраиваемое устройство.  Чтобы добавить настраиваемые устройства, выполните следующие действия.  

1.  Выберите список **устройств,** > **изменить**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Выбор правки" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Выбор **правки**  
    :::image-end:::  
    
1.  Выберите **Добавление настраиваемой устройства**.  
1.  На **эмулированных устройствах**введите имя устройства, ширину экрана и высоту экрана для настраиваемого устройства.  Соотношение [пикселей устройства,][MDNWindowDevicePixelRatio] [строка агента пользователя][MDNUserAgent]и поля [типа](#set-the-device-type) устройства необязательны.  Поле типа устройства по умолчанию является **мобильным.**  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Создание настраиваемой устройства" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Создание настраиваемой устройства  
    :::image-end:::  
    
### <a name="show-rulers"></a>Показать линейки  

Если необходимо измерить размеры экрана, можно использовать линейки для измерения размера экрана в пикселях.  Выберите **дополнительные**  >  **параметры Показать линейки,** чтобы отображать линейки выше и слева от вашего представления.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Элемент меню для отображения правителей" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Элемент меню для отображения правителей  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Линейки сверху и слева от представления" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Линейки сверху и слева от представления  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a>Масштабирование представления  

Чтобы проверить внешний вид и внешний вид страницы на нескольких уровнях масштабирования, используйте список **Масштабирование,** чтобы увеличить или выйти.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a>Throttle сети и ЦП  

На мобильных устройствах часто имеются ограничения сети и ЦП.  Проверьте, как быстро загружается страница и как она реагирует на различные скорости интернета и ЦП.  

Throttle сети и ЦП.  

1.  Выберите **список Throttle** и измените предустановленную на **среднеуровневую** мобильную или **низкоуровневую.**  
    *   **Мобильный телефон среднего уровня** имитирует `fast 3G` и подгонает ЦП.  Он в четыре раза медленнее обычного.  
    *   **Мобильный телефон с низким** уровнем уровня имитирует `slow 3G` и подавляет ЦП.  Это в шесть раз медленнее обычного.  
    
Все регулирование зависит от нормальной возможности ноутбука или рабочего стола.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Список дроссельной заслонки в панели инструментов устройств" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Список **дроссельной заслонки** в панели инструментов устройств  
:::image-end:::  

> [!NOTE]
> Если список **Throttle скрыт,** панель инструментов **устройства** слишком узкая.  Чтобы получить доступ **к списку Throttle,** увеличите ширину панели **инструментов устройства.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Панель **инструментов устройства**  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a>Затормажает только ЦП  

Чтобы затормалить только ЦП, а не сеть, выполните следующие действия.

1.  Выберите панель **Performance** и выберите **Параметры захвата** \. ![ Параметры захвата ](../media/capture-settings-icon.msft.png) \).
1.  Выберите **замедление**  >  **4x** ЦП или **замедление 6x.**
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Список ЦП в панели Performance" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Список **ЦП** в панели **Performance**  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a>Throttle сеть только  

Чтобы затормалить сеть, выполните следующие действия.

1.  Выберите средство **Network.**
1.  Выберите **Online**  >  **Fast 3G** или Slow **3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Список Throttle в панели Network" lightbox="../media/device-mode-network-throttle.msft.png":::
       Список **Throttle** в панели Network  
    :::image-end:::  
    
    Или выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\) **** `3G` **** **** для открытия командного меню , введите и выберите Включить быстрое регулирование 3G или включить медленное регулирование 3G .  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
Кроме того, можно установить регулирование сети с панели **Performance.**  

1.  Выберите **Параметры** захвата \. Параметры захвата \) и выберите список Сети и измените заранее на ![ быстрый ](../media/capture-settings-icon.msft.png) **3G** или **медленный 3G**. ****  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Настройка регулирования сети с панели Performance" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Настройка регулирования сети с панели **Performance**  
    :::image-end:::  
    
## <a name="override-geolocation"></a>Переопределение геолокации  

:::row:::
   :::column span="":::
      Если ваша страница зависит от сведений о геолокации с мобильного устройства для правильной отрисовки, предопределите различные геолокации с помощью пользовательского интерфейса, переопределяемого геолокацией.  

      1.  Выберите **Настройка и управление DevTools** `...` \( \) > **Дополнительные датчики**  >  **инструментов**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики геолокации" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Датчики** геолокации  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Откройте командное меню.  
          *   Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).  
      1. Введите `Sensors` и выберите **датчики show**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики для геолокации" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Показать датчики** для геолокации  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

На панели **Датчики** можно выбрать одно из заранее заранее задаваемых расположений, включенных в DevTools, с помощью выпадаемого **** меню Location.  Чтобы ввести настраиваемую расположение, выберите **другое...** и введите координаты настраиваемого расположения.  Чтобы проверить страницу в состоянии ошибки при недоступности сведений о расположении, выберите **расположение недоступно.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Панель датчиков с заранее выбранным расположением" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    **Панель** датчиков с выбранным заранее расположением.  
:::image-end:::

## <a name="set-orientation"></a>Настройка ориентации  

:::row:::
   :::column span="":::
      Если ваша страница зависит от сведений об ориентации с мобильного устройства для правильного отображения, откройте пользовательский интерфейс ориентации.  

      1.  Выберите **Настройка и управление DevTools** `...` \( \) > **Дополнительные датчики**  >  **инструментов**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики для ориентации" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Датчики** для ориентации  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Откройте командное меню.  
          *   Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).  
      1. Введите `Sensors` и выберите **датчики show**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики для ориентации" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Показать датчики** для ориентации  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

На панели **Датчики** можно выбрать предустановленную ориентацию из выпадаемого меню "Ориентация". ****  Чтобы ввести собственную ориентацию, выберите **настраиваемую**ориентацию и введите собственные значения [альфа-версии,][MDNDeviceOrientaitonAlpha] [бета-версии][MDNDeviceOrientaitonGamma] и гаммы. [][MDNDeviceOrientaitonBeta]  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Параметры ориентации на панели Датчики" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Параметры** ориентации на **панели Датчики**  
:::image-end:::  

## <a name="set-user-agent-string"></a>Настройка строки агента пользователя  

:::row:::
   :::column span="":::
      Если ваша страница зависит от строки агента пользователя с мобильного устройства для правильной визуализации, используйте панель условий Сети для предоставления различных строк агента пользователя. ****  
      
      1.  Выберите **Настройка и управление DevTools** `...` \( \) > **дополнительные условия**сети  >  **инструментов.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Запись условий сети в меню More tools" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         **Запись условий** сети в **меню More tools**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Откройте командное меню.  
          *   Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).  
      1. Введите `Network conditions` и выберите условия Show **Network**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Показать условия сети" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Показать условия сети**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Рядом с **агентом пользователя**выберите **автоматический** почтовый ящик Select.  Затем выберите **Настраиваемый...,** чтобы выбрать из списка заранее задав строки агента пользователя.  Чтобы ввести собственную строку агента пользователя, введите строку **в Ввод пользовательского агента.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Установите строку агента пользователя в Microsoft Edge на macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Установите строку агента пользователя в Microsoft Edge на macOS  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Начало работы с удаленной отладки устройств Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый порядок — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
