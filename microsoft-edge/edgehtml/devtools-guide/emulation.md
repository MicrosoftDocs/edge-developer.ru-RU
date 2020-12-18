---
description: Использование панели эмуляции для тестирования различных профилей браузера, размеров и разрешений экрана, а также координат расположения GPS
title: DevTools — эмуляция
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, разработка, эмуляция устройства, адаптивный дизайн, географическое местонахождение, разрешение
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235363"
---
# <span data-ttu-id="09934-104">Эмуляция</span><span class="sxs-lookup"><span data-stu-id="09934-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="09934-105">Новый Microsoft Edge создан с использованием Chromium и начинается с версии 75.</span><span class="sxs-lookup"><span data-stu-id="09934-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="09934-106">Для получения дополнительных [сведений скачайте новый Microsoft Edge][MicrosoftNewEdge]и опробуйте новые инструменты разработчика [Microsoft Edge (Chromium).][DevtoolsGuideChromium]</span><span class="sxs-lookup"><span data-stu-id="09934-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="09934-107">Чтобы эмулировать различные устройства, браузеры, размеры экрана и разрешения в новых devTools, перейдите к эмуляции мобильных устройств в [Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="09934-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="09934-108">Панель **эмуляции** помогает в следующих действиях.</span><span class="sxs-lookup"><span data-stu-id="09934-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="09934-109">Имитация [различных профилей устройств,](#device) [браузеров](#browser-profile)и [размеров и разрешений экрана](#display)</span><span class="sxs-lookup"><span data-stu-id="09934-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="09934-110">Проверка различных параметров и координат [географического местонахождения](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="09934-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="Панель эмуляции Microsoft Edge DevTools" lightbox="./media/emulation.png":::
   <span data-ttu-id="09934-112">Панель эмуляции Microsoft \*\*\*\* Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="09934-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="09934-113">Кнопка **"Сохранить параметры** эмуляции" сохраняет все изменения, внесенные в параметры эмуляции рабочего стола по умолчанию, даже если закрыть и повторно открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="09934-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="09934-114">Кнопка **сброса параметров** эмуляции сбрасывает параметры эмуляции обратно в профиль браузера рабочего стола по умолчанию и строку агента пользователя Microsoft Edge с отключенным GPS.</span><span class="sxs-lookup"><span data-stu-id="09934-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="09934-115">Если какой-либо из этих параметров \*\*\*\* изменен по умолчанию, на вкладке "Эмуляция" отображается информационное оповещение о том, что эмулируется определенный аспект поведения браузера.</span><span class="sxs-lookup"><span data-stu-id="09934-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="09934-116">Устройство</span><span class="sxs-lookup"><span data-stu-id="09934-116">Device</span></span>  

<span data-ttu-id="09934-117">Выберите из предустановленного списка профилей устройств с Windows, которые автоматически настраивают другие параметры эмуляции или указывают собственную **настраиваемую конфигурацию.**</span><span class="sxs-lookup"><span data-stu-id="09934-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="09934-118">Чтобы сбросить все средства эмуляции, снова переключиться на значение **"По** умолчанию".</span><span class="sxs-lookup"><span data-stu-id="09934-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="09934-119">Режим</span><span class="sxs-lookup"><span data-stu-id="09934-119">Mode</span></span>  

### <span data-ttu-id="09934-120">Профиль браузера</span><span class="sxs-lookup"><span data-stu-id="09934-120">Browser profile</span></span>  

<span data-ttu-id="09934-121">Чтобы имитировать страницу, запущенную на устройстве \*\*\*\* с Windows Phone, можно быстро изменить параметр профиля браузера на **Windows Phone.**</span><span class="sxs-lookup"><span data-stu-id="09934-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="09934-122">Строка агента пользователя</span><span class="sxs-lookup"><span data-stu-id="09934-122">User agent string</span></span>  

<span data-ttu-id="09934-123">Изменение строки агента пользователя для имитации другого браузера — хороший первый шаг в отладке ошибок, которые происходят только в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="09934-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="09934-124">Сценарии используют строку агента пользователя для определения используемого браузера.</span><span class="sxs-lookup"><span data-stu-id="09934-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="09934-125">Сценарий может быть и на переднем, и на тыловом, и на переднем, и на тыловом.</span><span class="sxs-lookup"><span data-stu-id="09934-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="09934-126">Хотя код не использует обнаружение браузера, он может наследовать его от сторонняя библиотека JavaScript или серверный сценарий.</span><span class="sxs-lookup"><span data-stu-id="09934-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="09934-127">Проблема обнаружения браузера заключается в том, что вы можете масштабировать функции \(или изменить\) на веб-странице, используя предположения о возможностях браузера.</span><span class="sxs-lookup"><span data-stu-id="09934-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="09934-128">Вместо этого следует рассмотреть возможность обнаружения функций для обнаружения возможностей браузера.</span><span class="sxs-lookup"><span data-stu-id="09934-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="09934-129">Непредвиденное поведение может произойти из-за одной из следующих ситуаций.</span><span class="sxs-lookup"><span data-stu-id="09934-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="09934-130">Код, нацеленный на Windows Internet Explorer 8 может работать по-разному в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="09934-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="09934-131">Функция, которую должен поддерживать браузер, отключена из-за предположения разработчика.</span><span class="sxs-lookup"><span data-stu-id="09934-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="09934-132">Если изменение строки агента пользователя укалит проблему, обнаружение браузера, скорее всего, является неуявным.</span><span class="sxs-lookup"><span data-stu-id="09934-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="09934-133">Монитор</span><span class="sxs-lookup"><span data-stu-id="09934-133">Display</span></span>  

<span data-ttu-id="09934-134">Отображение эмуляции для предварительного просмотра сайта на экранах разных размеров и разрешений.</span><span class="sxs-lookup"><span data-stu-id="09934-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="09934-135">обычные настольные мониторы</span><span class="sxs-lookup"><span data-stu-id="09934-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="09934-136">меньшие мобильные экраны</span><span class="sxs-lookup"><span data-stu-id="09934-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="09934-137">более новые дисплеи с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="09934-137">newer high-resolution displays</span></span>  

<span data-ttu-id="09934-138">Эмуляции адаптированы для того, чтобы пытаться соответствовать физическим измерениям эмулированных экранов.</span><span class="sxs-lookup"><span data-stu-id="09934-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="09934-139">Эмулированные пиксели могут отображаться сжатыми или расширенными.</span><span class="sxs-lookup"><span data-stu-id="09934-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="09934-140">Эмуляция не рекомендуется, если требуется протестировать идеальное расположение элементов HTML в пикселях.</span><span class="sxs-lookup"><span data-stu-id="09934-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="09934-141">Эмуляция, тем не менее, хорошо для тестирования адаптивной разработки и выявления проблем с позиционированием более крупных элементов.</span><span class="sxs-lookup"><span data-stu-id="09934-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="09934-142">Ориентация</span><span class="sxs-lookup"><span data-stu-id="09934-142">Orientation</span></span>  

<span data-ttu-id="09934-143">Выберите альбомную **или** **кисть в альбомном режиме.**</span><span class="sxs-lookup"><span data-stu-id="09934-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="09934-144">Разрешение</span><span class="sxs-lookup"><span data-stu-id="09934-144">Resolution</span></span>  

<span data-ttu-id="09934-145">Выберите один из предустановленных разрешений популярных устройств или укажите собственную **настраиваемую** config.  Поддерживаются разрешения до 80 дюймов и 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="09934-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="09934-146">Геолокация</span><span class="sxs-lookup"><span data-stu-id="09934-146">Geolocation</span></span>  

<span data-ttu-id="09934-147">Если ваш веб-сайт использует [API географического][MdnGeolocationUsing] расположения для предоставления служб на основе расположения, на рабочем столе доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="09934-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="09934-148">легко протестировать различные координаты GPS</span><span class="sxs-lookup"><span data-stu-id="09934-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="09934-149">легко тестировать различные состояния датчиков</span><span class="sxs-lookup"><span data-stu-id="09934-149">easily test different sensor states</span></span>  

<span data-ttu-id="09934-150">Параметры переопрепреируют любые фактические координаты GPS и состояние датчика на устройствах, поддерживаюх географическое положение.</span><span class="sxs-lookup"><span data-stu-id="09934-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="09934-151">Прежде чем использовать расположение устройства, веб-сайт должен запросить у пользователя и получить разрешение.</span><span class="sxs-lookup"><span data-stu-id="09934-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="09934-152">Проверьте, как сайт работает с разрешениями на доступ к расположению и без них, на панели параметров Microsoft **Edge.**</span><span class="sxs-lookup"><span data-stu-id="09934-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="09934-153">**...** >  **Параметры**  >  **Просмотр дополнительных параметров**  >  **Разрешения веб-сайта**  >  **Управление**</span><span class="sxs-lookup"><span data-stu-id="09934-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Управление разрешениями веб-сайта с панели параметров Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="09934-155">Управление разрешениями веб-сайта с панели **параметров** Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="09934-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="09934-156">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="09934-156">Shortcuts</span></span>

| <span data-ttu-id="09934-157">Действие</span><span class="sxs-lookup"><span data-stu-id="09934-157">Action</span></span>  | <span data-ttu-id="09934-158">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="09934-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="09934-159">Сброс параметров эмуляции</span><span class="sxs-lookup"><span data-stu-id="09934-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Загрузка нового браузера Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API географического местонахождения | MDN"  
