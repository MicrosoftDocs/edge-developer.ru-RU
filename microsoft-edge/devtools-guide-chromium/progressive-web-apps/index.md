---
description: Используйте панель приложений для проверки, изменения и отлаки манифестов веб-приложения, сотрудников служб и рабочих кэшей служб.
title: Debug Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 79edf4b04c85db33e89d18ec1832138a61f4f884
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235152"
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

# Debug Progressive Web Apps  

Используйте панель **приложений** для проверки, изменения и отлажки манифестов веб-приложений, сотрудников служб и рабочих кэшей служб.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

В этом руководстве обсуждаются только функции прогрессивного веб-приложения на панели **приложений.**  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Сводка  

*   С помощью **области манифеста** проверьте манифест веб-приложения и активируете события Add to Homescreen.  
*   С помощью области **"Сотрудники** службы" можно выполнять целый ряд задач, связанных с работой службы, таких как прекращение регистрации или обновление службы, эмуляция событий push-данных, отключение или остановка работы службы.  
*   Просмотр рабочего кэша службы из области **хранения** кэша.  
*   Отрегистрировать сотрудников службы и очистить все хранилища и **** кэши одним нажатием кнопки в области очистки хранилища.  
    
## Манифест веб-приложения  

Если вы хотите, чтобы пользователи могли добавлять приложение на свои домашние экраны для мобильных устройств, вам потребуется манифест веб-приложения.  Манифест определяет, как приложение отображается на домашнем экране, куда направить пользователя при запуске с домашнего экрана и как оно выглядит при запуске.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

После того как манифест настроен, вы **** можете проверить **** его с помощью области манифеста панели приложений.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="The Manifest Pane" lightbox="../media/manifest-pane.msft.png":::
   The **Manifest** Pane  
:::image-end:::  

*   Чтобы посмотреть на источник манифеста, щелкните ссылку **под** меткой манифеста приложения \( на `https://airhorner.com/manifest.json` предыдущем рисунке\).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   В **разделах** "Удостоверение" и **"Презентация"** просто отображаются поля из источника манифеста на более удобном для пользователя дисплее.  
*   В **разделе "Значки"** отображаются все указанные вами значки.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Служебные сценарии  

Сотрудники служб являются фундаментальной технологией в будущей веб-платформе.  Это сценарии, которые браузер выполняет в фоновом режиме, отдельно от веб-страницы.  Эти сценарии позволяют получить доступ к функциям, которые не требуют веб-страницы или взаимодействия с пользователем, например push-уведомления, фоновую синхронизацию и автономные функции.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Панель **"Рабочие службы"** на панели приложений — это основное место в DevTools для проверки и отладки сотрудников служб. ****  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="The Service Workers pane" lightbox="../media/service-workers-pane.msft.png":::
   The **Service Workers** pane  
:::image-end:::  

*   Если рабочий работник службы установлен на открытую в данный момент страницу, он будет указан на этой области.  Например, на предыдущем рисунке установлен рабочий работник службы для `https://weather-pwa-sample.firebaseapp.com` области .  
*   Автономный **контрольный** ящик помещает DevTools в автономный режим.  Это эквивалентно автономному режиму, доступного на панели **"Сеть"** или параметру `Go offline` в меню [команд.][DevtoolsCommandMenuIndex]  
*   При **перезагрузке при** обновлении необходимо, чтобы рабочий работник службы обновлял каждую загрузку страницы.  
*   Обход **для сетевого checkbox** обходит рабочий процесс службы и заставляет браузер перейти в сеть для запрашиваемого ресурса.  
*   **Кнопка** "Обновить" выполняет одно разовую обновление указанного рабочего сотрудника службы.  
*   **Кнопка** push-уведомлений эмулирует push-уведомление без полезной нагрузки (также известной как **"tickle**\").  
*   Кнопка **"Синхронизация"** эмулирует событие фоновой синхронизации.  
*   Кнопка **"Отрегистрить"** отрегистрет указанного сотрудника службы.  Ознакомьтесь [с очисткой хранилища,](#clear-storage) чтобы отоимнуть регистрацию сотрудника службы и очистить хранилище и кэш одним нажатием кнопки.  
*   **Строка** источника сообщает, когда был установлен работающий в данный момент рабочий день службы.  Ссылка — это имя файла источника рабочего службы.  Щелкнув ссылку, вы отправите вас к источнику рабочего службы.  
*   **Строка** состояния сообщает о состоянии рабочего сотрудника службы.  Номер ИД рядом с зеленым индикатором состояния \( на предыдущем рисунке\) — для активного рабочего `#36` рабочего.  Рядом с состоянием вы **** увидите кнопку запуска \(если рабочий работник **** службы остановлен\) или кнопку остановки \(если рабочий работник службы запущен\).  Рабочие службы должны быть остановлены и запущены браузером в любое время.  Явное остановка рабочего сотрудника службы с помощью кнопки **остановки** может имитировать это.  Остановка работы службы — это отличный способ проверить поведение кода при повторном вработке.  Он часто выявляет ошибки из-за ошибок, предполагающих постоянное глобальное состояние.  
*   В **строке** "Клиенты" указывается источник, к который имеет область действия для рабочего сотрудника службы.  **Кнопка** фокуса в основном полезна при включаемом всех **контрольных** окнах.  Если этот контрольный список включен, в списке будут перечислены все зарегистрированные сотрудники службы.  Если нажать кнопку **фокуса** рядом с сотрудником службы, работающим на другой вкладке, Microsoft Edge будет фокусироваться на этой вкладке.  
    
Если сотрудник службы вызывает ошибки, появляется новая метка **"Ошибки".**  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Кэши рабочих служб  

В **области хранилища** кэша содержится список ресурсов, которые были кэшироваться только для чтения с помощью [API][MDNWebCacheAPI]кэша \(service worker\) .  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="The Cache Storage Pane" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   The **Cache Storage** Pane  
:::image-end:::  

> [!NOTE]
> При первом откройте кэш и добавьте в него ресурс, DevTools может не обнаружить изменение.  Перезагрузите страницу, и вы увидите кэш.  

Если у вас два или более кэша, они **** будут указаны ниже в выпаданом списке "Хранилище кэша".  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="The Cache Storage dropdown" lightbox="../media/cache-pane-cache-storage.msft.png":::
   The **Cache Storage** dropdown  
:::image-end:::  

## Использование квоты  

Некоторые ответы в области **хранения** кэша могут быть помечены как непрозрачивые.  Это означает ответ, полученный из другого источника, например из **CDN** или удаленного API, если [CORS][FetchHttpCorsProtocol] не включен.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Чтобы избежать утечки информации между доменами, к размеру непрозрачной реакции, используемой для вычисления ограничений квот хранилища (например, о том, было ли исключение выброшено)и сообщается API, значительно добавлено `QuotaExceeded` `navigator.storage` заполнение.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Сведения об этом заполнении отличаются в зависимости от браузера, но для Microsoft Edge это означает, что минимальный размер любого кэширования непрозрачной реакции на общий объем использования хранилища составляет примерно **** [7 Мбайт.][ChromiumIssues796060#c17]  Это следует помнить при определении необходимого объема непрозрачной реакции, так как вы можете легко превысить ограничения квоты хранилища намного раньше, чем ожидалось в противном случае, в зависимости от фактического размера непрозрачной информации.  

Связанные руководства:  

*   [Stack Overflow: какие ограничения применяются к непрозрачной реакции?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Очистка хранилища  

Очистка **области** хранения — очень полезная функция при разработке последовательных веб-приложений.  С помощью этой области можно оторегистрировать службы и очистить все кэши и хранилище одним нажатием кнопки.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Проблема Chromium 796060: значение хранилища кэша растет при каждом обновлении, когда код аналитики находится в HTML-коде"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш веб-API | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: какие ограничения применяются к непрозрачной реакции?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
