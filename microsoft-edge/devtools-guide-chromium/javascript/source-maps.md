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

# <a name="map-preprocessed-code-to-source-code"></a><span data-ttu-id="8733f-104">Карта предварительного кода в исходный код</span><span class="sxs-lookup"><span data-stu-id="8733f-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="8733f-105">Держите код клиента читаемым и отладки даже после объединения, минификации или компилляции.</span><span class="sxs-lookup"><span data-stu-id="8733f-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="8733f-106">Используйте исходные карты, чтобы сопопооставить исходный код с скомпилным кодом.</span><span class="sxs-lookup"><span data-stu-id="8733f-106">Use source maps to map your source code to your compiled code.</span></span>  

### <a name="summary"></a><span data-ttu-id="8733f-107">Сводка</span><span class="sxs-lookup"><span data-stu-id="8733f-107">Summary</span></span>  

*   <span data-ttu-id="8733f-108">Используйте исходные карты для совмещений минифицированного кода с исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="8733f-108">Use Source Maps to map minified code to source code.</span></span>  <span data-ttu-id="8733f-109">Затем вы сможете читать и отлаговка скомпилировать код в исходном источнике.</span><span class="sxs-lookup"><span data-stu-id="8733f-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="8733f-110">Используйте только предварительные процессоры, способные производить исходные карты.</span><span class="sxs-lookup"><span data-stu-id="8733f-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="8733f-111">Убедитесь, что веб-сервер может обслуживать исходные карты.</span><span class="sxs-lookup"><span data-stu-id="8733f-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a><span data-ttu-id="8733f-112">Начало работы с препроцессорами</span><span class="sxs-lookup"><span data-stu-id="8733f-112">Get started with preprocessors</span></span>  

<span data-ttu-id="8733f-113">В этой статье рассказывается, как взаимодействовать с исходными картами JavaScript в панели источников DevTools.</span><span class="sxs-lookup"><span data-stu-id="8733f-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a><span data-ttu-id="8733f-114">Использование поддерживаемых препроцессора</span><span class="sxs-lookup"><span data-stu-id="8733f-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="8733f-115">Используйте мини-fier, который способен создавать исходные карты.</span><span class="sxs-lookup"><span data-stu-id="8733f-115">Use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="8733f-116">Для расширенного представления перейдите на исходные [карты: языки, инструменты и другую страницу вики-информации.][GitHubWikiSourceMapsLanguagesTools]</span><span class="sxs-lookup"><span data-stu-id="8733f-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="8733f-117">Следующие типы препроцессоров обычно используются в сочетании с исходными картами:</span><span class="sxs-lookup"><span data-stu-id="8733f-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="8733f-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="8733f-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="8733f-119">Компиляторы \.[Компилятор закрытия][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Дартс][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="8733f-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="8733f-120">Minifiers \.[UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="8733f-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <a name="source-maps-in-devtools-sources-panel"></a><span data-ttu-id="8733f-121">Исходные карты в панели Источников DevTools</span><span class="sxs-lookup"><span data-stu-id="8733f-121">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="8733f-122">Исходные карты из препроцессоров приводят к загрузке исходных файлов в дополнение к добытым файлам.</span><span class="sxs-lookup"><span data-stu-id="8733f-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="8733f-123">Затем вы используете оригиналы для набора точек остановок и шага по коду.</span><span class="sxs-lookup"><span data-stu-id="8733f-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="8733f-124">Тем временем Microsoft Edge фактически запускает ваш заминированный код.</span><span class="sxs-lookup"><span data-stu-id="8733f-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  <span data-ttu-id="8733f-125">Запуск кода создает иллюзию запуска сайта разработки в производстве.</span><span class="sxs-lookup"><span data-stu-id="8733f-125">The running of the code gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="8733f-126">При запуске исходных карт в DevTools следует заметить, что JavaScript не компилироваться, а все отдельные файлы JavaScript, на которые он ссылается, отображаются.</span><span class="sxs-lookup"><span data-stu-id="8733f-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and all of the individual JavaScript files it references are displayed.</span></span>  <span data-ttu-id="8733f-127">Исходные карты в DevTools используют исходные сопоставления, но в основе функции фактически выполняется скомпилирован код.</span><span class="sxs-lookup"><span data-stu-id="8733f-127">Source Maps in DevTools is using source mapping, but the underlying functionality actually runs the compiled code.</span></span>  <span data-ttu-id="8733f-128">Любые ошибки, журналы и брейк-пойнты на карте кода разработчика для отладки.</span><span class="sxs-lookup"><span data-stu-id="8733f-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging.</span></span>  <span data-ttu-id="8733f-129">Таким образом, в действительности это дает вам иллюзию, что вы работаете на сайте разработчика в производстве.</span><span class="sxs-lookup"><span data-stu-id="8733f-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <a name="enable-source-maps-in-settings"></a><span data-ttu-id="8733f-130">Включить исходные карты в настройках</span><span class="sxs-lookup"><span data-stu-id="8733f-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="8733f-131">Исходные карты включены по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8733f-131">Source Maps are enabled by default</span></span><!-- \(as of Microsoft Edge 39\)--><span data-ttu-id="8733f-132">, но если вы хотите дважды проверить или включить их; сначала откройте DevTools, выберите Настройка и управление **DevTools** `...` \( \) > **параметры**.</span><span class="sxs-lookup"><span data-stu-id="8733f-132">, but if you want to double-check or enable them; first open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="8733f-133">На области **"Предпочтения"** в **статье Источники**включаем **включить исходные карты JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="8733f-133">On the **Preferences** pane, under **Sources**, turn on **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="8733f-134">Вы также можете включить исходные **карты включить CSS.**</span><span class="sxs-lookup"><span data-stu-id="8733f-134">You may also turn on the **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Включить исходные карты" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="8733f-136">Включить исходные карты JavaScript</span><span class="sxs-lookup"><span data-stu-id="8733f-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a><span data-ttu-id="8733f-137">Отладка с помощью исходных карт</span><span class="sxs-lookup"><span data-stu-id="8733f-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="8733f-138">Когда отладка кода и исходных карт включена, исходные карты показываются в двух местах:</span><span class="sxs-lookup"><span data-stu-id="8733f-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="8733f-139">В консоли \(ссылкой на источник должен быть исходный файл, а не созданный\)</span><span class="sxs-lookup"><span data-stu-id="8733f-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="8733f-140">При перешагнул код \(ссылки в стеке вызовов должны открыть исходный файл\)</span><span class="sxs-lookup"><span data-stu-id="8733f-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a><span data-ttu-id="8733f-141">@sourceURL и displayName</span><span class="sxs-lookup"><span data-stu-id="8733f-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="8733f-142">Хотя эта спецификация не является частью спецификации Source Map, она позволяет значительно упростить разработку при `@sourceURL` работе с evals.</span><span class="sxs-lookup"><span data-stu-id="8733f-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="8733f-143">Помощник отображается аналогично свойству и упоминается в спецификациях `//# sourceMappingURL` Source Map V3.</span><span class="sxs-lookup"><span data-stu-id="8733f-143">The helper is displayed similar to the `//# sourceMappingURL` property and is mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="8733f-144">Включив в код следующий специальный комментарий, который является evaled, вы можете назвать evals и inline scripts and styles, чтобы каждый из них был более логичным именем в devTools.</span><span class="sxs-lookup"><span data-stu-id="8733f-144">By including the following special comment in your code, which is evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="8733f-145">Перейдите на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="8733f-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="8733f-146">ролик</span><span class="sxs-lookup"><span data-stu-id="8733f-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="8733f-147">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8733f-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="8733f-148">Откройте DevTools и перейдите на панель **Источники.**</span><span class="sxs-lookup"><span data-stu-id="8733f-148">Open the DevTools and navigate to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="8733f-149">Введите имя файла в **поле Имя кода:** поле ввода.</span><span class="sxs-lookup"><span data-stu-id="8733f-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="8733f-150">Выберите **кнопку компилятор.**</span><span class="sxs-lookup"><span data-stu-id="8733f-150">Choose the **compile** button.</span></span>  
1.  <span data-ttu-id="8733f-151">Оповещение отображается с оцененной суммой из источника CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="8733f-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="8733f-152">При расширении **подгруппы Источники** теперь отображается новый файл с настраиваемым иным файлом, который был введен ранее.</span><span class="sxs-lookup"><span data-stu-id="8733f-152">If you expand the **Sources** sub-panel you now display a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="8733f-153">Если дважды щелкнуть, чтобы просмотреть этот файл, он содержит составленный JavaScript для исходного источника.</span><span class="sxs-lookup"><span data-stu-id="8733f-153">If you double-click to view this file, it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="8733f-154">В последней строке, однако, находится `// @sourceURL` комментарий, указывающий исходный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="8733f-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="8733f-155">Это может помочь вам в отладки при работе с языковыми абстракциями.</span><span class="sxs-lookup"><span data-stu-id="8733f-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Работа с sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="8733f-157">Работа с</span><span class="sxs-lookup"><span data-stu-id="8733f-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8733f-158">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8733f-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

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
> <span data-ttu-id="8733f-168">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8733f-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8733f-169">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и Пола [Бакауса][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation и UX\).</span><span class="sxs-lookup"><span data-stu-id="8733f-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8733f-171">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8733f-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
