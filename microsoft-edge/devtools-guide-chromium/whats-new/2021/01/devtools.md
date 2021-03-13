---
description: Средство What's New теперь является Welcome, Visual Font Editor в области стилей, средства отладки CSS Flexbox и другие.
title: Новые возможности в DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2722da0093b3ba6521b5190e61bb208e02a2041e
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408341"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Что нового в DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>What's New is now Welcome  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Средство **What's New** в Microsoft Edge DevTools теперь имеет новый внешний вид и новое имя:  **Welcome**.  Средство **Welcome** по-прежнему отображает последние новости и обновления DevTools.  Теперь он также включает ссылки на документацию Microsoft Edge DevTools, способы отправки отзывов и другие.  Чтобы **отобразить** средство Welcome после каждого обновления в Microsoft Edge, выберите почтовый ящик рядом с вкладками **Open после** каждого обновления под заголовком.  Чтобы закрыть средство **Welcome,** выберите **X** в правой части заголовка вкладки.  Если вы предпочитаете оригинальный инструмент **What's New,** перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и удалите почтовый ящик рядом со вкладками  >  **** **Enable Welcome.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Выделено средство Welcome" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   Выделено средство **Welcome**  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Редактор visual Font в области Стилей  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

При работе со шрифтами в CSS используйте новый визуальный [редактор шрифтов.][DevtoolsInspectStylesEditFonts]  Вы можете определить откатные шрифты и использовать ползунки для определения веса, размера, высоты строки и интервалов.  Редактор **шрифта** помогает выполнить следующие действия.  

*   Переключение между единицами для различных свойств шрифта  
*   Переключатель между ключевыми словами для различных свойств шрифта  
*   Преобразование единиц  
*   Создание точного кода CSS  
    
Чтобы включить этот эксперимент, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новые средства редактора шрифтов  >  **** в **области Стилей**.  Дополнительные сведения перейдите к редактированию стилей и параметров шрифтов CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Редактор visual Font выделен в области Стилей" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   Редактор visual **Font выделен** в области **Стилей**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Средства отладки CSS Flexbox  

Функции отладки Flexbox находятся в активной разработке.  Чтобы включить эксперимент для следующих двух функций, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новые  >  **** **функции отладки CSS Flexbox**.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1136394 и][CR1136394] [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>Новый значок Flexbox (flex) помогает определить и отобразить контейнеры flex  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

В **инструменте Elements** новый значок Flexbox (flex) помогает определить контейнеры Flexbox в коде.  Выберите значок Flexbox \(flex\) для того, чтобы включить или отключить эффект наложения, который описывает контейнер Flexbox.  Можно настроить цвет наложения в области **Макет,** расположенной рядом со **Стили** и **Вычисления.**  

:::row:::
   :::column span="":::
      Чтобы включить и отключить эффект наложения, который описывает контейнер Flexbox, выберите значок Flexbox `flex` \( \) .  
   :::column-end:::
   :::column span="":::
      Вы можете настроить цвет наложения в области **Макет** рядом со **стили** и **вычисления**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Выделены значок Flexbox (flex) и веб-страницы" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Значок и веб-страницы **Flexbox** `flex` \( \) выделены :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Наложения Flexbox, выделенные в области Макет" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Наложения **Flexbox,** выделенные в области **Макет**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-gridlines-when-flexbox-layouts-change-using-css-properties"></a>Отображение значков выравнивания и линий сетки при изменении макетов Flexbox с помощью свойств CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

При редактировании CSS для макета Flexbox автокомплекты CSS в области **Стилей** теперь отображают полезные значки рядом с соответствующими свойствами Flexbox.  Чтобы попробовать эту новую функцию, откройте средство **Elements** и выберите контейнер flex.  Затем добавьте или измените свойство в этом контейнере в области **Стилей.**  

:::row:::
   :::column span="":::
      В меню автозаполнения теперь отображаются значки, которые указывают влияние свойств выравнивания, таких как `align-content` и `align-items` .  
   :::column-end:::
   :::column span="":::
      Кроме того, в DevTools теперь отображается направляющая строка, которая поможет вам лучше просмотреть `align-items` свойство CSS.  Поддерживается `gap` также свойство CSS.  На следующем рисунке за установлено свойство CSS и отображается шаблон штриховки для `gap` `gap: 12px;` каждого пробела.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Меню автозаполнения, выделенное для свойств CSS, которые начинаются с выравнивания" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Меню autocomplete, выделенное для свойств CSS, которые начинаются с `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Пробел Flexbox в свойствах и веб-странице CSS выделен" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` в свойствах CSS и выделенной веб-странице  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Быстро добавьте средства с помощью новой кнопки More Tools  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Теперь у вас есть новый способ открыть дополнительные средства в Microsoft Edge DevTools.  После этого эксперимента значок **More Tools** отображается в качестве знака плюс `+` () справа от основной панели.  Чтобы отобразить список других средств для добавления в главную панель, выберите значок **More Tools** `+` \( \) .  Чтобы включить этот эксперимент, перейдите к [параметрам][DevtoolsCustomizeIndexSettings]  >  **Эксперименты,** а затем выберите почтовый ящик рядом с включить + меню вкладки кнопки, чтобы **открыть больше средств**.  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Дополнительные средства, выделенные в DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Дополнительные средства,** выделенные в DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Вспомогательные технологии теперь объявляют положение и количество предложений CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

При редактировании CSS вы получаете отсев функций.  Эта функция была недоступна пользователям вспомогательных технологий, так как она объявлена в Microsoft Edge версии 89.  Пользователь вспомогательных технологий теперь может перемещаться по предложениям CSS в области **Стилей.**  В microsoft Edge версии 88 и ранее вспомогательные технологии, объявленные пользователем, переходили по списку предложений при редактировании CSS в области `Suggestion` **Стилей.**  В microsoft Edge версии 89 пользователь вспомогательных технологий теперь слышит позицию и количество текущего предложения.  Каждое предложение объявляется по мере перемещения пользователя по списку предложений, таких как Предложение 3 из 5.  Чтобы узнать больше о написании CSS в DevTools, перейдите на [изменение CSS][DevtoolsCssReferenceChangeCss].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1157329][CR1157329].  

Чтобы просмотреть видео, которое отображает и читает вслух несколько предложений с включенным этим экспериментом, перейдите в voiceover, объявляя параметры [devtools](https://youtu.be/9TcUpleEwwA) на YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Предложение, выделено в области Стилей" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Список, `suggestion` выделенный в области **Стилей**  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Эмулировать Surface Duo и Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Проверьте внешний вид веб-сайта или приложения на следующих устройствах в Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
**Включи функции экспериментальной** веб-платформы, чтобы получить доступ к новой функции экранирования экрана [CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]  Перейдите `edge://flags` к флажку рядом с функциями **экспериментальной веб-платформы**и перейдите к ней.  Чтобы улучшить веб-сайт или приложение для двухэкранных и складных устройств, используйте следующие функции при [эмулации устройства.][DevtoolsDeviceModeIndex]  

*   [Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]— это когда веб-сайт \(или app\) отображается на обоих экранах.  
*   [Отрисовка шва,][DualScreenIntroductionHowToWorkWithSeam]который является пространством между двумя экранами.  
    
Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Эмулировать двойной экран" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Эмулировать двойной экран  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Средства разработки Microsoft Edge для Visual Studio версии кода 1.1.2  

Средства [разработки Microsoft Edge для Visual Studio][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.2 для Microsoft Visual Studio код имеет следующие изменения со времени предыдущего выпуска.  Microsoft Visual Studio обновления кода автоматически.  Чтобы вручную обновить версию 1.1.2, перейдите к [обновлению расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Добавлена **кнопка Закрыть экземпляр** к каждому элементу в целевом списке \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Неровная версия [Microsoft Edge DevTools][DevtoolsMain] с 84.0.522.63 до [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Включено [debugger для Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] в качестве зависимостей \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Реализованный параметр параметры для изменения тем расширения \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Вы можете файл проблемы и внести свой вклад в расширение [на vscode-edge-devtools GitHub репо][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Захват экрана узла за пределами viewport  

В microsoft Edge версии 89 скриншоты узлов более точны, захватывая полный узел, даже если содержимое узла не отображается в представлении.  В **инструменте Elements** наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите снимок экрана **узла Capture**.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Снимок экрана узла, выделенного в контексте меню в средстве Elements" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Снимок экрана** узла, выделенного в контексте меню в **средстве Elements**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Обновления инструмента Elements  

#### <a name="support-forcing-the-target-css-state"></a>Поддержка принудительного состояния :target CSS  

Теперь можно использовать DevTools для принудительного [использования псевдокласса][MdnDocsWebCssTarget] CSS.  Псевдокласс запускается, когда уникальный элемент \(целевой элемент\) имеет фрагмент `:target` `id` URL-адреса.  Например, `http://www.example.com/index.html#section1` `:target` URL-адрес запускает псевдокласс на элементе HTML с `id="section1"` помощью .  Чтобы попробовать демонстрацию с выделенной частью 1, перейдите к [CSS:target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Выделенная веб-страница без принудительного CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Веб-страницу, выделенную без принудительного CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forced and webpage highlighted  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Использование элементов Duplicate для копирования элементов  

Используйте новый ярлык **элемента Дубликат,** чтобы клонировать элемент.  В **инструменте Elements** наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\), выберите **элемент Дубликат**.  Новый элемент создается под выбранным элементом.  Чтобы дублировать элемент с помощью клавиши, выберите `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) или `Shift` + `Option` + `Down Arrow` \(macOS\).  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Элемент Duplicate выделен в контексте меню элемента в средстве Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   Элемент **Duplicate выделен** в контексте меню элемента в **средстве Elements**  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Выбор цветов для настраиваемого свойства CSS  

В **области Стилей** теперь отображаются цветовые выборщики для настраиваемого свойства CSS.  Чтобы пройти цикл через форматы RGBA, HSLA и Hex цветового значения, удерживайте и выберите `Shift` выбор цвета.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Выбор цветов для настраиваемого свойства CSS" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Выбор цветов для настраиваемого свойства CSS  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Копирование классов и свойств CSS  

Теперь можно быстрее скопировать свойства CSS с помощью нескольких новых параметров в контекстной меню.  В **инструменте Elements** выберите элемент.  Чтобы скопировать значение в области **Стилей,** наведите курс на класс CSS или свойство CSS, откройте контекстное меню \(правой кнопкой мыши\) и выберите вариант копирования.  

:::row:::
   :::column span="":::
      Копирование параметров для класса CSS.  
      
      | Параметр | Сведения |  
      |:--- |:--- |  
      | **Выбор копирования** | Скопируйте имя текущего селектора. |  
      | **Правило копирования** | Скопируйте правило текущего селектора. |  
      | **Копирование всех деклараций** | Скопируйте все объявления в соответствии с текущим правилом, включая не допустимые и префиксные свойства. |  
   :::column-end:::
   :::column span="":::
      Копирование параметров свойства CSS.  
      
      | Параметр | Сведения |      
      |:--- |:--- |  
      | **Декларация копирования** | Скопируйте объявление текущей строки. |  
      | **Скопируйте свойство** | Скопируйте свойство текущей строки. |  
      | **Значение copy** | Скопируйте значение текущей строки. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Копирование параметров класса CSS в контекстной меню" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Копирование параметров класса CSS в контекстной меню  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Копирование параметров свойства CSS в контекстной меню" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Копирование параметров свойства CSS в контекстной меню  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1152391][CR1152391].  

### <a name="cookies-updates"></a>Обновления файлов cookie  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Новый параметр отображения файлов cookie с декодом URL-адресов  

Теперь вы можете отобразить значение cookies с декодированием URL-адресов в **области Cookies.**  Чтобы отобразить расшифровку cookie, перейдите к области ****  >  **cookie-файлов** приложений, выберите любое cookie в списке и выберите почтовый ящик рядом с декодированием **URL-адреса.**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Возможность отображения файлов cookie с декодом URL-адресов" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Возможность отображения файлов cookie, расшифровав URL-адрес  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Фильтрация и очистка видимых файлов cookie  

В Microsoft Edge версии 88 **** или более ранней версии средство приложения предоставляет только способ очистки всех файлов cookie с помощью кнопки **Clear all cookies.**  В Microsoft Edge версии 89 теперь можно выбрать фильтруемое cookie **Clear,** чтобы удалить только фильтрованные файлы cookie.  Чтобы отфильтровать файлы cookie, перейдите **к**  >  **cookie-файлам приложений**и введите текстовое ящик **фильтра.**  Чтобы удалить отображаемое печенье, выберите кнопку **Clear filtered cookies.**  Чтобы отобразить все остальные файлы cookie, очистить текст фильтра.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Очистка только видимых файлов cookie" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Очистка только видимых файлов cookie  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Новый вариант очистки сторонних файлов cookie в области хранения  

DevTools теперь очищает только первопартийные файлы cookie по умолчанию.  Чтобы очистить данные веб-сайта и только однопартийные файлы cookie, перейдите в **хранилище**приложений, а затем выберите  >  **** clear **site data.**  

Чтобы очистить данные веб-сайта и все файлы cookie, перейдите в **хранилище**  >  **приложений.**  Выберите почтовый ящик рядом с **включив**сторонние файлы cookie, а затем выберите **clear site data.**  

Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Возможность очистки сторонних файлов cookie" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Возможность очистки сторонних файлов cookie  
:::image-end:::  

### <a name="network-tool-updates"></a>Обновления сетевых инструментов  

#### <a name="persist-record-network-log-setting"></a>Параметр сетевого журнала сохраняемой записи  

В microsoft Edge версии 88 или более ранней версии DevTools сбрасывает параметр журнала журнала записи сети при обновлении веб-страницы. ****  В microsoft Edge версии 89 в DevTools теперь сохраняется параметр **журнала журнала записи** сети.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Журнал записи сети" lightbox="../../media/2021/01/network-log.msft.png":::
   Журнал записи сети  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>Online option is now No throttling option  

Параметр сетевой эмуляции **Online** теперь переименован в **No Throttling.**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Нет параметра регулирования" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Нет параметра регулирования**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Новые параметры копирования в средстве консоли, средстве Sources и области стилей

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Копирование объекта в средстве консоли и источников  

Теперь можно скопировать значения объектов в **средствах консоли** и **источников.**  Возможность копирования значений объектов полезна при работе с большими объектами.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1148353][CR1148353] и [1149859][CR1149859].  

:::row:::
   :::column span="":::
      В **средстве Консоли** наведите курсор на объект, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите **объект Copy**.  
   :::column-end:::
   :::column span="":::
      В **** средстве Источники на точке останова наведите **** курсор на объект, в окне всплывающее окно Объекта выделяем объект, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите объект **Copy**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Копирование объекта в консоли" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Копирование объекта в **консоли**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Копирование объекта в источниках" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Копирование объекта в **источниках**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Скопируйте имя файла в инструменте Sources и области стилей  

Теперь можно скопировать имя файла с помощью контекстного меню.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1155120][CR1155120].  

:::row:::
   :::column span="":::
      В **средстве Источники** введите имя файла, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите **имя файла Copy**.  
   :::column-end:::
   :::column span="":::
      В **инструменте Elements** > **стилей** наведите курсор на имя файла, откройте контекстное меню \(правой кнопкой мыши\), а затем выберите имя файла **Copy**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Скопируйте имя файла в Источниках" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Скопируйте имя файла в **Источниках**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Скопируйте имя файла в области Стилей" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Скопируйте имя файла в **области Стилей**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Сведения об обновлениях в Frame  

#### <a name="service-workers-information-in-frame-details"></a>Сведения о работниках служб в подробностях Frame  

В DevTools теперь перечислены выделенные работники службы в родительском кадре.  На следующем рисунке отображаются сведения о сотрудниках службы.  Чтобы отобразить сведения об сотруднике службы, перейдите к **сотрудникам службы кадров**приложений и  >  ****  >  `top`  >  **** выберите сотрудника службы.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Сведения о работниках служб в подробностях Frames" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Сведения о работниках** служб в **подробностях Frames**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Измерение сведений о памяти в подробностях Frame  

Теперь состояние API отображается `performance.measureMemory()` в разделе доступность **API.**  Новый `performance.measureMemory()` API оценивает использование памяти всей веб-страницы.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Измерение памяти" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Измерение памяти  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Отброшенные кадры в средстве Performance  

При [анализе производительности нагрузки][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]в средстве Performance раздел **Frames** теперь отмечает отброшенные кадры как красные.  Чтобы отобразить частоту кадров, наведите курс на отброшенный кадр.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Отброшенные кадры" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Отброшенные кадры  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Новый расчет контрастности цвета — расширенный перцептивный контрастный алгоритм (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Расширенный перцептивный контрастный алгоритм [(APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] заменяет коэффициент контраста руководящих принципов [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] в [цветопоискатель][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA — это новый способ вычисления контраста.  Он основан на современных исследованиях по восприятию цвета.  По сравнению с рекомендациями AA/AAA APCA больше зависит от контекста.  Контраст рассчитывается на основе следующих пространственных свойств текста, цвета и контекста.  

*   Пространственные свойства текста, которые включают вес шрифта и размер.  
*   Пространственные свойства цвета, которые включают предполагаемый контраст между текстом и фоном.  
*   Пространственные свойства контекста, которые включают окружающий свет, окружение и предназначенную цель.  
    
Чтобы включить этот эксперимент, перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и выберите почтовый ящик рядом с включить новый расширенный перцептивный контрастный алгоритм (APCA), заменив предыдущее отношение контраста и рекомендации  >  **** **AA/AAA**.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA в выборке цвета" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA в выборке цвета  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Новые возможности в DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Просмотр соотношения контрастности текстового элемента в справочном справочнике Color Picker - Accessibility | Документы Майкрософт"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Изменение CSS — справочные | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — эмулировать двухэкранные и складные устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — эмулировать мобильные устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Производительность записи нагрузки — справочные | Документы Майкрософт"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Обзор средств разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Раздел 1 . CSS :целевая демонстрация для нового в DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229. Реализация выпадающих параметров для изменения тем | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: в том числе отладка для Microsoft Edge в качестве зависимостей | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Обновление версии Edge DevTools до 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248. Добавьте кнопки одного закрытия в панель экземпляров | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Выберите характеристики шрифта и фоновые цвета, чтобы обеспечить достаточный контраст для чтения | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Доверенные типы | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — расширение marketplace | Visual Studio Код"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR978059]: https://crbug.com/978059 "Выпуск 978059. Удаление файлов cookie при их фильтрации удалите все файлы cookie, а не только фильтрующие файлы | Ошибки Chromium"  
[CR997625]: https://crbug.com/997625 "Выпуск 997625: новая функция req | Необходимо выбрать, чтобы увидеть значение url-декодирования в файлах cookie | Ошибки Chromium"  
[CR1003629]: https://crbug.com/1003629 "Выпуск 1003629. Узел захвата больше не снимет снимок экрана узла ниже складки. | Ошибки Chromium"  
[CR1012337]: https://crbug.com/1012337 "Выпуск 1012337: Clear Site Data уничтожает сеанс Google на сайтах, не в google, | Ошибки Chromium"  
[CR1028078]: https://crbug.com/1028078 "Выпуск 1028078: в списке | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Выпуск 1054281: запрос на функции: Устройства DevTools должны подражать складным и двухэкранным устройствам | Ошибки Chromium"  
[CR1075865]: https://crbug.com/1075865 "Выпуск 1075865. Показать отброшенные кадры в графике devtools | Ошибки Chromium"  
[CR1093229]: https://crbug.com/1093229 "Выпуск 1093229: DevTools: предложение специализированного пользовательского интерфейса редактора шрифтов | Ошибки Chromium"  
[CR1121900]: https://crbug.com/1121900 "Выпуск 1121900: DevTools: обновление логики вычислений контрастности в новых спецификациях | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1122580]: https://crbug.com/1122580 "Выпуск 1122580: невозможно отключить запись сети при перезагрузке | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139949]: https://crbug.com/1139949 "Выпуск 1139949: наложение на Flexbox | Ошибки Chromium"  
[CR1147016]: https://crbug.com/1147016 "Выпуск 1147016. Выбор цвета не отображается в функции var(). | Ошибки Chromium"  
[CR1148353]: https://crbug.com/1148353 "Выпуск 1148353: запрос на функции: скопируйте объект с консоли devtools | Ошибки Chromium"  
[CR1149859]: https://crbug.com/1149859 "Выпуск 1149859: [запрос на функции][Консоль] добавьте объект копирования в элемент буфера обмена в контекстное меню | Ошибки Chromium"  
[CR1150797]: https://crbug.com/1150797 "Выпуск 1150797. Добавление меню контекста дубликатов элементов в панель Element | Ошибки Chromium"  
[CR1152391]: https://crbug.com/1152391 "Выпуск 1152391: поддержка копирования контекстного меню CSS в панели стилей | Ошибки Chromium"  
[CR1155120]: https://crbug.com/1155120 "Выпуск 1155120: [FR]Поддержка имени и номера строки | Ошибки Chromium"  
[CR1156628]: https://crbug.com/1156628 "Выпуск 1156628: DevTools: добавьте поддержку :target in force element state feature | Ошибки Chromium"  
[CR1157329]: https://crbug.com/1157329 "Выпуск 1157329: Доступность — рассказчик: Диктор не объявляет количество и положение для предложений, доступных для кода в вкладке Стили | Ошибки Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contrast (Enhanced) — способ удовлетворения WCAG (быстрая ссылка) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contrast (Minimum) — как соответствовать требованиям WCAG (быстрая ссылка) | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/01/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Местообладатель spanning"  
