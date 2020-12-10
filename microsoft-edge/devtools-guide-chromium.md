---
description: Знакомство со средствами разработчика Microsoft EDGE (Chromium)
title: Инструменты разработчика Microsoft EDGE (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8f773db3d175f8b5128e1558809334c8f2de4bd7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204007"
---
# Инструменты разработчика Microsoft EDGE (Chromium)  

Microsoft Edge использует проект Chromium Open Source для более лучшей веб-совместимости и меньшего разбиения на разные базовые веб-платформы.  Это изменение должно облегчить создание и тестирование веб-сайтов в Microsoft EDGE и убедиться в том, что они работают должным образом даже при просмотре в другом браузере на базе Chromium (например, Google Chrome, Vivaldi, Opera или Brave).  

Поскольку веб-сайты увеличили использование в непрерывном массиве типов устройств, сложность и накладные расходы, участвующие в тестировании веб-сайтов, были развернуты. Поскольку веб-разработчики (особенно те, которые используют небольшие компании \) должны тестироваться в различных системах, вы можете обнаружить, что сайты хорошо подходят для всех типов устройств и для всех браузеров.  Теперь, когда Microsoft Edge базируется на Chromium, группа Microsoft Edge стала упростила матрицу путем выравнивания веб-платформы Microsoft Edge с помощью других браузеров на основе Chromium и предоставила разработчикам средства для создания визуальных средств, как внутри браузера, так и с другими средствами разработчика, которые вы используете каждый день (например, код Visual Studio).  

Если вы выйдете из Microsoft EDGE и вы в основном разрабатываете в Chromium-браузере, вам нужно прямо дома.  Средства разработчика Microsoft Edge \ (Chromium \) точно так же, как и инструменты разработчика, которые вы уже знаете и используете.  Дополнительные сведения можно найти [в разделе новые возможности DevTools Microsoft EDGE (Chromium)][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft EDGE (Chromium) DevTools" lightbox="./devtools-guide-chromium/media/devtools.png":::
   Microsoft EDGE (Chromium) DevTools  
:::image-end:::  

Если вы выйдете новый Microsoft EDGE и вы уже разработали в Microsoft Edge \ (EdgeHTML \), у вас появились новые средства, которые помогут вам легко и быстро создавать и тестировать веб-сайты в Microsoft Edge.  

## Открытие DevTools  

Если вы никогда раньше не использовали DevTools, инструменты разработчика Microsoft Edge — это набор средств, которые непосредственно встроены в браузер Microsoft Edge.  С помощью этих DevTools вы можете сделать следующее:  

*   Проверка и внесение изменений на веб-сайт HTML  
*   Редактирование CSS и мгновенное просматривайте просмотр веб-сайта  
*   Просмотр всех `console.log()` операторов из кода JavaScript на стороне внешнего пользователя  
*   Отладка сценария с помощью задания точек останова и пошагового прохода по строке  

все прямо в браузере.  Ниже приведены примеры некоторых функциональных возможностей, предоставляемых DevTools, для облегчения и более быстрой сборки и тестирования веб-сайтов в Microsoft Edge.  

Открытие DevTools  

*   нажмите клавишу `F12` 
*   Нажмите `Ctrl` + `Shift` + `I` на Windows или Linux \ ( `Command` + `Option` + `I` на macOS \).  

Если вы хотите просмотреть HTML или CSS для элемента на сайте, щелкните элемент правой кнопкой мыши и выберите команду **проверить** , чтобы перейти на панель элементы.  Вы также можете нажать `Ctrl` + `Shift` + `C` в Windows или Linux \ ( `Command` + `Option` + `C` на macOS \), чтобы открыть DevTools в **режиме проверки элементов** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** ".  

Если вы хотите просмотреть журналы из клиентского кода JavaScript или быстро запустить какой-либо сценарий, нажмите `Ctrl` + `Shift` + `J` на Windows или Linux или `Command` + `Option` + `J` на macOS, чтобы открыть панель консоли в DevTools.  

## Основные средства  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Основные инструменты для Microsoft EDGE (Chromium) DevTools" lightbox="./devtools-guide-chromium/media/devtools-core-tools.png":::
   Основные инструменты для Microsoft EDGE (Chromium) DevTools  
:::image-end::: 

В Microsoft Edge \ (Chromium \) DevTools включены следующие панели.  

*   Панель **Элементы** для редактирования HTML и CSS, изучения свойств специальных возможностей, просмотра прослушивателей событий и определения точек останова для изменений DOM  
*   **Консоль** для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также для запуска JavaScript в контексте выбранного окна или кадра  
*   Панель « **источники** », в которой можно открывать и редактировать код, задавать точки останова, пошагово прокручивать код и просматривать состояние веб-сайта в одной строке JavaScript за один раз.  
*   Панель **Сеть** для отслеживания и проверки запросов и ответов из кэша сети и браузера   
*   Панель **Производительность** для профилирования времени и системных ресурсов, запрашиваемых вашим сайтом  
*   Панель**Память** для оценки использования ресурсов памяти и сравнения моментальных снимков кучи в разных состояниях среды выполнения кода.  
*   Панель **приложения** для проверки, изменения и отладки манифестов веб-приложения, рабочих процессов служб и рабочих процессов служб.  Вы также можете проверять хранение, базы данных и кэширование на панели **приложения** и управлять ими.  
*   Панель **безопасности** для устранения проблем с безопасностью и проверки правильности реализации HTTPS на веб-сайте.  HTTPS обеспечивает безопасность и целостность данных как для вашего сайта, так и для пользователей, которые предоставляют личную информацию на вашем сайте.  
*   Панель **аудитов** \ (теперь переименовывает **Lighthouse**\), чтобы запустить аудит веб-сайта.  Результаты аудита помогают улучшить качество сайта следующими способами.  
    *   Перехватывать распространенные ошибки, связанные с обеспечением доступности веб-сайта, его безопасности, выполнения и т. д.  
    *   Устраните все ошибки.  
    *   Создание PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Пожалуйста, отправляйте свои [Отзывы и запросы функций](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Расширения  

Возможно, вы использовали расширения для DevTools, которые помогут вам диагностировать и отлаживать проблемы при создании веб-сайтов или приложений.  Вы можете получить расширения для Microsoft EDGE на странице [надстроек Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  На странице [надстроек Microsoft Edge][MicrosoftEdgeAddonsExtensions] вы можете просматривать расширения DevTools из категории " **средства разработчика** " или поиска по определенному расширению.  

Вы также можете добавлять расширения из [веб-магазина Chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Веб-магазин Chrome в Microsoft Edge" lightbox="./devtools-guide-chromium/media/allow-extensions-from-stores.png":::
   Веб-магазин Chrome в Microsoft Edge  
:::image-end:::  

В верхней части экрана выберите **Разрешить расширения из других магазинов** и нажмите кнопку **Разрешить** в появившемся диалоговом окне.  

> [!NOTE]
> Расширения, установленные из источников, отличных от Microsoft Store, не проверяются и могут повлиять на производительность браузера.  

Нажмите кнопку **Добавить в хром** , чтобы добавить расширение DevTools в Microsoft Edge.  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Добавление расширения из веб-магазина Chrome в Microsoft Edge" lightbox="./devtools-guide-chromium/media/install-extension-from-chrome-store.png":::
   Добавление расширения из веб-магазина Chrome в Microsoft Edge  
:::image-end:::  

## Ярлыки  

Эти сочетания клавиш управляют основным окном DevTools, работают во всех инструментах или оба.  

| Действие | Windows или Linux | macOS |  
|:--- |:--- | :--- |  
| Показать/скрытьСредства разработчика \(открывает последнюю просмотренную панель) | `F12` / `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Отображение панели консоли | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Показать DevTools в **режиме проверки элемента** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** " | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Показать параметры | `?` / `Fn`+`F1` | `?` / `Fn`+`F1` |  
| Переход к следующей панели | `Ctrl`+`]` | `Command`+`]` |  
| Показать предыдущую панель | `Ctrl`+`[` | `Command`+`[` |  
| Закрепите DevTools в последней использованной вакансии.  Если DevTools остается в положении по умолчанию для всего сеанса, этот ярлык отсоединяет DevTools в отдельном окне. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Переключение **режима устройства** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Переключение **режима проверки элемента** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** " | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Показать меню команд | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Показать или скрыть денежный ящик | `Esc` | `Esc` |  
| Обновление.  Страница будет обновлена с помощью кэша.  | `F5` / `Ctrl`+`R` | `Command`+`R` |  
| Жесткое обновление.  Это заставляет Microsoft Edge загрузить ресурсы еще раз и перезагрузить.  Возможно, используемые ресурсы могут поступать из кэшированной версии. | `Ctrl`+`F5` / `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста на текущей панели.  Не поддерживается в панелях аудит, приложения и безопасность | `Ctrl`+`F` | `Command`+`F` |  
| Отображение панели поиска в ящике, позволяющей искать текст во всех загруженных ресурсах | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Открытие файла на панели «источники» | `Ctrl`+`O` / `Ctrl`+`P` | `Command`+`O` / `Command`+`P` |  
| Увеличить масштаб | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Ctrl`+`-` | `Command`+`-` |  
| Восстановление масштаба по умолчанию | `Ctrl`+`0` | `Command`+`0` |  
| Выполнить сниппет | `Ctrl`+`O`или `Ctrl` + `P` введите `!` имя сценария, а затем нажмите клавишу `Enter` | Нажмите клавишу `Command` + `O` или `Command` + `P` , введите `!` имя сценария, а затем нажмите клавишу `Enter` |  
| Отображение нередактируемого исходного кода HTML на новой вкладке | `Ctrl`+`U` | Н/Д |  

> [!NOTE]
> При отладке и приостановке в точке останова сначала восстанавливается ярлык **обновления** .  

## См. также  

*   [DevTools для начинающих: Приступая к работе с HTML и моделью DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Протокол DevTools Microsoft EDGE (Chromium)][DevtoolsProtocolChromiumIndex]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

Если вы хотите просмотреть [последние функции DevTools][DevtoolsGuideChromiumWhatsNewIndex], скачайте [Microsoft Edge Канарские][MicrosoftedgeinsiderDownload], который строится на ночь.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools для начинающих: Приступая к работе с HTML и моделью DOM | Документы Microsoft"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Новые возможности Microsoft EDGE (Chromium) DevTools | Документы Microsoft"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Протокол Microsoft EDGE (Chromium) DevTools Protocol | Документы Microsoft"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Надстройки Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  
