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
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a><span data-ttu-id="05f13-104">Использование манифеста Веб-приложения для интеграции прогрессивного веб-приложения в операционную систему</span><span class="sxs-lookup"><span data-stu-id="05f13-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="05f13-105">Манифест веб-приложения веб-сайта определяет, как ваше прогрессивное веб-приложение \(PWA\) выглядит и ведет себя при установке на устройстве.</span><span class="sxs-lookup"><span data-stu-id="05f13-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="05f13-106">На самом базовом уровне Манифест содержит сведения о имени приложения, значках, которые можно использовать для представления приложения в системных меню, а также цвета темы, которые операционная система \(OS\) использует в панели заголовков.</span><span class="sxs-lookup"><span data-stu-id="05f13-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="05f13-107">Манифест также позволяет разблокировать мощные функции, которые позволяют приложению вести себя так же, как и другие приложения в системе.</span><span class="sxs-lookup"><span data-stu-id="05f13-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a><span data-ttu-id="05f13-108">Использование ярлыков для обеспечения быстрого доступа к функциям</span><span class="sxs-lookup"><span data-stu-id="05f13-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="05f13-109">Большинство операционных систем обеспечивают быстрый доступ к ключевым функциям приложения с помощью ярлыков в контекстном меню, подключенном к значку приложения.</span><span class="sxs-lookup"><span data-stu-id="05f13-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="05f13-110">Чтобы использовать ярлыки в PWA, включите свойство `shortcuts` в манифест веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="05f13-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="05f13-111">В следующем фрагменте кода отображается определение ярлыка в манифесте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="05f13-111">The following code snippet displays how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="05f13-112">При добавлении в полный манифест веб-приложения добавление предыдущего фрагмента кода позволяет выполнить два ярлыка в контекстное меню на значке приложения.</span><span class="sxs-lookup"><span data-stu-id="05f13-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="05f13-113">Первый называется и `Play Later` имеет настраиваемый значок.</span><span class="sxs-lookup"><span data-stu-id="05f13-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="05f13-114">Второй называется и `Subscriptions` не имеет значка, так как свойство `icons` необязательно.</span><span class="sxs-lookup"><span data-stu-id="05f13-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="05f13-115">Свойство также необязательно и может использоваться для `description` предоставления дополнительных сведений для целей доступности.</span><span class="sxs-lookup"><span data-stu-id="05f13-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <a name="identify-your-app-as-a-share-target"></a><span data-ttu-id="05f13-116">Определение приложения в качестве целевого показателя share</span><span class="sxs-lookup"><span data-stu-id="05f13-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="05f13-117">Многие операционные системы позволяют пользователям быстро обмениваться ссылками и файлами с родными приложениями.</span><span class="sxs-lookup"><span data-stu-id="05f13-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="05f13-118">Прогрессивные веб-приложения также могут участвовать в этой функции с помощью `share_target` участника Манифеста веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="05f13-118">Progressive Web Apps can participate in this feature as well, using the `share_target` member of the Web App Manifest.</span></span>  <span data-ttu-id="05f13-119">Используя, `share_target` вы определяете страницу \(похожую на форму\) и параметры, которые вы ожидаете `"action"` передать в нее.</span><span class="sxs-lookup"><span data-stu-id="05f13-119">Using `share_target`, you define the `"action"` page \(similar to a form\) and the parameters you expect to be passed into it.</span></span>  <span data-ttu-id="05f13-120">В следующем фрагменте кода отображается пример использования `share_target` .</span><span class="sxs-lookup"><span data-stu-id="05f13-120">The following code snippet displays an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="05f13-121">При добавлении в манифест веб-приложения это создается как `"/share.html"` страница действий для share.</span><span class="sxs-lookup"><span data-stu-id="05f13-121">When added to the Web App Manifest, this establishes `"/share.html"` as the action page for a share.</span></span> <span data-ttu-id="05f13-122">Кроме того, он определяет три параметра, которые будут переданы на эту страницу действий: `"title"` `"text"` и `"url"` .</span><span class="sxs-lookup"><span data-stu-id="05f13-122">Additionally, it defines three parameters that would be passed to that action page:`"title"`, `"text"`, and `"url"`.</span></span>  <span data-ttu-id="05f13-123">Эти параметры будут храниться в `"name"` объекте `"description"` `"link"` [ShareData][GitHubWicgWebShareDomSharedata] и его свойствах.</span><span class="sxs-lookup"><span data-stu-id="05f13-123">These parameters will be stored in the `"name"`, `"description"`, and `"link"` properties of the [ShareData][GitHubWicgWebShareDomSharedata] object.</span></span>  <span data-ttu-id="05f13-124">По умолчанию страница действия получает параметры в рамках запроса GET, но можно указать запрос и кодить \(as \), как это было бы в `method` `enctype` веб-форме.</span><span class="sxs-lookup"><span data-stu-id="05f13-124">By default, the action page receives the parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <a name="see-also"></a><span data-ttu-id="05f13-125">См. также</span><span class="sxs-lookup"><span data-stu-id="05f13-125">See also</span></span>  

<span data-ttu-id="05f13-126">Чтобы узнать больше о манифестах веб-приложений, перейдите к следующему списку связанных тем.</span><span class="sxs-lookup"><span data-stu-id="05f13-126">To learn more about Web App Manifests, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="05f13-127">Манифесты веб-приложения</span><span class="sxs-lookup"><span data-stu-id="05f13-127">Web App Manifests</span></span>][MDNWebAppManifests]  
*   [<span data-ttu-id="05f13-128">Цель веб-обмена</span><span class="sxs-lookup"><span data-stu-id="05f13-128">Web Share Target</span></span>][GitHubWicgWebShareTarget]
*   [<span data-ttu-id="05f13-129">Веб-доля</span><span class="sxs-lookup"><span data-stu-id="05f13-129">Web Share</span></span>][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Веб-приложение | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Целевой API веб-| WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Словарь ShareData — API веб-| WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "API веб-| WICG"
