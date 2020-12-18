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
# Рекомендации по проектированию расширений Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

На следующей странице представлены различные аспекты проектирования и поведение пользовательского интерфейса, которые следует учитывать при создании расширений Microsoft Edge.  

## Значки  

Значки расширения следует делать с помощью векторной графики.  Чтобы упаковить расширение, необходимо создать несколько разных размеров значка для расширения и три дополнительных размера.  Расширения Microsoft Edge не поддерживают значки SVG.  

Перед созданием значков расширений [][ExtensionsGuidesAccessibility] просмотрите руководство по специальным возможности, чтобы убедиться, что ваши значки имеют достаточно высокую контрастность и отображаются как в светлых, так и в темных темах Microsoft Edge.  

Несмотря на то что любой формат изображения webkit поддерживается, значки PNG рекомендуется использовать для поддержки прозрачности.  

### Значки для расширения  

Для расширения необходимо создать один размер значка для действия браузера или действия страницы и один размер значка для области **расширений.**  Для поддержки дисплеев с высоким разрешением может быть предоставлено несколько размеров.  

Расширение должно иметь действие браузера или значок действия страницы.  Значки действий браузера и действия страницы можно изменить во время работы с помощью метода [browserAction.setIcon][MSDApiBrowseractionSeticon] или [pageAction.setIcon.][MDNApiPageactionSeticon]  

#### Действие браузера  

Предпочтительными размерами для значков действий браузера и действий страницы являются `20px` `25px` , , и `30px` `40px` .  Другие поддерживаемые размеры: `19px` `35px` , и `38px` .  

В следующем [manifest.jsфрагменте][ExtensionsApisupportManifestkeys] файла показан стандартный значок действия браузера высокой [четкости,][MDNManifestjsonBrowserAction] заданный с помощью browser_action ключа.  Тот же синтаксис применяется для [page_action][MDNManifestjsonPageAction] ключа.  

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

Если действие браузера настроено расширением, оно отображается в меню "Действия" после выбора кнопки "Больше(...) или справа от адресной панели, если пользователь переглушил кнопку "Показать" рядом с адресной панели. **** ****  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Действие браузера в меню действий":::
         Действие браузера в меню действий :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Действие браузера":::
         Действие браузера :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Действие "Страница"  

Ключ [page_action][MDNManifestjsonPageAction] имеет тот же синтаксис манифеста JSON, [что и][MDNManifestjsonBrowserAction] browser_action ключа.  Действие страницы также имеет те же требования к размеру значка, что и действие браузера.  

Если действие страницы указано вmanifest.js[в][ExtensionsApisupportManifestkeys] файле, оно отображается в адресной панели каждый раз, когда используется метод [pageAction.show.][MDNApiPageactionShow]  

:::image type="complex" source="../media/pageaction.png" alt-text="Действие "Страница"":::
   Действие "Страница"
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Пользовательский интерфейс управления  

Когда пользователи переходят в области расширений, переходя в **** меню **"Подробнее(...)** и выбрав "Расширения", рядом с именем расширения отображается значок.  

Необходимо указать следующие размеры значков.  

| Раздел | Сведения |  
|:--- |:--- |  
| `48px` | Значок для отображения стандартного разрешения. |  
| `128px` | Значок для отображения с высоким разрешением. |  
| `176px` | Значок для отображения еще более высокого разрешения. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Пользовательский интерфейс управления":::
   Пользовательский интерфейс управления
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Значки для упаковки  

Когда расширение будет готово к упаковке, необходимо иметь три дополнительных размера значка.  

| Size | Сведения |  
|:--- |:--- |  
| 44px | Используется в пользовательском интерфейсе Windows **** \(**Список приложений,** системные  \>  ****  \>  **& параметров**\). |  
| 50px | Требование упаковки \(не отображается в любом месте\). |  
| 150px | Используется в качестве значка для Microsoft Store. |  


Чтобы [определить,][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] где находятся эти значки, см. руководство по упаковке вручную или [manifoldJS.][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]  Это зависит от того, какой метод упаковки вы выбрали.  

#### Значок Microsoft Store  

Если значок Размером 150px для Microsoft Store имеет прозрачный фон, цвет акцента устройства пользователя отображается в качестве фонового цвета значка.  

Например, если пользователь выбрал красный цвет в качестве цвета акцента, прозрачный фон значка магазина отображается как желтый.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Цвет акцентов Windows":::
          Цвет акцентов Windows :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Автоматически выбранный цвет фона":::
         Автоматически выбранный цвет фона :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Если вы хотите выбрать собственный цвет фона для Microsoft Store, необходимо сделать фон непрозрачной.  

> [!NOTE]
> Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.  [Обратитесь][AkaExtensionRequest] к нам с запросами на Microsoft Store, и ваш запрос рассматривается на будущее обновление.  

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
