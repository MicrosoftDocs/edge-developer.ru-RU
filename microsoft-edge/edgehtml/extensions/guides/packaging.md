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
# <span data-ttu-id="a5ef6-104">Упаковка расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5ef6-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="a5ef6-105">Итак, вы завершили расширение и готовы упаковть его.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="a5ef6-106">Вам может быть интересно узнать, какие дальнейшие действия необходимо предпринять для получения этих данных от потенциальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="a5ef6-107">Это руководство призвано научить вас делать именно это.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="a5ef6-108">Руководство по упаковке расширений является исчерпывающим, так как оно охватывает все, что вам нужно знать о упаковке, даже более подробные, nitty gritty сведения.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="a5ef6-109">Если вы не хотите узнать все, что нужно знать о упаковке расширения, вы не готовы к этому.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="a5ef6-110">Мы добавили поддержку расширений в ManifoldJS, средство с открытым кодом Node.js, которое отнимает большую часть ваших пакетов.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="a5ef6-111">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="a5ef6-112">[Получите к нам](https://aka.ms/extension-request) свои запросы, чтобы стать частью Microsoft Store, и мы будем учесть, что вы будете обновляться в будущем.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="a5ef6-113">Используйте описанную ниже схему процесса, чтобы сооставить свою упаковку adventure!</span><span class="sxs-lookup"><span data-stu-id="a5ef6-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="a5ef6-114">Расширения в Центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="a5ef6-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="a5ef6-115">Независимо от того, какой маршрут создания пакета вы выберете ( вручную или ManifoldJS), первым шагом является регистрация учетной записи разработчика Windows и регистрация имен расширений.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="a5ef6-116">После этого можно перейти к созданию [](./packaging/creating-and-testing-extension-packages.md) и тестированию пакетов расширений, чтобы узнать, как создаются AppX и вручную упаковываются расширения, или перейти к более простому маршруту и перейти к использованию [ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)для упаковки расширений.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a5ef6-117">После того как вы обратитесь к нам и утвердите свое расширение в Microsoft Store, ознакомьтесь с контрольным списком отправки [приложения.](https://docs.microsoft.com/windows/uwp/publish/app-submissions)</span><span class="sxs-lookup"><span data-stu-id="a5ef6-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="a5ef6-118">Создание и тестирование пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="a5ef6-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="a5ef6-119">В этом разделе руководства поется о создании пакета расширения вручную после того, как вы настроите учетную запись разработчика Windows и зарезервировали свои имена [расширений.](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="a5ef6-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="a5ef6-120">Если вам интересно узнать более подробные сведения о упаковке расширения, ознакомьтесь с этим документом.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="a5ef6-121">Также включены сведения о том, как протестировать и [распаковать упакованное расширение.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="a5ef6-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="a5ef6-122">Эта информация актуальна, даже если вы прошли маршрут упаковки ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="a5ef6-123">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="a5ef6-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="a5ef6-124">Этап локализации пакета приходится между созданием appxmanifest.xml файла и последней командой для упаковки расширения.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="a5ef6-125">Это позволяет указать языки, поддерживаемые вашими расширениями в списке Microsoft Store, и язык, на котором имя расширения отображается в Windows.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="a5ef6-126">Вы можете перейти к [локализации](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) имени и описания Microsoft Store в этом разделе руководства, если расширение не поддерживает несколько языков.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="a5ef6-127">Использование ManifoldJS для расширений пакетов</span><span class="sxs-lookup"><span data-stu-id="a5ef6-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="a5ef6-128">Маршрут средства для упаковки расширения, ManifoldJS будет упаковывать расширение в оснастку с минимальными усилиями на конце.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="a5ef6-129">Предодайте несколько ресурсов Windows или Microsoft Store после заполнения некоторых свойств AppXManifest, и расширение будет упаковано в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="a5ef6-130">После упаковки расширения см. [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) раздел тестирования создания и тестирования расширения Microsoft Edge, чтобы узнать, как его выгрузить или распаковать.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="a5ef6-131">Запуск комплекта сертификации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="a5ef6-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="a5ef6-132">После того как у вас есть упакованное расширение, вы можете запустить его с помощью комплекта сертификации приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="a5ef6-133">Это позволит выполнить ряд тестов пакета расширения, чтобы убедиться, что он готов к microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a5ef6-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
