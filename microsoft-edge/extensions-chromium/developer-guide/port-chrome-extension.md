---
description: Процесс переноса расширения Chrome на Microsoft Edge.
title: Расширение Chrome для порта в Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195161"
---
# <span data-ttu-id="19dc1-104">Перенос расширения</span><span class="sxs-lookup"><span data-stu-id="19dc1-104">Port your extension</span></span>  

<span data-ttu-id="19dc1-105">Microsoft EDGE позволяет переносить расширение Chrome с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="19dc1-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="19dc1-106">API расширения и ключи манифестов, поддерживаемые хромом, совместимы с кодом Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="19dc1-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="19dc1-107">Список API-интерфейсов, поддерживаемых Microsoft EDGE, можно найти в разделе [Поддержка API][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="19dc1-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="19dc1-108">Чтобы перенести расширение Chrome, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19dc1-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="19dc1-109">Изучите API расширения Chrome, используемые в расширениях, с помощью списка [поддерживаемых интерфейсов API][ExtensionApiSupport] расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="19dc1-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="19dc1-110">Если расширение использует API, которые не поддерживаются Microsoft EDGE, он может не переноситься напрямую.</span><span class="sxs-lookup"><span data-stu-id="19dc1-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="19dc1-111">Если имя `Chrome` используется либо в имени, либо в описании расширения, измените расширение `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="19dc1-111">If the name `Chrome` is being used in either the name or the description of the extension, rebrand the extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="19dc1-112">Этот этап необходим для передачи процесса сертификации.</span><span class="sxs-lookup"><span data-stu-id="19dc1-112">This step is required to pass the certification process.</span></span>  
1.  <span data-ttu-id="19dc1-113">Протестируйте расширение, чтобы убедиться в том, что он работает в Microsoft EDGE, с помощью [неопубликованных приложений][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="19dc1-113">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="19dc1-114">Если вы сталкиваетесь с проблемами, вы можете выполнить отладку расширений в Microsoft Edge с помощью DevTools или [обратиться к нам][mailtoExtensionMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="19dc1-114">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="19dc1-115">Следуйте [рекомендациям по публикации][ExtensionsPublishPublishExtension] , чтобы опубликовать расширение в магазине надстроек Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="19dc1-115">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="19dc1-116">Если расширение обменивается сообщениями с собственным приложением с помощью `chrome.runtime.connectNative` API, убедитесь в том, что вы установили `allowed_origins` для `extension://[Microsoft-Catalog-extensionID]` собственного файла манифеста узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="19dc1-116">If the extension exchanges messages with a native app using `chrome.runtime.connectNative` API, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="19dc1-117">Это позволяет приложению идентифицировать расширение.</span><span class="sxs-lookup"><span data-stu-id="19dc1-117">This enables the app to identify the extension.</span></span>  
    
## <span data-ttu-id="19dc1-118">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="19dc1-118">Next steps</span></span>  

<span data-ttu-id="19dc1-119">После того как пакет расширения будет готов к публикации в магазине надстроек Microsoft EDGE, [Создайте учетную запись разработчика][ExtensionsPublishCreateDevAccount] и [опубликуйте расширение][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="19dc1-119">Once your extension package is ready to be published to Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Поддержка API | Документы Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Неопубликованного расширение | Документы Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Регистрация для разработчиков | Документы Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Опубликовать расширение | Документы Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовые платежи | Разработчик Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
