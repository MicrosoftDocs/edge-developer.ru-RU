---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Если вы поставщик поиска, посмотрите, как убедиться, что Microsoft Edge поддерживает вашу службу.
title: Обнаружение поставщика поиска — руководство разработчика
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb21182e910cb91658dd4fb204f7f7783843f447
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235793"
---
# <span data-ttu-id="e1498-104">Обнаружение службы поиска</span><span class="sxs-lookup"><span data-stu-id="e1498-104">Search provider discovery</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e1498-105">Интеграция с богатым поиском встроена в адресную планку Microsoft Edge, включая предложения поиска, результаты из Интернета, историю браузера и избранное.</span><span class="sxs-lookup"><span data-stu-id="e1498-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="e1498-106">Microsoft Edge следует спецификации [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) для обнаружения и использования поставщиков веб-поиска.</span><span class="sxs-lookup"><span data-stu-id="e1498-106">Microsoft Edge follows the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification to discover and use web search providers.</span></span>  <span data-ttu-id="e1498-107">Если вы поставщик поиска, вот как убедиться, что Microsoft Edge поддерживает вашу службу.</span><span class="sxs-lookup"><span data-stu-id="e1498-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e1498-108">Для обеспечения безопасности и конфиденциальности пользователей Microsoft Edge требует, чтобы все поисковые запросы проводились по SSL.</span><span class="sxs-lookup"><span data-stu-id="e1498-108">For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>  

<span data-ttu-id="e1498-109">Чтобы включить интеграцию Microsoft Edge поисковой системы с поисковой системы, в качестве URL-адресов должны быть указаны `https` следующие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="e1498-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>  

*   <span data-ttu-id="e1498-110">Сайт, содержащий ссылку на документ описания</span><span class="sxs-lookup"><span data-stu-id="e1498-110">The site that contains the reference to the description document</span></span>  
*   <span data-ttu-id="e1498-111">URL-адрес самого документа описания</span><span class="sxs-lookup"><span data-stu-id="e1498-111">The URL to the description document itself</span></span>  
*   <span data-ttu-id="e1498-112">Шаблон поискового запроса</span><span class="sxs-lookup"><span data-stu-id="e1498-112">The search query template</span></span>  
    
1.  <span data-ttu-id="e1498-113">Предо OpenSearch, который содержит имя поставщика поиска, и шаблон, который будет применяться для создания поиска.</span><span class="sxs-lookup"><span data-stu-id="e1498-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span>  <span data-ttu-id="e1498-114">Вот пример документа:</span><span class="sxs-lookup"><span data-stu-id="e1498-114">Here is an example document:</span></span>  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  <span data-ttu-id="e1498-115">Включите ссылку на файл описания OpenSearch в разделе "Загон" страниц (обычно это будет домашняя страница сайта и страницы результатов поиска), например:</span><span class="sxs-lookup"><span data-stu-id="e1498-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>  
    
    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```  
    
<span data-ttu-id="e1498-116">Когда пользователь перейдите в службу поиска, OpenSearch описание будет автоматически сохранено и сохранено для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="e1498-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span>  <span data-ttu-id="e1498-117">После этого пользователь сможет перейти к настройкам Microsoft Edge и добавить службу поиска в свой список поставщиков поиска для адресной панели Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e1498-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>  

<span data-ttu-id="e1498-118">Дополнительные сведения о создании OpenSearch описания см. в спецификации [OpenSearch OpenSearch 1.1.](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md)</span><span class="sxs-lookup"><span data-stu-id="e1498-118">See the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification for further details on creating your OpenSearch description document.</span></span>  
