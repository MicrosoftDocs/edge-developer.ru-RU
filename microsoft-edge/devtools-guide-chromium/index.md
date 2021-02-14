---
description: Как узнать о средствах разработчика Microsoft Edge (Chromium)
title: Средства разработчика Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 05b757b7cb399815d072b9d6038873cfd118a59d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327493"
---
# Обзор средств разработчика Microsoft Edge (Chromium)  

Microsoft Edge принял проект Chromium с открытым исходным кодом.  Новый браузер Microsoft Edge позволяет улучшить совместимость веб-сайтов и уменьшить фрагментацию различных веб-платформ.  Это изменение должно упростить создание и тестирование веб-страниц в Microsoft Edge.  Новый Microsoft Edge должен помочь вашим веб-сайтам работать в нужном случае при их открытие в других браузерах на основе Chromium.  Браузеры на основе Chromium включают Google Chrome, Vivaldi, Opera, Состав и новый Microsoft Edge.  

Интернет стал использовать все большее количество типов устройств.  Сложность и накладные расходы, связанные с тестированием веб-страниц, быстро растет.  Такие веб-разработчики, как вы, должны тестироваться в различных системах.  Чтобы веб-страницы хорошо работали на всех типах устройств и браузерах, это может оказаться практически невозможным, особенно если вы работаете в небольшой компании.  Новый Microsoft Edge теперь основан на Chromium.  Команда Microsoft Edge упростила матрицу, выровнив веб-платформу Microsoft Edge с другими браузерами на основе Chromium.  Новый Microsoft Edge предоставляет лучшие в своем классе возможности разработки.  Этот опыт выполняется в браузере и наряду с другими инструментами разработчика, которые вы используете каждый день, например Visual Studio Code.  

Как разработчик браузера на основе Chromium вы должны быть в безопасности нового браузера Microsoft Edge.  Microsoft Edge \(Chromium\) DevTools работает так же, как средства разработчика, которые вы уже знаете и используете.  Средства разработчика Microsoft Edge \(Chromium\) часто называютСя Microsoft Edge \(Chromium\) DevTools или DevTools.  Дополнительные сведения см. в новых функциях [Microsoft Edge (Chromium) DevTools.][DevtoolsGuideChromiumWhatsNewIndex]  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Если вы ранее разрабатывали для Microsoft Edge \(EdgeHTML\) и оценивали новый Microsoft Edge, теперь он предоставляет отличные новые инструменты для создания и тестирования веб-страниц проще и быстрее.  

## Откройте DevTools  

Microsoft Edge DevTools — это набор инструментов, встроенных непосредственно в браузер Microsoft Edge.  DevTools позволяет выполнять следующие задачи непосредственно в браузере.  

*   Проверка и внесение изменений в веб-страницу HTML  
*   Редактирование CSS и мгновенное просмотр отображения веб-страницы  
*   Просмотрите все `console.log()` утверждения из кода JavaScript переднего кода  
*   Отлагоерка скрипта, настройка точек останова и пошаговое пошаговое написание кода  
    
Дополнительные примеры функций, которые предоставляет DevTools, упрощают и ускоряют сборку и тестирование веб-страницы в Microsoft Edge.  

Открытие DevTools  

*   Выбор `F12` 
*   Выберите `Ctrl` + `Shift` + `I` \(Windows/Linux\) или `Command` + `Option` + `I` \(macOS\)  
    
Если вы хотите увидеть HTML-код или CSS для элемента на сайте, щелкните правой кнопкой мыши элемент и выберите "Проверить", чтобы перейти к средству **Elements.** ****  Чтобы открыть DevTools в режиме **inspect Element,** выберите `Ctrl` + `Shift` + `C` \(Windows/Linux\) или `Command` + `Option` + `C` \(macOS\). Режим **проверки** элементов позволяет выбрать элемент на веб-странице и отобразить HTML и CSS в **средстве Elements.**  

Если вы хотите просмотреть журналы из кода JavaScript переднего кода или быстро выполнить скрипт, откройте **консоль.**   Чтобы запустить консоль **в** DevTools, выберите `Ctrl` + `Shift` + `J` \(Windows/Linux\) или `Command` + `Option` + `J` \(macOS\).  

## Основные средства  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Основные средства Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Основные средства Microsoft Edge (Chromium) DevTools  
:::image-end::: 

Microsoft Edge \(Chromium\) DevTools включает следующие средства.  

*   Инструмент **Elements** для редактирования HTML и CSS, проверки свойств доступности, просмотра прослушивателей событий и изменения точек останова изменения DOM  
*   Консоль **для** просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM и запуска JavaScript в контексте выбранного окна или кадра  
*   Средство **Sources** для открытия и редактирования кода, назначения точек останова, пошагового кода и отображения состояния веб-страницы
*   **Сетевое** средство для отслеживания и проверки запросов и ответов из кэша сети и браузера   
*   Средство **"Производительность"** для профиля времени и системных ресурсов, необходимых для сайта  
*   Средство **"Память"** для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях времени работы кода  
*   Средство **приложения** для проверки, изменения и отлажки манифестов веб-приложения, сотрудников служб и рабочих кэшей служб.  Вы также можете проверять хранилище, базы данных и кэши из средства **application** и управлять ими.  
*   Средство **безопасности** для отлаки проблем безопасности и обеспечения правильной реализации HTTPS на веб-странице.  ПРОТОКОЛ HTTPS обеспечивает важную безопасность и целостность данных как для сайта, так и для пользователей, которые предоставляют персональные данные на вашем сайте.  
*   Средство **аудита** \(теперь **переименовано Lighthouse**\) для запуска аудита веб-страницы.  Результаты аудита помогают улучшить качество сайта следующими способами.  
    *   Catch common errors related to making your webpage accessible, secure, performant, and so on.  
    *   Исправьте каждую ошибку.  
    *   Создание PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Отправьте свои [отзывы и запросы на функции.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Расширения  

Возможно, вы получили доступ к DevTools с помощью расширений при диагностике и отладке проблем при построении веб-страниц \(или приложений\). Расширения Microsoft Edge приобретаются из надстройки [Microsoft Edge.][MicrosoftEdgeAddonsExtensions]  В [надстройке Microsoft Edge][MicrosoftEdgeAddonsExtensions]перейдите к расширениям DevTools из категории "Инструменты разработчика" или найдите определенное расширение. ****  

Вы также можете добавить расширения из [веб-магазина Chrome.][GoogleChromeWebstoreExtensions]  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Веб-магазин Chrome в Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Веб-магазин Chrome в Microsoft Edge  
:::image-end:::  

В верхней части выберите "Разрешить **расширения"** из других хранилищ, а затем выберите **"Разрешить"** в от появляются диалоговые окно.  

> [!NOTE]
> Расширения, установленные не из Microsoft Store, не являются непроверенными и могут повлиять на производительность браузера.  

Choose **Add to Chrome** to add your DevTools extension to Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Добавление расширения из веб-магазина Chrome в Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Добавление расширения из веб-магазина Chrome в Microsoft Edge  
:::image-end:::  

## Ярлыки  

Следующие ярлыки контролируют главное окно DevTools, работают во всех средствах или и то, и другое.  

| Действие | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Show/Hide DevTools \(opens to last viewed tool\) | `F12` или `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Показать консоль | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Отображение Элемента DevTools в режиме **inspect,** который позволяет выбрать элемент и отобразить HTML и CSS в **средстве Elements** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Показать параметры | `?` или `Fn`+`F1` | `?` или `Fn`+`F1` |  
| Показать следующую панель | `Ctrl`+`]` | `Command`+`]` |  
| Показать предыдущую панель | `Ctrl`+`[` | `Command`+`[` |  
| Закрепление DevTools в последней используемой позиции.  Если DevTools остается в позиции по умолчанию для всего сеанса, ярлык отсоединяя DevTools в отдельное окно | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Режим **перегона устройства** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** that allows to you to choose an element and display the HTML and CSS in the **Elements** tool | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Показать меню команд | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Show/Hide the Drawer | `Esc` | `Esc` |  
| Обновление.  Обновляет веб-страницу с помощью кэша.  | `F5` или `Ctrl`+`R` | `Command`+`R` |  
| Жесткое обновление.  Заставляет Microsoft Edge снова загружать ресурсы и перезагружать их.  Используемые ресурсы могут быть из кэшной версии | `Ctrl`+`F5` или `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста на текущей панели.  Не поддерживается в средствах аудита, приложений и безопасности | `Ctrl`+`F` | `Command`+`F` |  
| Показать средство поиска в средстве "Drawer", которое позволяет искать текст во всех загруженных ресурсах | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Открытие файла на панели источников | `Ctrl`+`O` или `Ctrl`+`P` | `Command`+`O` или `Command`+`P` |  
| Масштабирование | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Ctrl`+`-` | `Command`+`-` |  
| Восстановление уровня масштабирования по умолчанию | `Ctrl`+`0` | `Command`+`0` |  
| Запуск фрагмента кода | `Ctrl`+`O`или `Ctrl` + `P` , `!` введите после имени скрипта, а затем нажмите `Enter` | Нажмите `Command` + `O` или `Command` + `P` введите `!` имя сценария, а затем нажмите `Enter` |  
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

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools для начинающих: начало работы с HTML и doM | Документы Майкрософт"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Новые возможности Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Протокол Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Надстройки Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  
