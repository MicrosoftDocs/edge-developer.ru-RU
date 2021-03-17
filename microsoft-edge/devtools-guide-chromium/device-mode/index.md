---
description: Использование виртуальных устройств в Microsoft Edge для создания веб-сайтов с мобильными устройствами.
title: Эмулировать мобильные устройства в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, девтуолы, эмуляция, устройство, моделирование, мобильный телефон
ms.openlocfilehash: bb081ddd5f773e5e9ae6a1b83b5fcb13408df6cb
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439453"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="78e10-104">Эмулировать мобильные устройства в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="78e10-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="78e10-105">Используйте **эмуляцию** устройства, чтобы приблизить внешний вид и ответы страницы на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="78e10-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="78e10-106">Microsoft Edge DevTools предоставляет коллекцию функций, которые помогут вам подражать мобильным устройствам.</span><span class="sxs-lookup"><span data-stu-id="78e10-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="78e10-107">Коллекция содержит следующие функции.</span><span class="sxs-lookup"><span data-stu-id="78e10-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="78e10-108">Имитация мобильного представления</span><span class="sxs-lookup"><span data-stu-id="78e10-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="78e10-109">Throttle сеть</span><span class="sxs-lookup"><span data-stu-id="78e10-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="78e10-110">Throttle the CPU</span><span class="sxs-lookup"><span data-stu-id="78e10-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="78e10-111">Имитация геолокации</span><span class="sxs-lookup"><span data-stu-id="78e10-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="78e10-112">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="78e10-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="78e10-113">Настройка строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="78e10-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <a name="limitations"></a><span data-ttu-id="78e10-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="78e10-114">Limitations</span></span>  

<span data-ttu-id="78e10-115">**Эмуляция** устройства — это [аппроксимация][WikiApproximation] внешний вид вашей страницы на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="78e10-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="78e10-116">**Эмуляция устройства** фактически не запускает код на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="78e10-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="78e10-117">Вместо этого вы имитируете работу мобильных пользователей с ноутбука или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="78e10-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="78e10-118">Некоторые аспекты мобильных устройств никогда не эмулированы в DevTools.</span><span class="sxs-lookup"><span data-stu-id="78e10-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="78e10-119">Например, архитектура мобильных процессоров отличается от архитектуры процессоров ноутбука или настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="78e10-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="78e10-120">Если вы сомневаетесь, лучше всего запустить страницу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="78e10-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="78e10-121">Используйте [Удаленное отладка][DevToolsRemoteDebugging] для взаимодействия с кодом страницы из компьютера, пока страница фактически работает на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="78e10-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="78e10-122">Вы можете просматривать, изменять, отлаговка, профиль или все четыре во время взаимодействия с кодом.</span><span class="sxs-lookup"><span data-stu-id="78e10-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="78e10-123">Компьютер может быть ноутбуком или настольным компьютером.</span><span class="sxs-lookup"><span data-stu-id="78e10-123">Your machine may be a notebook or desktop computer.</span></span>  

## <a name="simulate-a-mobile-viewport"></a><span data-ttu-id="78e10-124">Имитация мобильного представления</span><span class="sxs-lookup"><span data-stu-id="78e10-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="78e10-125">Выберите эмуляцию устройства **Toggle** \. Панель инструментов устройства \) или выберите Настройка и управление эмуляцией ![ ](../media/toggle-device-toolbar-dark-icon.msft.png) **DevTools** `...` \( \*\*\*\* \) > устройства, чтобы открыть пользовательский интерфейс, который позволяет имитировать мобильный видпорт.</span><span class="sxs-lookup"><span data-stu-id="78e10-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar](../media/toggle-device-toolbar-dark-icon.msft.png)\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="78e10-127">Панель инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="78e10-128">По умолчанию панель инструментов устройства открывается в режиме Responsive Viewport.</span><span class="sxs-lookup"><span data-stu-id="78e10-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <a name="responsive-viewport-mode"></a><span data-ttu-id="78e10-129">Режим "Отзывчивый режим просмотра"</span><span class="sxs-lookup"><span data-stu-id="78e10-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="78e10-130">Чтобы быстро проверить внешний вид и внешний вид страницы на нескольких размерах экрана, перетащите ручки для повторного размера представления до требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="78e10-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="78e10-131">Вы также можете ввести определенные значения в полях ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="78e10-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="78e10-132">На следующем рисунке за установлена ширина, а высота `626` `516` — .</span><span class="sxs-lookup"><span data-stu-id="78e10-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Ручки для изменения размеров представления в режиме Responsive Viewport" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="78e10-134">Ручки для изменения размеров представления в режиме Responsive Viewport</span><span class="sxs-lookup"><span data-stu-id="78e10-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <a name="show-media-queries"></a><span data-ttu-id="78e10-135">Показать запросы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="78e10-135">Show media queries</span></span>  

<span data-ttu-id="78e10-136">Если вы определили запросы мультимедиа на своей странице, переперейти к измерениям viewport, где эти запросы мультимедиа вступает в силу, показывая точки разлома запроса мультимедиа над представлением.</span><span class="sxs-lookup"><span data-stu-id="78e10-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="78e10-137">Выберите **дополнительные**  >  **параметры Показать запросы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="78e10-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Показать запросы мультимедиа" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="78e10-139">Показать запросы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="78e10-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="78e10-140">Выберите точку разлома, чтобы изменить ширину представления, чтобы запрос мультимедиа был срабатываем.</span><span class="sxs-lookup"><span data-stu-id="78e10-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Выберите точку разрыва, чтобы изменить ширину представления" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="78e10-142">Выберите точку разрыва, чтобы изменить ширину представления</span><span class="sxs-lookup"><span data-stu-id="78e10-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <a name="set-the-device-type"></a><span data-ttu-id="78e10-143">Настройка типа устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-143">Set the device type</span></span>  

<span data-ttu-id="78e10-144">Используйте список **типа устройства** для имитации мобильного устройства или настольного устройства.</span><span class="sxs-lookup"><span data-stu-id="78e10-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Список типов устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="78e10-146">Список **типов** устройств</span><span class="sxs-lookup"><span data-stu-id="78e10-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="78e10-147">В следующей таблице описываются различия между доступными вариантами типа устройства.</span><span class="sxs-lookup"><span data-stu-id="78e10-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="78e10-148">В столбце метода рендеринга указывается, отрисовка страницы Microsoft Edge в качестве мобильного или настольного представления.</span><span class="sxs-lookup"><span data-stu-id="78e10-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="78e10-149">Столбец Cursor ссылается на тип курсора, отображаемого при наведении на странице.</span><span class="sxs-lookup"><span data-stu-id="78e10-149">The Cursor icon column refers to what type of cursor is displayed when you hover on the page.</span></span>  <span data-ttu-id="78e10-150">В срабатывом столбце События указывается, запускается ли страница или события при взаимодействии `touch` `click` со страницей.</span><span class="sxs-lookup"><span data-stu-id="78e10-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="78e10-151">Параметр</span><span class="sxs-lookup"><span data-stu-id="78e10-151">Option</span></span> | <span data-ttu-id="78e10-152">Метод отрисовки</span><span class="sxs-lookup"><span data-stu-id="78e10-152">Rendering method</span></span> | <span data-ttu-id="78e10-153">Значок Cursor</span><span class="sxs-lookup"><span data-stu-id="78e10-153">Cursor icon</span></span> | <span data-ttu-id="78e10-154">События, срабатыва</span><span class="sxs-lookup"><span data-stu-id="78e10-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="78e10-155">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-155">Mobile</span></span> | <span data-ttu-id="78e10-156">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-156">Mobile</span></span> | <span data-ttu-id="78e10-157">Круг</span><span class="sxs-lookup"><span data-stu-id="78e10-157">Circle</span></span> | <span data-ttu-id="78e10-158">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="78e10-158">touch</span></span> |  
| <span data-ttu-id="78e10-159">Mobile \(без касания\)</span><span class="sxs-lookup"><span data-stu-id="78e10-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="78e10-160">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-160">Mobile</span></span> | <span data-ttu-id="78e10-161">Обычный</span><span class="sxs-lookup"><span data-stu-id="78e10-161">Normal</span></span> | <span data-ttu-id="78e10-162"> выберите </span><span class="sxs-lookup"><span data-stu-id="78e10-162">choose</span></span> |  
| <span data-ttu-id="78e10-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="78e10-163">Desktop</span></span> | <span data-ttu-id="78e10-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="78e10-164">Desktop</span></span> | <span data-ttu-id="78e10-165">Обычный</span><span class="sxs-lookup"><span data-stu-id="78e10-165">Normal</span></span> | <span data-ttu-id="78e10-166"> выберите </span><span class="sxs-lookup"><span data-stu-id="78e10-166">choose</span></span> |  
| <span data-ttu-id="78e10-167">Desktop \(touch\)</span><span class="sxs-lookup"><span data-stu-id="78e10-167">Desktop \(touch\)</span></span> | <span data-ttu-id="78e10-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="78e10-168">Desktop</span></span> | <span data-ttu-id="78e10-169">Круг</span><span class="sxs-lookup"><span data-stu-id="78e10-169">Circle</span></span> | <span data-ttu-id="78e10-170">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="78e10-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="78e10-171">Если список **типа** устройства не отображается, выберите **Дополнительные параметры**  >  **Добавить тип устройства.**</span><span class="sxs-lookup"><span data-stu-id="78e10-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <a name="mobile-device-viewport-mode"></a><span data-ttu-id="78e10-172">Режим представления мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="78e10-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="78e10-173">Чтобы имитировать размеры определенного мобильного устройства, выберите устройство из **списка Устройств.**</span><span class="sxs-lookup"><span data-stu-id="78e10-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Список устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="78e10-175">Список **устройств**</span><span class="sxs-lookup"><span data-stu-id="78e10-175">The **Device** list</span></span>  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a><span data-ttu-id="78e10-176">Поверните представление на ориентацию ландшафта</span><span class="sxs-lookup"><span data-stu-id="78e10-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="78e10-177">Проверьте веб-страницу в ландшафтной ориентации.</span><span class="sxs-lookup"><span data-stu-id="78e10-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="78e10-178">Чтобы повернуть представление в ландшафтную ориентацию, выберите **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="78e10-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Страница, отображаемая в ландшафтной ориентации" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="78e10-180">Страница, отображаемая в ландшафтной ориентации</span><span class="sxs-lookup"><span data-stu-id="78e10-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="78e10-181">Кнопка **Вращать** исчезает, если панель **инструментов устройства** узкая.</span><span class="sxs-lookup"><span data-stu-id="78e10-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="78e10-183">Панель **инструментов устройства**</span><span class="sxs-lookup"><span data-stu-id="78e10-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="78e10-184">Дополнительные сведения перейдите в [set orientation](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="78e10-184">For more information, navigate to [Set orientation](#set-orientation).</span></span>  

#### <a name="show-device-frame"></a><span data-ttu-id="78e10-185">Показать кадр устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-185">Show device frame</span></span>  

<span data-ttu-id="78e10-186">Отображение физической рамки устройства вокруг представления при имитации размеров определенного мобильного устройства, например iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="78e10-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="78e10-187">Откройте **дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="78e10-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="78e10-188">Выберите **кадр устройства Show**.</span><span class="sxs-lookup"><span data-stu-id="78e10-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="78e10-189">Если кадр устройства для определенного устройства не отображается, это означает, что в DevTools нет искусства для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="78e10-189">If a device frame for a particular device is not displayed, it means that DevTools does not have art for the option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Показать кадр устройства" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="78e10-191">Показать кадр устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Кадр устройства для iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="78e10-193">Кадр устройства для iPhone 6</span><span class="sxs-lookup"><span data-stu-id="78e10-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a><span data-ttu-id="78e10-194">Добавление настраиваемого мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-194">Add a custom mobile device</span></span>  

<span data-ttu-id="78e10-195">Если необходимый параметр мобильного устройства не включен в список по умолчанию, можно добавить настраиваемое устройство.</span><span class="sxs-lookup"><span data-stu-id="78e10-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="78e10-196">Чтобы добавить настраиваемые устройства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78e10-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="78e10-197">Выберите список **устройств,** > **изменить**.</span><span class="sxs-lookup"><span data-stu-id="78e10-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Выбор правки" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="78e10-199">Выбор **правки**</span><span class="sxs-lookup"><span data-stu-id="78e10-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="78e10-200">Выберите **Добавление настраиваемой устройства**.</span><span class="sxs-lookup"><span data-stu-id="78e10-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="78e10-201">На **эмулированных устройствах**введите имя устройства, ширину экрана и высоту экрана для настраиваемого устройства.</span><span class="sxs-lookup"><span data-stu-id="78e10-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="78e10-202">Соотношение [пикселей устройства,][MDNWindowDevicePixelRatio] [строка агента пользователя][MDNUserAgent]и поля [типа](#set-the-device-type) устройства необязательны.</span><span class="sxs-lookup"><span data-stu-id="78e10-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="78e10-203">Поле типа устройства по умолчанию является **мобильным.**</span><span class="sxs-lookup"><span data-stu-id="78e10-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Создание настраиваемой устройства" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="78e10-205">Создание настраиваемой устройства</span><span class="sxs-lookup"><span data-stu-id="78e10-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <a name="show-rulers"></a><span data-ttu-id="78e10-206">Показать линейки</span><span class="sxs-lookup"><span data-stu-id="78e10-206">Show rulers</span></span>  

<span data-ttu-id="78e10-207">Если необходимо измерить размеры экрана, можно использовать линейки для измерения размера экрана в пикселях.</span><span class="sxs-lookup"><span data-stu-id="78e10-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="78e10-208">Выберите **дополнительные**  >  **параметры Показать линейки,** чтобы отображать линейки выше и слева от вашего представления.</span><span class="sxs-lookup"><span data-stu-id="78e10-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Элемент меню для отображения правителей" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="78e10-210">Элемент меню для отображения правителей</span><span class="sxs-lookup"><span data-stu-id="78e10-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Линейки сверху и слева от представления" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="78e10-212">Линейки сверху и слева от представления</span><span class="sxs-lookup"><span data-stu-id="78e10-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a><span data-ttu-id="78e10-213">Масштабирование представления</span><span class="sxs-lookup"><span data-stu-id="78e10-213">Zoom the viewport</span></span>  

<span data-ttu-id="78e10-214">Чтобы проверить внешний вид и внешний вид страницы на нескольких уровнях масштабирования, используйте список **Масштабирование,** чтобы увеличить или выйти.</span><span class="sxs-lookup"><span data-stu-id="78e10-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="78e10-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="78e10-216">Zoom</span></span>**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a><span data-ttu-id="78e10-217">Throttle сети и ЦП</span><span class="sxs-lookup"><span data-stu-id="78e10-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="78e10-218">На мобильных устройствах часто имеются ограничения сети и ЦП.</span><span class="sxs-lookup"><span data-stu-id="78e10-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="78e10-219">Проверьте, как быстро загружается страница и как она реагирует на различные скорости интернета и ЦП.</span><span class="sxs-lookup"><span data-stu-id="78e10-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="78e10-220">Throttle сети и ЦП.</span><span class="sxs-lookup"><span data-stu-id="78e10-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="78e10-221">Выберите **список Throttle** и измените предустановленную на **среднеуровневую** мобильную или **низкоуровневую.**</span><span class="sxs-lookup"><span data-stu-id="78e10-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="78e10-222">**Мобильный телефон среднего уровня** имитирует `fast 3G` и подгонает ЦП.</span><span class="sxs-lookup"><span data-stu-id="78e10-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="78e10-223">Он в четыре раза медленнее обычного.</span><span class="sxs-lookup"><span data-stu-id="78e10-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="78e10-224">**Мобильный телефон с низким** уровнем уровня имитирует `slow 3G` и подавляет ЦП.</span><span class="sxs-lookup"><span data-stu-id="78e10-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="78e10-225">Это в шесть раз медленнее обычного.</span><span class="sxs-lookup"><span data-stu-id="78e10-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="78e10-226">Все регулирование зависит от нормальной возможности ноутбука или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="78e10-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Список дроссельной заслонки в панели инструментов устройств" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="78e10-228">Список **дроссельной заслонки** в панели инструментов устройств</span><span class="sxs-lookup"><span data-stu-id="78e10-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="78e10-229">Если список **Throttle скрыт,** панель инструментов **устройства** слишком узкая.</span><span class="sxs-lookup"><span data-stu-id="78e10-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="78e10-230">Чтобы получить доступ **к списку Throttle,** увеличите ширину панели **инструментов устройства.**</span><span class="sxs-lookup"><span data-stu-id="78e10-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов устройства" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="78e10-232">Панель **инструментов устройства**</span><span class="sxs-lookup"><span data-stu-id="78e10-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a><span data-ttu-id="78e10-233">Затормажает только ЦП</span><span class="sxs-lookup"><span data-stu-id="78e10-233">Throttle the CPU only</span></span>  

<span data-ttu-id="78e10-234">Чтобы затормалить только ЦП, а не сеть, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78e10-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="78e10-235">Выберите панель **Performance** и выберите **Параметры захвата** \. ![ Параметры захвата ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="78e10-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>
1.  <span data-ttu-id="78e10-236">Выберите **замедление**  >  **4x** ЦП или **замедление 6x.**</span><span class="sxs-lookup"><span data-stu-id="78e10-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Список ЦП в панели Performance" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="78e10-238">Список **ЦП** в панели **Performance**</span><span class="sxs-lookup"><span data-stu-id="78e10-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a><span data-ttu-id="78e10-239">Throttle сеть только</span><span class="sxs-lookup"><span data-stu-id="78e10-239">Throttle the network only</span></span>  

<span data-ttu-id="78e10-240">Чтобы затормалить сеть, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78e10-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="78e10-241">Выберите средство **Network.**</span><span class="sxs-lookup"><span data-stu-id="78e10-241">Choose the **Network** tool.</span></span>
1.  <span data-ttu-id="78e10-242">Выберите **Online**  >  **Fast 3G** или Slow **3G**.</span><span class="sxs-lookup"><span data-stu-id="78e10-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Список Throttle в панели Network" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="78e10-244">Список **Throttle** в панели Network</span><span class="sxs-lookup"><span data-stu-id="78e10-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="78e10-245">Или выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\) \*\*\*\* `3G` \*\*\*\* \*\*\*\* для открытия командного меню , введите и выберите Включить быстрое регулирование 3G или включить медленное регулирование 3G .</span><span class="sxs-lookup"><span data-stu-id="78e10-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="78e10-247">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="78e10-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="78e10-248">Кроме того, можно установить регулирование сети с панели **Performance.**</span><span class="sxs-lookup"><span data-stu-id="78e10-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="78e10-249">Выберите **Параметры** захвата \. Параметры захвата \) и выберите список Сети и измените заранее на ![ быстрый ](../media/capture-settings-icon.msft.png) **3G** или **медленный 3G**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="78e10-249">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Настройка регулирования сети с панели Performance" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="78e10-251">Настройка регулирования сети с панели **Performance**</span><span class="sxs-lookup"><span data-stu-id="78e10-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <a name="override-geolocation"></a><span data-ttu-id="78e10-252">Переопределение геолокации</span><span class="sxs-lookup"><span data-stu-id="78e10-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="78e10-253">Если ваша страница зависит от сведений о геолокации с мобильного устройства для правильной отрисовки, предопределите различные геолокации с помощью пользовательского интерфейса, переопределяемого геолокацией.</span><span class="sxs-lookup"><span data-stu-id="78e10-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="78e10-254">Выберите **Настройка и управление DevTools** `...` \( \) > **Дополнительные датчики**  >  **инструментов**.</span><span class="sxs-lookup"><span data-stu-id="78e10-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики геолокации" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="78e10-256">**Датчики** геолокации</span><span class="sxs-lookup"><span data-stu-id="78e10-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="78e10-257">Откройте командное меню.</span><span class="sxs-lookup"><span data-stu-id="78e10-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="78e10-258">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="78e10-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="78e10-259">Введите `Sensors` и выберите **датчики show**.</span><span class="sxs-lookup"><span data-stu-id="78e10-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики для геолокации" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="78e10-261">**Показать датчики** для геолокации</span><span class="sxs-lookup"><span data-stu-id="78e10-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="78e10-262">На панели **Датчики** можно выбрать одно из заранее заранее задаваемых расположений, включенных в DevTools, с помощью выпадаемого \*\*\*\* меню Location.</span><span class="sxs-lookup"><span data-stu-id="78e10-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="78e10-263">Чтобы ввести настраиваемую расположение, выберите **другое...**</span><span class="sxs-lookup"><span data-stu-id="78e10-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="78e10-264">и введите координаты настраиваемого расположения.</span><span class="sxs-lookup"><span data-stu-id="78e10-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="78e10-265">Чтобы проверить страницу в состоянии ошибки при недоступности сведений о расположении, выберите **расположение недоступно.**</span><span class="sxs-lookup"><span data-stu-id="78e10-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Панель датчиков с заранее выбранным расположением" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="78e10-267">**Панель** датчиков с выбранным заранее расположением.</span><span class="sxs-lookup"><span data-stu-id="78e10-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <a name="set-orientation"></a><span data-ttu-id="78e10-268">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="78e10-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="78e10-269">Если ваша страница зависит от сведений об ориентации с мобильного устройства для правильного отображения, откройте пользовательский интерфейс ориентации.</span><span class="sxs-lookup"><span data-stu-id="78e10-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="78e10-270">Выберите **Настройка и управление DevTools** `...` \( \) > **Дополнительные датчики**  >  **инструментов**.</span><span class="sxs-lookup"><span data-stu-id="78e10-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики для ориентации" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="78e10-272">**Датчики** для ориентации</span><span class="sxs-lookup"><span data-stu-id="78e10-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="78e10-273">Откройте командное меню.</span><span class="sxs-lookup"><span data-stu-id="78e10-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="78e10-274">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="78e10-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="78e10-275">Введите `Sensors` и выберите **датчики show**.</span><span class="sxs-lookup"><span data-stu-id="78e10-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики для ориентации" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="78e10-277">**Показать датчики** для ориентации</span><span class="sxs-lookup"><span data-stu-id="78e10-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="78e10-278">На панели **Датчики** можно выбрать предустановленную ориентацию из выпадаемого меню "Ориентация". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="78e10-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="78e10-279">Чтобы ввести собственную ориентацию, выберите **настраиваемую**ориентацию и введите собственные значения [альфа-версии,][MDNDeviceOrientaitonAlpha] [бета-версии][MDNDeviceOrientaitonGamma] и гаммы. [][MDNDeviceOrientaitonBeta]</span><span class="sxs-lookup"><span data-stu-id="78e10-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Параметры ориентации на панели Датчики" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="78e10-281">**Параметры** ориентации на **панели Датчики**</span><span class="sxs-lookup"><span data-stu-id="78e10-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <a name="set-user-agent-string"></a><span data-ttu-id="78e10-282">Настройка строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="78e10-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="78e10-283">Если ваша страница зависит от строки агента пользователя с мобильного устройства для правильной визуализации, используйте панель условий Сети для предоставления различных строк агента пользователя. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="78e10-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="78e10-284">Выберите **Настройка и управление DevTools** `...` \( \) > **дополнительные условия**сети  >  **инструментов.**</span><span class="sxs-lookup"><span data-stu-id="78e10-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Запись условий сети в меню More tools" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="78e10-286">**Запись условий** сети в **меню More tools**</span><span class="sxs-lookup"><span data-stu-id="78e10-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="78e10-287">Откройте командное меню.</span><span class="sxs-lookup"><span data-stu-id="78e10-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="78e10-288">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="78e10-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="78e10-289">Введите `Network conditions` и выберите условия Show **Network**.</span><span class="sxs-lookup"><span data-stu-id="78e10-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Показать условия сети" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="78e10-291">Показать условия сети</span><span class="sxs-lookup"><span data-stu-id="78e10-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="78e10-292">Рядом с **агентом пользователя**выберите **автоматический** почтовый ящик Select.</span><span class="sxs-lookup"><span data-stu-id="78e10-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="78e10-293">Затем выберите **Настраиваемый...,** чтобы выбрать из списка заранее задав строки агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="78e10-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="78e10-294">Чтобы ввести собственную строку агента пользователя, введите строку **в Ввод пользовательского агента.**</span><span class="sxs-lookup"><span data-stu-id="78e10-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Установите строку агента пользователя в Microsoft Edge на macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="78e10-296">Установите строку агента пользователя в Microsoft Edge на macOS</span><span class="sxs-lookup"><span data-stu-id="78e10-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="78e10-297">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="78e10-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Начало работы с удаленной отладки устройств Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый порядок — Википедия"  

> [!NOTE]
> <span data-ttu-id="78e10-305">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="78e10-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="78e10-306">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="78e10-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="78e10-308">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="78e10-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
