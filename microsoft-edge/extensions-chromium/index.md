---
description: Обзор создания и публикации расширений Microsoft Edge (Chromium).
title: Обзор расширений Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик, расширения chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327528"
---
# Обзор расширений Microsoft Edge (Chromium)  

Расширение — это небольшая программа, которую вы \(разработчик\) используете для добавления или изменения компонентов Microsoft Edge \(Chromium\).  Расширение предназначено для улучшения ежедневного просмотра пользователем.  Он предоставляет нишевые функции, важные для целевой аудитории.  

Вы можете создать расширение, если у вас есть идея или продукт, основанный на любом из следующих условий.  

*   Определенный веб-браузер.  
*   Усовершенствования функций определенных веб-страниц.  
    
К примерам сопутствующих проектов относятся блокаторы и диспетчеры паролей.  

Расширение имеет структуру, аналогичную обычному веб-приложению.  Как минимум, он должен включать следующие функции.

*   JSON-файл манифеста приложения, содержащий базовые сведения о платформе.  
*   Файл JavaScript, который определяет функциональность.  
*   HTML-файлы и CSS-файлы, которые определяют пользовательский интерфейс.  

Чтобы работать непосредственно с веб-частью браузера, например с окном или вкладкой, необходимо отправлять запросы API и часто ссылаться на браузер по имени.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Расширение Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Расширение Microsoft Edge \(Chromium\)  
:::image-end:::  

## Базовое руководство  

Некоторые из самых популярных браузеров для создания расширений для: Safari, Firefox, Chrome, Opera, Чтобы создать и Microsoft Edge.  Отличные места для начала учебников по разработке расширений и изучения документации — это сайты, которые находятся в организациях браузера.  Следующая таблица не является точной и может использоваться в качестве отправной точки.  

| Браузер | На основе Chromium? | Веб-страницы разработки расширений |  
|:--- |:--- |:--- |  
| Safari | Нет | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Нет | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Хром | Да | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Да | [dev.opera.com/extensions][OperaDevExtensions] |  
| Сша | Да | Использование [веб-магазина Chrome][GoogleChromeWebstoreCategoryExtensions] |  
| новый Microsoft Edge | Да | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Во многих учебниках сайтов используются API браузера, которые могут не совпадать с браузером, для которого вы разрабатываете.  В большинстве случаев расширение Chromium работает как есть в разных браузерах Chromium, а API работают ожидаемым образом.  Только некоторые менее распространенные API могут быть строго специфическими для браузера.  Ссылки на учебники см. также в [этой ссылке.](#see-also)  

## Почему Chromium?  

Если ваша цель — опубликовать расширение в хранилище расширений для каждого браузера, его необходимо изменить для каждой версии, чтобы оно было целевым и запускалось в каждой отдельной среде браузера.  Например, расширения [Safari могут использовать][AppleDeveloperSafariservicesAppExtensions] как веб-, так и исходный код для взаимодействия с аналогами приложений.  Последние четыре браузера в предыдущей таблице используют один и тот же пакет кода и свести к минимуму требования к обслуживанию параллельных версий.  Эти браузеры основаны на проекте [Chromium с открытым исходным кодом.][|::ref1::|Home]  

Создайте расширение Chromium, чтобы написать наименьший объем кода.  Кроме того, он ориентирован на максимальное количество хранилищ расширений и максимальное количество пользователей, которые находят и приобретают ваше расширение.  

Следующее содержимое в основном посвящено расширениям Chromium.  

## Совместимость браузеров и тестирование расширений  

Иногда четность API не существует между браузерами Chromium.  Например, существуют различия в API удостоверений и платежей.  Чтобы убедиться, что расширение соответствует ожиданиям клиентов, просмотрите состояние API с помощью следующих официальных документы браузера.  

*   [API Chrome][ChromeDeveloperExtensionsApiIndex]  
*   [API расширения, поддерживаемые в Opera][OperaDevExtensionsApis]  
*   [Перенос расширения Chrome в Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
Необходимые API определяют изменения, которые необходимо внести для устранения различий между каждым браузером.  Это может означать, что необходимо создать несколько разные пакеты кода с небольшими отличиями для каждого магазина.  

Чтобы протестировать расширение в различных средах перед отправкой в хранилище браузера, разгрузите его в браузер во время разработки.  

## Публикация расширения в хранилищах браузера  

Вы можете отправлять расширения браузера и искать их в следующих хранилищах браузера.  

*   [Надстройки браузера Firefox][MozillaAddonsFirefoxExtensions]  
*   [Веб-магазин Chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Надстройки оперы][OperaAddonsExtensions]  
*   [Надстройки Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Некоторые магазины позволяют скачивать перечисленные расширения из других браузеров.  Однако хранилища браузеров не гарантируют доступ к браузерам.  Чтобы пользователи могли найти ваше расширение в разных браузерах, необходимо сохранить описание в каждом хранилище расширений браузера.  

Пользователям может потребоваться установить расширение в разных браузерах. В этом сценарии можно перенести существующие расширения Chromium из одного браузера в другой.  

### Перенос существующего расширения в Microsoft Edge  

Если вы уже разработали расширение для другого браузера Chromium, вы можете отправить его в магазин надстройки Microsoft Edge. Вам не нужно переописывать расширение и убедитесь, что оно работает в Microsoft Edge.  При переносе существующего расширения Chromium в другие браузеры Chromium убедитесь, что те же API или альтернативы доступны для вашего целевого браузера.  

For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]. После переноса расширения в целевой браузер необходимо опубликовать его.  

### Публикация на веб-сайте надстройки Microsoft Edge  

Чтобы начать публикацию расширения в Microsoft [][MicrosoftDeveloperRegistration] Edge, необходимо зарегистрировать учетную запись разработчика с учетной записью электронной почты MSA, чтобы отправить описание расширения в Магазин.  Учетная запись электронной почты MSA включает `@outlook.com` `@live.com` и т. д.  При выборе адреса электронной почты для регистрации рассмотрите возможность передачи или передачи прав владельца расширения другим лицам в вашей организации.  После завершения регистрации вы можете создать новую отправку расширения в магазин.  

Чтобы отправить расширение в Магазин, убедитесь, что вы предоставили следующие элементы.  

*   Архивный \( `.zip` \) файл, содержащий файлы кода.  
*   Все необходимые визуальные ресурсы, включая логотип и небольшую рекламную плитку.  
*   Необязательный рекламный носиттель, например снимки экрана, рекламные плитки и URL-адрес видео.  
*   Сведения о расширении, такие как имя, краткое описание и ссылка на политику конфиденциальности.  

> [!NOTE]
> У разных хранилищ могут быть разные требования к отправке.  В списке выше приводится перечень [требований][ExtensionsChromiumPublish] для публикации расширения для Microsoft Edge.  

После успешной отправки расширения расширение проходит проверку и проходит или не проходит сертификацию.  Владельцы уведомлены о результатах и при необходимости выдаются дальнейшие действия.  При отправке обновления расширения в Магазин начинается новый процесс проверки.  

## См. также  

*   [Перенос расширения Google Chrome][ExtensionworkshopPorting]  
*   [Создание расширения приложения Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Ваше первое расширение (Firefox)][MDNWebextensionsYourFirst]  
*   [Руководство по началу работы (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Начало работы (опера)][OperaDevExtensionsGettingStarted]  
*   [Начало работы с расширениями Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Перенос расширения Chrome в Microsoft Edge (Chromium) | Документы Майкрософт"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Начало работы с расширениями Microsoft Edge (Chromium) | Документы Майкрософт"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Публикация расширения | Документы Майкрософт"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Разработка расширений для Microsoft Edge | Разработчик (Майкрософт)"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Центр партнеров | Разработчик (Майкрософт)"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Расширения для Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Safari App Extensions | Разработчик Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Создание расширения приложения Safari | Разработчик Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Что такое расширения? | Разработчик Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "API Chrome | Разработчик Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Руководство по началу работы | Разработчик Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Перенос расширения Google Chrome | Семинар по расширению"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Расширения браузера | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Ваше первое расширение | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Расширения | Надстройки для Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Расширения | Надстройки Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Документация по расширениям | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API расширения, поддерживаемые в Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Начало работы | Dev. Opera"  
