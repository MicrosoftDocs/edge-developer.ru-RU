---
description: Узнайте, как можно упаковть расширение.
title: Расширения — упаковка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, web development, html, css, javascript, developer
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398499"
---
# <a name="packaging-microsoft-edge-extensions"></a>Упаковка расширений Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Таким образом, вы, наконец, завершили расширение и готовы упаковть его. Возможно, вам будет интересно, какие дальнейшие шаги необходимо предпринять для получения этого в руки потенциальных пользователей. Это руководство предназначено для обучения тому, как это сделать.  

Руководство по упаковке расширения является всеобъемлющим в том, что оно охватывает все, что вы хотите знать о упаковке, даже более тонкие, nitty песчаные детали. Если вы не хотите узнать все, что нужно знать о упаковке расширения, вам повезло. Мы добавили поддержку расширений в ManifoldJS, средство Node.js с открытым исходным кодом, которое отнимает большую часть проблемы упаковки.  

> [!NOTE]
> Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью. [Связаться с нами](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) с вашими запросами на участие в Microsoft Store, и мы рассмотрим вас для будущего обновления.  

Используйте схему процесса ниже, чтобы наметить ваше приключение упаковки!  

## [<a name="extensions-in-the-windows-dev-center"></a>Расширения в Центре разработки для Windows](./packaging/extensions-in-the-windows-dev-center.md)  

Независимо от того, какой маршрут создания пакета вы выбираете вручную или manifoldJS, первым шагом является регистрация учетной записи разработчика Windows и регистрация имени(ы) вашего расширения.  

После этого можно перейти к созданию [](./packaging/creating-and-testing-extension-packages.md) и тестированию пакетов расширений, чтобы узнать, как создаются и вручную упаковываются приложения, или перейти к более простому маршруту и перейти к использованию [пакетных](./packaging/using-ManifoldJS-to-package-extensions.md)расширений.  

> [!NOTE]
> После того как вы обратитесь к нам и получили одобрение на расширение в Microsoft Store, ознакомьтесь с контрольным списком отправки [приложений.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)  


## [<a name="creating-and-testing-extension-packages"></a>Создание и тестирование пакетов расширений](./packaging/creating-and-testing-extension-packages.md)  

Этот раздел руководства проходит через ручное создание пакета расширения после того, как вы настроите учетную запись разработчика Windows и зарезервировали свое имя [расширения (s).](./packaging/extensions-in-the-windows-Dev-Center.md) Если вам интересны более подробные сведения о упаковке расширения, ознакомьтесь с этим.  

Также включена информация о том, как протестировать и [распаковать упакованное расширение.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Эта информация актуальна, даже если вы прошли маршрут упаковки ManifoldJS.  

## [<a name="localizing-extension-packages"></a>Локализация пакетов расширений](./packaging/localizing-extension-packages.md)  

Этап локализации пакета включает создание appxmanifest.xml файла и запуск последней команды для упаковки расширения.  
Это позволяет указать языки, поддерживаемые вашими расширениями в списке Microsoft Store, и язык, на котором имя вашего расширения отображается в Windows.  

В этом разделе руководства можно перейти к локализации имени и описания microsoft [Store,](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) если расширение не поддерживает несколько языков.  

## [<a name="using-manifoldjs-to-package-extensions"></a>Использование ManifoldJS для расширений пакетов](./packaging/using-ManifoldJS-to-package-extensions.md)  

Маршрут инструмента для упаковки расширения, ManifoldJS будет упаковывать расширение в оснастке с минимальными усилиями на конце. Предостерегайте несколько активов Windows/Microsoft Store после заполнения некоторых свойств AppXManifest, и расширение будет упаковано в ближайшее время.  

После упаковки расширения см. [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) в разделе Тестирование в разделе Создание и тестирование расширения Microsoft Edge, чтобы узнать, как его разгрузить или распаковать.  

## [<a name="running-the-windows-app-certification-kit"></a>Запуск комплекта сертификации приложений для Windows](./packaging/running-the-windows-app-certification-kit.md)  

После того как у вас есть пакетное расширение, вы можете запустить его через комплект сертификации приложений Windows. При этом в пакете расширения будет выполниться ряд тестов, чтобы убедиться, что он готов для Microsoft Store.  
