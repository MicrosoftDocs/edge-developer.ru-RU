---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Узнайте, как упаковать расширение.
title: Расширения — упаковка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ea4d6a4450d47d116164fd8481fdfb0f79bd30b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235720"
---
# Упаковка расширений Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Итак, вы завершили расширение и готовы упаковть его. Вам может быть интересно узнать, какие дальнейшие действия необходимо предпринять для получения этих данных от потенциальных пользователей. Это руководство призвано научить вас делать именно это.

Руководство по упаковке расширений является исчерпывающим, так как оно охватывает все, что вам нужно знать о упаковке, даже более подробные, nitty gritty сведения. Если вы не хотите узнать все, что нужно знать о упаковке расширения, вы не готовы к этому. Мы добавили поддержку расширений в ManifoldJS, средство с открытым кодом Node.js, которое отнимает большую часть ваших пакетов.

> [!NOTE]
> Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью. [Получите к нам](https://aka.ms/extension-request) свои запросы, чтобы стать частью Microsoft Store, и мы будем учесть, что вы будете обновляться в будущем.


Используйте описанную ниже схему процесса, чтобы сооставить свою упаковку adventure!


## [Расширения в Центре разработки для Windows](./packaging/extensions-in-the-windows-dev-center.md)

Независимо от того, какой маршрут создания пакета вы выберете ( вручную или ManifoldJS), первым шагом является регистрация учетной записи разработчика Windows и регистрация имен расширений.

После этого можно перейти к созданию [](./packaging/creating-and-testing-extension-packages.md) и тестированию пакетов расширений, чтобы узнать, как создаются AppX и вручную упаковываются расширения, или перейти к более простому маршруту и перейти к использованию [ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)для упаковки расширений.

> [!NOTE]
> После того как вы обратитесь к нам и утвердите свое расширение в Microsoft Store, ознакомьтесь с контрольным списком отправки [приложения.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)


## [Создание и тестирование пакетов расширений](./packaging/creating-and-testing-extension-packages.md)

В этом разделе руководства поется о создании пакета расширения вручную после того, как вы настроите учетную запись разработчика Windows и зарезервировали свои имена [расширений.](./packaging/extensions-in-the-windows-Dev-Center.md) Если вам интересно узнать более подробные сведения о упаковке расширения, ознакомьтесь с этим документом.

Также включены сведения о том, как протестировать и [распаковать упакованное расширение.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Эта информация актуальна, даже если вы прошли маршрут упаковки ManifoldJS.

## [Локализация пакетов расширений](./packaging/localizing-extension-packages.md)
Этап локализации пакета приходится между созданием appxmanifest.xml файла и последней командой для упаковки расширения.
Это позволяет указать языки, поддерживаемые вашими расширениями в списке Microsoft Store, и язык, на котором имя расширения отображается в Windows.

Вы можете перейти к [локализации](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) имени и описания Microsoft Store в этом разделе руководства, если расширение не поддерживает несколько языков.

## [Использование ManifoldJS для расширений пакетов](./packaging/using-ManifoldJS-to-package-extensions.md)

Маршрут средства для упаковки расширения, ManifoldJS будет упаковывать расширение в оснастку с минимальными усилиями на конце. Предодайте несколько ресурсов Windows или Microsoft Store после заполнения некоторых свойств AppXManifest, и расширение будет упаковано в течение некоторого времени.

После упаковки расширения см. [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) раздел тестирования создания и тестирования расширения Microsoft Edge, чтобы узнать, как его выгрузить или распаковать.


## [Запуск комплекта сертификации приложений для Windows](./packaging/running-the-windows-app-certification-kit.md)

После того как у вас есть упакованное расширение, вы можете запустить его с помощью комплекта сертификации приложений для Windows. Это позволит выполнить ряд тестов пакета расширения, чтобы убедиться, что он готов к microsoft Store.
