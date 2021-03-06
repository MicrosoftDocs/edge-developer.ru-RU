---
description: В этом руководстве представлен обзор компонентов и стандартов разработчика, включенных в Microsoft Edge.
title: Новые возможности в EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, web development, html, css, javascript, developer, devtools
ms.custom: RS5
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6b53163115ad7db8e5b792cadda0c59b93b6711b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399227"
---
# <a name="microsoft-edge-developer-guide"></a>Руководство по разработчикам Microsoft Edge  

> [!TIP]
> Мы сотрудничаем с другими браузерами и веб-сообществом в принятии [веб-документов MDN](https://developer.mozilla.org/) в качестве окончательного места для полезной, объективной, браузерно-агностиковой документации для текущих и новых веб-технологий на основе стандартов. [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/)  Сведения о поддержке API edgeHTML можно найти непосредственно на каждой странице веб-справочной [библиотеки MDN.](https://developer.mozilla.org/docs/Web)  Посетите состояние платформы Microsoft Edge [для](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) последних функций, поддерживаемых в Microsoft Edge.  

## <a name="whats-new-in-edgehtml-18"></a>Новые возможности в EdgeHTML 18  

EdgeHTML 18 включает следующие новые и обновленные функции, отправляемые в текущем выпуске платформы Microsoft Edge, по мере обновления [Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) \(10/2018, Сборка 17763\).  Изменения в определенных [сборках предварительного](https://insider.windows.com) просмотра предварительной версии Windows см. в [веб-сайте Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](./whats-new.md)  

Ниже приводится permalink для следующего списка изменений: [https://docs.microsoft.com/microsoft-edge/dev-guide](#new-apis-in-edgehtml-18) .  

## <a name="new-and-updated-features"></a>Новые и обновленные функции  

### <a name="autoplay-policies"></a>Политики автозапуска  

С обновлением Windows 10 Октябрь 2018 Microsoft Edge предоставляет клиентам возможность персонализировать свои предпочтения просмотра на веб-сайтах, которые автоигрируют носители со звуком, чтобы свести к минимуму отвлекающие факторы в Интернете и сохранить пропускную способность.  Пользователи могут настраивать поведение мультимедиа с помощью элементов управления автоматической воспроизведением как на глобальном, так и на сайте.  Кроме того, Microsoft Edge автоматически подавляет автоматическое воспроизведение мультимедиа на фоновых вкладок.  

Ознакомьтесь с руководством [по](./browser-features/autoplay-policies.md) политикам автоплея, чтобы получить подробные сведения и практические сведения, чтобы обеспечить хорошее взаимодействие пользователей со средствами массовой информации, которые можно найти на вашем сайте.  

### <a name="chakra-improvements"></a>Улучшения chakra  

EdgeHTML 18 включает обновления для двигателя JavaScript Chakra для поддержки новых функций ES и WASM, а также улучшения производительности и производительности.  Подробные сведения о [выпуске ChakraCore 1.11.](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111)  

### <a name="css-updates"></a>Обновления CSS  

Мы продвинулись вперед в экспериментальной реализации [CSS Masking](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) \(за флагом Маски *CSS* enable\) с дополнительной поддержкой маски-композитных, [маск-позиций](https://developer.mozilla.org/docs/Web/CSS/mask-position)и [маски-повторения](https://developer.mozilla.org/docs/Web/CSS/mask-repeat). [](https://developer.mozilla.org/docs/Web/CSS/mask-composite)  Для совместимости веб-сайтов Microsoft Edge также поддерживает следующие свойства *webkit-:* -webkit-mask, -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-mask-size.  

Кроме того, Microsoft Edge [](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap) теперь поддерживает переполнение и частичную поддержку [overscroll-behaviour](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) \( `auto` и `contain` значения\).  

### <a name="developer-tools"></a>Средства разработчика  

Последнее обновление Microsoft Edge DevTools добавляет ряд удобств как для пользовательского интерфейса, так и под капотом, включая новые выделенные панели для сотрудников службы и хранилища, средства поиска исходных файлов в Debugger, а также новые домены Edge DevTools Protocol для отладки стилей и макетов и API консоли.  

[DevTools в последнем обновлении Windows 10 (EdgeHTML 18)](./whats-new.md) имеет все сведения.  

### <a name="listening-to-your-feedback"></a>Прослушивание отзывов  

Мы прислушиваемся к вашим отзывам и реализуем поддержку нескольких запрашиваемого API в EdgeHTML 18, включая метод [DataTransfer.setDragImage(),](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) используемый для настройки настраиваемого изображения при перетаскивание и сбросе, и [secureConnectionStart](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart)— свойство API времени выполнения ресурсов, которое можно использовать для возврата хронометра непосредственно перед началом процесса рукопожатия браузера для обеспечения текущего подключения.  

Кроме того, никто не любит перенаписывать коллекцию атрибутов, поэтому мы добавили поддержку [Element.getAttributeNames,](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) чтобы вернуть имена атрибутов элемента в качестве массива строк, а также [Element.toggleAttribute,](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) чтобы переманить атрибут boolean \(удаление, если присутствует, и добавление если нет\).  

### <a name="progressive-web-apps"></a>Прогрессивные веб-приложения  

#### <a name="lifetime-background-script"></a>Сценарий фона продолжительности жизни  

Приложения JavaScript Windows 10 \(веб-приложения, запущенные в процессе\) теперь поддерживают необязательный фоновый сценарий для каждого приложения, который запускается до активации любых представлений и выполняется в течение всего `WWAHost.exe` процесса.  С помощью этого можно отслеживать и изменять навигацию, отслеживать состояние навигации, отслеживать ошибки навигации и запускать код до активации представлений.  

Если указано как [StartPage](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) в манифесте [приложения,](/uwp/schemas/appxpackage/appx-package-manifest)каждое из представлений приложения \(windows\) подвергается скрипту в качестве экземпляров нового класса [WebUIView,](/uwp/api/windows.ui.webui.webuiview) предоставляя те же события, свойства и методы, что и общие \(Win32\) [WebView](/uwp/api/windows.web.ui.iwebviewcontrol).  Сценарий может прослушивать событие [NewWebUIViewCreated,](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) чтобы перехватить управление навигацией для нового представления:  

```javascript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```  

 Любая активация приложения со сценарием фона в качестве сценария будет зависеть `StartPage` от самого скрипта для навигации.  

#### <a name="text-scaling"></a>Масштабирование текста  

Обновление Windows 10 октября 2018 г. вводит параметр Make [text bigger](/windows/uwp/design/input/text-scaling#user-experience) для улучшения доступности для конечного пользователя, а pwAs, установленные на Windows \(кроме того, UWP и большинство настольных приложений\) теперь поддерживают эту функцию автоматически.  Для элементов управления PWAs и WebView текстовая шкала работает так же, как масштабирование DPI.  Если пользователь изменяет как текстовую шкалу, так и масштаб DPI, результатом является результат этих двух.  

 Для руководства по проектированию ознакомьтесь с руководством [по](/windows/uwp/design/input/text-scaling) масштабации текста в *Центре разработки Windows.*  

### <a name="service-worker-updates"></a>Обновления сотрудника службы  

Сведения о том, какие работники службы и как они работают, ознакомьтесь с сводной сводке [API API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) service worker, написанной нашими партнерами в MDN.  В EdgeHTML 18 было несколько обновлений для вспомогательных служб Microsoft Edge.  Это позволяет работнику службы использовать `fetchEvent` [preloadResponse](https://developer.mozilla.org/docs/Web/API/FetchEvent) для обещания ответа, а в [результатеClientId](https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) возвращает ID клиента, который контролирует текущий сотрудник службы.  
Интерфейс [NavigationPreloadManager](https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) предоставляет методы управления предварительной загрузкой ресурсов, что позволяет параллельно делать запрос во время загрузки сотрудника службы, избегая задержки времени.  Ознакомьтесь с [недавно поддерживаемыми свойствами API](#new-apis-in-edgehtml-18) для списка методов и свойств предварительной загрузки service Worker.  

### <a name="web-authentication"></a>Проверка подлинности в Интернете  

Microsoft Edge теперь включает [неоконченную](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge) поддержку нового API веб-проверки подлинности \(aka [WebAuthN](https://w3c.github.io/webauthn)\).  Веб-проверка подлинности предоставляет открытое, масштабируемое и интероперабельное решение для упрощения проверки подлинности, что позволяет улучшить и обеспечить безопасность пользователей, заменив пароли более надежными учетными данными, связанными с оборудованием.  Реализация в Microsoft Edge позволяет использовать [Windows Hello,](https://www.microsoft.com/windows/windows-hello) позволяя пользователям войти с их лицом, отпечатками пальцев или ПИН-кодом, а также внешними аутентификаторами, например ключами безопасности FIDO2 или ключами безопасности FIDO U2F, для безопасной проверки подлинности веб-сайтов. [](https://fidoalliance.org)  

Дополнительные сведения перенапорку в блоге "Введение веб-проверки подлинности [в Microsoft Edge".](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge)  

### <a name="webdriver"></a>WebDriver  

WebDriver теперь является функцией [Windows](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) по запросу \(FoD\), что упрощает автоматизацию тестирования в Microsoft Edge и получения нужной версии для устройства.  При установке [WebDriver](https://www.w3.org/TR/webdriver) больше не нужно будет вручную соответствовать сборке/ветвью/вкусу, ваш веб-диск будет автоматически обновляться, чтобы соответствовать любым новым обновлениям Windows 10.  

Вы можете установить WebDriver, включив режим разработчика, или **** установить его в качестве автономных, переехав в параметры Apps Apps & Функции Управление необязательными  >  ****  >  ****  >  **функциями.**  Дополнительные сведения можно получить в объявлении [WebDriver на сайте Блога Windows.](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand)  

### <a name="web-notification-properties"></a>Свойства веб-уведомлений  

В настоящее время для веб-уведомлений поддерживаются четыре новых  [свойства:](https://developer.mozilla.org/docs/Web/API/notification/actions) [действия,](https://developer.mozilla.org/docs/Web/API/notification/badge) [значки,](https://developer.mozilla.org/docs/Web/API/notification/image)изображения и, улучшающие нашу возможность создания уведомлений в Интернете, совместимых с существующими системами уведомлений, при этом не зависят от  `maxActions` платформы.  

### <a name="webview"></a>Веб-представление  

#### <a name="service-workers"></a>Служебные сценарии  

[Теперь сотрудники](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) служб поддерживаются в области управления WebView в дополнение к браузеру Microsoft Edge и приложениям Для Windows 10 JavaScript.  Все вкусы веб-браузера Microsoft Edge \([PWA,](/microsoft-edge/hosting/webview) [UWP,](/uwp/api/Windows.UI.Xaml.Controls.WebView) [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)\) службы поддержки, однако имейте в виду, что [API Push](https://developer.mozilla.org/docs/Web/API/Push_API) еще не доступен для версий UWP и Win32.  

Архитектуры приложений x64 требуют нейтральных пакетов \(Любой ЦП\) или x64, так как сотрудники служб не поддерживаются в процессах WoW64.  \(Чтобы сохранить пространство диска, версия WoW необходимых DLLs не входит в Windows.\)  

#### <a name="win32-webview-updates"></a>Обновления Win32 WebView  

Приложения EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) для настольных компьютеров Windows \(Win32\) обновлены несколькими новыми функциями, в том числе возможностью вводить скрипт на загрузку страницы до запуска любых других скриптов на странице \([AddInitializeScript](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript)\) и узнать, когда определенный веб-сайт WebViewControl получает или теряет фокус \([GotFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [LostFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus)\).  

Кроме того, теперь можно создать новый WebViewControl в качестве открытого окна [из window.open.](https://developer.mozilla.org/docs/Web/API/Window/open)  Событие [NewWindowRequested](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) по-прежнему сообщает приложению, когда скрипт внутри WebViewControl вызывает window.open, как всегда, но с EdgeHTML 18 его [NewWindowRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) включает возможность принимать отсрочку \([GetDeferral](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral)\) для того, чтобы установить новый WebViewControl \([NewWindow](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow)\) в качестве цели для окна.open.:  

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

Наконец, пользователи питания могут заметить приближение веб-просмотра настольных приложений \(ранее именуемого Win32WebViewHost\), внутреннего системного приложения, представляющего WebView Win32, в следующих местах:  

*   В Центре действий Windows 10.  Источник этих уведомлений следует понимать как из веб-приложения Win32.  
*   В параметрах доступа к устройству пользовательский интерфейс \( `Settings`  >  `Privacy`  >  `Camera/Location/Microphone` \).  Отключение любого из этих параметров отключает доступ ко всем webViews, установленным в приложениях Win32.  

![Параметр доступа к устройству для просмотра веб-приложений для настольных приложений](./media/desktop-app-web-viewer.png)  

## <a name="deprecated-features"></a>Неподготовленные функции  

### <a name="xss-filter-now-retired"></a>Фильтр XSS теперь отменен  

С помощью EdgeHTML 18 мы удаляем фильтр XSS в Microsoft Edge.  Наши клиенты остаются защищенными благодаря современным стандартам, таким как Политика безопасности контента [(CSP),](https://developer.mozilla.org/docs/Web/HTTP/CSP)которые обеспечивают более мощные, исполнительные и безопасные механизмы для защиты от атак впрыска контента с высокой совместимостью в современных браузерах.  

## <a name="new-apis-in-edgehtml-18"></a>Новые API в EdgeHTML 18  

Полный список новых API в EdgeHTML 18.  Они перечислены в формате [имя интерфейса]. [имя api].  

> [!NOTE] 
> Хотя следующие API выставлены в DOM, поведение некоторых из них может по-прежнему быть в разработке и скрыто за экспериментальным флагом.  Обратитесь  [к статусу платформы Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) для официального слова о поддержке функций.  

<iframe height='580' scrolling='no' title='Новые API в EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. новые <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> API pen в EdgeHTML 18 </a> msEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> CodePen </a> .</iframe>  

## <a name="previous-edgehtml-releases"></a>Предыдущие выпуски EdgeHTML  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./whats-new/edgehtml-13.md)  

[EdgeHTML 14 / Windows build 14393 (8/2016)](./whats-new/edgehtml-14.md)  

[EdgeHTML 15 / Сборка Windows 15063 (4/2017)](./whats-new/edgehtml-15.md)  

[EdgeHTML 16 / Сборка Windows 16299 (10/2017)](./whats-new/edgehtml-16.md)  

[EdgeHTML 17 / Windows build 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)  
