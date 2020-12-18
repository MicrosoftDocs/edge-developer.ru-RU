---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Узнайте о корпоративных аспектах расширений Microsoft Edge и посмотрите, как они похожи на приложения UWP.
title: Расширения для предприятий
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7c23bc24e20b7b00b8779f209dcac8c795067fd5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235819"
---
# <span data-ttu-id="e8a88-104">Расширения для предприятий</span><span class="sxs-lookup"><span data-stu-id="e8a88-104">Extensions for Enterprise</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="e8a88-105">Расширения Microsoft Edge имеют аналогичный рабочий процесс по сравнению с другими корпоративными приложениями UWP.</span><span class="sxs-lookup"><span data-stu-id="e8a88-105">Microsoft Edge extensions have a similar workflow when compared to other enterprise UWP apps.</span></span> <span data-ttu-id="e8a88-106">Ниже приведены сведения о корпоративных аспектах расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8a88-106">The information below details enterprise specific aspects of Microsoft Edge extensions.</span></span>

## <span data-ttu-id="e8a88-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e8a88-107">Prerequisites</span></span>
<span data-ttu-id="e8a88-108">Ниже предложено разработать, упаковить и развернуть расширение Microsoft Edge для предприятий.</span><span class="sxs-lookup"><span data-stu-id="e8a88-108">The following items are suggested to develop, package, and deploy a Microsoft Edge extension for enterprise:</span></span>

+ <span data-ttu-id="e8a88-109">Учетная запись портала разработчика Windows для подписания и выпуска расширения в корпоративном частном магазине.</span><span class="sxs-lookup"><span data-stu-id="e8a88-109">Windows Developer Portal account, to sign and release the extension to the enterprise private store.</span></span> <span data-ttu-id="e8a88-110">Дополнительные [сведения см. в открываемой учетной](/windows/uwp/publish/opening-a-developer-account) записи разработчика.</span><span class="sxs-lookup"><span data-stu-id="e8a88-110">See [Opening a developer account](/windows/uwp/publish/opening-a-developer-account) for more details.</span></span>
+ <span data-ttu-id="e8a88-111">Microsoft Store для бизнеса или образования для распространения приложения на предприятии.</span><span class="sxs-lookup"><span data-stu-id="e8a88-111">Microsoft Store for Business or Education, to distribute the application to the enterprise.</span></span> <span data-ttu-id="e8a88-112">Дополнительные [сведения см.](/microsoft-store/) в документации Microsoft Store для бизнеса и образования.</span><span class="sxs-lookup"><span data-stu-id="e8a88-112">See the [Microsoft Store for Business and Education documentation](/microsoft-store/) for more details.</span></span>
+ <span data-ttu-id="e8a88-113">Определите, в каких версиях Windows 10 будет работать расширение Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8a88-113">Identify which versions of Windows 10 will be running the Microsoft Edge extension.</span></span> <span data-ttu-id="e8a88-114">Список существующих выпусков [Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) см. в сведениях о выпуске Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e8a88-114">See [Windows 10 release information](https://www.microsoft.com/itpro/windows-10/release-information) for a listing of existing Windows 10 releases.</span></span>

> [!NOTE]
> <span data-ttu-id="e8a88-115">Загрузку неосвояемого приложения можно считать альтернативой использованию портала разработчика Windows для подписи выпуска расширения.</span><span class="sxs-lookup"><span data-stu-id="e8a88-115">Sideloading can be considered an alternative to using the Windows Developer Portal to sign the release the extension.</span></span> <span data-ttu-id="e8a88-116">Дополнительные сведения см. ниже в действиях по загрузке неогрузки расширений.</span><span class="sxs-lookup"><span data-stu-id="e8a88-116">See the behaviour of sideloading extensions below for more details.</span></span>

## <span data-ttu-id="e8a88-117">Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="e8a88-117">Windows Information Protection</span></span>
<span data-ttu-id="e8a88-118">В настоящее время расширения Microsoft Edge не работают с настройками Windows Information Protection (WIP).</span><span class="sxs-lookup"><span data-stu-id="e8a88-118">Microsoft Edge extensions currently don't honor Windows Information Protection (WIP) settings.</span></span> <span data-ttu-id="e8a88-119">Если предприятие беспокоится о защите данных, поддержку расширений не следует включить для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8a88-119">If an enterprise is concerned about data protection, extensions support should not be enabled for Microsoft Edge.</span></span>

<span data-ttu-id="e8a88-120">Чтобы отключить расширения для сотрудников, настройте групповую политику и параметры Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="e8a88-120">To disable extensions for employees, configure Group Policy and Microsoft Intune settings.</span></span> <span data-ttu-id="e8a88-121">Дополнительные сведения о политиках, которые необходимо настроить, см. в доступных [политиках для Microsoft Edge.](https://technet.microsoft.com/itpro/microsoft-edge/available-policies)</span><span class="sxs-lookup"><span data-stu-id="e8a88-121">For more info on which policies to configure, see [Available policies for Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).</span></span>

## <span data-ttu-id="e8a88-122">Расширения упаковки</span><span class="sxs-lookup"><span data-stu-id="e8a88-122">Packaging Extensions</span></span>
<span data-ttu-id="e8a88-123">Прежде чем предприятие сможет распространять расширение среди своих сотрудников, его необходимо упаковать.</span><span class="sxs-lookup"><span data-stu-id="e8a88-123">Before an enterprise can distribute an extension to its employees, it must first be packaged.</span></span> <span data-ttu-id="e8a88-124">Инструкции по расширению упаковки доступны в руководстве [по упаковке.](./guides/packaging.md)</span><span class="sxs-lookup"><span data-stu-id="e8a88-124">Instructions on packaging extensions are available in the [Packaging](./guides/packaging.md) guide.</span></span>

> [!TIP]
> <span data-ttu-id="e8a88-125">Обязательно протестировать установку и запуск расширения во всех версиях Windows 10, чтобы убедиться, что оно будет работать ожидаемым образом перед распространением.</span><span class="sxs-lookup"><span data-stu-id="e8a88-125">Be sure to test installing and running your extension on all the versions of Windows 10 to ensure it will work as expected before distributing.</span></span>

## <span data-ttu-id="e8a88-126">Распространение расширений</span><span class="sxs-lookup"><span data-stu-id="e8a88-126">Distributing Extensions</span></span>
<span data-ttu-id="e8a88-127">После упаковки расширения оно может быть распространено среди сотрудников через Microsoft Store, Microsoft Store для бизнеса или путем загрузки нео sideloading.</span><span class="sxs-lookup"><span data-stu-id="e8a88-127">Once an extension has been packaged, it can be distributed to employees through the Microsoft Store, Microsoft Store for Business, or by sideloading.</span></span>

<span data-ttu-id="e8a88-128">Расширения, распространяемых несмотря на то, что Microsoft Store для бизнеса может быть назначен сотрудникам или добавлен в частный магазин, где все сотрудники могут получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="e8a88-128">Extensions distributed though the Microsoft Store for Business can either be assigned to employees, or added to a private store where all employees can access them.</span></span> <span data-ttu-id="e8a88-129">Это можно сделать, следуя руководству по распространению [бизнес-приложений для](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) предприятий.</span><span class="sxs-lookup"><span data-stu-id="e8a88-129">This can be done by following the [Distribute "Line-of-Business" (LOB) apps to enterprises](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) guide.</span></span>

<span data-ttu-id="e8a88-130">Для загрузки неоконченных расширений устройства (неугодные или управляемые) должны быть разблокированы для загрузки неоконченных расширений.</span><span class="sxs-lookup"><span data-stu-id="e8a88-130">To sideload extensions, devices (unmanaged or managed) must be unlocked for sideloading.</span></span> <span data-ttu-id="e8a88-131">Дополнительные сведения о загрузке неоконтружаных расширений см. в дополнительных сведениях о загрузке неоконтружаных приложений в [Windows 10.](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10)</span><span class="sxs-lookup"><span data-stu-id="e8a88-131">See [Sideload LOB apps in Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) for more info on how to sideload packaged extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8a88-132">Если предприятие разрабатывает и распространяет расширение внутри организации, предприятию потребуется учетная запись Microsoft Store для бизнеса (или для образовательных проектов) и учетная запись портала разработчика Windows.</span><span class="sxs-lookup"><span data-stu-id="e8a88-132">If the enterprise is both developing and distributing the extension internally, the enterprise will require both the Microsoft Store for Business (or Education) and a Windows Developer Portal account.</span></span>

### <span data-ttu-id="e8a88-133">Поведение неогруженных расширений</span><span class="sxs-lookup"><span data-stu-id="e8a88-133">Behavior of Sideloaded Extensions</span></span>
<span data-ttu-id="e8a88-134">В отличие от расширений, распространяемых через Microsoft Store (или Microsoft Store для бизнеса), неогруженные расширения обрабатываются в Microsoft Edge по-разному.</span><span class="sxs-lookup"><span data-stu-id="e8a88-134">Unlike extensions distributed through the Microsoft Store (or the Microsoft Store for Business), sideloaded extensions are treated differently in Microsoft Edge.</span></span>

<span data-ttu-id="e8a88-135">Первое различие влияет на поведение неогруженных расширений после установки.</span><span class="sxs-lookup"><span data-stu-id="e8a88-135">The first difference affects how sideloaded extensions behave after installation.</span></span> <span data-ttu-id="e8a88-136">В отличие от расширений из Microsoft Store, неогруженные расширения не сразу отображают уведомление "У вас есть новое расширение" и должны быть вручную включены пользователем.</span><span class="sxs-lookup"><span data-stu-id="e8a88-136">Unlike extensions from the Microsoft Store, sideloaded extensions do not immediately display the "You have a new extension" notification and need to be manually turned on by the user.</span></span>

<span data-ttu-id="e8a88-137">Чтобы включить расширение, откройте меню "Еще" **(...)** и выберите **"Расширения",** и в списке установленных расширений должно отображено неогруженное расширение.</span><span class="sxs-lookup"><span data-stu-id="e8a88-137">To turn on the extension, open the **More (...)** menu, select **"Extensions"** and you should see the sideloaded extension in the list of installed extensions.</span></span> <span data-ttu-id="e8a88-138">Щелкните расширение и включайте его.</span><span class="sxs-lookup"><span data-stu-id="e8a88-138">Click on the extension and turn it on.</span></span>

<span data-ttu-id="e8a88-139">Второе различие влияет на то, как неогруженные расширения отображаются в браузере.</span><span class="sxs-lookup"><span data-stu-id="e8a88-139">The second difference affects how sideloaded extensions appear in the browser.</span></span> <span data-ttu-id="e8a88-140">Например, уведомление "У вас новое расширение" и список установленных расширений содержат дополнительное предупреждение о том, что расширение находится из неизвестного источника.</span><span class="sxs-lookup"><span data-stu-id="e8a88-140">For example, both the "You have a new extension" notification and the list of installed extensions include an additional warning stating that the extension is from an unknown source.</span></span>

![предупреждение о загрузке неогрузки 1](./media/sideload-permissionflyout.PNG)

![предупреждение о загрузке неогрузки 2](./media/sideload-l1warning.PNG)

<span data-ttu-id="e8a88-143">Третье и последнее различие влияет на поведение неогруженных расширений при запуске браузера.</span><span class="sxs-lookup"><span data-stu-id="e8a88-143">The third and final difference affects how sideloaded extensions behave on browser startup.</span></span> <span data-ttu-id="e8a88-144">Неогруженные расширения на устройствах, которые либо присоединились к домену, либо с включенной поддержкой MDM, будут вести себя как расширения из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e8a88-144">Sideloaded extensions on devices that are either domain-joined or MDM enabled will behave like extensions from the Microsoft Store.</span></span> <span data-ttu-id="e8a88-145">Однако неогруженные расширения на устройствах, которые не присоединились к домену или не включены в MDM, будут отключены во время запуска браузера и требовать от пользователя явного действия.</span><span class="sxs-lookup"><span data-stu-id="e8a88-145">However, sideloaded extensions on devices that are not domain-joined or MDM enabled will be turned off during browser startup and require the user to take explicit action.</span></span>

<span data-ttu-id="e8a88-146">Вскоре после запуска браузера (через около 10 секунд бездействия) в нижней части окна появится следующее уведомление.</span><span class="sxs-lookup"><span data-stu-id="e8a88-146">Shortly after browser startup (after ~10 seconds of inactivity) the following notification will appear near the bottom of the window.</span></span>

![уведомление о загрузке неогрузки](./media/sideload-scareUI.PNG)

<span data-ttu-id="e8a88-148">При каждом запуске Microsoft Edge пользователям потребуется выбрать "Включить", чтобы использовать расширение.</span><span class="sxs-lookup"><span data-stu-id="e8a88-148">Each time Microsoft Edge is launched, users will need to select "Turn on anyway" in order to use the extension.</span></span>
