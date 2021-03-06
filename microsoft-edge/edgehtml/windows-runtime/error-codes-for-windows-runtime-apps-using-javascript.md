---
description: Коды ошибок для приложений среды выполнения Windows, использующих JavaScript
title: Коды ошибок для приложений среды выполнения Windows, использующих JavaScript
ms.custom: ''
ms.date: 11/03/2020
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e7241d675a6f488e70eefb20c40149683f965c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398492"
---
# <a name="error-codes-for-windows-runtime-apps-using-javascript"></a>Коды ошибок для приложений среды выполнения Windows, использующих JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Ниже представлены коды ошибок, отображаемые консолью Microsoft Visual Studio при разработке приложений для запуска Windows с помощью JavaScript.  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9601: "Не может загрузить *remoteURI*.  Приложение не может загружать удаленный веб-контент в локальном контексте". | Дополнительные сведения о том, что разрешено в веб-контексте, см. в странице [Features and restrictions by context.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9602: "'Javascript:" является недопустимым значением атрибута и будет игнорироваться.  Не используйте URL-адреса javascript:' в локальном контексте." | В целях безопасности нельзя использовать URL-адреса javascript:' в локальном контексте.  Дополнительные сведения о том, что разрешено в локальном контексте, см. в дополнительных сведениях Об особенностях [и ограничениях по контексту.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9603: "Не может загрузить ActiveX, который имеет класс ID *класса*.  Приложения не могут загружать ActiveX элементов управления". | Приложения для windows runtime с помощью JavaScript не поддерживают настраиваемые Microsoft ActiveXcontrols.  Если вам нужен элемент управления пользовательским интерфейсом, используйте стандартный веб-элемент управления, библиотеку элементов управления или создайте собственный настраиваемый элемент управления.  Если требуется выполнить настраиваемую логику, создайте настраиваемый объект windows Runtime.  Сведения о других отличиях HTML, CSS и JavaScript см. в [html-коде, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9604: "Не может *перейти к uri,* так как в нем используется кодить недействительный символ.  Приложение может перемещаться только по файлам с кодом UTF8". | Все HTML, JavaScript и CSS, доступ к которые доступны во время запуска Windows, должны быть закодированы как 8-битный формат преобразования Юникод (UTF-8).  Сведения о других отличиях HTML, CSS и JavaScript см. в [html-коде, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9605: "Не может перейти к *targetURI* из *sourceURI,* так как URI назначения находится в более высокой зоне безопасности.  Вы не можете перемещаться из зоны с более низкой безопасностью в зону с более высокой безопасностью, если вы не переходите в локальный контекст URI из URI веб-контекста и вы зарегистрировали локальный контекст URI с помощью метода MSApp.addPublicLocalApplicationUri". | Дополнительные сведения [см. в сайте MSApp.addPublicLocalApplicationUri.][PreviousVersionsHh771917]  |  
| APPHOST9606: "Не может загрузить *uri,* так как он использует подключение HTTP и мета-элемент ms-https-connections-only.  Только подключения HTTPS разрешены при использовании мета элемента ms-https-connections-only.  Используйте подключение HTTPS или, если вам не требуется безопасное подключение, удалите элемент мета". | Дополнительные сведения см. [в странице Как требовать подключения HTTPS.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9607: "Приложение не может запустить URI в *uri* из-за этой ошибки: *failureCode*." | Недостающий ресурс или недействительный файл являются распространенными причинами этой ошибки.  |  
| APPHOST9608: "Приложение не могло перейти на страницу about:blank из-за этой ошибки: *errorCode."* |  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9610: "Приложение обнаружило ошибку при подготовке к переходу на настраиваемую страницу ошибок: *errorCode."* |  |  
| APPHOST9611: "Приложение не могло перейти на настраиваемую страницу ошибок из-за этой ошибки: *errorCode."* |  |  
| APPHOST9613: "Приложение не могло перейти в *uri*  из-за этой ошибки: *errorCode*." |  |  
| APPHOST9614: "Документ в iframe запрашивал запрашиваемую *doc-режимDocMode,* но система применяет режим *doc currentDocMode.*  Iframe будет использовать *режим doc currentDocMode".* | Дополнительные сведения о отображение удаленного веб-контента см. в странице [How to link to external web pages.][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615: "Приложение не может скачать файл в *uri,* так как он вызывался программным образом за пределами локального контекста". | Возникает, когда содержимое в веб-контексте пытается программным образом скачать файл.  |  
| APPHOST9616: "Этот URI не может использовать API геолокации.  API geolocation можно вызывать только из URI, который входит в пакет или входит в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, что разрешено в веб-контексте, см. в странице [Features and restrictions by context.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9617: "Этот URI не может использовать API буфера обмена.  API буфера обмена можно вызывать только из URI, который входит в пакет или входит в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, что разрешено в веб-контексте, см. в странице [Features and restrictions by context.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9618: "Этот URI не может использовать window.close.  Метод window.close можно вызвать только из упакованного контента, загруженного с помощью схемы URI ms-appx". | Дополнительные сведения о том, что разрешено в веб-контексте, см. в странице [Features and restrictions by context.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9619: "Приложение не может перейти к *uri,* так как страница в веб-контексте не может быть документом верхнего уровня приложения.  Загрузи страницу в iframe вместо этого." | Вы не можете переходить на страницу верхнего уровня на удаленную веб-страницу, но приложение может отображать веб-страницу в [iframe][MDNIframe].  Дополнительные сведения о отображение удаленного веб-контента см. в странице [How to link to external web pages.][PreviousVersionsWindowsAppsHh780594]  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9620: "Это приложение было закрыто из-за использования подключения HTTP и мета элемента ms-https-connections-only.  Только подключения HTTPS разрешены при использовании мета элемента ms-https-connections-only.  Используйте подключение HTTPS или, если вам не требуется безопасное подключение, удалите элемент мета". | Дополнительные сведения см. [в странице Как требовать подключения HTTPS.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9623: "Приложение не могло разрешить *URL-адрес* из-за этой ошибки: *errorCode."* | Распространенной причиной этой ошибки является отсутствующий файл.  |  
| APPHOST9624: "Приложение не может использовать скрипт ** для загрузки URL-адреса, так как URL-адрес запускает другое приложение.  Только прямое взаимодействие с пользователем может запустить другое приложение". | Приложения не могут запускать другие приложения напрямую.  Другие приложения могут быть запущены пользователем при реализации определенных контрактов.  Дополнительные сведения: [Контракты приложений и расширения][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Была обнаружена прямая ссылка на файл `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` ресурсов.  Эта ссылка вызывает сбои при работе за пределами среды отладки". | Из-за пути файла этот PNG-файл рассматривается как локализованный ресурс, что приводит к ошибке в том, что локализованные ресурсы не могут `logo.scale-140.png` ссылаться напрямую.  Если вы собираетесь использовать этот файл в качестве языкового ресурса, см. в приложении Globalizing your app [(HTML).][PreviousVersionsWindowsAppsHh465006]  В противном случае попробуйте переименовать проблемный каталог.  |  

## <a name="see-also"></a>См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование времени запуска Windows в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс Geolocator | Документы Майкрософт"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "метод addPublicLocalApplicationUri | Документы Майкрософт"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Как требовать подключения HTTPS (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Контракты и расширения приложений (приложения для windows runtime) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Глобализация приложения (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Функции и ограничения по контексту (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Функции и различия HTML, CSS и JavaScript (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Связь с внешними веб-страницами (HTML) | Документы Майкрософт"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
