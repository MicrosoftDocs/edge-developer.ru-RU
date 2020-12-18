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
# Обнаружение службы поиска  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Интеграция с богатым поиском встроена в адресную планку Microsoft Edge, включая предложения поиска, результаты из Интернета, историю браузера и избранное.  Microsoft Edge следует спецификации [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) для обнаружения и использования поставщиков веб-поиска.  Если вы поставщик поиска, вот как убедиться, что Microsoft Edge поддерживает вашу службу.  

> [!IMPORTANT]
> Для обеспечения безопасности и конфиденциальности пользователей Microsoft Edge требует, чтобы все поисковые запросы проводились по SSL.  

Чтобы включить интеграцию Microsoft Edge поисковой системы с поисковой системы, в качестве URL-адресов должны быть указаны `https` следующие ресурсы:  

*   Сайт, содержащий ссылку на документ описания  
*   URL-адрес самого документа описания  
*   Шаблон поискового запроса  
    
1.  Предо OpenSearch, который содержит имя поставщика поиска, и шаблон, который будет применяться для создания поиска.  Вот пример документа:  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  Включите ссылку на файл описания OpenSearch в разделе "Загон" страниц (обычно это будет домашняя страница сайта и страницы результатов поиска), например:  
    
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
    
Когда пользователь перейдите в службу поиска, OpenSearch описание будет автоматически сохранено и сохранено для использования в дальнейшем.  После этого пользователь сможет перейти к настройкам Microsoft Edge и добавить службу поиска в свой список поставщиков поиска для адресной панели Microsoft Edge.  

Дополнительные сведения о создании OpenSearch описания см. в спецификации [OpenSearch OpenSearch 1.1.](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md)  
