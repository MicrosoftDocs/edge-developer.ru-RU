---
description: Узнайте, как распространять расширения с помощью альтернативных методов, не использующих проверенные хранилища
title: Альтернативный метод распространения расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343152"
---
# <span data-ttu-id="4fca7-104">Альтернативные методы распространения расширений</span><span class="sxs-lookup"><span data-stu-id="4fca7-104">Alternate extension distribution methods</span></span>  

<span data-ttu-id="4fca7-105">Как правило, расширения распространяются через магазин надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fca7-105">Generally, extensions are distributed through the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="4fca7-106">В некоторых сценариях разработчикам может потребоваться распространять расширения с помощью альтернативных методов.</span><span class="sxs-lookup"><span data-stu-id="4fca7-106">There are some scenarios where developers may need to distribute extensions using alternate methods.</span></span> <span data-ttu-id="4fca7-107">Например:</span><span class="sxs-lookup"><span data-stu-id="4fca7-107">For example:</span></span>

1.  <span data-ttu-id="4fca7-108">Расширение связано с другим программным обеспечением и должно быть установлено вместе с остальными пакетными программами.</span><span class="sxs-lookup"><span data-stu-id="4fca7-108">The extension is associated with other software, and it should be installed together with the rest of the bundled software.</span></span>   
1.  <span data-ttu-id="4fca7-109">Сетевые администраторы хотят распространять расширение по всей организации.</span><span class="sxs-lookup"><span data-stu-id="4fca7-109">Network administrators want to distribute an extension throughout their organization.</span></span>   

<span data-ttu-id="4fca7-110">Расширения, которые не загружаются из магазина надстройки Edge, называются расширениями, установленными извне.</span><span class="sxs-lookup"><span data-stu-id="4fca7-110">Extensions that are not loaded from the Edge Add-ons store are referred to as externally installed extensions.</span></span> <span data-ttu-id="4fca7-111">Следующий список предоставляет альтернативные методы распространения внешних установленных расширений.</span><span class="sxs-lookup"><span data-stu-id="4fca7-111">The following list provides alternate methods of distributing externally installed extensions.</span></span> 

*   <span data-ttu-id="4fca7-112">Используйте реестр Windows (только для Windows).</span><span class="sxs-lookup"><span data-stu-id="4fca7-112">Use the Windows registry (Windows only).</span></span>  
*   <span data-ttu-id="4fca7-113">Используйте JSON-файл предпочтений (macOS и Linux).</span><span class="sxs-lookup"><span data-stu-id="4fca7-113">Use a preferences JSON file (macOS and Linux).</span></span>  
    
## <span data-ttu-id="4fca7-114">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="4fca7-114">Before you begin</span></span>  

<span data-ttu-id="4fca7-115">Убедитесь, что расширение опубликовано в магазине надстройки Microsoft Edge, или упакуйте файл и убедитесь, что оно успешно устанавливается `.crx` на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fca7-115">Ensure that you publish your extension in the Microsoft Edge Add-ons store, or package a `.crx` file and ensure that it installs successfully on your computer.</span></span>  <span data-ttu-id="4fca7-116">При установке файла с помощью url-адреса убедитесь, что вы можете перейти к `.crx` `update_URL` расширению по этому URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="4fca7-116">If you install the `.crx` file using the `update_URL`, ensure you can navigate to your extension at that URL.</span></span>  

<span data-ttu-id="4fca7-117">Кроме того, убедитесь, что у вас есть следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-117">Also, ensure that you have the following information.</span></span>    

1.  <span data-ttu-id="4fca7-118">Путь к файлу `.crx` или `update_URL` расширение.</span><span class="sxs-lookup"><span data-stu-id="4fca7-118">The file path of the `.crx` file, or the `update_URL` of your extension.</span></span>
1.  <span data-ttu-id="4fca7-119">Версия расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-119">The version of your extension.</span></span>  <span data-ttu-id="4fca7-120">Сведения о версии доступны в файле манифеста или в Microsoft Edge после `edge://extensions` загрузки упакованного расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-120">The version information is available in your manifest file, or in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>   
1.  <span data-ttu-id="4fca7-121">ИД расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-121">The ID of your extension.</span></span>  <span data-ttu-id="4fca7-122">Сведения об ИД доступны в Microsoft Edge после `edge://extensions` загрузки упакованного расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-122">The ID information is available in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>  

> [!NOTE] 
> <span data-ttu-id="4fca7-123">В следующих примерах `1.0` используется как версия, так `aaaaaaaaaabbbbbbbbbbcccccccccc` и для ИД.</span><span class="sxs-lookup"><span data-stu-id="4fca7-123">The following examples use `1.0` as the version, and `aaaaaaaaaabbbbbbbbbbcccccccccc` for the ID.</span></span>  

## <span data-ttu-id="4fca7-124">Использование реестра Windows (только для Windows)</span><span class="sxs-lookup"><span data-stu-id="4fca7-124">Use the Windows registry (Windows only)</span></span>  

<span data-ttu-id="4fca7-125">Чтобы распространить расширение с помощью реестра Windows, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4fca7-125">To distribute your extension using the Windows registry, perform the following steps.</span></span>

1.  <span data-ttu-id="4fca7-126">Найдите или создайте следующий ключ реестра:</span><span class="sxs-lookup"><span data-stu-id="4fca7-126">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="4fca7-127">32-битная версия Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-127">32-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`.</span></span>  
    *   <span data-ttu-id="4fca7-128">64-битная версия Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-128">64-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`.</span></span>  
1.  <span data-ttu-id="4fca7-129">Создайте новый ключ или папку в папке **Extensions** с тем же именем, что и у вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-129">Create a new key, or folder, under **Extensions** with the same name as the ID of your extension.</span></span> <span data-ttu-id="4fca7-130">Например, создайте ключ с `aaaaaaaaaabbbbbbbbbbcccccccccc` именем.</span><span class="sxs-lookup"><span data-stu-id="4fca7-130">For example, create the key with the name `aaaaaaaaaabbbbbbbbbbcccccccccc`.</span></span>  
1.  <span data-ttu-id="4fca7-131">В **ключе Extensions** создайте `update_url` свойство и установите значение `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-131">In the **Extensions** key, create the `update_url` property, and set the value to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="4fca7-132">Свойство указывает на файл расширения в магазине надстройки `update_url` `.crx` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4fca7-132">The `update_url` property points to the `.crx` file of your extension in the Microsoft Edge Add-ons store.</span></span>  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="4fca7-133">Если вы хотите установить расширение из веб-магазина Chrome, установите `update_url` значение . `https://clients2.google.com/service/update2/crx`</span><span class="sxs-lookup"><span data-stu-id="4fca7-133">If you want to install an extension from the Chrome Web Store, set the value of `update_url` to `https://clients2.google.com/service/update2/crx`.</span></span>  
  
1.  <span data-ttu-id="4fca7-134">Убедитесь, что расширение указано в Microsoft Edge. `edge://extensions`</span><span class="sxs-lookup"><span data-stu-id="4fca7-134">Verify that your extension is listed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="4fca7-135">Использование JSON-файла предпочтений (macOS и Linux)</span><span class="sxs-lookup"><span data-stu-id="4fca7-135">Use a preferences JSON file (macOS and Linux)</span></span>  

<span data-ttu-id="4fca7-136">Чтобы распространить расширение с помощью JSON-файла настроек, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4fca7-136">To distribute your extension using a preferences JSON file, perform the following steps.</span></span>

1.  <span data-ttu-id="4fca7-137">При использовании Linux убедитесь, что файл расширения доступен на компьютере, на который `.crx` будет установлено расширение.</span><span class="sxs-lookup"><span data-stu-id="4fca7-137">When using Linux, ensure your `.crx` extension file is available on the machine that the extension will be installed on.</span></span> <span data-ttu-id="4fca7-138">Скопируйте файл расширения в локальный каталог или используйте сетевую папку, достижимую `.crx` с компьютера.</span><span class="sxs-lookup"><span data-stu-id="4fca7-138">Copy the `.crx` extension file to a local directory, or use a  network share that is reachable from the machine.</span></span> 
1.  <span data-ttu-id="4fca7-139">Создайте JSON-файл, имя которого соответствует ИД расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-139">Create a JSON file where the name of the file corresponds to the ID of your extension.</span></span> <span data-ttu-id="4fca7-140">Например, создайте JSON-файл с именем `aaaaaaaaaabbbbbbbbbbcccccccccc.json` файла.</span><span class="sxs-lookup"><span data-stu-id="4fca7-140">For example, create a JSON file with the file name `aaaaaaaaaabbbbbbbbbbcccccccccc.json`.</span></span>  
1.  <span data-ttu-id="4fca7-141">В зависимости от операционной системы сохраните JSON-файл в одной из следующих папок.</span><span class="sxs-lookup"><span data-stu-id="4fca7-141">Depending on your operating system, save the JSON file to one of the following folders.</span></span>   
    *   **<span data-ttu-id="4fca7-142">macOS</span><span class="sxs-lookup"><span data-stu-id="4fca7-142">macOS</span></span>**  
        *   <span data-ttu-id="4fca7-143">Для конкретного пользователя:</span><span class="sxs-lookup"><span data-stu-id="4fca7-143">User specific:</span></span> `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   <span data-ttu-id="4fca7-144">Все пользователи:</span><span class="sxs-lookup"><span data-stu-id="4fca7-144">All users:</span></span> `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        <span data-ttu-id="4fca7-145">Чтобы запретить неавторизованной установке расширений для всех пользователей, убедитесь, что файл расширения только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-145">To prevent unauthorized users from installing extensions for all users, ensure your extension file is read only.</span></span> <span data-ttu-id="4fca7-146">Кроме того, убедитесь, что выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="4fca7-146">Additionally, ensure that the following conditions are met:</span></span>
        
        *   <span data-ttu-id="4fca7-147">Каждый каталог в пути принадлежит корню пользователя.</span><span class="sxs-lookup"><span data-stu-id="4fca7-147">Every directory in the path is owned by the user root.</span></span>  
        *   <span data-ttu-id="4fca7-148">Каждому каталогу в пути назначена группа `admin` `wheel` или каталог.</span><span class="sxs-lookup"><span data-stu-id="4fca7-148">Every directory in the path is assigned to the `admin` or `wheel` group.</span></span>  
        *   <span data-ttu-id="4fca7-149">Все каталоги в пути не могут быть переоценены в мире.</span><span class="sxs-lookup"><span data-stu-id="4fca7-149">Every directory in the path isn't world writable.</span></span>  
        *   <span data-ttu-id="4fca7-150">Путь также должен быть без символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="4fca7-150">The path must also be free of symbolic links.</span></span>  
        
    *   **<span data-ttu-id="4fca7-151">Linux</span><span class="sxs-lookup"><span data-stu-id="4fca7-151">Linux</span></span>**  
        *   <span data-ttu-id="4fca7-152">Для конкретного пользователя:</span><span class="sxs-lookup"><span data-stu-id="4fca7-152">User specific:</span></span> `~/.config/microsoft-edge/External Extensions/`  
        *   <span data-ttu-id="4fca7-153">Все пользователи:</span><span class="sxs-lookup"><span data-stu-id="4fca7-153">All users:</span></span> `/usr/share/microsoft-edge/extensions/`  
1.  <span data-ttu-id="4fca7-154">В зависимости от сценария скопируйте соответствующий код, который следует за файлом JSON.</span><span class="sxs-lookup"><span data-stu-id="4fca7-154">Depending on your scenario, copy the appropriate code that follows to your JSON file.</span></span> 
    *   <span data-ttu-id="4fca7-155">Применяется только к Linux.</span><span class="sxs-lookup"><span data-stu-id="4fca7-155">Applies to Linux only.</span></span> <span data-ttu-id="4fca7-156">При установке из файла укажите расположение и используемую версию `external_crx` и `external_version` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-156">If you install from a file, specify the location and version using `external_crx` and `external_version`.</span></span>  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   <span data-ttu-id="4fca7-157">Применимо к macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="4fca7-157">Applies to macOS and Linux.</span></span> <span data-ttu-id="4fca7-158">При установке с помощью URL-адреса обновления `update_URL` укажите `external_update_url` его.</span><span class="sxs-lookup"><span data-stu-id="4fca7-158">If you install from an `update_URL`, specify the update URL using `external_update_url`.</span></span> 
        
        <span data-ttu-id="4fca7-159">Скопируйте следующий код в файл JSON при установке только из локальных файлов `.crx` в Linux.</span><span class="sxs-lookup"><span data-stu-id="4fca7-159">Copy the following code to your JSON file when installing from local `.crx` files on Linux only.</span></span>  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  <span data-ttu-id="4fca7-160">Скопируйте следующий код в файл JSON при установке из магазина надстроек Microsoft Edge на macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="4fca7-160">Copy the following code to your JSON file when installing from the Microsoft Edge Add-ons store on macOS and Linux.</span></span>
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  <span data-ttu-id="4fca7-161">Чтобы установить расширения для определенных региональных es, перечислите поддерживаемые с помощью `supported_locale` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-161">To install extensions for specific locales, list the supported locales using `supported_locale`.</span></span>  <span data-ttu-id="4fca7-162">Вы также можете указать родительские языковые языки, чтобы установить расширение для всех языковых языков, которые используют этот родительский.</span><span class="sxs-lookup"><span data-stu-id="4fca7-162">You may also specify parent locales to install your extension for all language locales that use that parent.</span></span> <span data-ttu-id="4fca7-163">Например, при использовании родительского языка расширение устанавливается для всех английских региональных es, например `en` `en-US` , и так `en-GB` далее.</span><span class="sxs-lookup"><span data-stu-id="4fca7-163">For example, when using the parent locale `en`, your extension installs for all English locales, such as `en-US`, `en-GB`, and so on.</span></span>  <span data-ttu-id="4fca7-164">Когда пользователи изменяют свой региональный уровень в браузере, внешние установленные расширения будут установлены.</span><span class="sxs-lookup"><span data-stu-id="4fca7-164">When users change their locale in their browser, externally installed extensions are uninstalled.</span></span>  <span data-ttu-id="4fca7-165">Чтобы установить расширение для любого локаула, не используйте `supported_locales` .</span><span class="sxs-lookup"><span data-stu-id="4fca7-165">To install your extension for any locale, do not use `supported_locales`.</span></span>  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  <span data-ttu-id="4fca7-166">Убедитесь, что расширение установлено в Microsoft Edge. `edge://extensions`</span><span class="sxs-lookup"><span data-stu-id="4fca7-166">Verify that your extension is installed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="4fca7-167">Обновление и удалить расширения, установленные извне</span><span class="sxs-lookup"><span data-stu-id="4fca7-167">Update and uninstall externally installed extensions</span></span>

<span data-ttu-id="4fca7-168">Microsoft Edge сканирует записи метаданных в реестре каждый раз, когда браузер запускается, и вносит изменения во внешние расширения.</span><span class="sxs-lookup"><span data-stu-id="4fca7-168">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any changes to the externally installed extensions.</span></span>  

<span data-ttu-id="4fca7-169">Чтобы обновить расширение до новой версии, обновите версию в файле манифеста, а затем обновите версию в реестре.</span><span class="sxs-lookup"><span data-stu-id="4fca7-169">To update your extension to a new version, update the version in the manifest file, and then update the version in the registry.</span></span>  

<span data-ttu-id="4fca7-170">Возможно, потребуется удалить установленные извне расширения, которые были установлены в составе пакета программного обеспечения, ранее установленного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fca7-170">You may need to uninstall externally installed extensions, which were installed as part of a bundle of software that was previously installed on the machine.</span></span>  <span data-ttu-id="4fca7-171">Чтобы удалить расширение, удалите JSON-файл настроек или удалите ключ из реестра.</span><span class="sxs-lookup"><span data-stu-id="4fca7-171">To uninstall your extension, remove your preferences JSON file or remove the key from the registry.</span></span>   

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="4fca7-172">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4fca7-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  <span data-ttu-id="4fca7-173">Здесь находится исходная [страница.](https://developer.chrome.com/apps/external_extensions)</span><span class="sxs-lookup"><span data-stu-id="4fca7-173">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4fca7-175">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4fca7-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
