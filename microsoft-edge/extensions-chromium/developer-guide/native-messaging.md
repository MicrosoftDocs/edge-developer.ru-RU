---
description: Native messaging documentation
title: Native Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, extensions development, browser extensions, addons, partner center, developer
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100254"
---
# <span data-ttu-id="22ed8-104">Native messaging</span><span class="sxs-lookup"><span data-stu-id="22ed8-104">Native messaging</span></span>  

<span data-ttu-id="22ed8-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span><span class="sxs-lookup"><span data-stu-id="22ed8-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="22ed8-106">The native application host sends and receives messages with extensions using standard input and standard output.</span><span class="sxs-lookup"><span data-stu-id="22ed8-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="22ed8-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span><span class="sxs-lookup"><span data-stu-id="22ed8-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="22ed8-108">However, native applications are not installed or managed by Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22ed8-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="22ed8-109">To acquire the extension and native application host, you have two distribution models.</span><span class="sxs-lookup"><span data-stu-id="22ed8-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="22ed8-110">Package your extension and the host together.</span><span class="sxs-lookup"><span data-stu-id="22ed8-110">Package your extension and the host together.</span></span>  <span data-ttu-id="22ed8-111">When a user installs the package, both the extension and the host are installed.</span><span class="sxs-lookup"><span data-stu-id="22ed8-111">When a user installs the package, both the extension and the host are installed.</span></span>
*   <span data-ttu-id="22ed8-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="22ed8-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span><span class="sxs-lookup"><span data-stu-id="22ed8-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="22ed8-114">Step 1 - Add permissions to the extension manifest</span><span class="sxs-lookup"><span data-stu-id="22ed8-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="22ed8-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span><span class="sxs-lookup"><span data-stu-id="22ed8-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="22ed8-116">The following code snippet is an example of **manifest.json**.</span><span class="sxs-lookup"><span data-stu-id="22ed8-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```  

## <span data-ttu-id="22ed8-117">Step 2 - Create your native messaging host manifest file</span><span class="sxs-lookup"><span data-stu-id="22ed8-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="22ed8-118">Native applications must provide a native messaging host manifest file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="22ed8-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span><span class="sxs-lookup"><span data-stu-id="22ed8-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span></span>  <span data-ttu-id="22ed8-120">The browser reads and validates the native messaging host manifest.</span><span class="sxs-lookup"><span data-stu-id="22ed8-120">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="22ed8-121">The browser does not install or manage the native messaging host manifest file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-121">The browser does not install or manage the native messaging host manifest file.</span></span>  

```json
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
```  

<span data-ttu-id="22ed8-122">The host manifest file must be a valid JSON file that contains the following keys.</span><span class="sxs-lookup"><span data-stu-id="22ed8-122">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="22ed8-123">Specifies the name of the native messaging host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-123">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="22ed8-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span><span class="sxs-lookup"><span data-stu-id="22ed8-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="22ed8-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span><span class="sxs-lookup"><span data-stu-id="22ed8-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="22ed8-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span><span class="sxs-lookup"><span data-stu-id="22ed8-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="22ed8-127">Describes the application.</span><span class="sxs-lookup"><span data-stu-id="22ed8-127">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="22ed8-128">Specifies the path to the native messaging host binary.</span><span class="sxs-lookup"><span data-stu-id="22ed8-128">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="22ed8-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="22ed8-130">On macOS and Linux, the path must be absolute.</span><span class="sxs-lookup"><span data-stu-id="22ed8-130">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="22ed8-131">The host process starts with the current directory set to the directory that contains the host binary.</span><span class="sxs-lookup"><span data-stu-id="22ed8-131">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="22ed8-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span><span class="sxs-lookup"><span data-stu-id="22ed8-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="22ed8-133">Specifies the type of the interface used to communicate with the native messaging host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-133">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="22ed8-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="22ed8-135">The only acceptable value is `stdio`.</span><span class="sxs-lookup"><span data-stu-id="22ed8-135">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="22ed8-136">Specifies the list of extensions that have access to the native messaging host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-136">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="22ed8-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span><span class="sxs-lookup"><span data-stu-id="22ed8-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="22ed8-138">Sideload your extension to test native messaging with the host.</span><span class="sxs-lookup"><span data-stu-id="22ed8-138">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="22ed8-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span><span class="sxs-lookup"><span data-stu-id="22ed8-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="22ed8-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span><span class="sxs-lookup"><span data-stu-id="22ed8-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="22ed8-141">Choose **Load unpacked**, and then select your extension package to sideload.</span><span class="sxs-lookup"><span data-stu-id="22ed8-141">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="22ed8-142">Choose **OK**.</span><span class="sxs-lookup"><span data-stu-id="22ed8-142">Choose **OK**.</span></span>
1.  <span data-ttu-id="22ed8-143">Navigate to `edge://extensions` page and verify your extension is listed.</span><span class="sxs-lookup"><span data-stu-id="22ed8-143">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="22ed8-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span><span class="sxs-lookup"><span data-stu-id="22ed8-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>

<span data-ttu-id="22ed8-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span><span class="sxs-lookup"><span data-stu-id="22ed8-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="22ed8-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span><span class="sxs-lookup"><span data-stu-id="22ed8-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="22ed8-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span><span class="sxs-lookup"><span data-stu-id="22ed8-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="22ed8-148">Step 3 - Copy the native messaging host manifest file to your system</span><span class="sxs-lookup"><span data-stu-id="22ed8-148">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="22ed8-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span><span class="sxs-lookup"><span data-stu-id="22ed8-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span></span>  <span data-ttu-id="22ed8-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span><span class="sxs-lookup"><span data-stu-id="22ed8-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="22ed8-151">The location varies by platform.</span><span class="sxs-lookup"><span data-stu-id="22ed8-151">The location varies by platform.</span></span>  

### [<span data-ttu-id="22ed8-152">Windows</span><span class="sxs-lookup"><span data-stu-id="22ed8-152">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="22ed8-153">The manifest file may be located anywhere in the file system.</span><span class="sxs-lookup"><span data-stu-id="22ed8-153">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="22ed8-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="22ed8-155">The following commands are examples of registry keys.</span><span class="sxs-lookup"><span data-stu-id="22ed8-155">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="22ed8-156">To add a registry key to the directory with the manifest key.</span><span class="sxs-lookup"><span data-stu-id="22ed8-156">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="22ed8-157">Run command in command prompt.</span><span class="sxs-lookup"><span data-stu-id="22ed8-157">Run command in command prompt.</span></span>    
    
    1.  <span data-ttu-id="22ed8-158">Run the following command.</span><span class="sxs-lookup"><span data-stu-id="22ed8-158">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="22ed8-159">Create a `.reg` file and run it.</span><span class="sxs-lookup"><span data-stu-id="22ed8-159">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="22ed8-160">Copy the following command into a `.reg` file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-160">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="22ed8-161">Run the `.reg` file.</span><span class="sxs-lookup"><span data-stu-id="22ed8-161">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="22ed8-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span><span class="sxs-lookup"><span data-stu-id="22ed8-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span>  <span data-ttu-id="22ed8-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span><span class="sxs-lookup"><span data-stu-id="22ed8-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="22ed8-164">macOS</span><span class="sxs-lookup"><span data-stu-id="22ed8-164">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="22ed8-165">To store the manifest file, complete one of the following actions.</span><span class="sxs-lookup"><span data-stu-id="22ed8-165">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="22ed8-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="22ed8-167">For example, the manifest file must be stored in following location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-167">For example, the manifest file must be stored in following location.</span></span> 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="22ed8-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span><span class="sxs-lookup"><span data-stu-id="22ed8-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="22ed8-169">For example, the manifest file must be stored in following location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-169">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="22ed8-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span><span class="sxs-lookup"><span data-stu-id="22ed8-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="22ed8-171">Canary</span><span class="sxs-lookup"><span data-stu-id="22ed8-171">Canary</span></span>  
    *   <span data-ttu-id="22ed8-172">Dev</span><span class="sxs-lookup"><span data-stu-id="22ed8-172">Dev</span></span>  
    *   <span data-ttu-id="22ed8-173">Beta</span><span class="sxs-lookup"><span data-stu-id="22ed8-173">Beta</span></span>  

    <span data-ttu-id="22ed8-174">When using the Stable channel, `{Channel_Name}` is not required.</span><span class="sxs-lookup"><span data-stu-id="22ed8-174">When using the Stable channel, `{Channel_Name}` is not required.</span></span>  

### [<span data-ttu-id="22ed8-175">Linux</span><span class="sxs-lookup"><span data-stu-id="22ed8-175">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="22ed8-176">To store the manifest file, complete one of the following actions.</span><span class="sxs-lookup"><span data-stu-id="22ed8-176">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="22ed8-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="22ed8-178">The manifest file must be stored in following location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-178">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="22ed8-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span><span class="sxs-lookup"><span data-stu-id="22ed8-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="22ed8-180">The manifest file must be stored in following location.</span><span class="sxs-lookup"><span data-stu-id="22ed8-180">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="22ed8-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span><span class="sxs-lookup"><span data-stu-id="22ed8-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="22ed8-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22ed8-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="22ed8-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="22ed8-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="22ed8-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22ed8-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge Add-ons"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
