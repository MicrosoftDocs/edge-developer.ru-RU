---
description: Узнайте, как оценить производительность выполнения в Microsoft Edge DevTools.
title: Начало работы с анализом производительности выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 074c112b99abb4689cac2274338f2276bc46b4ae
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398723"
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

# <a name="get-started-with-analyzing-runtime-performance"></a>Начало работы с анализом производительности выполнения  

> [!NOTE]
> Чтобы узнать, как сделать загрузку страниц быстрее, перейдите к [оптимизации скорости веб-сайта][DevtoolsSpeedGetStarted].  

Производительность выполнения — это производительность страницы при ее запуске, а не загрузка.  В следующей статье руководства рассказывается об использовании панели Microsoft Edge DevTools Performance для анализа производительности выполнения.  С точки зрения модели **RAIL** навыки, которые вы узнаете в этом руководстве, полезны для анализа этапов ответа, анимации и простоя страницы.  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a>Начало работы  

В следующем руководстве вы открываете DevTools на странице в прямом эфире и используете панель **Performance,** чтобы найти узкие места производительности на странице.  

1.  Откройте Microsoft Edge в **режиме InPrivate.**  Режим InPrivate гарантирует, что Microsoft Edge работает в чистом состоянии.  Например, если установлено множество расширений, расширения могут создавать шум в измерениях производительности.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Загрузите следующую страницу в окне InPrivate.  Страница — это демонстрация, которую вы собираетесь профилю.  На странице показана куча маленьких значков, перемещаясь вверх и вниз.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\) для открытия DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       Демонстрация слева и DevTools справа  
    :::image-end:::  
    
    > [!NOTE]
    > Для остальных фигур DevTools [][DevtoolsCustomizePlacement] отсоедино в отдельное окно, чтобы лучше сосредоточиться на содержимом.  
    
### <a name="simulate-a-mobile-cpu"></a>Имитация мобильного ЦП  

Мобильные устройства имеют гораздо меньше мощности процессора, чем настольные компьютеры и ноутбуки.  При профилирование страницы используйте регулирование ЦП для имитации работы страницы на мобильных устройствах.  

1.  В DevTools выберите средство **Performance.**  
1.  Убедитесь, что **включен почтовый ящик Screenshots.**  
1.  Выберите **Параметры** захвата \(![ Параметры захвата][ImageCaptureSettingsIcon]\).  В DevTools раскрываются параметры, связанные с тем, как он фиксирует показатели производительности.  
1.  Для **ЦП**выберите **4x замедление.**  DevTools разгорарит ЦП так, чтобы он был в 4 раза медленнее обычного.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Throttle CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Throttle CPU  
    :::image-end:::  
    
    > [!NOTE]
    > При тестировании других страниц; если вы хотите убедиться, что каждая страница хорошо работает на мобильных устройствах низкого уровня, установите регулирование ЦП до **замедления 6x**.  Демонстрация не работает с 6x замедлением, поэтому она просто использует замедление 4x для учебных целей.  
    
### <a name="set-up-the-demo"></a>Настройка демонстрации  

Сложно создать демонстрацию производительности выполнения, которая последовательно работает для всех читателей веб-сайта.  В следующем разделе вы можете настроить демонстрацию, чтобы убедиться, что ваш опыт относительно соответствует скриншотам и описаниям, независимо от конкретной настройки.

1.  Выберите **кнопку Добавить 10,** пока синие значки не будут двигаться заметно медленнее, чем раньше.  На компьютере высокого уровня можно выбрать его около 20 раз.  
1.  Выберите **Оптимизируйте**.  Синие значки должны двигаться быстрее и более плавно.  
    
    > [!NOTE]
    > Чтобы лучше отобразить разницу между оптимизированной и не оптимизированной версиями, выберите кнопку **Вычитание 10** несколько раз и попробуйте еще раз.  
    > Если вы добавим слишком много синих значков, вы можете максимально выйти из ЦП, а затем вы не сможете наблюдать серьезные различия в результатах для двух версий.  
    
1.  Выберите **Un-Optimize**.  Синие значки снова перемещаются медленнее и с большей вялой скоростью.  
    
### <a name="record-runtime-performance"></a>Запись выполнения  

При движении оптимизированной версии страницы синие значки перемещаются быстрее.  Почему так?  Предполагается, что обе версии перемещают значки одинаковое количество пространства за одно и то же время.  Возьмите запись в панели Performance, чтобы узнать, как определить узкие места производительности в не оптимизированной версии.  

1.  В DevTools выберите **Запись** \(![ Запись][ImageRecordIcon]\).  DevTools фиксирует показатели производительности по мере выполнения страницы.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Профиль страницы" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Профиль страницы  
    :::image-end:::  
    
1.  Подождите несколько секунд.  
1.  Выберите **Остановку**.  DevTools прекращает запись, обрабатывает данные, а затем отображает результаты на панели Performance.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Результаты профиля" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Результаты профиля  
    :::image-end:::  
    
Wow, это подавляющее количество данных.  не волнуйтесь, вскоре процесс станет более емким.  

## <a name="analyze-the-results"></a>Анализ результатов  

После записи производительности страницы измерьте качество производительности страницы и найдите причины.  

### <a name="analyze-frames-per-second"></a>Анализ кадров в секунду  

Основной метрикой для измерения производительности любой анимации является кадры в секунду \(FPS\).  Пользователи рады, когда анимации запускаются с 60 FPS.  

1.  Просмотрите **диаграмму FPS.**  Всякий раз, когда красная планка отображается выше **FPS,** это означает, что рамка упала настолько низко, что это, вероятно, вредит пользовательскому опыту.  В общем, чем выше зеленая планка, тем выше FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Диаграмма **FPS**  
    :::image-end:::  
    
1.  Ниже **диаграммы FPS** отображается диаграмма **ЦП.**  Цвета в диаграмме **ЦП** соответствуют цветам в панели **Сводка** в нижней части панели Performance.  Тот факт, что **диаграмма ЦП** заполнена цветом, означает, что во время записи ЦП был максимум.  Всякий раз, когда ЦП в течение длительных периодов времени, это показатель того, что вы должны найти способы сделать меньше работы.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Диаграмма ЦП и панель сводки" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Диаграмма **ЦП** и **панель сводки**  
    :::image-end:::  
    
1.  Наведите курсор **на диаграммы FPS,** **CPU**или **NET.**  В DevTools показан снимок экрана страницы в этот момент времени.  Переместите мышь влево и вправо, чтобы переиграть запись.  Действие ссылается на очистку, и оно полезно для ручного анализа прогрессии анимации.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Просмотр экрана страницы вокруг отметки 2500 мс записи" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Просмотр экрана страницы вокруг отметки 2500 мс записи  
    :::image-end:::  
    
1.  В разделе **Frames** наведите курсор на один из зеленых квадратов.  DevTools показывает FPS для этого конкретного кадра.  Каждый кадр, вероятно, значительно ниже целевой 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Наведите курсор на кадр" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Наведите курсор на кадр  
    :::image-end:::  
    
Конечно, на дисплее указывается, что веб-страницы выполняются не очень хорошо.  Но в реальных сценариях это может быть не так понятно, поэтому все средства, необходимые для измерения, пригодятся.  

#### <a name="bonus-open-the-fps-meter"></a>Бонус: Откройте счетчик FPS  

Еще одним удобным средством является счетчик FPS, который предоставляет оценки для FPS в режиме реального времени по мере работы страницы.  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
1.  Начните `Rendering` печатать в **командном меню** и выберите **show Rendering**.  
1.  В **средстве визуализации** варим **счетчик FPS.**  Новая накладка отображается в правом верхнем правой части представления.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       Счетчик **FPS**  
        :::image-end:::  
    
1.  Выключите **счетчик FPS и** выберите, чтобы закрыть средство `Escape` **отрисовки.**  В этом руководстве не используется **счетчик FPS.**  
    
### <a name="find-the-bottleneck"></a>Найти узкое место  

После измерения и проверки того, что анимация не выполняется хорошо, следующий шаг — ответить на вопрос "почему?".  

1.  Если события не выбраны, панель **Сводки** показывает разбивку активности.  Большая часть времени отрисовки проводилась на странице.  Так как производительность — это искусство делать меньше работы, ваша цель состоит в том, чтобы сократить время, затраченное на выполнение рендеринга.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Панель Сводка" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       Панель **Сводка**  
    :::image-end:::  
    
1.  **Расширь раздел Main.**  DevTools со временем показывает вам схему действий на основном потоке.  X-axis представляет запись со временем.  Каждый бар представляет событие.  Более широкая планка означает, что событие заняло больше времени.  Y-axis представляет собой стек вызовов.  Если события укладываются друг на друга, это означает, что верхние события вызывают более низкие события.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Основной **** раздел  
    :::image-end:::  
    
1.  В записи много данных.  Масштабирование одного события; выберите, удерживайте и перетаскивайте курсор над обзором **,** который является разделом, который включает диаграммы **FPS,** **CPU**и **NET.**  В **основном** разделе и **панели Сводка** отображаются только сведения для выбранной части записи.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Масштабирование события" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Масштабирование события  
    :::image-end:::  
    
    > [!NOTE]
    > Другой способ масштабирования, фокусировать **основной** раздел, выбрать фон или событие, а также выбрать `W` , или `A` `S` `D` .  
    
    1.  Сосредоточься на красном треугольнике в правом верхнем справа от события **"Кадр** анимации".  Всякий раз, когда отображается красный треугольник, это предупреждение о том, что может возникнуть проблема, связанная с событием.  
    
    > [!NOTE]
    > Событие **"Запуск кадров анимации"** происходит при запуске [ `requestAnimationFrame()` вызова.][MDNWebRequestAnimationFrame]  
    
1.  Выберите событие **"Кадр анимации".**  На **панели Сводки** теперь показаны сведения об этом событии.  Обратите внимание на **ссылку Reveal.**  После его выбора в DevTools будет выделено событие, которое инициировало событие **"Кадры анимации".**  Кроме того, сосредоточься на **ссылкеapp.js:95.**  После его выбора отображается соответствующая строка в исходный код.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Дополнительные сведения о событии "Кадр анимации"." lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Дополнительные сведения о **событии "Кадр анимации".**  
    :::image-end:::  
    
    > [!NOTE]
    > После выбора события используйте клавиши стрелки, чтобы выбрать события рядом с ней.  
    
1.  В **событии app.update** имеется куча фиолетовых событий.  Если каждое фиолетовое событие было более широким, оно выглядит так, будто на каждом из них может быть красный треугольник.  
1.  Выберите одно из событий **фиолетового макета.**  DevTools предоставляет дополнительные сведения о событии в панели **Сводка.**  Действительно, существует предупреждение о принудительном повторном потоке \(другое слово для макета\).  
    
1.  В панели **Сводка** выберите ** ссылкуapp.js:71** в **статье Layout Forced**.  DevTools принимает вас к строке кода, которая заставила макет.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Строка кода, вызываемая принудительной компоновкой" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       Строка кода, вызываемая принудительной компоновкой  
    :::image-end:::  
    
    > [!NOTE]
    > Проблема с кодом заключается в том, что в каждом кадре анимации он изменяет стиль для каждого значка, а затем запрашивает положение каждого значка на странице.  Так как стили изменились, браузер не знает, изменилась ли каждая позиция значка, поэтому для вычисления новой позиции ему необходимо изменить макет значка.  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

Это было многому научиться.  Теперь в базовом рабочего процессах имеется прочная основа для анализа производительности выполнения.  Молодец.  

### <a name="bonus-analyze-the-optimized-version"></a>Бонус: анализ оптимизированной версии  

Используя только что выучатые процессы **** и инструменты, выберите Оптимизируйте в демонстрации, чтобы включить оптимизированный код, с помощью другой записи производительности и проанализировайте результаты.  От улучшенного кадра до сокращения событий в схеме пламени в разделе **Main** оптимизированная версия приложения работает гораздо меньше, что приводит к повышению производительности.  

> [!NOTE]
> Даже оптимизированная версия не является отличной, так как она управляет `top` свойством каждого значка.  Лучше придерживаться свойств, которые влияют только на композитную работу.  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a>Дальнейшие действия

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

Чтобы удобнее работать с инструментом **Performance,** практика позволяет совершенствоваться.  Попробуйте профилирование страниц и анализ результатов.  Если у вас возникли вопросы о **** результатах, используйте значок Отправка отзывов, выберите `Alt` + `Shift` + `I` \(Windows, Linux\), выберите `Option` + `Shift` + `I` \(macOS\) [][TwitterEdgeDevtools]или чирикать команду DevTools .  Если это возможно, включаем скриншоты или ссылки на воспроизводимые страницы.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Значок **Feedback** в Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   Значок **Отправка** отзывов в Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Наконец, существует множество способов повышения производительности выполнения.  В этой статье основное внимание было уделялось одному конкретному узкому узким местам анимации, чтобы предоставить вам целенаправленный тур по панели Performance, но это только одно из многих узких моментов, с которыми вы можете столкнуться.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools (Undock, dock to bottom, dock to left)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools — публикация чирикать | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\\\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
