---
description: Обзор расширений Microsoft Edge (Chromium), а также общие сведения о создании и публикации расширений браузера.
title: Расширения Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик, расширения chromium
ms.openlocfilehash: 04b9ffb7ec175bad4f980310819ea6d3551ef9f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230945"
---
# Обзор расширений Microsoft Edge (Chromium) 

Расширение — это небольшая программа, которую вы (разработчик\) можете использовать для добавления новых функций в Microsoft Edge \(Chromium\) или изменения существующих функций.  Расширение предназначено для улучшения ежедневного просмотра пользователем за счет предоставления функций ниш, которые важны для целевой аудитории.  

Вы можете создавать расширения, если ваша идея или продукт зависит от доступности определенного веб-браузера или дополняет возможности браузера, в которых функциональность, которую вы хотите предоставить, расширяет существующие веб-сайты.  К примерам сопутствующих проектов относятся adblockers и диспетчеры паролей.  

Расширение имеет структуру, аналогичную обычному веб-приложению.  Как минимум, он включает JSON-файл манифеста приложения, содержащий базовые сведения о платформе, файл JavaScript для определения функциональности и HTML-файл и CSS-файл для определения интерфейса пользователя (при необходимости).)  Для работы непосредственно с веб-частью браузера, например с окном или вкладкой, необходимо отправлять запросы API и часто ссылаться на браузер по имени.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Расширение Microsoft Edge (Chromium)":::
  Расширение Microsoft Edge \(Chromium\)  
:::image-end:::  

## Базовое руководство  

Некоторые из наиболее популярных браузеров, которые необходимо создать для: Safari, Firefox, Chrome, Opera, Safari и Microsoft Edge.  Отличные места для начала учебников по разработке расширений и изучения документации — это сайты, которые находятся в организациях браузера.  Следующая таблица не является точной, используйте ее в качестве отправной точки.  

| Браузер | На основе Chromium? | Домашняя страницы разработки расширений |  
|:--- |:--- |:--- |  
| Safari | Нет | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Нет | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Хром | Да | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Да | [dev.opera.com/extensions][OperaDevExtensions] |  
| Сша | Да | Использование [веб-магазина Chrome][GoogleChromeWebstoreCategoryExtensions] |  
| новый Microsoft Edge | Да | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Во многих учебниках сайтов используются API браузера, которые могут не совпадать с браузером, для которого вы разрабатываете.  В большинстве случаев расширение Chromium работает как есть в разных браузерах Chromium, а API работают ожидаемым образом.  Только некоторые менее распространенные API могут быть строго специфическими для браузера.  Ссылки на учебники см. также в [этой теме.](#see-also)  

## Почему Chromium?

Если ваша цель — опубликовать расширение в максимально возможном числе хранилищ расширений браузера, его необходимо изменить для нескольких версий, чтобы оно было целевым и запускалось в каждой отдельной среде браузера.  [Расширения Safari,][AppleDeveloperSafariservicesAppExtensions]в отличие от других типов расширений, могут использовать как веб-, так и исходный код для взаимодействия с другими приложениями.  [Расширения Firefox имеют][MDNWebextensions] более общие отношения с другими [][ExtensionworkshopPorting] типами расширений, но также следует учитывать некоторые различия.  Тем не менее, есть некоторые хорошие новости; Последние четыре браузера на приведенной выше диаграмме могут использовать один и тот же пакет кода и свести к минимуму требования к изменению и обслуживанию параллельных версий.  Это происходит потому, что браузеры основаны на проекте [Chromium с открытым исходным кодом.][|::ref1::|Home]  

Создание расширения Chromium позволяет написать наименьший объем кода, чтобы максимально увеличить количество хранилищ расширений, на которые вы нацелены, и, в конечном счете, количество пользователей, которые могут найти и приобрести расширение.  

Следующее содержимое в основном посвящено расширениям Chromium.  

## Совместимость с браузером и тестирование расширений  

Иногда четность API не существует между браузерами Chromium.  Например, существуют различия в API удостоверений и платежей.  Чтобы убедиться, что расширение соответствует ожиданиям клиентов, просмотрите состояния API с помощью официальной документации по браузеру, например API [Chrome,][ChromeDeveloperExtensionsApiIndex]API расширений, поддерживаемых в [Opera,][OperaDevExtensionsApis]и расширения [Chrome для Microsoft (Chromium) Edge.][ExtensionsChromiumDeveloperGuidePortChrome]  

В зависимости от необходимых API эти различия могут означать, что необходимо создать несколько разные пакеты кода с небольшими отличиями в коде для каждого магазина.  

При разработке расширения вы можете перегрузить его в браузер, чтобы протестировать его в различных средах перед отправкой расширения в хранилища браузера.  

## Публикация расширения в хранилищах браузера  

Вы можете отправлять расширения браузера и искать их в следующих хранилищах браузера.  

*   [Надстройки браузера Firefox][MozillaAddonsFirefoxExtensions]  
*   [Веб-магазин Chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Надстройки оперы][OperaAddonsExtensions]  
*   [Надстройки Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Некоторые магазины позволяют скачивать перечисленные расширения из других браузеров.  Скачивание из другого браузера может заранее сэкономить усилия \(разработчика\) и удалить требование отправки в дополнительные магазины, если пользователи могут переходить к существующим спискам в Магазине в разных браузерах.  Однако хранилища браузеров не гарантируют доступ к браузерам.  Чтобы ваши пользователи могли найти расширение в разных браузерах, необходимо сохранить описание в каждом хранилище расширений браузера.  

Расширение может иметь перекрывающиеся аудитории, которые часто используют несколько браузеров, или вы можете обнаружить, что оно должно быть нацелено на аудиторию, которую раньше не было.  Для этого существующие расширения Chromium могут быть перенесены из одного браузера в другой.  

### Перенос существующего расширения в Microsoft Edge  

Если вы уже разработали расширение для другого браузера Chromium и хотите предложить его и убедиться, что оно работает через Microsoft Edge, вам не нужно переописывать расширение.  Перенос существующих расширений Chromium в другие браузеры Chromium прост, если вы используете API, доступные в разных браузерах, или если существуют другие API, которые предоставляют необходимые функции.  

Дополнительные сведения о переносе расширения Chrome см. в дополнительных сведениях о переносе расширений Chrome в [Microsoft (Chromium) Edge.][ExtensionsChromiumDeveloperGuidePortChrome]  После переноса расширения в целевой браузер необходимо опубликовать его.  

### Публикация на веб-сайте надстройки Microsoft Edge  

Чтобы начать публикацию расширения в Microsoft [][MicrosoftDeveloperRegistration] Edge, необходимо зарегистрировать учетную запись разработчика с учетной записью электронной почты MSA \(@outlook.com, @live.com и т. д.), чтобы отправить описание расширения в Магазине.  При выборе адреса электронной почты для регистрации рассмотрите возможность передачи или передачи прав владельца расширения другим лицам в вашей организации.  После завершения регистрации вы можете создать новую отправку расширения в магазин.  

Чтобы отправить расширение в Магазин, необходимо выполнить следующие требования.  

*   Архивный файл \(.zip\), содержащий файлы кода.  
*   Все необходимые визуальные ресурсы, включая логотип и небольшую рекламную плитку.  
*   Необязательный рекламный носиттель, например снимки экрана, более крупные рекламные плитки, URL-адрес или любое сочетание с видео вашего расширения.  
*   Сведения о расширении, такие как имя, краткое описание, длинное описание и ссылка на политику конфиденциальности.  

> [!NOTE]
> Разные хранилища могут предъявлять разные требования к отправке.  В списке выше приводится перечень [требований][ExtensionsChromiumPublish] для публикации расширения в Microsoft Edge.  

После завершения процесса отправки расширение проходит проверку и проходит сертификацию или завершается с неудачей.  Владельцы уведомлены о результатах и при необходимости выдаются дальнейшие действия.  При отправке в Магазин обновленного расширения, включая обновления сведений о расширении, начинается новый процесс проверки.  

## См. также  

*   [Перенос расширения Google Chrome][ExtensionworkshopPorting]  
*   [Создание расширения приложения Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Ваше первое расширение (Firefox)][MDNWebextensionsYourFirst]  
*   [Руководство по началу работы (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Начало работы (опера)][OperaDevExtensionsGettingStarted]  
*   [Начало работы с расширениями Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Перенос расширения Chrome в Microsoft (Chromium) Edge | Документы Майкрософт"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Начало работы с расширениями Microsoft Edge (Chromium) | Документы Майкрософт"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Публикация расширения | Документы Майкрософт"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Разработка расширений для Microsoft Edge | Разработчик (Майкрософт)"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Центр партнеров | Разработчик (Майкрософт)"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Расширения для Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Расширения приложений Safari | Разработчик Apple"  
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

[OperaDevExtensions]: https://dev.opera.com/extensions "Документация по расширениям | Dev.Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API расширения, поддерживаемые в Opera | Dev.Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Начало работы | Dev.Opera"  
