---
description: Узнать о средствах разработчика Microsoft Edge (Chromium)
title: Средства разработчика Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 29ded7376ab1788998acf059c6677916a52d5d15
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408278"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Обзор средств разработки Microsoft Edge (Chromium)  

Microsoft Edge приняла проект с открытым исходным кодом Chromium.  Новый браузер Microsoft Edge создает лучшую веб-совместимость и уменьшает фрагментацию различных веб-платформ.  Это изменение должно упростить создание и тестирование веб-страниц в Microsoft Edge.  Новый Microsoft Edge должен помочь веб-сайтам работать так, как ожидалось, когда они открываются в других браузерах на основе хрома.  Браузеры на основе хрома включают Google Chrome, Vivaldi, Opera, Brave и новый Microsoft Edge.  

Веб вырос в использовании во все расширяемом массиве типов устройств.  Сложность и накладные расходы, связанные с тестированием веб-страниц, быстро возросли.  Такие веб-разработчики, как вы, должны протестировать различные системы.  Чтобы убедиться, что веб-страницы хорошо работают на всех типах устройств и браузерах, это может оказаться практически невозможным, особенно если вы работаете в небольшой компании.  Новый Microsoft Edge теперь основан на Chromium.  Команда Microsoft Edge упростила матрицу, выровнив веб-платформу Microsoft Edge с другими браузерами на основе хрома.  Новый Microsoft Edge предоставляет лучший в своем классе опыт разработки.  Этот опыт выполняется в браузере и наряду с другими средствами разработки, которые вы используете каждый день, например Visual Studio Code.  

Как разработчик браузера на основе хрома вы должны чувствовать себя комфортно в новом браузере Microsoft Edge.  Microsoft Edge \(Chromium\) DevTools работает так же, как и средства разработчика, которые вы уже знаете и используете.  Средства разработчика Microsoft Edge \(Chromium\) часто называются Microsoft Edge \(Chromium\) DevTools или DevTools.  Дополнительные сведения см. в новых решениях [Microsoft Edge (Chromium) DevTools.][DevtoolsGuideChromiumWhatsNewIndex]  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Если вы ранее разрабатывали для Microsoft Edge \(EdgeHTML\) и оценивали новый Microsoft Edge, теперь он предоставляет отличные новые средства для создания и тестирования веб-страниц проще и быстрее.  

## <a name="open-the-devtools"></a>Откройте DevTools  

Microsoft Edge DevTools — это набор инструментов, встроенных непосредственно в браузер Microsoft Edge.  DevTools позволяет выполнять следующие задачи непосредственно в браузере.  

*   Проверка и внесение изменений на веб-страницу HTML  
*   Изменить CSS и мгновенно просмотреть, как отрисовка веб-страницы  
*   Просмотрите все утверждения из переднего кода `console.log()` JavaScript  
*   Отламыв сценарий, установите точки разрыва и перешагите строку кода по строке  
    
Дополнительные примеры функций, которые предоставляют DevTools, чтобы упростить и ускорить создание и тестирование веб-страницы в Microsoft Edge.  

Открытие DevTools  

*   Выбор `F12` 
*   Выберите `Ctrl` + `Shift` + `I` \(Windows/Linux\) `Command` + `Option` + `I` или \(macOS\)  
    
Если вы хотите увидеть HTML или CSS для элемента на вашем сайте, щелкните правой кнопкой мыши элемент и выберите **Проверить,** чтобы перейти в **элемент Elements.**  Чтобы открыть DevTools в **режиме Inspect Element,** выберите `Ctrl` + `Shift` + `C` \(Windows/Linux\) `Command` + `Option` + `C` или \(macOS\). Режим **Элемента Inspect позволяет** выбрать элемент на веб-странице и отобразить HTML и CSS в **средстве Elements.**  

Если вы хотите просмотреть журналы из переднего кода JavaScript или быстро запустить сценарий, откройте **консоль**.   Чтобы запустить **консольный** инструмент в DevTools, выберите `Ctrl` + `Shift` + `J` \(Windows/Linux\) `Command` + `Option` + `J` или \(macOS\).  

## <a name="core-tools"></a>Основные средства  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Основные средства Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Основные средства Microsoft Edge (Chromium) DevTools  
:::image-end::: 

В Microsoft Edge \(Chromium\) DevTools содержатся следующие средства.  

*   Средство **Elements** для редактирования HTML и CSS, проверки свойств доступности, просмотра слушателей событий и набора точек перенастройки DOM  
*   Консоль **для** просмотра и фильтрации сообщений журналов, проверки объектов JavaScript и узлов DOM и запуска JavaScript в контексте выбранного окна или кадра  
*   Средство **Sources** для открытия и редактирования кода, набора точек разрыва, шага по коду и отображения состояния веб-страницы
*   Средство **Network** для мониторинга и проверки запросов и ответов из кэша сети и браузера   
*   Средство **performance** для профиля времени и системных ресурсов, необходимых вашему сайту  
*   Средство **памяти** для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях времени работы кода  
*   Средство **приложения** для проверки, изменения и отработки манифестов веб-приложений, сотрудников служб и кэшей сотрудников службы.  Вы также можете проверять и управлять хранилищем, базами данных и кэшами из **средства приложения.**  
*   Средство **безопасности** для отлагораживание проблем безопасности и обеспечения правильной реализации HTTPS на веб-странице.  HTTPS обеспечивает критически важную безопасность и целостность данных как для вашего сайта, так и для пользователей, которые предоставляют личную информацию на вашем сайте.  
*   Средство **аудита** \(теперь **переименовано Маяк**\) для запуска аудита веб-страницы.  Результаты аудита помогают повысить качество сайта следующими способами.  
    *   Ловите распространенные ошибки, связанные с доступностью, безопасностью, выполнением и так далее.  
    *   Исправление каждой ошибки.  
    *   Сборка PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Отправка [отзывов и запросов на функции.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## <a name="extensions"></a>Расширения  

Возможно, вы получили доступ к DevTools с помощью расширений при диагностике и отладке проблем при построении веб-страниц \(или apps\). Расширения Microsoft Edge приобретаются из [надстройок Microsoft Edge.][MicrosoftEdgeAddonsExtensions]  В [надстройке Microsoft Edge][MicrosoftEdgeAddonsExtensions]просмотрите расширения DevTools из категории средства разработчика или найдите определенное расширение. ****  

Кроме того, можно добавить расширения из [Веб-магазина Chrome.][GoogleChromeWebstoreExtensions]  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store в Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store в Microsoft Edge  
:::image-end:::  

В верхней части выберите **Разрешить расширения** из других магазинов, а затем выберите **Разрешить** в диалоговом окантове, который отображается.  

> [!NOTE]
> Расширения, установленные из источников, не в microsoft Store, непроверены и могут влиять на производительность браузера.  

Выберите **Добавить в Chrome,** чтобы добавить расширение DevTools в Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Добавление расширения из Chrome Web Store в Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Добавление расширения из Chrome Web Store в Microsoft Edge  
:::image-end:::  

## <a name="shortcuts"></a>Ярлыки  

Следующие ярлыки контролируют главное окно DevTools, работают во всех средствах или обоих.  

| Действие | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Show/Hide DevTools \(открывает для последнего просмотра средство\) | `F12` или `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Показать консоль | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Покажите devTools в режиме **Inspect Element Mode,** который позволяет выбрать элемент и отобразить HTML и CSS в **средстве Elements** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Показать параметры | `?` или `Fn`+`F1` | `?` или `Fn`+`F1` |  
| Показать следующую панель | `Ctrl`+`]` | `Command`+`]` |  
| Показать предыдущую панель | `Ctrl`+`[` | `Command`+`[` |  
| Dock the DevTools in the last position used.  Если devTools остаются в позиции по умолчанию для всего сеанса, ярлык отсоединяя DevTools в отдельное окно | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Режим управления **устройствами** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode,** который позволяет выбрать элемент и отобразить HTML и CSS в **средстве Elements** | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Показать меню команды | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Показать/скрыть ящик | `Esc` | `Esc` |  
| Обновление.  Обновляет веб-страницу с помощью кэша.  | `F5` или `Ctrl`+`R` | `Command`+`R` |  
| Hard Refresh.  Заставляет Microsoft Edge снова загружать ресурсы и перезагружать их.  Используемые ресурсы могут приходить из кэшной версии | `Ctrl`+`F5` или `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста в текущей панели.  Не поддерживается в средствах аудита, приложения и безопасности | `Ctrl`+`F` | `Command`+`F` |  
| Показать средство поиска в ящике, которое позволяет искать текст во всех загруженных ресурсах | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Откройте файл в панели Источники | `Ctrl`+`O` или `Ctrl`+`P` | `Command`+`O` или `Command`+`P` |  
| Масштабирование | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Ctrl`+`-` | `Command`+`-` |  
| Восстановление масштабирования по умолчанию | `Ctrl`+`0` | `Command`+`0` |  
| Выполнить фрагмент | `Ctrl`+`O`или `Ctrl` + `P` , `!` введите с именем скрипта, а затем выберите `Enter` | Выберите `Command` + `O` или `Command` + `P` введите `!` с именем скрипта, а затем выберите `Enter` |  
| Показать нередактируемый исходный код HTML на новой вкладке | `Ctrl`+`U` | Н/Д |  

> [!NOTE]
> Если вы отладили и приостановили работу в точке перерыва, ярлык **"Обновление"** сначала возобновляет время запуска.  

## <a name="see-also"></a>См. также  

*   [DevTools для начинающих: начало работы с HTML и DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Протокол Microsoft Edge (Chromium) DevTools][DevtoolsProtocolChromiumIndex]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Если вы хотите просмотреть последние функции, приходя в [DevTools,][DevtoolsGuideChromiumWhatsNewIndex]скачайте [Microsoft Edge Canary,][MicrosoftedgeinsiderDownload]который строится ночью.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools для начинающих: начало работы с HTML и doM | Документы Майкрософт"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2021/02/devtools "Что нового в Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Microsoft Edge (Chromium) Протокол DevTools | Документы Майкрософт"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Надстройки Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  
