---
description: A comprehensive reference of Microsoft Edge DevTools Network panel features.
title: Network Analysis reference
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools
ms.openlocfilehash: 758623482ab2179987c6467f8e30c72d8893d710
ms.sourcegitcommit: addfd27bb765c92880a59f259dc702f6e4e1bf28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2020
ms.locfileid: "11092316"
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

# <span data-ttu-id="e8b22-104">Network Analysis reference</span><span class="sxs-lookup"><span data-stu-id="e8b22-104">Network Analysis reference</span></span>  

<span data-ttu-id="e8b22-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span><span class="sxs-lookup"><span data-stu-id="e8b22-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="e8b22-106">Record network requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-106">Record network requests</span></span>  

<span data-ttu-id="e8b22-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span><span class="sxs-lookup"><span data-stu-id="e8b22-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="The Network panel" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="e8b22-109">The **Network** panel</span><span class="sxs-lookup"><span data-stu-id="e8b22-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-110">Stop recording network requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-110">Stop recording network requests</span></span>  

<span data-ttu-id="e8b22-111">To stop recording requests, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-112">Select **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\) on the **Network** panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-112">Select **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\) on the **Network** panel.</span></span>  <span data-ttu-id="e8b22-113">It turns grey to indicate that DevTools is no longer recording requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="e8b22-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span><span class="sxs-lookup"><span data-stu-id="e8b22-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="e8b22-115">Clear requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-115">Clear requests</span></span>  

<span data-ttu-id="e8b22-116">Select **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-116">Select **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="The Network panel" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="e8b22-118">The **Clear** button</span><span class="sxs-lookup"><span data-stu-id="e8b22-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-119">Save requests across page loads</span><span class="sxs-lookup"><span data-stu-id="e8b22-119">Save requests across page loads</span></span>  

<span data-ttu-id="e8b22-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="e8b22-121">DevTools saves all requests until you disable **Preserve log**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="The Network panel" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="e8b22-123">The **Preserve Log** checkbox</span><span class="sxs-lookup"><span data-stu-id="e8b22-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-124">Capture screenshots during page load</span><span class="sxs-lookup"><span data-stu-id="e8b22-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="e8b22-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span><span class="sxs-lookup"><span data-stu-id="e8b22-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="e8b22-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="e8b22-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span><span class="sxs-lookup"><span data-stu-id="e8b22-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="e8b22-128">After capturing a screenshot, you interact with it in the following ways.</span><span class="sxs-lookup"><span data-stu-id="e8b22-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="e8b22-129">Hover over a screenshot to view the point at which that screenshot was captured.</span><span class="sxs-lookup"><span data-stu-id="e8b22-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="e8b22-130">A yellow line is displayed on the **Overview** pane.</span><span class="sxs-lookup"><span data-stu-id="e8b22-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="e8b22-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span><span class="sxs-lookup"><span data-stu-id="e8b22-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="e8b22-132">Double-click a thumbnail to zoom into it.</span><span class="sxs-lookup"><span data-stu-id="e8b22-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="The Network panel" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="e8b22-134">Hovering over a screenshot</span><span class="sxs-lookup"><span data-stu-id="e8b22-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="The Network panel" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="e8b22-135">Change loading behavior</span><span class="sxs-lookup"><span data-stu-id="e8b22-135">Change loading behavior</span></span>  

### <span data-ttu-id="e8b22-136">Emulate a first-time visitor by disabling the browser cache</span><span class="sxs-lookup"><span data-stu-id="e8b22-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="e8b22-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span><span class="sxs-lookup"><span data-stu-id="e8b22-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="e8b22-138">DevTools disables the browser cache.</span><span class="sxs-lookup"><span data-stu-id="e8b22-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="e8b22-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span><span class="sxs-lookup"><span data-stu-id="e8b22-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="The Network panel" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="e8b22-141">The **Disable Cache** checkbox</span><span class="sxs-lookup"><span data-stu-id="e8b22-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8b22-142">Disable the browser cache from the Network Conditions drawer</span><span class="sxs-lookup"><span data-stu-id="e8b22-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="e8b22-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e8b22-144">Open the **Network Conditions** drawer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e8b22-145">Check or uncheck the **Disable cache** checkbox.</span><span class="sxs-lookup"><span data-stu-id="e8b22-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e8b22-146">Manually clear the browser cache</span><span class="sxs-lookup"><span data-stu-id="e8b22-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="e8b22-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="The Network panel" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="e8b22-149">Selecting **Clear Browser Cache**</span><span class="sxs-lookup"><span data-stu-id="e8b22-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-150">Emulate offline</span><span class="sxs-lookup"><span data-stu-id="e8b22-150">Emulate offline</span></span>  

<span data-ttu-id="e8b22-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="e8b22-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span><span class="sxs-lookup"><span data-stu-id="e8b22-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="e8b22-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate an offline network experience.</span><span class="sxs-lookup"><span data-stu-id="e8b22-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="The Network panel" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="e8b22-155">The **Offline** dropdown menu</span><span class="sxs-lookup"><span data-stu-id="e8b22-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-156">Emulate slow network connections</span><span class="sxs-lookup"><span data-stu-id="e8b22-156">Emulate slow network connections</span></span>  

<span data-ttu-id="e8b22-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span><span class="sxs-lookup"><span data-stu-id="e8b22-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="The Network panel" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="e8b22-159">The **Throttling** dropdown menu</span><span class="sxs-lookup"><span data-stu-id="e8b22-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-160">You may select from different presets, such as Slow 3G or Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="e8b22-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="e8b22-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="e8b22-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span><span class="sxs-lookup"><span data-stu-id="e8b22-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="e8b22-163">Emulate slow network connections from the Network Conditions drawer</span><span class="sxs-lookup"><span data-stu-id="e8b22-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="e8b22-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="e8b22-165">Open the **Network Conditions** drawer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e8b22-166">Select your connection speed from the **Throttling** menu.</span><span class="sxs-lookup"><span data-stu-id="e8b22-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="e8b22-167">Manually clear browser cookies</span><span class="sxs-lookup"><span data-stu-id="e8b22-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="e8b22-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="The Network panel" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="e8b22-170">Selecting **Clear Browser Cookies**</span><span class="sxs-lookup"><span data-stu-id="e8b22-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-171">Override the user agent</span><span class="sxs-lookup"><span data-stu-id="e8b22-171">Override the user agent</span></span>  

<span data-ttu-id="e8b22-172">To manually override the user agent, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-173">Open the **Network Conditions** drawer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="e8b22-174">Uncheck **Select automatically**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="e8b22-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span><span class="sxs-lookup"><span data-stu-id="e8b22-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="e8b22-176">Filter requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-176">Filter requests</span></span>  

### <span data-ttu-id="e8b22-177">Filter requests by properties</span><span class="sxs-lookup"><span data-stu-id="e8b22-177">Filter requests by properties</span></span>  

<span data-ttu-id="e8b22-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="e8b22-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span><span class="sxs-lookup"><span data-stu-id="e8b22-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="e8b22-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e8b22-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="The Network panel" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="e8b22-182">The **Filter** text box</span><span class="sxs-lookup"><span data-stu-id="e8b22-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-183">You may use multiple properties simultaneously by separating each property with a space.</span><span class="sxs-lookup"><span data-stu-id="e8b22-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="e8b22-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="e8b22-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="e8b22-185">The multi-property filters are equivalent to `AND` operations.</span><span class="sxs-lookup"><span data-stu-id="e8b22-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="e8b22-186">operations are currently not supported.</span><span class="sxs-lookup"><span data-stu-id="e8b22-186">operations are currently not supported.</span></span>  

<span data-ttu-id="e8b22-187">The complete list of supported properties.</span><span class="sxs-lookup"><span data-stu-id="e8b22-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="e8b22-188">Property</span><span class="sxs-lookup"><span data-stu-id="e8b22-188">Property</span></span> | <span data-ttu-id="e8b22-189">Details</span><span class="sxs-lookup"><span data-stu-id="e8b22-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="e8b22-190">Only display resources from the specified domain.</span><span class="sxs-lookup"><span data-stu-id="e8b22-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="e8b22-191">You may use a wildcard character \(`*`\) to include multiple domains.</span><span class="sxs-lookup"><span data-stu-id="e8b22-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="e8b22-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span><span class="sxs-lookup"><span data-stu-id="e8b22-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="e8b22-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="e8b22-194">Displays the resources that contain the specified HTTP response header.</span><span class="sxs-lookup"><span data-stu-id="e8b22-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="e8b22-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="e8b22-196">Use `is:running` to find `WebSocket` resources.</span><span class="sxs-lookup"><span data-stu-id="e8b22-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="e8b22-197">Displays resources that are larger than the specified size, in bytes.</span><span class="sxs-lookup"><span data-stu-id="e8b22-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="e8b22-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span><span class="sxs-lookup"><span data-stu-id="e8b22-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="e8b22-199">Displays resources that were retrieved over a specified HTTP method type.</span><span class="sxs-lookup"><span data-stu-id="e8b22-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="e8b22-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="e8b22-201">Displays resources of a specified MIME type.</span><span class="sxs-lookup"><span data-stu-id="e8b22-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="e8b22-202">DevTools populate the dropdown with all MIME types  that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="e8b22-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span><span class="sxs-lookup"><span data-stu-id="e8b22-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="e8b22-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span><span class="sxs-lookup"><span data-stu-id="e8b22-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="e8b22-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span><span class="sxs-lookup"><span data-stu-id="e8b22-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="e8b22-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="e8b22-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span><span class="sxs-lookup"><span data-stu-id="e8b22-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="e8b22-208">DevTools populate the autocomplete with all of the cookie names that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="e8b22-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span><span class="sxs-lookup"><span data-stu-id="e8b22-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="e8b22-210">DevTools populate the autocomplete with all of the cookie values that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="e8b22-211">Displays resources that match the specific HTTP status code.</span><span class="sxs-lookup"><span data-stu-id="e8b22-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="e8b22-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span><span class="sxs-lookup"><span data-stu-id="e8b22-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="e8b22-213">Filter requests by type</span><span class="sxs-lookup"><span data-stu-id="e8b22-213">Filter requests by type</span></span>  

<span data-ttu-id="e8b22-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-215">XHR</span><span class="sxs-lookup"><span data-stu-id="e8b22-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-216">JS</span><span class="sxs-lookup"><span data-stu-id="e8b22-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-217">CSS</span><span class="sxs-lookup"><span data-stu-id="e8b22-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-218">Img</span><span class="sxs-lookup"><span data-stu-id="e8b22-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-219">Media</span><span class="sxs-lookup"><span data-stu-id="e8b22-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-220">Font</span><span class="sxs-lookup"><span data-stu-id="e8b22-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-221">Doc</span><span class="sxs-lookup"><span data-stu-id="e8b22-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-222">WS</span><span class="sxs-lookup"><span data-stu-id="e8b22-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="e8b22-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-224">Manifest</span><span class="sxs-lookup"><span data-stu-id="e8b22-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-225">Other</span><span class="sxs-lookup"><span data-stu-id="e8b22-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-226">Any other type not listed.</span><span class="sxs-lookup"><span data-stu-id="e8b22-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e8b22-227">If the buttons do not display, the **Filters** pane may be hidden.</span><span class="sxs-lookup"><span data-stu-id="e8b22-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="e8b22-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="e8b22-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="e8b22-229">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span><span class="sxs-lookup"><span data-stu-id="e8b22-229">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="The Network panel" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="e8b22-231">Using the Type filters to display JS, CSS, and Document resources</span><span class="sxs-lookup"><span data-stu-id="e8b22-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-232">Filter requests by time</span><span class="sxs-lookup"><span data-stu-id="e8b22-232">Filter requests by time</span></span>  

<span data-ttu-id="e8b22-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span><span class="sxs-lookup"><span data-stu-id="e8b22-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="e8b22-234">The filter is inclusive.</span><span class="sxs-lookup"><span data-stu-id="e8b22-234">The filter is inclusive.</span></span>  <span data-ttu-id="e8b22-235">Any request that was active during the highlighted time is shown.</span><span class="sxs-lookup"><span data-stu-id="e8b22-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="The Network panel" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="e8b22-237">Filtering out any requests that were inactive around 300 ms</span><span class="sxs-lookup"><span data-stu-id="e8b22-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-238">Hide data URLs</span><span class="sxs-lookup"><span data-stu-id="e8b22-238">Hide data URLs</span></span>  

<span data-ttu-id="e8b22-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span><span class="sxs-lookup"><span data-stu-id="e8b22-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="e8b22-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span><span class="sxs-lookup"><span data-stu-id="e8b22-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="e8b22-241">Check the **Hide data URLs** checkbox to hide the requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="The Network panel" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="e8b22-243">The **Hide Data URLs** checkbox</span><span class="sxs-lookup"><span data-stu-id="e8b22-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="e8b22-244">Sort requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-244">Sort requests</span></span>  

<span data-ttu-id="e8b22-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span><span class="sxs-lookup"><span data-stu-id="e8b22-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="e8b22-246">Sort by column</span><span class="sxs-lookup"><span data-stu-id="e8b22-246">Sort by column</span></span>  

<span data-ttu-id="e8b22-247">Select the header of any column in the Requests to sort requests by that column.</span><span class="sxs-lookup"><span data-stu-id="e8b22-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="e8b22-248">Sort by activity phase</span><span class="sxs-lookup"><span data-stu-id="e8b22-248">Sort by activity phase</span></span>  

<span data-ttu-id="e8b22-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span><span class="sxs-lookup"><span data-stu-id="e8b22-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-250">Start Time</span><span class="sxs-lookup"><span data-stu-id="e8b22-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-251">The first request that was initiated is at the top.</span><span class="sxs-lookup"><span data-stu-id="e8b22-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-252">Response Time</span><span class="sxs-lookup"><span data-stu-id="e8b22-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-253">The first request that started downloading is at the top.</span><span class="sxs-lookup"><span data-stu-id="e8b22-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-254">End Time</span><span class="sxs-lookup"><span data-stu-id="e8b22-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-255">The first request that finished is at the top.</span><span class="sxs-lookup"><span data-stu-id="e8b22-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-256">Total Duration</span><span class="sxs-lookup"><span data-stu-id="e8b22-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-257">The request with the shortest connection settings and request or response is at the top.</span><span class="sxs-lookup"><span data-stu-id="e8b22-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-258">Latency</span><span class="sxs-lookup"><span data-stu-id="e8b22-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-259">The request that waited the shortest time for a response is at the top.</span><span class="sxs-lookup"><span data-stu-id="e8b22-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e8b22-260">These descriptions assume that each respective option is ranked from shortest to longest.</span><span class="sxs-lookup"><span data-stu-id="e8b22-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="e8b22-261">Selecting the header of the **Waterfall** column reverses the order.</span><span class="sxs-lookup"><span data-stu-id="e8b22-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="The Network panel" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="e8b22-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span><span class="sxs-lookup"><span data-stu-id="e8b22-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e8b22-264">Analyze requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-264">Analyze requests</span></span>  

<span data-ttu-id="e8b22-265">So long as DevTools are open, it logs all requests in the Network panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="e8b22-266">Use the Network panel to analyze requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="e8b22-267">View a log of requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-267">View a log of requests</span></span>  

<span data-ttu-id="e8b22-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span><span class="sxs-lookup"><span data-stu-id="e8b22-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="e8b22-269">Selecting or hovering over requests reveals more information about each item.</span><span class="sxs-lookup"><span data-stu-id="e8b22-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="e8b22-271">The Requests table</span><span class="sxs-lookup"><span data-stu-id="e8b22-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-272">The Requests table displays the following columns by default.</span><span class="sxs-lookup"><span data-stu-id="e8b22-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-273">Name</span><span class="sxs-lookup"><span data-stu-id="e8b22-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-274">The filename of, or an identifier for, the resource.</span><span class="sxs-lookup"><span data-stu-id="e8b22-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-275">Status</span><span class="sxs-lookup"><span data-stu-id="e8b22-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-276">The HTTP status code.</span><span class="sxs-lookup"><span data-stu-id="e8b22-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-277">Type</span><span class="sxs-lookup"><span data-stu-id="e8b22-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-278">The MIME type of the requested resource.</span><span class="sxs-lookup"><span data-stu-id="e8b22-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-279">Initiator</span><span class="sxs-lookup"><span data-stu-id="e8b22-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-280">The following objects or processes initiate requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="e8b22-281">**Parser**  The HTML parser for Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8b22-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="e8b22-282">**Redirect**  An HTTP redirect.</span><span class="sxs-lookup"><span data-stu-id="e8b22-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="e8b22-283">**Script**  A JavaScript function.</span><span class="sxs-lookup"><span data-stu-id="e8b22-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="e8b22-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span><span class="sxs-lookup"><span data-stu-id="e8b22-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-285">Size</span><span class="sxs-lookup"><span data-stu-id="e8b22-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-286">The combined size of the response headers plus the response body, as delivered by the server.</span><span class="sxs-lookup"><span data-stu-id="e8b22-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-287">Time</span><span class="sxs-lookup"><span data-stu-id="e8b22-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span><span class="sxs-lookup"><span data-stu-id="e8b22-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="e8b22-289">Waterfall</span><span class="sxs-lookup"><span data-stu-id="e8b22-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-290">A visual breakdown of the activity for each request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="e8b22-291">Add or remove columns</span><span class="sxs-lookup"><span data-stu-id="e8b22-291">Add or remove columns</span></span>  

<span data-ttu-id="e8b22-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span><span class="sxs-lookup"><span data-stu-id="e8b22-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="e8b22-293">Currently displayed options have checkmarks next to each item.</span><span class="sxs-lookup"><span data-stu-id="e8b22-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="e8b22-295">Adding a column to the Requests table</span><span class="sxs-lookup"><span data-stu-id="e8b22-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8b22-296">Add custom columns</span><span class="sxs-lookup"><span data-stu-id="e8b22-296">Add custom columns</span></span>  

<span data-ttu-id="e8b22-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="e8b22-299">Adding a custom column to the Requests table</span><span class="sxs-lookup"><span data-stu-id="e8b22-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-300">View the timing relationship of requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="e8b22-301">Use the Waterfall to view the timing relationships of requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="e8b22-302">The default organization of the Waterfall uses the start time of the requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="e8b22-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span><span class="sxs-lookup"><span data-stu-id="e8b22-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="e8b22-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="e8b22-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="e8b22-306">The Waterfall column of the **Requests** pane</span><span class="sxs-lookup"><span data-stu-id="e8b22-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Network panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="e8b22-307">View a preview of a response body</span><span class="sxs-lookup"><span data-stu-id="e8b22-307">View a preview of a response body</span></span>  

<span data-ttu-id="e8b22-308">To view a preview of a response body, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-309">Select the URL of the request, under the **Name** column of the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e8b22-310">Select the **Preview** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="e8b22-311">This tab is mostly useful for viewing images.</span><span class="sxs-lookup"><span data-stu-id="e8b22-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="e8b22-313">The **Preview** tab</span><span class="sxs-lookup"><span data-stu-id="e8b22-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-314">View a response body</span><span class="sxs-lookup"><span data-stu-id="e8b22-314">View a response body</span></span>  

<span data-ttu-id="e8b22-315">To view the response body to a request, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-316">Select the URL of the request, under the **Name** column of the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e8b22-317">Select the **Response** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="e8b22-319">The **Response** tab</span><span class="sxs-lookup"><span data-stu-id="e8b22-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-320">View HTTP headers</span><span class="sxs-lookup"><span data-stu-id="e8b22-320">View HTTP headers</span></span>  

<span data-ttu-id="e8b22-321">To view HTTP header data about a request, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-322">Select the URL of the request, under the **Name** column of the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e8b22-323">Select the **Headers** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="The Network panel" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="e8b22-325">The **Headers** tab</span><span class="sxs-lookup"><span data-stu-id="e8b22-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8b22-326">View HTTP header source</span><span class="sxs-lookup"><span data-stu-id="e8b22-326">View HTTP header source</span></span>  

<span data-ttu-id="e8b22-327">By default, the Headers tab shows header names alphabetically.</span><span class="sxs-lookup"><span data-stu-id="e8b22-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="e8b22-328">To view the HTTP header names in the order received, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-329">Open the **Headers** tab for the request that interests you.</span><span class="sxs-lookup"><span data-stu-id="e8b22-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e8b22-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e8b22-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e8b22-331">Select **view source**, next to the **Request Header** or **Response Header** section.</span><span class="sxs-lookup"><span data-stu-id="e8b22-331">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="e8b22-332">View query string parameters</span><span class="sxs-lookup"><span data-stu-id="e8b22-332">View query string parameters</span></span>  

<span data-ttu-id="e8b22-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-334">Open the **Headers** tab for the request that interests you.</span><span class="sxs-lookup"><span data-stu-id="e8b22-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="e8b22-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="e8b22-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="e8b22-336">Go to the **Query String Parameters** section.</span><span class="sxs-lookup"><span data-stu-id="e8b22-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="e8b22-338">The **Query String Parameters** section</span><span class="sxs-lookup"><span data-stu-id="e8b22-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8b22-339">View query string parameters source</span><span class="sxs-lookup"><span data-stu-id="e8b22-339">View query string parameters source</span></span>  

<span data-ttu-id="e8b22-340">To view the query string parameter source of a request, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-341">Go to the Query String Parameters section.</span><span class="sxs-lookup"><span data-stu-id="e8b22-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e8b22-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e8b22-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e8b22-343">Select **view source**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-343">Select **view source**.</span></span>  

#### <span data-ttu-id="e8b22-344">View URL-encoded query string parameters</span><span class="sxs-lookup"><span data-stu-id="e8b22-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="e8b22-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-346">Go to the Query String Parameters section.</span><span class="sxs-lookup"><span data-stu-id="e8b22-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="e8b22-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="e8b22-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="e8b22-348">Select **view URL encoded**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-348">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="e8b22-349">View cookies</span><span class="sxs-lookup"><span data-stu-id="e8b22-349">View cookies</span></span>  

<span data-ttu-id="e8b22-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-351">Select the URL of the request, under the **Name** column of the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e8b22-352">Select the **Cookies** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="e8b22-354">The Cookies tab</span><span class="sxs-lookup"><span data-stu-id="e8b22-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-355">View the timing breakdown of a request</span><span class="sxs-lookup"><span data-stu-id="e8b22-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="e8b22-356">To view the timing breakdown of a request, use the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-357">Select the URL of the request, under the **Name** column of the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="e8b22-358">Select the **Timing** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="e8b22-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="e8b22-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="e8b22-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="e8b22-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="e8b22-362">The **Timing** tab</span><span class="sxs-lookup"><span data-stu-id="e8b22-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-363">More information about each of the phases.</span><span class="sxs-lookup"><span data-stu-id="e8b22-363">More information about each of the phases.</span></span>  

<span data-ttu-id="e8b22-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="e8b22-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="e8b22-365">Preview a timing breakdown</span><span class="sxs-lookup"><span data-stu-id="e8b22-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="e8b22-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="e8b22-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="e8b22-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="e8b22-369">Previewing the timing breakdown of a request</span><span class="sxs-lookup"><span data-stu-id="e8b22-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="e8b22-370">Timing breakdown phases explained</span><span class="sxs-lookup"><span data-stu-id="e8b22-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="e8b22-371">More information about each of the phases that may display in the **Timing** tab.</span><span class="sxs-lookup"><span data-stu-id="e8b22-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-372">Queueing</span><span class="sxs-lookup"><span data-stu-id="e8b22-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-373">The browser queues requests when any of the following are true.</span><span class="sxs-lookup"><span data-stu-id="e8b22-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="e8b22-374">Higher priority requests exist.</span><span class="sxs-lookup"><span data-stu-id="e8b22-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="e8b22-375">Six TCP connections are open for the same origin, which is the limit.</span><span class="sxs-lookup"><span data-stu-id="e8b22-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="e8b22-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span><span class="sxs-lookup"><span data-stu-id="e8b22-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="e8b22-377">The browser is briefly allocating space in the disk cache.</span><span class="sxs-lookup"><span data-stu-id="e8b22-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-378">Stalled</span><span class="sxs-lookup"><span data-stu-id="e8b22-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-379">The request is stalled for any of the reasons described in **Queueing**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-380">DNS Lookup</span><span class="sxs-lookup"><span data-stu-id="e8b22-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-381">The browser is resolving the IP address for the request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-382">Initial connection</span><span class="sxs-lookup"><span data-stu-id="e8b22-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span><span class="sxs-lookup"><span data-stu-id="e8b22-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-384">Proxy negotiation</span><span class="sxs-lookup"><span data-stu-id="e8b22-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="e8b22-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-386">Request sent</span><span class="sxs-lookup"><span data-stu-id="e8b22-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-387">The request is being sent.</span><span class="sxs-lookup"><span data-stu-id="e8b22-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-388">ServiceWorker Preparation</span><span class="sxs-lookup"><span data-stu-id="e8b22-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-389">The browser is starting the service worker.</span><span class="sxs-lookup"><span data-stu-id="e8b22-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-390">Request to ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="e8b22-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-391">The request is being sent to the service worker.</span><span class="sxs-lookup"><span data-stu-id="e8b22-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-392">Waiting \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="e8b22-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-393">The browser is waiting for the first byte of a response.</span><span class="sxs-lookup"><span data-stu-id="e8b22-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="e8b22-394">TTFB stands for Time To First Byte.</span><span class="sxs-lookup"><span data-stu-id="e8b22-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="e8b22-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span><span class="sxs-lookup"><span data-stu-id="e8b22-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-396">Content Download</span><span class="sxs-lookup"><span data-stu-id="e8b22-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-397">The browser is receiving the response.</span><span class="sxs-lookup"><span data-stu-id="e8b22-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-398">Receiving Push</span><span class="sxs-lookup"><span data-stu-id="e8b22-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-399">The browser is receiving data for this response via HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="e8b22-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-400">Reading Push</span><span class="sxs-lookup"><span data-stu-id="e8b22-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-401">The browser is reading the local data previously received.</span><span class="sxs-lookup"><span data-stu-id="e8b22-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="e8b22-402">View initiators and dependencies</span><span class="sxs-lookup"><span data-stu-id="e8b22-402">View initiators and dependencies</span></span>  

<span data-ttu-id="e8b22-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="e8b22-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span><span class="sxs-lookup"><span data-stu-id="e8b22-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="e8b22-406">Viewing the initiators and dependencies of a request</span><span class="sxs-lookup"><span data-stu-id="e8b22-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="e8b22-408">The green request is the initiator of the dependency.</span><span class="sxs-lookup"><span data-stu-id="e8b22-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="e8b22-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span><span class="sxs-lookup"><span data-stu-id="e8b22-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="e8b22-410">And so on.</span><span class="sxs-lookup"><span data-stu-id="e8b22-410">And so on.</span></span>  

### <span data-ttu-id="e8b22-411">View load events</span><span class="sxs-lookup"><span data-stu-id="e8b22-411">View load events</span></span>  

<span data-ttu-id="e8b22-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="e8b22-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span><span class="sxs-lookup"><span data-stu-id="e8b22-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="e8b22-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span><span class="sxs-lookup"><span data-stu-id="e8b22-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-416">View the total number of requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-416">View the total number of requests</span></span>  

<span data-ttu-id="e8b22-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e8b22-418">This number only tracks requests that have been logged since DevTools was opened.</span><span class="sxs-lookup"><span data-stu-id="e8b22-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e8b22-419">If other requests occurred before DevTools was opened, those requests are not counted.</span><span class="sxs-lookup"><span data-stu-id="e8b22-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="The Network panel" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="e8b22-421">The total number of requests since DevTools were opened</span><span class="sxs-lookup"><span data-stu-id="e8b22-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-422">View the total download size</span><span class="sxs-lookup"><span data-stu-id="e8b22-422">View the total download size</span></span>  

<span data-ttu-id="e8b22-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span><span class="sxs-lookup"><span data-stu-id="e8b22-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e8b22-424">This number only tracks requests that have been logged since DevTools was opened.</span><span class="sxs-lookup"><span data-stu-id="e8b22-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="e8b22-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span><span class="sxs-lookup"><span data-stu-id="e8b22-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="The Network panel" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="e8b22-427">The total download size of requests</span><span class="sxs-lookup"><span data-stu-id="e8b22-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="e8b22-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="e8b22-429">View the stack trace that caused a request</span><span class="sxs-lookup"><span data-stu-id="e8b22-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="e8b22-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="e8b22-432">The stack trace leading up to a resource request</span><span class="sxs-lookup"><span data-stu-id="e8b22-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-433">View the uncompressed size of a resource</span><span class="sxs-lookup"><span data-stu-id="e8b22-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="e8b22-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span><span class="sxs-lookup"><span data-stu-id="e8b22-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="e8b22-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span><span class="sxs-lookup"><span data-stu-id="e8b22-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="e8b22-437">Export requests data</span><span class="sxs-lookup"><span data-stu-id="e8b22-437">Export requests data</span></span>  

### <span data-ttu-id="e8b22-438">Save all network requests to a HAR file</span><span class="sxs-lookup"><span data-stu-id="e8b22-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="e8b22-439">To save all network requests to a HAR file, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="e8b22-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="e8b22-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span><span class="sxs-lookup"><span data-stu-id="e8b22-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e8b22-441">Select **Save as HAR with Content**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-441">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="e8b22-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span><span class="sxs-lookup"><span data-stu-id="e8b22-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="e8b22-443">You are not able to filter requests.</span><span class="sxs-lookup"><span data-stu-id="e8b22-443">You are not able to filter requests.</span></span>  <span data-ttu-id="e8b22-444">You are also not able to save a single request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="e8b22-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span><span class="sxs-lookup"><span data-stu-id="e8b22-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="e8b22-446">Just drag-and-drop the HAR file into the Requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="e8b22-448">Selecting **Save as HAR with Content**</span><span class="sxs-lookup"><span data-stu-id="e8b22-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-449">Copy one or more requests to the clipboard</span><span class="sxs-lookup"><span data-stu-id="e8b22-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="e8b22-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span><span class="sxs-lookup"><span data-stu-id="e8b22-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-451">Copy Link Address</span><span class="sxs-lookup"><span data-stu-id="e8b22-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-452">Copy the URL of the request to the clipboard.</span><span class="sxs-lookup"><span data-stu-id="e8b22-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-453">Copy Response</span><span class="sxs-lookup"><span data-stu-id="e8b22-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-454">Copy the response body to the clipboard.</span><span class="sxs-lookup"><span data-stu-id="e8b22-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-455">Copy as Fetch</span><span class="sxs-lookup"><span data-stu-id="e8b22-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-456">Copy as cURL</span><span class="sxs-lookup"><span data-stu-id="e8b22-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-457">Copy the request as a cURL command.</span><span class="sxs-lookup"><span data-stu-id="e8b22-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-458">Copy All as Fetch</span><span class="sxs-lookup"><span data-stu-id="e8b22-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-459">Copy All as cURL</span><span class="sxs-lookup"><span data-stu-id="e8b22-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-460">Copy all requests as a chain of cURL commands.</span><span class="sxs-lookup"><span data-stu-id="e8b22-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="e8b22-461">Copy All as HAR</span><span class="sxs-lookup"><span data-stu-id="e8b22-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="e8b22-462">Copy all requests as HAR data.</span><span class="sxs-lookup"><span data-stu-id="e8b22-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="e8b22-464">Selecting **Copy Response**</span><span class="sxs-lookup"><span data-stu-id="e8b22-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="e8b22-465">Change the layout of the Network panel</span><span class="sxs-lookup"><span data-stu-id="e8b22-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="e8b22-466">You may expand or collapse sections of the Network panel UI to focus important information.</span><span class="sxs-lookup"><span data-stu-id="e8b22-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="e8b22-467">Hide the Filters pane</span><span class="sxs-lookup"><span data-stu-id="e8b22-467">Hide the Filters pane</span></span>  

<span data-ttu-id="e8b22-468">By default, DevTools show the **Filters pane**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="e8b22-469">Select **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span><span class="sxs-lookup"><span data-stu-id="e8b22-469">Select **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="The Network panel" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="e8b22-471">The Hide Filters button</span><span class="sxs-lookup"><span data-stu-id="e8b22-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-472">Use large request rows</span><span class="sxs-lookup"><span data-stu-id="e8b22-472">Use large request rows</span></span>  

<span data-ttu-id="e8b22-473">Use large rows when you want more whitespace in your network requests table.</span><span class="sxs-lookup"><span data-stu-id="e8b22-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="e8b22-474">Some columns also provide a little more information when using large rows.</span><span class="sxs-lookup"><span data-stu-id="e8b22-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="e8b22-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span><span class="sxs-lookup"><span data-stu-id="e8b22-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="e8b22-477">An example of large request rows in the **Requests** pane</span><span class="sxs-lookup"><span data-stu-id="e8b22-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="e8b22-478">Select the **Use large request rows** checkbox to enable large rows.</span><span class="sxs-lookup"><span data-stu-id="e8b22-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="e8b22-480">The **Use large request rows** checkbox</span><span class="sxs-lookup"><span data-stu-id="e8b22-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="e8b22-481">Hide the Overview pane</span><span class="sxs-lookup"><span data-stu-id="e8b22-481">Hide the Overview pane</span></span>  

<span data-ttu-id="e8b22-482">By default, DevTools show the **Overview pane**.</span><span class="sxs-lookup"><span data-stu-id="e8b22-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="e8b22-483">Deselect the **Show Overview** checkbox to hide it.</span><span class="sxs-lookup"><span data-stu-id="e8b22-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="The Network panel" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="e8b22-485">The **Show Overview** checkbox</span><span class="sxs-lookup"><span data-stu-id="e8b22-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Debug Progressive Web Apps | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Data URLs | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Proxy server - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="e8b22-489">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8b22-489">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e8b22-490">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e8b22-490">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="e8b22-492">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8b22-492">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
