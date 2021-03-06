---
description: Удаленное отладка живого контента на устройстве Android с компьютера Windows или macOS.
title: Начало работы с устройствами удаленной отладки Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 61fad793ca03dbef68a5f769dbfd25e780fd9930
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398261"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="get-started-with-remote-debugging-android-devices"></a><span data-ttu-id="26626-104">Начало работы с устройствами удаленной отладки Android</span><span class="sxs-lookup"><span data-stu-id="26626-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="26626-105">Удаленное отладка живого контента на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="26626-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="26626-106">На следующей странице руководства рассказывается о том, как выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="26626-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="26626-107">Настройка устройства Android для удаленной отладки и обнаружение его на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="26626-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="26626-108">Проверка и отлаживка живого контента на устройстве Android на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="26626-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="26626-109">Содержимое screencast с устройства Android на экземпляр DevTools на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="26626-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="26626-110">Удаленная отладка приложения Microsoft Edge на устройствах iOS в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26626-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="26626-111">В следующем руководстве основное внимание уделяется удаленной отладке Microsoft Edge на устройствах с Android.</span><span class="sxs-lookup"><span data-stu-id="26626-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="26626-112">Если у вас есть macOS-устройство, выполните руководство по отладке [Brightcove,][BrightcoveSupportDebuggingMobileDevices] чтобы удаленно отладить Microsoft Edge на устройстве iOS с помощью Safari.</span><span class="sxs-lookup"><span data-stu-id="26626-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="26626-113">Дополнительные сведения о средстве веб-инспектора в Safari перейдите к [средствам веб-разработки Safari.][AppleDeveloperSafariTools]</span><span class="sxs-lookup"><span data-stu-id="26626-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <a name="step-1-discover-your-android-device"></a><span data-ttu-id="26626-114">Шаг 1. Откройте для себя устройство Android</span><span class="sxs-lookup"><span data-stu-id="26626-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="26626-115">Рабочий процесс ниже работает для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="26626-115">The workflow below works for most users.</span></span>  <span data-ttu-id="26626-116">Дополнительные справки можно найти в [разделе Устранение неполадок. В разделе DevTools](#troubleshooting-devtools-is-not-detecting-the-android-device) не обнаружен раздел устройства Android.</span><span class="sxs-lookup"><span data-stu-id="26626-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="26626-117">Откройте экран **Параметры разработчика** на Android.</span><span class="sxs-lookup"><span data-stu-id="26626-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="26626-118">Дополнительные сведения можно получить в меню Настройка параметров разработчика на [устройстве.][AndroidDeveloperStudioDevOptions]</span><span class="sxs-lookup"><span data-stu-id="26626-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="26626-119">Выберите **включить отладку USB.**</span><span class="sxs-lookup"><span data-stu-id="26626-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="26626-120">На компьютере разработки откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="26626-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="26626-121">Перейдите на `edge://inspect` страницу в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="26626-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Страница edge://inspect Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="26626-123">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="26626-123">Figure 1.</span></span>  <span data-ttu-id="26626-124">Страница `edge://inspect` в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="26626-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="26626-125">Подключите устройство Android непосредственно к компьютеру разработки с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="26626-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="26626-126">При первой попытке подключения следует отобразить подсказку о том, как DevTools обнаруживает неизвестное устройство.</span><span class="sxs-lookup"><span data-stu-id="26626-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="26626-127">Примите предложение **разрешить отладку USB** на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="26626-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Запрос разрешения разрешить отладку USB на устройстве Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="26626-129">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="26626-129">Figure 2.</span></span>  <span data-ttu-id="26626-130">Запрос **разрешения разрешить отладку** USB на устройстве Android</span><span class="sxs-lookup"><span data-stu-id="26626-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="26626-131">Если отображается имя модели устройства Android, microsoft Edge успешно установила подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="26626-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="26626-132">Далее в [разделе Шаг 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)</span><span class="sxs-lookup"><span data-stu-id="26626-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a><span data-ttu-id="26626-133">Устранение неполадок: DevTools не обнаруживает устройство Android</span><span class="sxs-lookup"><span data-stu-id="26626-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="26626-134">Воспользуйтесь следующими советами, которые помогут устранить ошибки в правильных настройках оборудования.</span><span class="sxs-lookup"><span data-stu-id="26626-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="26626-135">Если вы используете концентратор USB, попробуйте подключить устройство Android непосредственно к компьютеру разработки.</span><span class="sxs-lookup"><span data-stu-id="26626-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="26626-136">Попробуйте отключить USB-кабель между устройством Android и машиной разработки, а затем повторно подключить USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="26626-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="26626-137">Выполните задачу, пока экраны android и машин разработки будут разблокированы.</span><span class="sxs-lookup"><span data-stu-id="26626-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="26626-138">Убедитесь, что usb-кабель работает.</span><span class="sxs-lookup"><span data-stu-id="26626-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="26626-139">Вы должны иметь возможность проверять файлы на устройстве Android на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="26626-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="26626-140">Чтобы убедиться, что программное обеспечение настроено правильно, используйте следующие советы.</span><span class="sxs-lookup"><span data-stu-id="26626-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="26626-141">Если на компьютере разработки работает Windows, попробуйте вручную установить драйверы USB для устройства Android.</span><span class="sxs-lookup"><span data-stu-id="26626-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="26626-142">Дополнительные сведения перейдите к [установке usb-драйверов OEM.][AndroidDeveloperToolsOemUsb]</span><span class="sxs-lookup"><span data-stu-id="26626-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="26626-143">Некоторые сочетания устройств Windows и Android \(особенно Samsung\) требуют дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="26626-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="26626-144">Дополнительные сведения можно получить в [DevTools Devices, не обнаруживающее][Stackoverflow21925992]устройство при подключении.</span><span class="sxs-lookup"><span data-stu-id="26626-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="26626-145">Используйте следующие советы, чтобы помочь устранить неполадки, если на устройстве **Android** не отображается подсказка разрешить отладку USB.</span><span class="sxs-lookup"><span data-stu-id="26626-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="26626-146">Отключение и повторное подключение USB-кабеля в то время как DevTools находится в центре внимания на вашем компьютере разработки и вашем домашнем экране Android показывает.</span><span class="sxs-lookup"><span data-stu-id="26626-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="26626-147">Запрос отображается, если экраны android или компьютера разработки заблокированы.</span><span class="sxs-lookup"><span data-stu-id="26626-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="26626-148">Обновление параметров отображения для устройства Android и машины разработки, чтобы каждый из них не заснул.</span><span class="sxs-lookup"><span data-stu-id="26626-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="26626-149">Настройка режима USB для Android для PTP.</span><span class="sxs-lookup"><span data-stu-id="26626-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="26626-150">Дополнительные сведения: перейдите в Galaxy S4 не показывает диалоговое окно [авторизации отладки USB.][StackexchangeAndroid101933]</span><span class="sxs-lookup"><span data-stu-id="26626-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="26626-151">Чтобы **сбросить** его в новое состояние, выберите отладку usb-отладки с экрана **"Параметры** разработчика" на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="26626-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="26626-152">Если решение, которое не упоминается на этой странице или в [Устройствах DevTools,][Stackoverflow21925992] не обнаруживает устройство при подключении к переполнению стека, добавьте решение к вопросу переполнения стека.</span><span class="sxs-lookup"><span data-stu-id="26626-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="26626-153">.</span><span class="sxs-lookup"><span data-stu-id="26626-153">.</span></span>  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a><span data-ttu-id="26626-154">Шаг 2. Отлаговка контента на устройстве Android с компьютера разработки</span><span class="sxs-lookup"><span data-stu-id="26626-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="26626-155">Откройте Microsoft Edge на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="26626-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="26626-156">Перейдите к , отображается имя модели устройства Android, а `edge://inspect` затем серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="26626-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="26626-157">Ниже следует отобразить версию Microsoft Edge, запущенную на устройстве, с номером версии в скобки.</span><span class="sxs-lookup"><span data-stu-id="26626-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="26626-158">Каждая открытая вкладка Microsoft Edge получает уникальный раздел.</span><span class="sxs-lookup"><span data-stu-id="26626-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="26626-159">Вы можете взаимодействовать с этой вкладке из раздела.</span><span class="sxs-lookup"><span data-stu-id="26626-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Подключенное удаленное устройство" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="26626-161">Рисунок 3.</span><span class="sxs-lookup"><span data-stu-id="26626-161">Figure 3.</span></span>  <span data-ttu-id="26626-162">Подключенное удаленное устройство</span><span class="sxs-lookup"><span data-stu-id="26626-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="26626-163">В **вкладке Открыть с текстовым полем URL-адреса** введите URL-адрес и выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="26626-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="26626-164">Страница открывается в новой вкладке на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="26626-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="26626-165">Выберите **проверку** рядом с только что открываемой URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="26626-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="26626-166">Открывается новый экземпляр DevTools.</span><span class="sxs-lookup"><span data-stu-id="26626-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a><span data-ttu-id="26626-167">Другие действия: фокус, обновление или закрытие вкладки</span><span class="sxs-lookup"><span data-stu-id="26626-167">More actions: focus, refresh, or close a tab</span></span>  

<span data-ttu-id="26626-168">Выберите **вкладку фокуса,** **перезагрузить**или закрыть рядом со вкладками, которые необходимо сосредоточиться, обновить или закрыть. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="26626-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, refresh, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Кнопки фокусии, обновления или закрытия вкладки" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="26626-170">Рисунок 4.</span><span class="sxs-lookup"><span data-stu-id="26626-170">Figure 4.</span></span>  <span data-ttu-id="26626-171">Кнопки фокусии, обновления или закрытия вкладки</span><span class="sxs-lookup"><span data-stu-id="26626-171">The buttons for focusing, refreshing, or closing a tab</span></span>  
:::image-end:::  

### <a name="inspect-elements"></a><span data-ttu-id="26626-172">Проверка элементов</span><span class="sxs-lookup"><span data-stu-id="26626-172">Inspect elements</span></span>  

<span data-ttu-id="26626-173">Перейдите к **инструменту Elements** экземпляра DevTools и наведите курсор на элемент, чтобы выделить его в представлении устройства Android.</span><span class="sxs-lookup"><span data-stu-id="26626-173">Navigate to the **Elements** tool of your DevTools instance, and hover on an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="26626-174">Вы также можете выбрать элемент на экране устройства Android, чтобы выбрать его в **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="26626-174">You may also select an element on your Android device screen to select it in the **Elements** tool.</span></span>  <span data-ttu-id="26626-175">Выберите **элемент** \( Выберите элемент \) значок в экземпляре ![ DevTools, а затем выберите элемент ][ImageSelectElementIcon] на экране устройства Android.</span><span class="sxs-lookup"><span data-stu-id="26626-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="26626-176">**Элемент Select** отключен после первого выбора, поэтому необходимо повторно включить его каждый раз, когда вы хотите использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="26626-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <a name="screencast-your-android-screen-to-your-development-machine"></a><span data-ttu-id="26626-177">Screencast your Android screen to your development machine</span><span class="sxs-lookup"><span data-stu-id="26626-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="26626-178">Выберите **значок Toggle Screencast** \( Toggle Screencast \) для просмотра содержимого устройства Android в экземпляре ![ ][ImageToggleScreencastIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="26626-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="26626-179">Вы можете взаимодействовать со скринкастом следующими способами.</span><span class="sxs-lookup"><span data-stu-id="26626-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="26626-180">Выборы переводятся в касания, выпустив соответствующие сенсорные события на устройстве.</span><span class="sxs-lookup"><span data-stu-id="26626-180">Chooses are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="26626-181">Клавиши на компьютере отправляются на устройство.</span><span class="sxs-lookup"><span data-stu-id="26626-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="26626-182">Чтобы смоделировать жест щепотки, `Shift` удерживайте во время перетаскивание.</span><span class="sxs-lookup"><span data-stu-id="26626-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="26626-183">Для прокрутки используйте трекпад или колесо мыши или найдите указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="26626-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="26626-184">Используйте следующие советы, чтобы помочь вам скринкаст.</span><span class="sxs-lookup"><span data-stu-id="26626-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="26626-185">Screencasts отображает только содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="26626-185">Screencasts only display page content.</span></span>  <span data-ttu-id="26626-186">Прозрачные части экрана представляют интерфейсы устройств, такие как адресная стойка Microsoft Edge, панели состояния Android или клавиатура Android.</span><span class="sxs-lookup"><span data-stu-id="26626-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="26626-187">Screencasts отрицательно влияет на частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="26626-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="26626-188">Отключение скринкастинга при измерении свитков или анимаций, чтобы получить более точное представление о производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="26626-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="26626-189">Если экран устройства Android блокируется, содержимое экрана исчезает.</span><span class="sxs-lookup"><span data-stu-id="26626-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="26626-190">Разблокировать экран устройства Android, чтобы автоматически возобновить скринкаст.</span><span class="sxs-lookup"><span data-stu-id="26626-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="26626-191">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="26626-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Настройка параметров разработчика на устройстве | Разработчик Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB OEM | Разработчики Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Средства веб-разработки Safari | Разработчик Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Отладка на мобильных устройствах | Поддержка Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb — Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Устройства DevTools не обнаруживают устройство при подключении ."  

> [!NOTE]
> <span data-ttu-id="26626-198">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="26626-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="26626-199">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="26626-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="26626-201">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="26626-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
