---
description: Как узнать о средствах разработчика Microsoft Edge (Chromium)
title: Средства разработчика Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: fcae8f0974244e87ba781b94221cb5d8a1bb3dce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235156"
---
# Обзор средств разработчика Microsoft Edge (Chromium)  

Microsoft Edge принял проект Chromium с открытым исходным кодом, чтобы улучшить совместимость с веб-сайтами и уменьшить фрагментацию различных платформ.  Это изменение должно упростить сборку и тестирование веб-сайтов в Microsoft Edge и убедиться, что они работают ожидаемым образом, даже если они просматриваются в разных браузерах на основе Chromium (например, Google Chrome, Vivaldi, Opera или Opera\).  

По мере того, как интернет-сайт стал использовать все более расширяющийся массив типов устройств, сложность и накладные расходы, связанные с тестированием веб-сайтов, возрастают. Так как веб-разработчики (особенно в небольших компаниях) должны тестироваться с таким количеством различных систем, может оказаться практически невозможным гарантировать, что сайты будут хорошо работать на всех типах устройств и всех браузерах.  Теперь, когда Microsoft Edge основан на Chromium, группа разработчиков Microsoft Edge упростила матрицу, выровняя веб-платформу Microsoft Edge с другими браузерами на основе Chromium и предоставляя лучшие в своем классе инструменты для разработчиков как в браузере, так и с другими инструментами разработчика, которые вы используете каждый день (например, Visual Studio Code\).  

Если вы проверяете Microsoft Edge и разрабатываете его в основном в браузере на основе Chromium, вы должны быть дома.  Инструменты разработчика Microsoft Edge \(Chromium\) работают так же, как и инструменты разработчика, которые вы уже знаете и используете.  Дополнительные сведения см. в новых функциях [Microsoft Edge (Chromium) DevTools.][DevtoolsGuideChromiumWhatsNewIndex]  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Если вы проверяете новый Microsoft Edge и ранее разрабатывали его в Microsoft Edge \(EdgeHTML\), у вас теперь есть отличные новые инструменты, которые упрощают и ускоряют создание и тестирование веб-сайтов в Microsoft Edge.  

## Откройте DevTools  

Если вы никогда раньше не использовали DevTools, инструменты разработчика Microsoft Edge — это набор инструментов, встроенных непосредственно в браузер Microsoft Edge.  С помощью DevTools можно сделать следующее.  

*   Проверка и внесение изменений в веб-сайт HTML  
*   Редактирование CSS и мгновенное просмотр отображения веб-сайта  
*   См. все `console.log()` утверждения из кода JavaScript переднего кода  
*   Отлаговка скрипта путем установки точек останова и пошаговой пошаговой пошаговой пошаговости  
    
Все непосредственно в браузере.  Это лишь примеры некоторых функций, которые предоставляет DevTools, чтобы упростить и ускорить создание и тестирование веб-сайтов в Microsoft Edge.  

Открытие DevTools  

*   Выбор `F12` 
*   Выберите `Ctrl` + `Shift` + `I` в Windows/Linux \( `Command` + `Option` + `I` в macOS\)  
    
Если вы хотите увидеть HTML-код или CSS для элемента на сайте, щелкните правой кнопкой мыши элемент и выберите "Проверить", чтобы перейти на панель элементов. ****  Вы также можете нажать на `Ctrl` + `Shift` + `C` Windows/Linux \( на `Command` + macOS\), чтобы открыть `Option` + `C` **** DevTools **** в режиме inspect Element Mode, который позволяет выбрать элемент на сайте и увидеть HTML и CSS на панели элементов.  

Если вы хотите увидеть журналы из кода JavaScript переднего кода или быстро выполнить какой-либо сценарий, выберите в Windows,Linux или macOS, чтобы запустить панель консоли в `Ctrl` + `Shift` + `J` `Command` + `Option` + `J` DevTools. ****  

## Основные средства  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Основные средства Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Основные средства Microsoft Edge (Chromium) DevTools  
:::image-end::: 

Microsoft Edge \(Chromium\) DevTools включает следующие панели.  

*   Панель **Элементы** для редактирования HTML и CSS, изучения свойств специальных возможностей, просмотра прослушивателей событий и определения точек останова для изменений DOM  
*   **Консоль** для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также для запуска JavaScript в контексте выбранного окна или кадра  
*   Панель **источников** для открытия и редактирования кода в режиме времени, назначения точек останова, пошагового кода и просмотр состояния вашего веб-сайта по одной строке JavaScript за раз  
*   Панель **Сеть** для отслеживания и проверки запросов и ответов из кэша сети и браузера   
*   Панель **Производительность** для профилирования времени и системных ресурсов, запрашиваемых вашим сайтом  
*   Панель**Память** для оценки использования ресурсов памяти и сравнения моментальных снимков кучи в разных состояниях среды выполнения кода.  
*   Панель **приложений для** проверки, изменения и отлажки манифестов веб-приложений, сотрудников служб и рабочих кэшей служб.  Вы также можете проверять и управлять хранилищем, базами данных и кэшами на **панели** приложений.  
*   Панель **безопасности** для отлаки проблем безопасности и обеспечения правильной реализации HTTPS на веб-сайте.  ПРОТОКОЛ HTTPS обеспечивает важную безопасность и целостность данных как для сайта, так и для пользователей, которые предоставляют личную информацию на вашем сайте.  
*   Панель **аудита** \(теперь она **переименована Lighthouse**\) для запуска аудита вашего веб-сайта.  Результаты аудита помогают улучшить качество сайта следующими способами.  
    *   Catch common errors related to making your website accessible, secure, performant, and so on.  
    *   Исправьте каждую ошибку.  
    *   Создание PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Отправьте свои [отзывы и запросы на функции.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Расширения  

Возможно, вы использовали расширения DevTools для диагностики и отладки проблем при создании веб-сайтов или приложений.  Вы можете приобрести расширения для Microsoft Edge на странице ["Надстройки Microsoft Edge".][MicrosoftEdgeAddonsExtensions]  На странице ["Надстройки Microsoft Edge"][MicrosoftEdgeAddonsExtensions] можно просмотреть **** расширения DevTools из категории "Инструменты разработчика" или найти определенное расширение.  

Вы также можете добавить расширения из [веб-магазина Chrome.][GoogleChromeWebstoreExtensions]  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Веб-магазин Chrome в Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Веб-магазин Chrome в Microsoft Edge  
:::image-end:::  

At the top, choose **Allow extensions from other stores** and then choose **Allow** in the dialog that appears.  

> [!NOTE]
> Расширения, установленные не из Microsoft Store, не являются непроверенными и могут повлиять на производительность браузера.  

Choose **Add to Chrome** to add your DevTools extension to Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Добавление расширения из веб-магазина Chrome в Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Добавление расширения из веб-магазина Chrome в Microsoft Edge  
:::image-end:::  

## Ярлыки  

Эти ярлыки контролируют главное окно DevTools, работают во всех средствах или и то, и другое.  

| Действие | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Показать/скрытьСредства разработчика \(открывает последнюю просмотренную панель) | `F12` или `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Показать панель консоли | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Показать DevTools в режиме **проверки** элементов, который позволяет выбрать элемент на сайте и увидеть HTML и CSS на **панели элементов** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Показать параметры | `?` или `Fn`+`F1` | `?` или `Fn`+`F1` |  
| Показать следующую панель | `Ctrl`+`]` | `Command`+`]` |  
| Показать предыдущую панель | `Ctrl`+`[` | `Command`+`[` |  
| Закрепление DevTools в последней используемой позиции.  Если DevTools остается в позиции по умолчанию для всего сеанса, ярлык отсоединяя DevTools в отдельное окно | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Режим **перегона устройства** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** which lets you select an element on the site and see the HTML and CSS in the **Elements** panel | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Показать меню команд | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Show/Hide the Drawer | `Esc` | `Esc` |  
| Обновление.  Перезапахает страницу с помощью кэша.  | `F5` или `Ctrl`+`R` | `Command`+`R` |  
| Жесткое обновление.  Заставляет Microsoft Edge снова загружать ресурсы и перезагружать их.  Возможно, что использованные ресурсы приходят из кэшной версии | `Ctrl`+`F5` или `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста на текущей панели.  Не поддерживается в панелях аудита, приложений и безопасности | `Ctrl`+`F` | `Command`+`F` |  
| Отрисовка панели поиска в средстве "Drawer", которая позволяет искать текст во всех загруженных ресурсах | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Открытие файла на панели источников | `Ctrl`+`O` или `Ctrl`+`P` | `Command`+`O` или `Command`+`P` |  
| Масштабирование | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Ctrl`+`-` | `Command`+`-` |  
| Восстановление уровня масштабирования по умолчанию | `Ctrl`+`0` | `Command`+`0` |  
| Запуск фрагмента кода | `Ctrl`+`O`или `Ctrl` + `P` , `!` введите после имени скрипта, а затем нажмите `Enter` | Нажмите `Command` + `O` или `Command` + `P` `!` введите имя сценария, а затем нажмите `Enter` |  
| Показывать нередактируемый исходный код HTML на новой вкладке | `Ctrl`+`U` | Н/Д |  

> [!NOTE]
> Если отладка и приостановка в точке останова, ярлык **"Обновить"** сначала возобновляет работу.  

## См. также  

*   [DevTools для начинающих: начало работы с HTML и DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Протокол DevTools Microsoft Edge (Chromium)][DevtoolsProtocolChromiumIndex]  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Если вы хотите просмотреть последние функции, которые будут представлены в [DevTools,][DevtoolsGuideChromiumWhatsNewIndex]скачайте [Microsoft Edge Canary,][MicrosoftedgeinsiderDownload]который создается ночью.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools для начинающих: начало работы с HTML и DOM | Документы Майкрософт"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Новые возможности Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Протокол Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Надстройки Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  
