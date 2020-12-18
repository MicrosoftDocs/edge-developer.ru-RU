---
description: В этом руководстве представлен обзор функций и стандартов разработчика, включенных в EdgeHTML 15.
title: Новые функции и API в EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 126fbc5f2a077052654063237c669089a3376ab0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235783"
---
# Новые возможности EdgeHTML 15  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот изменения, внесенные в текущий выпуск платформы Microsoft Edge, с [версии Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) \(04/2017, сборка 15063\).  Общие сведения об изменениях браузера Microsoft Edge см. в новой версии Microsoft Edge в [Windows 10 Creators Update.](https://blogs.windows.com/msedgedev/2017/04/11)  

Изменения в последующих сборках Windows Insider Preview см. в подстройке "Что нового [в EdgeHTML".](../whats-new.md)  

Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_15](./edgehtml-15.md) .  

## Новые возможности  

### Настраиваемые свойства CSS  

Microsoft Edge теперь поддерживает [настраиваемые свойства CSS,](https://drafts.csswg.org/css-variables)то есть переменные CSS.  Переменные CSS позволяют создавать настраиваемые свойства CSS, которые можно повторно использовать во всех таблицах стилей, чтобы уменьшить количество дублирующихся данных, таких как повторяющиеся цвета.  Использовать переменные CSS просто:  

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Пересечение между пересечением  

В EdgeHTML 15 вводится спецификация [API "Пересечение](https://w3c.github.io/IntersectionObserver) пересечений".  API Intersection Intersection Позволяет асинхронно запрашивать положение и видимость элементов DOM относительно других элементов или глобального окне просмотра.  Этот API устраняет необходимость в пользовательском дорогом коде, создавая метод для эффективного уведомления элементов, когда они находятся в представлении.  

### JavaScript  

Оптимизация производительности находится на центральном этапе с помощью отзыва EdgeHTML 15 ядра JavaScript для Chakra.  С помощью Обновления Windows 10 Creators Update Компания Chakra сохраняет память, повторно откладывая функции и оптимизая аргументы кучи и улучшая производительность для минифицированного кода.  

Кроме того, в EdgeHTML 15 представлены следующие предварительные версии функций:  

#### Экспериментальные функции JavaScript  

Включено с `about:flags`  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) \([demo](https://webassembly.org/demo)\)  
*   [Общая память и атомарные](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

Дополнительные сведения см. в дополнительных сведениях об улучшенной производительности [JavaScript, WebAssembly](https://blogs.windows.com/msedgedev/2017/04/20) и общей памяти в Microsoft Edge.  

### API запроса оплаты  

Теперь [поддерживается API](https://w3.org/TR/payment-request) запроса на оплату, что позволяет упротить поиск и платежи в Интернете на ПК и телефонах с Windows 10.  Этот API позволяет Microsoft Edge действовать в качестве посредника между продавцами, потребителями и методами оплаты (например, кредитными картами\), которые потребители хранили в облаке.  Дополнительные сведения об API запроса платежей можно узнать в более простых веб-платежах: введение в [API](https://blogs.windows.com/msedgedev/2016/12/15) запроса платежей и руководство разработчика [API запроса](/microsoft-edge/dev-guide/device/payment-request-api) платежей.  

### TCP Fast Open (TFO)  
TCP Fast Open — это функция, которая сокращает количество кругового подключения, необходимого для открытия подключения TCP, что улучшает производительность сети браузера.  Дополнительные сведения см. в [подстроке "Создание более быстрого и безопасного веб-сайта с помощью TCP Fast Open".](https://blogs.windows.com/msedgedev/2016/06/15)  Из-за различий в взаимосвязи в различных сетевых topologies эти функции не включены по умолчанию в Microsoft Edge.  Чтобы включить его, введите адресную стойку и выберите в разделе "Сеть" для включить `about:flags` **быстрый TCP-открытие.** ****  

### WebRTC и поддержка видеокодека RTC с поддержкой  

EdgeHTML 15 поддерживает подмножество API WebRTC 1.0 для обеспечения связи с приложениями, построенными с более ранними версиями API W3C WebRTC-PC до 2015 г.  Подробные [сведения см. в справочнике по API WebRTC.](/previous-versions//mt806139(v=vs.85))  

Чтобы воспользоваться преимуществами наших самых сложных функций в одноранговом аудио- и видеосвязи, рекомендуем использовать API Real-Time [Communication).](https://ortc.org)  API ORTC лучше подходит для ситуаций, когда вы хотите настроить групповые аудио- и видеозвуки или напрямую управлять отдельными объектами транспорта, отправитель и приемник.  

Microsoft Edge поддерживает видео H.264/AVC и VP8 с ORTC и WebRTC 1.0 и предоставляет следующие функции для поддержки обоих типов кодеков: [abs-send-time,](https://webrtc.org/experiments/rtp-hdrext/abs-send-time) [goog-remb,](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03) [picture Loss Indication и Generic NACK feedback](https://tools.ietf.org/html/rfc4585), [RTP Retransmission](https://tools.ietf.org/html/rfc4588).  

Дополнительные сведения см. в введение [в WebRTC 1.0](https://blogs.windows.com/msedgedev/2017/01/31)и взаимодействие в режиме реального времени в Microsoft Edge.  

### WebVR  

Microsoft Edge теперь поддерживает [WebVR](https://immersive-web.github.io/webxr), экспериментальный API, который подключает экраны windows Mixed Reality к подключенным мониторам и Microsoft Edge.  Это подключение позволяет использовать содержимое ВИРТУАЛЬНОЙ РЕАЛЬНОСТИ на веб-сайте, то есть иммерсивные возможности виртуальной реальности больше не ограничиваются классическими приложениями.  

Виртуальная реальность в Microsoft Edge на платформе WebGL, API JavaScript для отрисовки 3D и двухd графики.  Поддерживаются приложения и приложения WebGL, построенные с помощью библиотек WebGL, таких как BabylonJS.  После подключения WebVR отправляет визуальные эффекты, соответствующие сведениям о положении и датчике вокруг гарнитуры.  API WebVR также поддерживает пространственные контроллеры благодаря расширению **API геймпада.**  Этот API по умолчанию находится вкл., поэтому нет необходимости в перегонах флага.  

<!--  Virtual reality in Microsoft Edge is powered by WebGL, a JavaScript API for rendering 3D and 2D graphics.  WebGL applications and applications built with WebGL libraries like BabylonJS are supported.  Once connected, WebVR sends visuals corresponding to the position and sensor information around the headset.  The WebVR API also supports spatial controllers thanks to an extension to the [Gamepad API](../dom/gamepad-api.md).  This API is on by default, so no need to toggle a flag.  -->  

Подробные сведения см. в справочнике по [API WebVR](/previous-versions/mt806281(v=vs.85)) и [API gamepad.](https://developer.mozilla.org/docs/Web/API/Gamepad_API)  

 > [!NOTE] 
 > Так как спецификация WebVR еще находится в разработке, реализация Microsoft Edge может измениться позже.  

## Обновленные функции  

### Политика безопасности контента (уровень 2)  

Сайты, уже использующие CSP 1, должны продолжать работать с поддержкой Microsoft Edge для CSP 2, однако лучше всего переключить все директивы, которые загружают рабочие сценарии на новую директиву, на будущий `frame-src` `child-src` сайт.  \(В CSP 3 больше не применяется к `frame-src` сотрудникам.\) CSP 2 также добавляет следующее:  

:::row:::
   :::column span="1":::
      Новые директивы  
   :::column-end:::
   :::column span="2":::
      `base-uri`, `child-src` , `form-action` и `frame-ancestors` `plugin-types` .  <!--  See [Microsoft Edge supported CSP directives](../security/content-security-policy.md) for more.  -->  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Поддержка сотрудников  
   :::column-end:::
   :::column span="2":::
      Сценарии фоновых рабочих служб управляются собственной политикой, отдельной от политики загрузки документа.  Как и в хост-документах, можно настроить CSP для рабочего в заголке ответа.  Кроме того, в CSP 2 новые возможности: флаги директивы `allow-scripts` `allow-same-origin` влияют на создание `sandbox` рабочих потоков.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Inline scripts and styles  
   :::column-end:::
   :::column span="2":::
      CSP 2 позволяет использовать скрипты и блоки стилей, предоставляя в качестве механизма для списка списков списков неисписаные и хеши.  Nonces — это случайные значения base-64, созданные на каждой загрузке страницы, которая отображается как в политике CSP, так и в тегах скриптов на странице.  Когда страница динамически создается при загрузке, сервер создает значение nonce, вставляет его в nonceToken на странице, а также объявляет его в http-загоне политики безопасности содержимого.  Хеши — это статические значения, созданные \(с помощью алгоритмов sha256, sha384 или sha512\) из содержимого элемента или элемента, которые затем заданы `<script>` `<style>` \(using `script-src` или directives\) в политике `style-src` CSP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Отчеты о нарушениях CSP  
   :::column-end:::
   :::column span="2":::
      Новое событие, `SecurityPolicyViolationEvent` которое теперь и выпущено при нарушении CSP.  Прежний механизм отчетности CSP `report-uri` по-прежнему поддерживается.  В отчеты о нарушении добавлено несколько новых полей, в том числе \(политика, которая была `effectiveDirective` нарушена\), `statusCode` \(код http-ответа\), \(URL-адрес ресурса для `sourceFile` нарушения\) и `lineNumber` `columnNumber` .  
   :::column-end:::
:::row-end:::  

### Проверка подлинности в Интернете  

Поддержка Microsoft Edge для новых **API веб-проверки** подлинности с использованием биометрии [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) была обновлена с помощью следующих изменений:  

<!--  Microsoft Edge support for the emerging [Web Authentication API](../device/web-authentication.md) using [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) biometrics has been updated with the following changes:  -->  

*   Первоначальная реализация экспериментального API веб-проверки подлинности, представленная в [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04) \(юбилейное обновление Windows 10, сборка 10240, 7/2016\) была представлена через API с префиксом [MS \(интерфейс MSCredentials\).](/previous-versions/mt697639(v=vs.85))  Хотя эти API по-прежнему доступны в EdgeHTML 15, они теперь не являются частью префиксов, основанных на стандартах API и поведения, определенных в более недавнем снимке спецификации, и, скорее всего, продолжат изменяться по мере развития спецификации до стандартизации. [](https://w3.org/TR/2016/WD-webauthn-20160928)  

*   Последняя реализация Microsoft Edge по умолчанию отключена и находится за флагом \(введите в адресной панели, чтобы включить `about:flags` функцию\).  

*   Microsoft Edge пока не поддерживает внешние учетные данные, такие как USB-ключи или Bluetooth устройств.  Текущий API ограничен внедренными учетными данными, хранимами в TPM.  Если TPM не доступен на устройстве, используется программный откат.  

*   Учетная запись пользователя Windows, зарегистрированная в текущий момент, должна быть настроена на поддержку по крайней мере ПИН-кода и, желательно, биометрии лиц или отпечатков пальцев.  Это гарантирует, что Windows сможет проверить подлинность доступа к TPM.  

*   Из предварительно [заданных расширений,](https://w3.org/TR/webauthn/#extension-predef) описанных в спецификации, Microsoft Edge поддерживает только [FIDO AppId](https://w3.org/TR/webauthn/#extension-appid) \( `webauthn_txAuthSimple` \) в настоящее время.  

*  В `timeoutSeconds` настоящее время этот параметр не оценивается  

### WebDriver  

EdgeHTML 15 обеспечивает ряд обновлений WebDriver, включая поддержку флага командной строки в тихом режиме и новых конечных точек команд:  

| Метод | Шаблон URI | Команда |  
|:--- |:---  |:--- |    
| POST | /session/{session id}/alert/accept | [Принять оповещение](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert) |  
| POST | /session/{session id}/alert/dismiss | [Оповещение об отклонении](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert) |  
| GET | /session/{session id}/alert/text | [Получить текст оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text) |  
| POST | /session/{session id}/alert/text | [Отправка текста оповещения](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text) |  
| POST | /session/{session id}/execute/async | [Выполнение а async Script](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script) |  
| POST | /session/{session id}/execute/sync | [Выполнение скрипта](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script) |  
| GET | /session/{session id}/window | [Get Window Handle](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle) |  
| GET | /session/{session id}/window/handles | [Get Window Handles](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles) |  

Дополнительные сведения и состояние других функций WebDriver можно узнать в [WebDriver.](../../webdriver/index.md)  

## Новые API в EdgeHTML 15  

Ниже полный список новых API в EdgeHTML 15.  Они перечислены в формате `[interface name].[api name]` .  

<iframe height='582' scrolling='no' title='Новые API EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> New EdgeHTML15 APIs </a> by Microsoft Edge Docs ( @MicrosoftEdgeDocumentation ) <a href='http://codepen.io/MicrosoftEdgeDocumentation'> on </a> <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 12 / Сборка Windows 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Сборка Windows 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Сборка Windows 14393 (8/2016)](./edgehtml-14.md)  
