---
description: В этом руководстве представлен обзор функций и стандартов разработчика, включенных в Microsoft Edge.
title: Новые возможности EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, веб-разработка, html, css, javascript, разработчик, devtools
ms.custom: RS5
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 15d3321e05f8a307d8014696f1ab78a8967f7129
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235271"
---
# Руководство разработчика Microsoft Edge

> [!TIP]
> Мы сотрудничаем с другими браузерами и веб-сообществом, внедряя веб-документы [MDN](https://developer.mozilla.org/) в качестве точного места для полезной, непреднастояющей документации браузера для текущих и новых веб-технологий на основе стандартов. [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) Подробные сведения о поддержке API EdgeHTML можно найти непосредственно на каждой странице библиотеки [веб-ссылок MDN.](https://developer.mozilla.org/docs/Web) Последние функции, [](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) поддерживаемые в Microsoft Edge, можно получить в статусе платформы Microsoft Edge. 

## Новые возможности EdgeHTML 18

EdgeHTML 18 включает следующие новые и обновленные функции, включенные в текущий выпуск платформы Microsoft Edge с обновлением Windows 10 за октябрь 2018 г. (сборка 17763, 10 октября [2018](/windows/uwp/whats-new/windows-10-build-17763) г.). Изменения в конкретных сборках [Windows Insider](https://insider.windows.com/) Preview см. в записях microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/) и [What's New in EdgeHTML.](./whats-new.md)

Ниже приводится permalink для следующего списка изменений: [https://aka.ms/devguide_edgehtml_18](./whats-new.md) .

## Новые и обновленные функции

### Политики автозапуска

С обновлением Windows 10 за октябрь 2018 г. Microsoft Edge предоставляет клиентам возможность персонализировать свои предпочтения браузера на веб-сайтах, которые автоматически воспроизведение мультимедиа со звуком, чтобы свести к минимуму отвлекающие факторы в Интернете и сэкономить пропускную способность. Пользователи могут настраивать поведение мультимедиа с помощью глобальных и индивидуальных элементов управления автоза воспроизведением. Кроме того, Microsoft Edge автоматически подавляет автозапок мультимедиа на фоновых вкладок.

Подробные [сведения](./browser-features/autoplay-policies.md) и практические руководства по обеспечению хорошего взаимодействия с пользователем с мультимедиа, который находится на сайте, можно найти в руководстве по политикам автозахва.

### Улучшения для chakra

EdgeHTML 18 включает обновления ядра JavaScript для Chakra для поддержки новых функций ES и WASM в дополнение к улучшениям производительности и производительности. Подробные сведения можно узнать в заметках о выпуске [ChakraCore 1.11.](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111)

### Обновления CSS

Мы добавили дополнительный прогресс в экспериментальной реализации маскировки [CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) (за флагом "Включить [](https://developer.mozilla.org/docs/Web/CSS/mask-position)маску *CSS"),* а также добавили поддержку композитных масок, [](https://developer.mozilla.org/docs/Web/CSS/mask-composite)положения маски и повторения [маски.](https://developer.mozilla.org/docs/Web/CSS/mask-repeat) Для обеспечения совместимости сайтов Microsoft Edge также поддерживает следующие свойства *-webkit-properties:* -webkit-mask, -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-size.

Кроме того, Microsoft Edge [](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) теперь поддерживает переполнение и [](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) частичную поддержку поведения переполнения `auto` (и `contain` значений).

### Средства разработчика

Последнее обновление Microsoft Edge DevTools добавляет ряд удобных функций как в пользовательский интерфейс, так и на первый план, включая новые выделенные панели для сотрудников службы и хранилища, средства поиска исходных файлов в отладке, а также новые домены протокола Edge DevTools для отладки стилей и макетов и консольных API.

[DevTools в последнем обновлении Windows 10 (EdgeHTML 18)](../devtools-guide/whats-new.md) имеет все сведения.

### Прослушивание ваших отзывов

Мы прослушиваем ваши отзывы и реализовали поддержку нескольких запрашиваемого API в EdgeHTML 18, включая метод, используемый для настройки пользовательского изображения при перетаскивание, а также свойство API синхронизации ресурсов производительности, которое можно использовать для возврата хронометра непосредственно перед тем, как браузер начнет процесс рукопожатия для защиты текущего [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) подключения. 

Кроме того, никто не поддерживает перечисленные атрибуты коллекции, поэтому мы добавили поддержку для возврата имен атрибутов элемента в качестве массива строк, а также для перегона [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) boolean атрибута (удаление, если присутствует [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) и добавление, если нет).

### Прогрессивные веб-приложения

#### Фоновый сценарий жизненного времени

Приложения JavaScript для Windows 10 ** (веб-приложения, запущенные в процессеWWAHost.exe) теперь поддерживают необязательный фоновый сценарий для каждого приложения, который запускается до активации любых представлений и запускается в течение всего процесса. Благодаря этому можно отслеживать и изменять навигацию, отслеживать состояние навигации, отслеживать ошибки навигации и запускать код перед активацией представлений. 

Если указано в манифесте приложения, каждое из представлений приложения (windows) предоставляется сценарию как экземпляры нового класса, предоставляя те же события, свойства и методы, что и общее [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) [](/uwp/schemas/appxpackage/appx-package-manifest) [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) (Win32) [WebView.](/uwp/api/windows.web.ui.iwebviewcontrol) Ваш сценарий может прослушивать событие [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) для перехвата управления навигацией для нового представления:

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Любая активация приложения с помощью фонового сценария будет зависеть от самого `StartPage` сценария для навигации.

#### Масштабирование текста

В обновлении Windows 10 за октябрь [**](/windows/uwp/design/input/text-scaling#user-experience) 2018 г. вводится параметр "Увеличить размер текста" для улучшения доступности конечных пользователей, и pwAs, установленные в Windows (в дополнение к UWP и большинству классических приложений), теперь поддерживают эту функцию автоматически. Для элементов управления PWAs и WebView текстовое масштабирование работает так же, как и масштабирование DPI. Если пользователь изменяет и текстовую шкалу, и масштаб DPI, результатом будет продукт этих двух.

 Рекомендации по проектированию можно получить в руководстве [по](/windows/uwp/design/input/text-scaling) масштабируемости текста UWP в *Центре разработки для Windows.*

### Обновления для рабочих служб 

Чтобы узнать, что такое сотрудники-службы и как они работают, ознакомьтесь со сводой [API]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) рабочих служб, написанной нашими партнерами на сайте MDN.  В EdgeHTML 18 было несколько обновлений для сотрудников служб, поддерживающих Microsoft Edge. Позволяет сотруднику службы использовать обещание ответа, а также возвращает ИД клиента, который текущий рабочий `fetchEvent` [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) службы контролирует.  
Интерфейс предоставляет методы для управления предварительной загрузкой ресурсов, что позволяет одновременно делать запрос во время загрузки рабочим процессом службы, избегая [`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) задержки времени. Ознакомьтесь со списком методов и свойств предварительной загрузки рабочих служб, которые поддерживаются [свойствами API.](#new-apis-in-edgehtml-18) 

### Проверка подлинности в Интернете

Теперь Microsoft Edge включает неподдерживаемую поддержку для нового [API](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) веб-проверки подлинности [(например, WebAuthN).](https://w3c.github.io/webauthn/) Веб-проверка подлинности предоставляет открытое, масштабируемое и совмещаемое решение для упрощения проверки подлинности, обеспечивая более надежную и безопасную работу пользователей, заменяя пароли более надежными аппаратными учетными данными. Реализация в Microsoft Edge позволяет [](https://www.microsoft.com/windows/windows-hello) пользователям в дополнение к внешним аутентификаторам, таким [](https://fidoalliance.org) как ключи безопасности FIDO2 или ключи безопасности FIDO U2F, в дополнение к внешним аутентификаторам, таким как ключи безопасности FIDO2 или КЛАВИШи безопасности FIDO U2F, безопасно войти на веб-сайты.

Дополнительные сведения можно найти в записи блога "Знакомство с [веб-проверкой](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge)подлинности в Microsoft Edge".

### WebDriver

WebDriver теперь является функцией [Windows](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) по запросу (FoD), что упрощает автоматизацию тестирования в Microsoft Edge и получения нужной версии для вашего устройства. При установке [WebDriver](https://www.w3.org/TR/webdriver) вам больше не нужно будет вручную соответствовать сборке, ветвьм и ветвям. Веб-диск будет автоматически обновляться в зависимости от новых обновлений Windows 10. 

Чтобы установить WebDriver, включив режим разработчика, или установить его как автономный, переходить к функциям > Apps > Apps & > Manage optional features. Дополнительные сведения можно узнать в объявлении [WebDriver на сайте блога Windows.](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand)

### Свойства веб-уведомлений
Теперь для веб-уведомлений поддерживаются четыре новых свойства: , и , улучшена возможность создания уведомлений в Интернете, совместимых с существующими системами уведомлений, в то же время независимо от [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) `maxActions` платформы.

### Веб-представление

#### Служебные сценарии
[Службы](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) теперь поддерживаются в веб-оке управления, в дополнение к браузеру Microsoft Edge и приложениям JavaScript для Windows 10. Все варианты веб-приложения Microsoft Edge[(PWA,](../hosting/webview/index.md) [UWP,](/uwp/api/Windows.UI.Xaml.Controls.WebView) [Win32)](/windows/communitytoolkit/controls/wpf-winforms/webview)поддерживают сотрудников службы, однако следует помнить, что [API Push](https://developer.mozilla.org/docs/Web/API/Push_API) еще не доступен для версий UWP и Win32.

Для архитектур приложений x64 требуются нейтральные *пакеты* (любой ЦП) или *пакеты x64,* так как рабочие процессы WoW64 не поддерживаются. (Чтобы сэкономить место на диске, версия требуемого DLL WoW не включена в Windows.)

#### Обновления Win32 WebView

В edgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) для классических приложений Для Windows (Win32) было обновлено несколько новых функций, в том числе возможность внедрять сценарий при загрузке страницы до запуска любых других сценариев на странице ( ) и знать, когда определенный [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) WebViewControl получает или теряет фокус ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Кроме того, теперь можно создать новый WebViewControl в качестве открытого [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) окна. Это событие по-прежнему сообщает приложению, когда сценарий внутри WebViewControl вызывает window.open, как всегда, но с EdgeHTML 18 включает возможность отсрочки ( ) для того, чтобы установить [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) новый WebViewControl ( ) в качестве целевого для [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) window.open:

```csharp
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);
```  

Наконец, power users might notice the appearance of the *Desktop App Web Viewer* (previously named *Win32WebViewHost),* an internal system app representing the Win32 WebView, in the following places:
- В центре *действий Windows 10.* Источник этих уведомлений должен быть понятен из Веб-просмотр, который был в приложении Win32.
- В пользовательском интерфейсе параметров доступа к устройству (*Settings->Privacy->Camera/Location/Microphone).* Отключение любого из этих параметров отключает доступ из всех веб-просмотров, установленных в приложениях Win32.

![Параметр доступа к устройству для просмотра классических приложений](./media/desktop-app-web-viewer.png)

## Неподготовленные функции

### Фильтр XSS теперь не замесан

С помощью EdgeHTML 18 мы удаляем фильтр XSS в Microsoft Edge. Наши клиенты остаются защищенными благодаря современным стандартам, таким как политика безопасности контента [(CSP),](https://developer.mozilla.org/docs/Web/HTTP/CSP)которые предоставляют более мощные, мощные, мощные и безопасные механизмы для защиты от атак путем вливания содержимого с высокой совместимостью в современных браузерах.

## Новые API в EdgeHTML 18

Полный список новых API в EdgeHTML 18. Они перечислены в формате [имя интерфейса]. [имя API].

> [!NOTE] 
> Несмотря на то что в модели DOM 2016 2013 2013 2013 2013 2013 2013 2013 2013 2013 2013, возможно, все еще находятся на стадии разработки и скрыты за экспериментальным флагом. Официальное слово о поддержке функций можно найти в статусе платформы [Microsoft Edge.](https://developer.microsoft.com/microsoft-edge/platform/status/)

<iframe height='580' scrolling='no' title='Новые API в EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. API-код для новых перьев в <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> EdgeHTML 18 от </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> </a> @MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>

## Предыдущие выпуски EdgeHTML

[EdgeHTML 13 / Сборка Windows 10586 (11/2015)](./whats-new/edgehtml-13.md)

[EdgeHTML 14 / Сборка Windows 14393 (8/2016)](./whats-new/edgehtml-14.md)

[EdgeHTML 15 / Сборка Windows 15063 (4/2017)](./whats-new/edgehtml-15.md)

[EdgeHTML 16 / Сборка Windows 16299 (10/2017)](./whats-new/edgehtml-16.md)

[EdgeHTML 17 / Сборка Windows 17134 (04/2018)](./whats-new/edgehtml-17.md)
