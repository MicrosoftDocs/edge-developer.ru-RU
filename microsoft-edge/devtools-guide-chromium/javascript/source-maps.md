---
description: Держите код клиента читаемым и отладки даже после объединения, минификации или компилляции.
title: Карта предварительного кода в исходный код
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: debea327be41ab8aa2da19aa8cc128a1897e51e5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398394"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="map-preprocessed-code-to-source-code"></a>Карта предварительного кода в исходный код  

Держите код клиента читаемым и отладки даже после объединения, минификации или компилляции.  Используйте исходные карты, чтобы сопопооставить исходный код с скомпилным кодом.  

### <a name="summary"></a>Сводка  

*   Используйте исходные карты для совмещений минифицированного кода с исходным кодом.  Затем вы сможете читать и отлаговка скомпилировать код в исходном источнике.  
*   Используйте только предварительные процессоры, способные производить исходные карты.  
*   Убедитесь, что веб-сервер может обслуживать исходные карты.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Начало работы с препроцессорами  

В этой статье рассказывается, как взаимодействовать с исходными картами JavaScript в панели источников DevTools.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Использование поддерживаемых препроцессора  

Используйте мини-fier, который способен создавать исходные карты.  <!--For the most popular options, navigate to preprocessor support section.  -->  Для расширенного представления перейдите на исходные [карты: языки, инструменты и другую страницу вики-информации.][GitHubWikiSourceMapsLanguagesTools]  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Следующие типы препроцессоров обычно используются в сочетании с исходными картами:  

*   Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Компиляторы \.[Компилятор закрытия][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Дартс][DartMain]\)  
*   Minifiers \.[UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-panel"></a>Исходные карты в панели Источников DevTools  

Исходные карты из препроцессоров приводят к загрузке исходных файлов в дополнение к добытым файлам.  Затем вы используете оригиналы для набора точек остановок и шага по коду.  Тем временем Microsoft Edge фактически запускает ваш заминированный код.  Запуск кода создает иллюзию запуска сайта разработки в производстве.  

При запуске исходных карт в DevTools следует заметить, что JavaScript не компилироваться, а все отдельные файлы JavaScript, на которые он ссылается, отображаются.  Исходные карты в DevTools используют исходные сопоставления, но в основе функции фактически выполняется скомпилирован код.  Любые ошибки, журналы и брейк-пойнты на карте кода разработчика для отладки.  Таким образом, в действительности это дает вам иллюзию, что вы работаете на сайте разработчика в производстве.  

### <a name="enable-source-maps-in-settings"></a>Включить исходные карты в настройках  

Исходные карты включены по умолчанию<!-- \(as of Microsoft Edge 39\)-->, но если вы хотите дважды проверить или включить их; сначала откройте DevTools, выберите Настройка и управление **DevTools** `...` \( \) > **параметры**.  На области **"Предпочтения"** в **статье Источники**включаем **включить исходные карты JavaScript.**  Вы также можете включить исходные **карты включить CSS.**  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Включить исходные карты" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Включить исходные карты JavaScript**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Отладка с помощью исходных карт  

Когда отладка кода и исходных карт включена, исходные карты показываются в двух местах:  

1.  В консоли \(ссылкой на источник должен быть исходный файл, а не созданный\)  
1.  При перешагнул код \(ссылки в стеке вызовов должны открыть исходный файл\)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a>@sourceURL и displayName  

Хотя эта спецификация не является частью спецификации Source Map, она позволяет значительно упростить разработку при `@sourceURL` работе с evals.  Помощник отображается аналогично свойству и упоминается в спецификациях `//# sourceMappingURL` Source Map V3.  

Включив в код следующий специальный комментарий, который является evaled, вы можете назвать evals и inline scripts and styles, чтобы каждый из них был более логичным именем в devTools.  

```javascript
//# sourceURL=source.coffee
```  

Перейдите на следующую страницу.  

*   [ролик][CssNinjaDemoSourceMapping]

Выполните следующие действия.  

1.  Откройте DevTools и перейдите на панель **Источники.**  
1.  Введите имя файла в **поле Имя кода:** поле ввода.  
1.  Выберите **кнопку компилятор.**  
1.  Оповещение отображается с оцененной суммой из источника CoffeeScript.  
    
При расширении **подгруппы Источники** теперь отображается новый файл с настраиваемым иным файлом, который был введен ранее.  Если дважды щелкнуть, чтобы просмотреть этот файл, он содержит составленный JavaScript для исходного источника.  В последней строке, однако, находится `// @sourceURL` комментарий, указывающий исходный исходный файл.  Это может помочь вам в отладки при работе с языковыми абстракциями.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Работа с sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Работа с `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel — компилятор JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Простой пример именования eval //# sourceURL"  

[DartMain]: https://www.dartlang.org "Дартс язык программирования"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/closure-compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Исходные карты: языки, инструменты и другие | Вики GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Начало работы — google/traceur-compiler | Вики GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и Пола [Бакауса][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation и UX\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
