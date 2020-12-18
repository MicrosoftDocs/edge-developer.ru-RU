---
description: С помощью windows Runtime (WinRT) вызовите собственный API Windows из приложения JavaScript.
title: Windows Runtime (WinRT) для JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Windows Runtime, WinRT, PWA, JavaScript
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bd67f052d0a836c754f7b58d0625e09ae8781cd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235849"
---
# Windows Runtime (WinRT) для JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

The [Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \(or simply WinRT\) is the collection of native API that power the [Universal Windows Platform](/windows/uwp/get-started/universal-application-platform-guide) \(UWP\) apps that run across all Windows [10 device families](/uwp/extension-sdks/device-families-overview).  API WinRT проецируемы на несколько разных языков, включая C#, C++, Visual Basic и JavaScript.  

Как веб-разработчик вы можете запросить эти API Windows из JavaScript, когда ваше веб-приложение работает как установленное приложение [для Windows 10](../progressive-web-apps/windows-features.md#set-up-and-run-your-universal-windows-app) \(запущено в процессе, а не в `wwahost.exe` браузере\).  Кроме того, веб-сайт, работающий в качестве приложения для Windows 10, может также использовать веб-управление [Microsoft Edge](#webview) для отображения удаленного и локального веб-содержимого, а также API [MSApp](#msapp) для обработки BLOB-содержимого и потоков, помимо прочего.  

Вот области пространства имен WinRT верхнего уровня, доступные всем приложениям для Windows 10:  

| Пространство имен WinRT | Описание |  
|:--- |:--- |  
| [AI](/uwp/api/windows.AI.MachineLearning.Preview) \(Preview\) | Содержит классы, которые позволяют приложениям загружать модели машинного обучения, привязывать данные как входные данные и оценивать результаты.  |  
| [ApplicationModel](/uwp/api/windows.applicationmodel) | Предоставляет приложению доступ к основным функциям системы и сведениям о времени работы пакета приложения, а также обрабатывает операции приостановки.  |  
| [Данные](/uwp/api/windows.data.html) | Предоставляет полезные классы для работы с различными форматами данных, включая HTML, JSON, PDF, текст и XML.  |  
| [Устройства](/uwp/api/windows.devices) | Это пространство имен предоставляет доступ к низкоуровневые поставщики устройств, включая ADC, GPIO, I2 C, PWM и SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Включает основные функции времени работы Windows, включая управление асинхронными операциями и доступ к хранилищам свойств.  Это пространство имен также определяет общие типы значений, которые представляют единый идентификатор ресурса \(URI\), даты и время, двухмерные измерения и другие базовые значения.  |  
| [Игры](/uwp/api/windows.gaming.input) |Предоставляет доступ к данным игрового контроллера, панели игры, мониторингу игры и игровому чату.  |  
| [Globalization](/uwp/api/windows.globalization) | Обеспечивает поддержку глобализации для языковых профилей, географических регионов и международных календарей.  |  
| [Графика](/uwp/api/windows.graphics) | Предоставляет базовые типы данных, содержащие сведения о том, как рисовать графику.  Эти структуры данных обычно используются для определения размера поверхностей при использовании класса CompositionVirtualDrawingSurface.  |  
| [Management](/uwp/api/windows.management) | Предоставляет возможности принудительной синхронизации с устройства управления мобильными устройствами \(MDM\) с сервером.  Этот протокол синхронизации MDM основан на стандарте Управления устройствами Open Mobile Alliance.  |  
| [Media](/uwp/api/windows.media) | Предоставляет классы для создания и работы с мультимедиа, такие как фотографии, аудиозаписи и видео.  |  
| [Сеть](/uwp/api/windows.networking) | Предоставляет доступ к именам хостов и конечным точкам, используемым сетевыми приложениями.  |  
| [Восприятие](/uwp/api/windows.perception) | Содержит классы для восприятия окружения пользователя, позволяя приложениям находить устройство и причину относительно поверхностей и голограмм вокруг пользователя.  |  
| [Безопасность](/uwp/api/windows.security.authentication.identity) | Предоставляет классы для проверки подлинности пользователей, управления учетными данными, операций шифрования и функций защиты корпоративных данных.  |  
| [Службы](/uwp/api/windows.services.cortana) | Предоставляет доступ к службам Майкрософт для кортаны, карт, Microsoft Store и целевого контента \(subscription\).  |  
| [Хранилище](/uwp/api/windows.storage) | Предоставляет классы для управления файлами, папками и настройками приложений.  |  
| [Система](/uwp/api/windows.system) | Включает функции системы, такие как запуск приложений, получение сведений о пользователе и профилирование памяти.  |  
| [Пользовательский интерфейс](/uwp/api/windows.ui) | Предоставляет приложению доступ к основным системным функциям и сведениям о времени работы пользовательского интерфейса.  **ПРИМЕЧАНИЕ.** API в пространстве имен недоступны для приложений JavaScript \(которые могут использовать эквивалентные технологии на основе `Windows.UI.Xaml` веб-стандартов\).  |  
| [Интернет](/uwp/api/windows.web) | Предоставляет сведения об ошибках, которые могут быть результатом операций веб-службы.  |  

Дополнительные сведения об использовании можно узнать с помощью [windows Runtime в JavaScript.](./using-the-windows-runtime-in-javascript.md)  Чтобы узнать, как запустить веб-сайт в качестве приложения для Windows, попробуйте [учебник "Адаптировать PWA для Windows".](../progressive-web-apps/windows-features.md)  

## Веб-представление  

С [помощью управления WebView в Microsoft Edge](../hosting/webview/index.md) можно проводить веб-содержимое в приложении для Windows 10.  Это аналогично использованию, но предоставляет намного больше возможностей и контроля `<iframe>` над опытом. [](../hosting/webview/index.md#webview-versus-iframe)  

## MSApp  

Глобальный объект [MSApp](./reference/msapp.md) \( \) предоставляет различные дополнительные функции для приложений Windows 10 на основе JavaScript, например программы для преобразования между веб-стандартами и эквивалентными типами объектов `window.MSApp` WinRT.  
