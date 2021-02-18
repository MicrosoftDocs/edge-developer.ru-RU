---
description: Процесс переноса расширения Chrome в Microsoft Edge
title: Перенос расширения Chrome в Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343138"
---
# <span data-ttu-id="e4037-104">Перенос расширения</span><span class="sxs-lookup"><span data-stu-id="e4037-104">Port your extension</span></span>  

<span data-ttu-id="e4037-105">Microsoft Edge позволяет переносить расширение Chrome с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="e4037-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="e4037-106">API расширения и ключи манифеста, поддерживаемые Chrome, совместимы с Кодом и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e4037-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="e4037-107">Список API, поддерживаемых Microsoft Edge, можно найти в [службе поддержки API.][ExtensionApiSupport]</span><span class="sxs-lookup"><span data-stu-id="e4037-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="e4037-108">Чтобы выполнить перенос расширения Chrome, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e4037-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="e4037-109">Просмотрите API расширений Chrome, используемые в ваших расширениях, в списке поддерживаемых [API][ExtensionApiSupport] расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e4037-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e4037-110">Если расширение использует API, не поддерживаемые Microsoft Edge, оно может не переносим напрямую.</span><span class="sxs-lookup"><span data-stu-id="e4037-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="e4037-111">В файле манифеста за установите `update_URL` для поля `https://edge.microsoft.com/extensionwebstorebase/v1/crx` ".</span><span class="sxs-lookup"><span data-stu-id="e4037-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="e4037-112">Значение указывает на файл расширения в магазине надстройки Microsoft Edge и позволяет Microsoft Edge проверять обновления `.crx` расширений.</span><span class="sxs-lookup"><span data-stu-id="e4037-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="e4037-113">Если используется в имени или описании расширения, повторно задайте для расширения `Chrome` `Microsoft Edge` название.</span><span class="sxs-lookup"><span data-stu-id="e4037-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="e4037-114">Чтобы пройти процесс сертификации, необходимо внести изменения.</span><span class="sxs-lookup"><span data-stu-id="e4037-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="e4037-115">Проверьте расширение, чтобы проверить, работает ли оно в Microsoft Edge, [выгрузив расширение нео][ExtensionsGettingStartedExtensionSideloading]том же.</span><span class="sxs-lookup"><span data-stu-id="e4037-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="e4037-116">Если у вас возникнут проблемы, вы можете отладить расширения в Microsoft Edge с помощью DevTools или связаться [с нами.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="e4037-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="e4037-117">Следуйте [рекомендациям по публикации,][ExtensionsPublishPublishExtension] чтобы опубликовать расширение в магазине надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e4037-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e4037-118">Если расширение обменивается сообщениями с использованием вашего приложения, убедитесь, что вы установили его в файле манифеста ведущего приложения для обмена `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e4037-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="e4037-119">Этот параметр позволяет приложению идентифицировать расширение.</span><span class="sxs-lookup"><span data-stu-id="e4037-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="e4037-120">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e4037-120">Next steps</span></span>  

<span data-ttu-id="e4037-121">После того как пакет расширения будет готов к публикации в магазине надстройки Microsoft [Edge,][ExtensionsPublishCreateDevAccount] создайте учетную запись разработчика и [опубликуйте расширение.][ExtensionsPublishPublishExtension]</span><span class="sxs-lookup"><span data-stu-id="e4037-121">After your extension package is ready to publish in the Microsoft Edge Add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Поддержка API | Документы Майкрософт"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Загрузка нео sideload расширения | Документы Майкрософт"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Регистрация разработчиков | Документы Майкрософт"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Опубликуйте расширение | Документы Майкрософт"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовая оплата | Разработчик Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
