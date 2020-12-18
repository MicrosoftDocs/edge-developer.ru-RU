---
description: Коды ошибок для приложений в среде разработки Windows, использующих JavaScript.
title: Коды ошибок для приложений среды выполнения Windows, использующих JavaScript
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5a04a9c348a29aee2ec5936e7d923377dd53b21c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235850"
---
# Коды ошибок для приложений среды выполнения Windows, использующих JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Вот коды ошибок, отображаемая консолью Microsoft Visual Studio при разработке приложений в среде разработки Windows с помощью JavaScript.  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9601: "Не может загрузить *remoteURI.*  Приложение не может загружать удаленное веб-содержимое в локальном контексте". | Дополнительные сведения о том, что разрешено в контексте веб-страницы, см. в сведениях о функциях и [ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9602: "'javascript:' is an invalid attribute value and will be ignored.  Не используйте ЮРИС "javascript:" в локальном контексте". | Из соображений безопасности нельзя использовать URIS "javascript:" в локальном контексте.  Дополнительные сведения о том, что разрешено в локальном контексте, см. в сведениях о функциях и [ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9603: "Не может загрузить подключаемый модуль ActiveX, который имеет класс *ID класса*.  Приложения не могут загружать ActiveX элементов управления". | Приложения в среде разработки Windows, использующие JavaScript, не поддерживают настраиваемые microsoft ActiveXcontrols.  Если вам нужен элемент управления пользовательского интерфейса, используйте стандартный веб-элемент управления, библиотеку элементов управления или создайте собственный пользовательский элемент управления.  Если необходимо выполнить пользовательскую логику, создайте настраиваемый объект времени выполнения Windows.  Сведения о других отличиях HTML, CSS и JavaScript см. в [htmL, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9604: "Не может перейти к *URI,* так как используется недопустимое кодировать символы.  Приложение может переходить только к файлам в коде UTF8". | Все КОДЫ HTML, JavaScript и CSS, к которые имеет доступ в среде runtime Windows, должны быть закодированы как 8-битный формат преобразования Юникод (UTF-8).  Сведения о других отличиях HTML, CSS и JavaScript см. в [htmL, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9605: "Не может перейти к *targetURI* из *sourceURI,* так как целевой URI находится в зоне повышенной безопасности.  Перейти из зоны с более низкой безопасностью в зону с более высокими уровнями безопасности нельзя, если вы не переходите к URI локального контекста из URI контекста веб-сайта и не регистрируете локальный URI контекста с помощью метода MSApp.addPublicLocalApplicationUri". | Дополнительные сведения [см. в msApp.addPublicLocalApplicationUri.][PreviousVersionsHh771917]  |  
| APPHOST9606: "Не может загрузить *URI,* так как используется HTTP-подключение и присутствует метаэлемент ms-https-connections-only.  При использовании метаэлемента ms-https-connections разрешены только HTTPS-подключения.  Используйте HTTPS-подключение или, если безопасное подключение не требуется, удалите метаэлемент". | Дополнительные сведения см. в [сведениях о том, как требовать подключение HTTPS.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9607: "Приложение не может запустить URI по *URI* из-за этой ошибки: *failureCode."* | Причиной этой ошибки являются отсутствующий ресурс или недопустимый файл.  |  
| APPHOST9608: "Приложению не удалось перейти на страницу about:blank из-за этой ошибки: *errorCode."* |  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9610: "Приложение обнаружило ошибку при подготовке к переходу на настраиваемую страницу ошибки: *errorCode."* |  |  
| APPHOST9611: "Приложению не удалось перейти на пользовательскую страницу ошибки из-за этой ошибки: *errorCode."* |  |  
| APPHOST9613: "Приложению не удалось перейти к *URI* из-за этой ошибки: *errorCode."* |  |  
| APPHOST9614: "Документ в iframe запросил режим документов *requestedDocMode,* но система применяет режим *документов currentDocMode.*  Iframe будет использовать режим *doc currentDocMode".* | Дополнительные сведения о отображнии удаленного веб-контента см. в ссылке [на внешние веб-страницы.][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615: "Приложение не может скачать файл по *URI,* так как он был вызван программным образом за пределами локального контекста". | Возникает, когда содержимое в веб-контексте пытается программным образом скачать файл.  |  
| APPHOST9616: "Этот URI не может использовать API географического местонахождения.  API географического местонахождения могут вызываться только из URI, который является частью пакета или включен в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, что разрешено в контексте веб-страницы, см. в сведениях о функциях и [ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9617: "Этот URI не может использовать API буфера обмена.  API буфера обмена могут вызываться только из URI, который является частью пакета или включен в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, что разрешено в контексте веб-страницы, см. в сведениях о функциях и [ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9618: "Этот URI не может использовать window.close.  Метод window.close можно вызвать только из упакованного содержимого, загруженного с помощью схемы URI ms-appx". | Дополнительные сведения о том, что разрешено в контексте веб-страницы, см. в сведениях о функциях и [ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9619: "Приложение не может перейти к *URI,* так как страница в веб-контексте не может быть документом верхнего уровня приложения.  Загрузит страницу в iframe". | Страницу верхнего уровня нельзя перейти на удаленную веб-страницу, но ваше приложение может отображать веб-страницу в [iframe.][MDNIframe]  Дополнительные сведения о отображнии удаленного веб-контента см. в ссылке [на внешние веб-страницы.][PreviousVersionsWindowsAppsHh780594]  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9620: "Это приложение было закрыто, так как оно использовало HTTP-подключение и присутствует метаэлемент ms-https-connections-only.  При использовании метаэлемента ms-https-connections разрешены только HTTPS-подключения.  Используйте HTTPS-подключение или, если безопасное подключение не требуется, удалите метаэлемент". | Дополнительные сведения см. в [сведениях о том, как требовать подключение HTTPS.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9623: "Приложению не удалось разрешить *URL-адрес* из-за этой ошибки: *errorCode."* | Распространенной причиной этой ошибки является отсутствие файла.  |  
| APPHOST9624: "Приложение не может использовать сценарий для загрузки *URL-адреса,* так как URL-адрес запускает другое приложение.  Запускать другое приложение может только прямое взаимодействие с пользователем". | Приложения не могут запускать другие приложения напрямую.  Другие приложения могут запускаться пользователем при реализации определенных контрактов.  Дополнительные сведения: [Контракты приложений и расширения][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Обнаружена прямая ссылка на файл `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` ресурсов.  Эта ссылка вызывает сбои при работе за пределами среды отладки". | Из-за пути к файлу этот PNG-файл рассматривается как локализованный ресурс, что приводит к ошибке в том, что локализованные ресурсы нельзя ссылаться `logo.scale-140.png` напрямую.  Если вы собираетесь использовать этот файл в качестве языкового ресурса, см. страницу "Глобализация приложения [(HTML)".][PreviousVersionsWindowsAppsHh465006]  В противном случае попробуйте переименовать проблемный каталог.  |  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование точки запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "Метод addPublicLocalApplicationUri | Документы Майкрософт"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Как требовать подключение HTTPS (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Контракты и расширения приложений (приложения для windows Runtime) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Глобализация приложения (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Функции и ограничения по контексту (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Функции и различия HTML, CSS и JavaScript (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Как связать внешние веб-страницы (HTML) | Документы Майкрософт"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
