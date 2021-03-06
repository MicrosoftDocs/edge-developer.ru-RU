---
description: Используйте панель приложений для проверки, изменения и отработки манифестов веб-приложений, сотрудников служб и кэшей сотрудников службы.
title: Отламывка прогрессивных веб-приложений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398541"
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

# <a name="debug-progressive-web-apps"></a>Отламывка прогрессивных веб-приложений  

Используйте панель **приложений** для проверки, изменения и отработки манифестов веб-приложений, сотрудников служб и кэшей сотрудников службы.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

В этом руководстве обсуждаются только функции прогрессивного веб-приложения панели **приложений.**  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a>Сводка  

*   Используйте области **Манифеста** для проверки манифеста веб-приложения и запуска событий Add to Homescreen.  
*   Используйте области **Service Workers** для целого ряда задач, связанных с рабочим обслуживанием, таких как незарегистрирование или обновление службы, эмуляция событий push-связи, отключение или остановка сотрудника службы.  
*   Просмотр кэша сотрудника службы из **области хранения** кэша.  
*   Незарегистрировать сотрудника службы и очистить все хранилища и кэши с помощью одной кнопки выберите из области **хранения Clear.**  
    
## <a name="web-app-manifest"></a>Манифест веб-приложения  

Если вы хотите, чтобы пользователи могли добавлять приложение на мобильные домашние экраны, вам нужен манифест веб-приложения.  Манифест определяет, как приложение отображается на домашнем экране, куда направлять пользователя при запуске с домашнего экрана и как выглядит приложение при запуске.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

После того, как вы настроите манифест, вы можете проверить его с помощью области **Манифест** **панели** приложений.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Области манифеста" lightbox="../media/manifest-pane.msft.png":::
   Области **манифеста**  
:::image-end:::  

*   Чтобы взглянуть на источник манифеста, выберите ссылку под меткой **Манифест приложения** \( на `https://airhorner.com/manifest.json` предыдущем рисунке\).  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   В **разделах Identity** и **Presentation** отображаются поля из источника манифеста в более удобном для пользователя дисплее.  
*   В **разделе Значки** отображаются все указанные значки.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a>Служебные сценарии  

Работники служб являются фундаментальной технологией в будущей веб-платформе.  Это скрипты, которые браузер выполняет в фоновом режиме, отдельно от веб-страницы.  Скрипты позволяют получать доступ к функциям, которые без необходимости веб-страницы или взаимодействия с пользователем, например push-уведомления, синхронизации фона и автономного взаимодействия.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

Панель **сотрудников служб** в панели **Приложений** — это основное место в DevTools для проверки и отладки сотрудников службы.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Области рабочих служб" lightbox="../media/service-workers-pane.msft.png":::
   Области **рабочих** служб  
:::image-end:::  

*   Если сотрудник службы установлен на открытую страницу в настоящее время, он указан на этой области.  Например, на предыдущем рисунке установлен сотрудник службы для области `https://weather-pwa-sample.firebaseapp.com` .  
*   Автономный **почтовый** ящик выводит DevTools в автономный режим.  Это эквивалентно автономному режиму, доступному с помощью средства **Network,** или параметру `Go offline` в [командном меню.][DevtoolsCommandMenuIndex]  
*   Обновление **при перезагрузке контрольного** ящика заставляет сотрудника службы обновляться на каждой загрузке страницы.  
*   Обход **сетевого почтового** ящика обходит сотрудника службы и заставляет браузер перейти в сеть для запрашиваемого ресурса.  
*   Кнопка **Update** выполняет одно время обновление указанного сотрудника службы.  
*   Кнопка **push** эмулирует push-уведомление без полезной нагрузки \(также известной как **щекотка**\).  
*   Кнопка **Sync** эмулирует событие фоновой синхронизации.  
*   Кнопка **Unregister** отрегистрирована указанному работнику службы.  Ознакомьтесь [с возможностью](#clear-storage) отрегистрации сотрудника службы и очистки хранилища и кэшей с помощью одной кнопки.  
*   Строка **Source** сообщает, когда был установлен работающий в настоящее время сотрудник службы.  Ссылка — это имя источника файла сотрудника службы.  Выбор по ссылке отправляет вас к источнику сотрудника службы.  
*   В **строке Status** указывается состояние сотрудника службы.  Номер ID рядом с зеленым индикатором состояния \( на предыдущем рисунке\) для действующего в настоящее время `#36` сотрудника службы.  Рядом со состоянием **** отображается кнопка запуска \(если сотрудник **** службы остановлен\) или кнопка остановки \(если рабочий службы запущен\).  Сотрудники службы предназначены для того, чтобы остановиться и начать работу с помощью браузера в любое время.  Явное прекращение работы сотрудника службы с помощью кнопки **остановки** может имитировать это.  Остановка сотрудника службы — это отличный способ проверить, как ведет себя код, когда сотрудник службы снова запускается обратно.  Он часто выявляет ошибки из-за ошибок в предположениях о сохраняемом глобальном состоянии.  
*   В **строке** "Клиенты" указывается происхождение, в которое будет вовсю засвеяна область действия сотрудника службы.  Кнопка **фокуса** в основном полезна при включении всех **контрольных** ящиков.  Когда этот контрольный ящик включен, все зарегистрированные сотрудники службы перечислены.  Если вы выбираете кнопку **фокуса** рядом с сотрудником службы, который работает на другой вкладке, Microsoft Edge фокусируется на этой вкладке.  
    
Если сотрудник службы вызывает какие-либо ошибки, появляется новая метка , называемая **Ошибки.**  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a>Кэши сотрудников службы  

В **области хранения** кэша содержится список ресурсов, которые кэшировали только для чтения с помощью [API][MDNWebCacheAPI]кэша \(service worker\) .  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Пространство хранения кэша" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   Пространство **хранения кэша**  
:::image-end:::  

> [!NOTE]
> При первом открываемом кэше и добавлении в него ресурса, DevTools может не обнаружить изменения.  Обновите страницу и отобразите кэш.  

Если открыты два или более кэшей, кэши **** отображаются под следующей каплей хранилища кэша.  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Отсев хранилища кэша" lightbox="../media/cache-pane-cache-storage.msft.png":::
   **Отсев хранилища кэша**  
:::image-end:::  

## <a name="quota-usage"></a>Использование квот  

Некоторые ответы в области **хранения** кэша могут быть помечены как "непрозрачивые".  Это относится к ответу, извлеченному из другого происхождения, например из **CDN** или удаленного API, когда [CORS][FetchHttpCorsProtocol] не включен.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Чтобы избежать утечек меж доменных сведений, к размеру непрозрачной реакции, используемой для вычисления ограничений квоты хранения\(например, будет ли выброшено исключение\) добавляется значительное обивка и `QuotaExceeded` `navigator.storage` сообщается API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Сведения об этой обивке варьируются от браузера до браузера, но для Microsoft Edge это означает, что минимальный размер, который любой один кэширования непрозрачной реакции способствует общему использованию хранилища составляет около [7 мегабайт][ChromiumIssues796060#c17]. ****  Помните обивку при определении того, сколько непрозрачной реакции необходимо кэширование, так как ограничения квоты на хранение могут быть превышены гораздо раньше, чем ожидались в зависимости от фактического размера непрозрачной информации.  

Связанные руководства:  

*   [Переполнение стека: какие ограничения применяются к непрозрачной реакции?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a>Очистка хранилища  

Пространство **Clear Storage** — это очень полезная функция при разработке прогрессивных веб-приложений.  Эта области позволяет отрегистрировать сотрудников службы и очистить все кэши и хранилища с помощью одной кнопки выбрать.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: значение хранилища кэша повышается при каждом обновлении, когда код Analytics находится в html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш — веб-| MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Переполнение стека: какие ограничения применяются к непрозрачной реакции?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
