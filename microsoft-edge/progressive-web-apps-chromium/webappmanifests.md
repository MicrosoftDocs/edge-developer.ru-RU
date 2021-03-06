---
title: Использование манифеста Веб-приложения для интеграции прогрессивного веб-приложения в операционную систему
description: Узнайте, как использовать Манифест веб-приложения для интеграции прогрессивного веб-приложения в операционную систему.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399101"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a>Использование манифеста Веб-приложения для интеграции прогрессивного веб-приложения в операционную систему

Манифест веб-приложения веб-сайта определяет, как ваше прогрессивное веб-приложение \(PWA\) выглядит и ведет себя при установке на устройстве.  На самом базовом уровне Манифест содержит сведения о имени приложения, значках, которые можно использовать для представления приложения в системных меню, а также цвета темы, которые операционная система \(OS\) использует в панели заголовков.  Манифест также позволяет разблокировать мощные функции, которые позволяют приложению вести себя так же, как и другие приложения в системе.  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a>Использование ярлыков для обеспечения быстрого доступа к функциям  

Большинство операционных систем обеспечивают быстрый доступ к ключевым функциям приложения с помощью ярлыков в контекстном меню, подключенном к значку приложения.  Чтобы использовать ярлыки в PWA, включите свойство `shortcuts` в манифест веб-приложения.  В следующем фрагменте кода отображается определение ярлыка в манифесте веб-приложения.  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

При добавлении в полный манифест веб-приложения добавление предыдущего фрагмента кода позволяет выполнить два ярлыка в контекстное меню на значке приложения.  Первый называется и `Play Later` имеет настраиваемый значок.  Второй называется и `Subscriptions` не имеет значка, так как свойство `icons` необязательно.  Свойство также необязательно и может использоваться для `description` предоставления дополнительных сведений для целей доступности.  

## <a name="identify-your-app-as-a-share-target"></a>Определение приложения в качестве целевого показателя share

Многие операционные системы позволяют пользователям быстро обмениваться ссылками и файлами с родными приложениями. Прогрессивные веб-приложения также могут участвовать в этой функции с помощью `share_target` участника Манифеста веб-приложений.  Используя, `share_target` вы определяете страницу \(похожую на форму\) и параметры, которые вы ожидаете `"action"` передать в нее.  В следующем фрагменте кода отображается пример использования `share_target` .

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

При добавлении в манифест веб-приложения это создается как `"/share.html"` страница действий для share. Кроме того, он определяет три параметра, которые будут переданы на эту страницу действий: `"title"` `"text"` и `"url"` .  Эти параметры будут храниться в `"name"` объекте `"description"` `"link"` [ShareData][GitHubWicgWebShareDomSharedata] и его свойствах.  По умолчанию страница действия получает параметры в рамках запроса GET, но можно указать запрос и кодить \(as \), как это было бы в `method` `enctype` веб-форме.

## <a name="see-also"></a>См. также  

Чтобы узнать больше о манифестах веб-приложений, перейдите к следующему списку связанных тем.  

*   [Манифесты веб-приложения][MDNWebAppManifests]  
*   [Цель веб-обмена][GitHubWicgWebShareTarget]
*   [Веб-доля][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Веб-приложение | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Целевой API веб-| WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Словарь ShareData — API веб-| WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "API веб-| WICG"
