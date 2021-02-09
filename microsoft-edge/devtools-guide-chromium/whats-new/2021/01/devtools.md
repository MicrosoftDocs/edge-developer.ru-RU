---
description: Теперь в качестве средства "Новые возможности" можно использовать редактор визуальных шрифтов в области стилей, средства отладки CSS Flexbox и другие возможности.
title: Новые возможности DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0a8a5e69281ced9421733059b554bd8cb997c7cd
ms.sourcegitcommit: 085046a5885c68243b763aaf6809fea43452403a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313778"
---
# Новые возможности DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Новые возможности теперь — добро пожаловать  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Новое **средство "Что нового"** в Microsoft Edge DevTools теперь имеет новый внешний вид и новое имя:  **Welcome**.  В **средстве** приветствия по-прежнему отображаются последние новости и обновления DevTools.  Теперь он также содержит ссылки на документацию Microsoft Edge DevTools, способы отправки отзывов и другие.  Чтобы **отобразить** средство приветствия после каждого обновления Microsoft Edge, после каждого обновления под заголовком выберите его рядом с вкладками **"Открыть".**  Чтобы закрыть средство **приветствия,** выберите **X** в правой части заголовка вкладки.  Если вы предпочитаете исходное средство **"Что** нового", перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и удалите его рядом с вкладками "Включить  >  **** **приветствие".**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="Выделено средство приветствия" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   Выделено **средство** приветствия  
:::image-end:::  

## Редактор визуальных шрифтов в области стилей  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

При работе со шрифтами в CSS используйте новый визуальный редактор [шрифтов.][DevtoolsInspectStylesEditFonts]  Можно определить откатные шрифты и использовать ползунки для определения веса, размера, высоты строки и интервалов шрифта.  Редактор **шрифтов** помогает выполнить следующие действия.  

*   Переключение между единицами для разных свойств шрифта  
*   Переключение между ключевыми словами для различных свойств шрифта  
*   Преобразование единиц  
*   Создание точного кода CSS  
    
Чтобы включить этот эксперимент, перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и выберите в области стилей новый редактор шрифтов рядом с параметром "Включить новые средства  >  **** **редактора шрифтов".**  Для получения дополнительных сведений перейдите к редактированию стилей и параметров шрифтов CSS в области стилей [в DevTools.][DevtoolsInspectStylesEditFonts]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1093229.][CR1093229]  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="Редактор визуальных шрифтов выделен в области стилей" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   Редактор **визуальных шрифтов** выделен в **области** стилей  
:::image-end:::  

## Средства отладки CSS Flexbox  

Функции отладки Flexbox находятся в активной разработке.  Чтобы включить эксперимент для следующих двух [][DevtoolsCustomizeIndexSettings]функций, перейдите к "Экспериментам параметров" и выберите этот параметр рядом с параметром "Включить новые функции отладки  >  **** **CSS Flexbox".**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1136394][CR1136394] и [1139949.][CR1139949]  

### Новый значок Flexbox (flex) помогает идентифицировать и отображать гибкие контейнеры  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

В **средстве Elements** новый значок Flexbox (flex) помогает идентифицировать контейнеры Flexbox в коде.  Выберите значок Flexbox \(flex\), чтобы включить или отключить эффект наложения, который описывает контейнер Flexbox.  Вы можете настроить цвет наложения в **** области макета, которая расположена рядом со стилями **и** **вычислениями.**  

:::row:::
   :::column span="":::
      Чтобы включить и отключить эффект наложения, который описывает контейнер Flexbox, выберите значок Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Вы можете настроить цвет наложения в **** области макета рядом со стилями **и** **вычислениями.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="Значок Flexbox (flex) и выделенная веб-страницу" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         Значок **Flexbox** \( `flex` \) и выделенная веб-страницу :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="Наложения Flexbox, выделенные в области макета" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         Наложения **Flexbox,** выделенные в области **макета**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Отображение значков выравнивания и линий сетки при изменении макетов Flexbox с помощью свойств CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

При редактировании CSS для макета Flexbox автозаполнения **** CSS в области стилей теперь отображают полезные значки рядом с соответствующими свойствами Flexbox.  Чтобы попробовать эту новую функцию, откройте средство **"Элементы"** и выберите гибкий контейнер.  Затем добавьте или измените свойство этого контейнера в **области** стилей.  

:::row:::
   :::column span="":::
      Теперь в меню автозаполнения отображаются значки, которые указывают на влияние таких свойств `align-content` выравнивания, как и `align-items` .  
   :::column-end:::
   :::column span="":::
      Кроме того, в DevTools теперь отображается направляющая строка, которая поможет вам лучше просмотреть `align-items` свойство CSS.  Также `gap` поддерживается свойство CSS.  На следующем рисунке за установлено свойство CSS и отображается шаблон ветвления для `gap` `gap: 12px;` каждого пробела.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Меню автозаполнения, выделенное для свойств CSS, которые начинаются с выравнивания" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Меню автозаполнеия, выделенное для свойств CSS, которые начинаются с `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Разрыв Flexbox в выделенной свойствах CSS и веб-странице" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` в свойствах CSS и выделенной веб-странице  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Быстрое добавление инструментов с помощью кнопки "Дополнительные средства"  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Теперь у вас есть новый способ открыть дополнительные средства в Microsoft Edge DevTools.  После того как вы **** включите этот эксперимент, значок "Дополнительные инструменты" будет отображаться в качестве знака плюса `+` () справа от главной панели.  Чтобы отобразить список других инструментов, добавляемого на главную панель, выберите значок "Дополнительные **средства"** `+` (\).  Чтобы включить этот эксперимент, [][DevtoolsCustomizeIndexSettings]перейдите к пункту "Эксперименты с настройками" и выберите этот пункт рядом с меню вкладок "Включить+ кнопка", чтобы открыть  >  **** **дополнительные инструменты.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Дополнительные средства, выделенные в DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Дополнительные средства,** выделенные в DevTools  
:::image-end:::  

## Теперь вспомогательные технологии объявляют положение и количество предложений CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

При редактировании CSS вы получаете в качестве простого окна функции.  Эта функция не была доступна пользователям вспомогательных технологий, так как она объявлена в Microsoft Edge версии 89.  Пользователь вспомогательных технологий теперь может перемещаться по предложениям CSS в **области** стилей.  В Microsoft Edge версии 88 и более ранних версиях технология поддержки, объявленная пользователем, перебрала список предложений при редактировании CSS в области `Suggestion` стилей. ****  В Microsoft Edge версии 89 пользователь вспомогательных технологий теперь слышит положение и количество текущих предложений.  Каждое предложение будет объявлено по мере того, как пользователь переходит по списку предложений, например предложений 3 из 5.  Чтобы узнать больше о написании CSS в DevTools, перейдите к [change CSS][DevtoolsCssReferenceChangeCss].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1157329.][CR1157329]  

Чтобы просмотреть видео, которое отображает и читает вслух несколько предложений, включив этот эксперимент, перейдите к voiceover, объявляя о параметрах [devtools](https://youtu.be/9TcUpleEwwA) на YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="Предложение, выделено в области стилей" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   Список, `suggestion` выделенный в области **стилей**  
:::image-end:::  

## Эмуляция Surface Duo и папки Samsung  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Проверьте внешний вид веб-сайта или приложения на следующих устройствах в Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Папка "Сумяно"][SamsungUsMobileGalaxyFold]  
    
**Включив** функции экспериментальной веб-платформы, вы получите доступ к новой функции [CSS-экрана][DualScreenWebCssMediaSpanning] и [API JavaScript для getWindowSegments.][DualScreenWebJavascriptGetwindowsegments]  Перейдите к функциям экспериментальной веб-платформы и перейдите к флагу и перейдите `edge://flags` **к ней.**  Чтобы улучшить веб-сайт или приложение для двухэкранных и папок устройств, используйте следующие функции при [эмуляциях устройства.][DevtoolsDeviceModeIndex]  

*   [Spanning][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]— это когда ваш веб-сайт \(или приложение\) отображается на обоих экранах.  
*   [Отрисовка пространства][DualScreenIntroductionHowToWorkWithSeam]между двумя экранами.  
    
Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1054281.][CR1054281]  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Эмуляция двойного экрана" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Эмуляция двойного экрана  
:::image-end:::  

## Инструменты разработчика Microsoft Edge для Visual Studio code версии 1.1.2  

В [Microsoft Edge Developer Tools для Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.2 для Microsoft Visual Studio Code были внесены следующие изменения по сравнению с предыдущим выпуском.  Microsoft Visual Studio Код автоматически обновляет расширения.  Чтобы вручную обновить расширение до версии 1.1.2, перейдите к обновлению [расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Добавлена **кнопка закрытия экземпляра** для каждого элемента в целевом списке \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Версия [Microsoft Edge DevTools][DevtoolsMain] с 84.0.522.63 до [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Включенный [отладок для Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] в качестве зависимости \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Реализован параметр параметров для изменения тем расширения \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Вы можете файлировать проблемы и вносить вклад в расширение в репозитарии [GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Снимок экрана узла захвата за пределами области просмотра  

В Microsoft Edge версии 89 снимки экрана узла более точны, захватывая полный узел, даже если содержимое узла не отображается в окнах просмотра.  В **средстве "Элементы"** наведите курсор на элемент, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите снимок экрана **узла захвата.**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1003629.][CR1003629]  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Снимок экрана узла захвата, выделенного в контекстное меню в средстве Элементы" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Снимок экрана узла** захвата, выделенного в контекстное меню в **средстве "Элементы"**  
:::image-end:::  

### Обновления средства "Элементы"  

#### Поддержка принудительного принудительного состояния CSS :target  

Теперь можно использовать DevTools для принудительного [использования псевдокласса CSS :target.][MdnDocsWebCssTarget]  Псевдокласс инициирует, когда уникальный элемент `:target` \(целевой элемент\) имеет фрагмент `id` URL-адреса.  Например, `http://www.example.com/index.html#section1` URL-адрес инициирует `:target` псевдокласс для HTML-элемента с `id="section1"` .  Чтобы попробовать демонстрацию с выделенной частью 1, перейдите к [разделу CSS :target demo.][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1156628.][CR1156628]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="Выделенная веб-страницу без принудительной CSS" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Выделенная веб-страницу без принудительной CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` Принудительный CSS и выделенная веб-страницу  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Использование дублирующихся элементов для копирования элементов  

Используйте новый ярлык **дубликата** элемента для клонирования элемента.  В **средстве "Элементы"** наведите курсор на элемент, откройте контекстное меню \(щелкните правой кнопкой мыши\), выберите элемент **Duplicate.**  Под выбранным элементом создается новый элемент.  Чтобы скопировать элемент с помощью сочетания клавиш, выберите `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) или `Shift` + `Option` + `Down Arrow` \(macOS\).  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1150797.][CR1150797]  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="Элемент Duplicate выделен в контекстное меню элемента в средстве Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   Элемент **Duplicate выделен** в контекстное меню элемента в **средстве Elements**  
:::image-end:::  

#### Палитра для настраиваемого свойства CSS  

Теперь **в** области стилей отображаются палитры для настраиваемого свойства CSS.  Чтобы перебирать форматы RGBA, HSLA и Hex значения цвета, удерживайте и выберите `Shift` палитру.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1147016.][CR1147016]  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Палитра для настраиваемого свойства CSS" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Палитра для настраиваемого свойства CSS  
:::image-end:::  

#### Копирование классов и свойств CSS  

Теперь можно быстрее копировать свойства CSS с помощью нескольких новых параметров в контекстное меню.  В **средстве "Элементы"** выберите элемент.  Чтобы скопировать значение, **** в области стилей наведите курсор на класс CSS или свойство CSS, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите параметр копирования.  

:::row:::
   :::column span="":::
      Параметры копирования для класса CSS.  
      
      | Параметр | Сведения |  
      |:--- |:--- |  
      | **Выбор копии** | Скопируйте имя текущего селектора. |  
      | **Правило копирования** | Скопируйте правило текущего селектора. |  
      | **Копирование всех объявлений** | Скопируйте все объявления в рамках текущего правила, включая недостоверные и префиксные свойства. |  
   :::column-end:::
   :::column span="":::
      Параметры копирования для свойства CSS.  
      
      | Параметр | Сведения |      
      |:--- |:--- |  
      | **Объявление копирования** | Скопируйте объявление текущей строки. |  
      | **Свойство Copy** | Скопируйте свойство текущей строки. |  
      | **Значение копирования** | Скопируйте значение текущей строки. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Копирование параметров класса CSS в контекстное меню" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Копирование параметров класса CSS в контекстное меню  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Копирование параметров свойства CSS в контекстное меню" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Копирование параметров свойства CSS в контекстное меню  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1152391.][CR1152391]  

### Обновления файлов cookie  

#### Новый параметр для отображения файлов cookie, расшифровав URL-адреса  

Теперь можно отобразить значение раскодирования URL-файлов cookie в области **файлов cookie.**  Чтобы отобразить расшифровки файлов cookie, перейдите в области "Файлы cookie приложения", выберите любой файл cookie в списке и выберите следующий контрольный список, чтобы отобразить раскодирование ****  >  **** **URL-адреса.**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [997625.][CR997625]  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Возможность отображения файлов cookie, расшифровав URL-адреса" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Возможность отображения файлов cookie, расшифровав URL-адреса  
:::image-end:::  

#### Фильтрация и очистка видимых файлов cookie  

В Microsoft Edge версии 88 **** или более ранней версии средство application предоставлялось только для очистки всех файлов cookie с помощью кнопки **"Очистить все файлы cookie".**  В Microsoft Edge версии 89 теперь можно выбрать "Очистить отфильтрованные файлы **cookie",** чтобы удалить только отфильтрованные файлы cookie.  Чтобы отфильтровать файлы cookie, перейдите к **файлу**  >  **cookie приложения**и введите текстовое сообщение **фильтра.**  Чтобы удалить отображаемые файлы cookie, выберите кнопку **"Очистить фильтруйте файлы cookie".**  Чтобы отобразить все остальные файлы cookie, очищает текст фильтра.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [978059.][CR978059]  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Очистка только видимых файлов cookie" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Очистка только видимых файлов cookie  
:::image-end:::  

#### Новый параметр для очистки сторонних файлов cookie в области хранилища  

По умолчанию DevTools очищает только файлы cookie от первого разработчика.  Чтобы очистить данные веб-сайта и только **** сторонние файлы cookie, перейдите в хранилище приложений и выберите  >  **** **"Очистить данные сайта".**  

Чтобы очистить данные веб-сайта и все файлы cookie, перейдите в **хранилище**  >  **приложений.**  Включите сторонние **** файлы cookie и выберите "Очистить **данные сайта".**  

Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1012337.][CR1012337]  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Возможность очистки сторонних файлов cookie" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Возможность очистки сторонних файлов cookie  
:::image-end:::  

### Обновления сетевых инструментов  

#### Параметр сетевого журнала "Сохранить запись"  

В Microsoft Edge версии 88 или более ранней версии DevTools сбрасывает параметр сетевого журнала записи при обновлении веб-страницы. ****  В Microsoft Edge версии 89 DevTools теперь сохраняет параметр **сетевого** журнала записи.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1122580.][CR1122580]  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Запись сетевого журнала" lightbox="../../media/2021/01/network-log.msft.png":::
   Запись сетевого журнала  
:::image-end:::  

#### Сетевой параметр теперь не является параметром регулирования  

Параметр сетевой эмуляции **Online** теперь переименован в **"Без регулирования".**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1028078.][CR1028078]  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Без параметра регулирования" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Без параметра регулирования**  
:::image-end:::  

### Новые параметры копирования в средстве "Консоль", "Источники" и области стилей

#### Копирование объекта в средстве "Консоль" и "Источники"  

Теперь можно копировать значения объектов в **средствах консоли** и **источников.**  Возможность копирования значений объектов полезна при работе с большими объектами.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1148353][CR1148353] и [1149859.][CR1149859]  

:::row:::
   :::column span="":::
      В **средстве консоли** наведите курсор на объект, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите **"Копировать объект".**  
   :::column-end:::
   :::column span="":::
      В средстве **источников** на точке останова наведите **** курсор на объект, во всплывающее окно "Объект" выделите объект, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите "Копировать **объект".**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Копирование объекта в консоли" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Копирование объекта **в** консоли  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Копирование объекта в источниках" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Копирование объекта в **источниках**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Копирование имени файла в области "Источники" и "Стили"  

Теперь можно скопировать имя файла с помощью контекстного меню.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к вопросу [1155120][CR1155120].  

:::row:::
   :::column span="":::
      В **средстве "Источники"** наведите курсор на имя файла, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Копировать имя файла".**  
   :::column-end:::
   :::column span="":::
      В области **"Элементы>** **** стили" наведите курсор на имя файла, откройте контекстное меню \(щелкните правой кнопкой мыши\), а затем выберите "Копировать **имя файла".**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Копирование имени файла в источниках" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Копирование имени файла в **источниках**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Копирование имени файла в области стилей" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Копирование имени файла в **области стилей**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Обновления сведений о фрейме  

#### Сведения о рабочих службах в сведениях о фрейме  

DevTools теперь перечисляет выделенный рабочий кадр службы в родительском кадре.  На следующем рисунке отображаются сведения о рабочих службах.  Чтобы отобразить сведения о рабочих службах, перейдите к **сотрудникам**службы кадров приложений, а затем  >  ****  >  `top`  >  **** выберите сотрудника службы.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1122507.][CR1122507]  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Сведения о рабочих службах в сведениях о кадрах" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Сведения о рабочих** службах в **сведениях о кадрах**  
:::image-end:::  

#### Измерение сведений о памяти в сведениях о кадрах  

Теперь `performance.measureMemory()` состояние API отображается в разделе доступности **API.**  Новый `performance.measureMemory()` API оценивает использование памяти всей веб-страницей.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139899.][CR1139899]  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Измерение памяти" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Измерение памяти  
:::image-end:::  

### Отброшенные кадры в средстве "Производительность"  

При [анализе производительности нагрузки в средстве "Производительность"][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]раздел **"Кадры"** пометит отброшенные кадры красным цветом.  Чтобы отобразить частоту кадров, наведите курсор на отброшенный кадр.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1075865.][CR1075865]  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Отброшенные кадры" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Отброшенные кадры  
:::image-end:::  

#### Новое вычисление цветовой контрастности — расширенный алгоритм perceptual Contrast Algorithm (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Расширенный [алгоритм perceptual Contrast Algorithm (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] заменяет коэффициент контрастности рекомендаций [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] в [палитре цветов.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]  APCA — это новый способ вычисления контрастности.  Он основан на современных исследованиях цветового восприятия.  По сравнению с рекомендациями AA/AAA, APCA более зависит от контекста.  Контраст вычисляется на основе следующих пространственных свойств текста, цвета и контекста.  

*   Пространственные свойства текста, которые включают вес и размер шрифта.  
*   Пространственные свойства цвета, которые включают воспринимаемую контрастность между текстом и фоном.  
*   Пространственные свойства контекста, которые включают внешнее освещение, окружение и предназначение.  
    
Чтобы включить этот эксперимент, [][DevtoolsCustomizeIndexSettings]перейдите к "Экспериментам с настройками" и выберите его рядом с параметром  >  **** Enable **new Advanced Perceptual Contrast Algorithm (APCA),** заменив предыдущее соотношение контрастности и рекомендации AA/AAA.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1121900.][CR1121900]  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA в палитре" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA в палитре  
:::image-end:::  

## Скачивание Microsoft Edge предварительных каналов  

Если вы используете Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Новые возможности DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Просмотр коэффициента контрастности текстового элемента в справочнике по специальным | Документы Майкрософт"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Change CSS - CSS reference | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Тестирование на устройствах с двумя и двумя экранами — эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного окна : эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Запись производительности загрузки — справочные данные по анализу производительности | Документы Майкрософт"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Изменение стилей и параметров шрифтов CSS в области стилей в devTools | Документы Майкрософт"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Обзор средств разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для двухэкранного обнаружения | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Раздел 1. CSS :target demo for What's New in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: включая отладок для Microsoft Edge в качестве зависимостей | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Upgrading Edge DevTools version to 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Add single close buttons to instances panel | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Выберите характеристики шрифта и цвета фона, чтобы обеспечить полнейую контрастность для обеспечения | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Надежные типы | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый | Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — | Visual Studio кода"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Средства Microsoft Edge для Visual Studio кода | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR978059]: https://crbug.com/978059 "Проблема 978059: удаление файлов cookie при их фильтрации, удаление всех файлов cookie, а не только отфильтрованных файлов | Ошибки Chromium"  
[CR997625]: https://crbug.com/997625 "Проблема 997625: новый | Требуется возможность увидеть значение раскодирования URL-адреса в файлах cookie | Ошибки Chromium"  
[CR1003629]: https://crbug.com/1003629 "Проблема 1003629: узел захвата больше не делает снимок экрана с узлом под папкой. | Ошибки Chromium"  
[CR1012337]: https://crbug.com/1012337 "Проблема 1012337: очистка данных сайта уничтожает сеанс Google на других сайтах | Ошибки Chromium"  
[CR1028078]: https://crbug.com/1028078 "Проблема 1028078: в списке | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Проблема 1054281: запрос функций: DevTools должен эмулировать устройства с двумя и двумя экранами | Ошибки Chromium"  
[CR1075865]: https://crbug.com/1075865 "Проблема 1075865: показывать отброшенные кадры на временной шкале devtools | Ошибки Chromium"  
[CR1093229]: https://crbug.com/1093229 "Проблема 1093229: DevTools: предложение специализированного пользовательского интерфейса редактора шрифтов | Ошибки Chromium"  
[CR1121900]: https://crbug.com/1121900 "Проблема 1121900: DevTools: обновление логики вычисления контрастности для каждого нового спецификации | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1122580]: https://crbug.com/1122580 "Проблема 1122580: невозможно отключить запись в сети при перезагрузке | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139949]: https://crbug.com/1139949 "Проблема 1139949: наложение Flexbox | Ошибки Chromium"  
[CR1147016]: https://crbug.com/1147016 "Проблема 1147016: палитра не отображается в функции var(). | Ошибки Chromium"  
[CR1148353]: https://crbug.com/1148353 "Проблема 1148353: запрос на функции: копирование объекта из консоли devtools | Ошибки Chromium"  
[CR1149859]: https://crbug.com/1149859 "Проблема 1149859: [запрос функции][консоль] добавьте объект копирования в элемент буфера обмена в контекстное меню | Ошибки Chromium"  
[CR1150797]: https://crbug.com/1150797 "Проблема 1150797: добавление контекстного меню дублирующихся элементов в панели элементов | Ошибки Chromium"  
[CR1152391]: https://crbug.com/1152391 "Проблема 1152391: поддержка копирования контекстного меню CSS в панели стилей | Ошибки Chromium"  
[CR1155120]: https://crbug.com/1155120 "Проблема 1155120: [FR]Support copy file name and line number | Ошибки Chromium"  
[CR1156628]: https://crbug.com/1156628 "Проблема 1156628: DevTools: добавление поддержки функции состояния элемента ":target in force" | Ошибки Chromium"  
[CR1157329]: https://crbug.com/1157329 "Проблема 1157329. Доступность — диктор: диктор не объявляет количество и положение предложений, доступных для кода на вкладке "Стили" | Ошибки Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Папка | Сум США"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contrast (Enhanced) — как выполнить встречи с WCAG (краткий справочник) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Контраст (минимум) — как выполнить встречи с WCAG (краткий справочник) | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/01/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Местоимлятель spanning"  
