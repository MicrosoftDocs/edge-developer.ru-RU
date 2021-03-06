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
# <a name="packaging-microsoft-edge-extensions"></a><span data-ttu-id="d5c95-104">Упаковка расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d5c95-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="d5c95-105">Таким образом, вы, наконец, завершили расширение и готовы упаковть его.</span><span class="sxs-lookup"><span data-stu-id="d5c95-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="d5c95-106">Возможно, вам будет интересно, какие дальнейшие шаги необходимо предпринять для получения этого в руки потенциальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d5c95-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="d5c95-107">Это руководство предназначено для обучения тому, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="d5c95-107">This guide is intended to teach you how to do just that.</span></span>  

<span data-ttu-id="d5c95-108">Руководство по упаковке расширения является всеобъемлющим в том, что оно охватывает все, что вы хотите знать о упаковке, даже более тонкие, nitty песчаные детали.</span><span class="sxs-lookup"><span data-stu-id="d5c95-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="d5c95-109">Если вы не хотите узнать все, что нужно знать о упаковке расширения, вам повезло.</span><span class="sxs-lookup"><span data-stu-id="d5c95-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="d5c95-110">Мы добавили поддержку расширений в ManifoldJS, средство Node.js с открытым исходным кодом, которое отнимает большую часть проблемы упаковки.</span><span class="sxs-lookup"><span data-stu-id="d5c95-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5c95-111">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="d5c95-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="d5c95-112">[Связаться с нами](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) с вашими запросами на участие в Microsoft Store, и мы рассмотрим вас для будущего обновления.</span><span class="sxs-lookup"><span data-stu-id="d5c95-112">[Reach out to us](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>  

<span data-ttu-id="d5c95-113">Используйте схему процесса ниже, чтобы наметить ваше приключение упаковки!</span><span class="sxs-lookup"><span data-stu-id="d5c95-113">Use the process outline below to map out your packaging adventure!</span></span>  

## [<a name="extensions-in-the-windows-dev-center"></a><span data-ttu-id="d5c95-114">Расширения в Центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="d5c95-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)  

<span data-ttu-id="d5c95-115">Независимо от того, какой маршрут создания пакета вы выбираете вручную или manifoldJS, первым шагом является регистрация учетной записи разработчика Windows и регистрация имени(ы) вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="d5c95-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>  

<span data-ttu-id="d5c95-116">После этого можно перейти к созданию [](./packaging/creating-and-testing-extension-packages.md) и тестированию пакетов расширений, чтобы узнать, как создаются и вручную упаковываются приложения, или перейти к более простому маршруту и перейти к использованию [пакетных](./packaging/using-ManifoldJS-to-package-extensions.md)расширений.</span><span class="sxs-lookup"><span data-stu-id="d5c95-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="d5c95-117">После того как вы обратитесь к нам и получили одобрение на расширение в Microsoft Store, ознакомьтесь с контрольным списком отправки [приложений.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)</span><span class="sxs-lookup"><span data-stu-id="d5c95-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>  


## [<a name="creating-and-testing-extension-packages"></a><span data-ttu-id="d5c95-118">Создание и тестирование пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="d5c95-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)  

<span data-ttu-id="d5c95-119">Этот раздел руководства проходит через ручное создание пакета расширения после того, как вы настроите учетную запись разработчика Windows и зарезервировали свое имя [расширения (s).](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="d5c95-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="d5c95-120">Если вам интересны более подробные сведения о упаковке расширения, ознакомьтесь с этим.</span><span class="sxs-lookup"><span data-stu-id="d5c95-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>  

<span data-ttu-id="d5c95-121">Также включена информация о том, как протестировать и [распаковать упакованное расширение.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="d5c95-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="d5c95-122">Эта информация актуальна, даже если вы прошли маршрут упаковки ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="d5c95-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>  

## [<a name="localizing-extension-packages"></a><span data-ttu-id="d5c95-123">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="d5c95-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)  

<span data-ttu-id="d5c95-124">Этап локализации пакета включает создание appxmanifest.xml файла и запуск последней команды для упаковки расширения.</span><span class="sxs-lookup"><span data-stu-id="d5c95-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>  
<span data-ttu-id="d5c95-125">Это позволяет указать языки, поддерживаемые вашими расширениями в списке Microsoft Store, и язык, на котором имя вашего расширения отображается в Windows.</span><span class="sxs-lookup"><span data-stu-id="d5c95-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>  

<span data-ttu-id="d5c95-126">В этом разделе руководства можно перейти к локализации имени и описания microsoft [Store,](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) если расширение не поддерживает несколько языков.</span><span class="sxs-lookup"><span data-stu-id="d5c95-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>  

## [<a name="using-manifoldjs-to-package-extensions"></a><span data-ttu-id="d5c95-127">Использование ManifoldJS для расширений пакетов</span><span class="sxs-lookup"><span data-stu-id="d5c95-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)  

<span data-ttu-id="d5c95-128">Маршрут инструмента для упаковки расширения, ManifoldJS будет упаковывать расширение в оснастке с минимальными усилиями на конце.</span><span class="sxs-lookup"><span data-stu-id="d5c95-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="d5c95-129">Предостерегайте несколько активов Windows/Microsoft Store после заполнения некоторых свойств AppXManifest, и расширение будет упаковано в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="d5c95-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>  

<span data-ttu-id="d5c95-130">После упаковки расширения см. [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) в разделе Тестирование в разделе Создание и тестирование расширения Microsoft Edge, чтобы узнать, как его разгрузить или распаковать.</span><span class="sxs-lookup"><span data-stu-id="d5c95-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>  

## [<a name="running-the-windows-app-certification-kit"></a><span data-ttu-id="d5c95-131">Запуск комплекта сертификации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="d5c95-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)  

<span data-ttu-id="d5c95-132">После того как у вас есть пакетное расширение, вы можете запустить его через комплект сертификации приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="d5c95-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="d5c95-133">При этом в пакете расширения будет выполниться ряд тестов, чтобы убедиться, что он готов для Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d5c95-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>  
