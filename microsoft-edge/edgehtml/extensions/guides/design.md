---
description: Узнайте о различных аспектах проектирования и поведении пользовательского интерфейса, которые следует учитывать при создании расширений Microsoft Edge.
title: Расширения — проектирование
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, javascript, проектирование, значки, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235733"
---
# <span data-ttu-id="2995b-104">Рекомендации по проектированию расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2995b-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="2995b-105">На следующей странице представлены различные аспекты проектирования и поведение пользовательского интерфейса, которые следует учитывать при создании расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2995b-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="2995b-106">Значки</span><span class="sxs-lookup"><span data-stu-id="2995b-106">Icons</span></span>  

<span data-ttu-id="2995b-107">Значки расширения следует делать с помощью векторной графики.</span><span class="sxs-lookup"><span data-stu-id="2995b-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="2995b-108">Чтобы упаковить расширение, необходимо создать несколько разных размеров значка для расширения и три дополнительных размера.</span><span class="sxs-lookup"><span data-stu-id="2995b-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="2995b-109">Расширения Microsoft Edge не поддерживают значки SVG.</span><span class="sxs-lookup"><span data-stu-id="2995b-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="2995b-110">Перед созданием значков расширений [][ExtensionsGuidesAccessibility] просмотрите руководство по специальным возможности, чтобы убедиться, что ваши значки имеют достаточно высокую контрастность и отображаются как в светлых, так и в темных темах Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2995b-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="2995b-111">Несмотря на то что любой формат изображения webkit поддерживается, значки PNG рекомендуется использовать для поддержки прозрачности.</span><span class="sxs-lookup"><span data-stu-id="2995b-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="2995b-112">Значки для расширения</span><span class="sxs-lookup"><span data-stu-id="2995b-112">Icons for your extension</span></span>  

<span data-ttu-id="2995b-113">Для расширения необходимо создать один размер значка для действия браузера или действия страницы и один размер значка для области **расширений.**</span><span class="sxs-lookup"><span data-stu-id="2995b-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="2995b-114">Для поддержки дисплеев с высоким разрешением может быть предоставлено несколько размеров.</span><span class="sxs-lookup"><span data-stu-id="2995b-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="2995b-115">Расширение должно иметь действие браузера или значок действия страницы.</span><span class="sxs-lookup"><span data-stu-id="2995b-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="2995b-116">Значки действий браузера и действия страницы можно изменить во время работы с помощью метода [browserAction.setIcon][MSDApiBrowseractionSeticon] или [pageAction.setIcon.][MDNApiPageactionSeticon]</span><span class="sxs-lookup"><span data-stu-id="2995b-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="2995b-117">Действие браузера</span><span class="sxs-lookup"><span data-stu-id="2995b-117">Browser action</span></span>  

<span data-ttu-id="2995b-118">Предпочтительными размерами для значков действий браузера и действий страницы являются `20px` `25px` , , и `30px` `40px` .</span><span class="sxs-lookup"><span data-stu-id="2995b-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="2995b-119">Другие поддерживаемые размеры: `19px` `35px` , и `38px` .</span><span class="sxs-lookup"><span data-stu-id="2995b-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="2995b-120">В следующем [manifest.jsфрагменте][ExtensionsApisupportManifestkeys] файла показан стандартный значок действия браузера высокой [четкости,][MDNManifestjsonBrowserAction] заданный с помощью browser_action ключа.</span><span class="sxs-lookup"><span data-stu-id="2995b-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="2995b-121">Тот же синтаксис применяется для [page_action][MDNManifestjsonPageAction] ключа.</span><span class="sxs-lookup"><span data-stu-id="2995b-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

<span data-ttu-id="2995b-122">Если действие браузера настроено расширением, оно отображается в меню "Действия" после выбора кнопки "Больше(...) или справа от адресной панели, если пользователь переглушил кнопку "Показать" рядом с адресной панели. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2995b-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Действие браузера в меню действий":::
         <span data-ttu-id="2995b-124">Действие браузера в меню действий</span><span class="sxs-lookup"><span data-stu-id="2995b-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Действие браузера":::
         <span data-ttu-id="2995b-126">Действие браузера</span><span class="sxs-lookup"><span data-stu-id="2995b-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="2995b-127">Действие "Страница"</span><span class="sxs-lookup"><span data-stu-id="2995b-127">Page action</span></span>  

<span data-ttu-id="2995b-128">Ключ [page_action][MDNManifestjsonPageAction] имеет тот же синтаксис манифеста JSON, [что и][MDNManifestjsonBrowserAction] browser_action ключа.</span><span class="sxs-lookup"><span data-stu-id="2995b-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="2995b-129">Действие страницы также имеет те же требования к размеру значка, что и действие браузера.</span><span class="sxs-lookup"><span data-stu-id="2995b-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="2995b-130">Если действие страницы указано вmanifest.js[в][ExtensionsApisupportManifestkeys] файле, оно отображается в адресной панели каждый раз, когда используется метод [pageAction.show.][MDNApiPageactionShow]</span><span class="sxs-lookup"><span data-stu-id="2995b-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Действие "Страница"":::
   <span data-ttu-id="2995b-132">Действие "Страница"</span><span class="sxs-lookup"><span data-stu-id="2995b-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="2995b-133">Пользовательский интерфейс управления</span><span class="sxs-lookup"><span data-stu-id="2995b-133">Management UI</span></span>  

<span data-ttu-id="2995b-134">Когда пользователи переходят в области расширений, переходя в \*\*\*\* меню **"Подробнее(...)** и выбрав "Расширения", рядом с именем расширения отображается значок.</span><span class="sxs-lookup"><span data-stu-id="2995b-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="2995b-135">Необходимо указать следующие размеры значков.</span><span class="sxs-lookup"><span data-stu-id="2995b-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="2995b-136">Раздел</span><span class="sxs-lookup"><span data-stu-id="2995b-136">Key</span></span> | <span data-ttu-id="2995b-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="2995b-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="2995b-138">Значок для отображения стандартного разрешения.</span><span class="sxs-lookup"><span data-stu-id="2995b-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="2995b-139">Значок для отображения с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="2995b-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="2995b-140">Значок для отображения еще более высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2995b-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Пользовательский интерфейс управления":::
   <span data-ttu-id="2995b-142">Пользовательский интерфейс управления</span><span class="sxs-lookup"><span data-stu-id="2995b-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="2995b-143">Значки для упаковки</span><span class="sxs-lookup"><span data-stu-id="2995b-143">Icons for packaging</span></span>  

<span data-ttu-id="2995b-144">Когда расширение будет готово к упаковке, необходимо иметь три дополнительных размера значка.</span><span class="sxs-lookup"><span data-stu-id="2995b-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="2995b-145">Size</span><span class="sxs-lookup"><span data-stu-id="2995b-145">Size</span></span> | <span data-ttu-id="2995b-146">Сведения</span><span class="sxs-lookup"><span data-stu-id="2995b-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2995b-147">44px</span><span class="sxs-lookup"><span data-stu-id="2995b-147">44px</span></span> | <span data-ttu-id="2995b-148">Используется в пользовательском интерфейсе Windows \*\*\*\* \(**Список приложений,** системные  \>  \*\*\*\*  \>  **& параметров**\).</span><span class="sxs-lookup"><span data-stu-id="2995b-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="2995b-149">50px</span><span class="sxs-lookup"><span data-stu-id="2995b-149">50px</span></span> | <span data-ttu-id="2995b-150">Требование упаковки \(не отображается в любом месте\).</span><span class="sxs-lookup"><span data-stu-id="2995b-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="2995b-151">150px</span><span class="sxs-lookup"><span data-stu-id="2995b-151">150px</span></span> | <span data-ttu-id="2995b-152">Используется в качестве значка для Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2995b-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="2995b-153">Чтобы [определить,][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] где находятся эти значки, см. руководство по упаковке вручную или [manifoldJS.][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]</span><span class="sxs-lookup"><span data-stu-id="2995b-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="2995b-154">Это зависит от того, какой метод упаковки вы выбрали.</span><span class="sxs-lookup"><span data-stu-id="2995b-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="2995b-155">Значок Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2995b-155">Microsoft Store icon</span></span>  

<span data-ttu-id="2995b-156">Если значок Размером 150px для Microsoft Store имеет прозрачный фон, цвет акцента устройства пользователя отображается в качестве фонового цвета значка.</span><span class="sxs-lookup"><span data-stu-id="2995b-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="2995b-157">Например, если пользователь выбрал красный цвет в качестве цвета акцента, прозрачный фон значка магазина отображается как желтый.</span><span class="sxs-lookup"><span data-stu-id="2995b-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Цвет акцентов Windows":::
          <span data-ttu-id="2995b-159">Цвет акцентов Windows</span><span class="sxs-lookup"><span data-stu-id="2995b-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Автоматически выбранный цвет фона":::
         <span data-ttu-id="2995b-161">Автоматически выбранный цвет фона</span><span class="sxs-lookup"><span data-stu-id="2995b-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="2995b-162">Если вы хотите выбрать собственный цвет фона для Microsoft Store, необходимо сделать фон непрозрачной.</span><span class="sxs-lookup"><span data-stu-id="2995b-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="2995b-163">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="2995b-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="2995b-164">[Обратитесь][AkaExtensionRequest] к нам с запросами на Microsoft Store, и ваш запрос рассматривается на будущее обновление.</span><span class="sxs-lookup"><span data-stu-id="2995b-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Accessibility | Документы Майкрософт"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Папка Assets — создание и тестирование пакета AppX расширения Microsoft Edge | Документы Майкрософт"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Упаковка с помощью ManifoldJS — использование ManifoldJS для создания пакетов Extension AppX | Документы Майкрософт"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Поддерживаемые ключи манифеста | Документы Майкрософт"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Связаться с нами"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction.setIcon() — API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pageAction.setIcon() — API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pageAction.show() — API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action — manifest.js| MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action — manifest.js| MDN"  
