---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Руководства по функциям браузера в Microsoft Edge.
title: Браузер — руководство для разработчиков
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2579fad881496e2197f9f696bb2c12c47c7f723e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235667"
---
# <span data-ttu-id="3706e-104">Функции браузера</span><span class="sxs-lookup"><span data-stu-id="3706e-104">Browser features</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## <span data-ttu-id="3706e-105">Политики автозапуска</span><span class="sxs-lookup"><span data-stu-id="3706e-105">Autoplay policies</span></span>  

 <span data-ttu-id="3706e-106">Microsoft Edge предоставляет клиентам возможность персонализировать свои предпочтения браузера на веб-сайтах, на которые автоматически передается мультимедиа со звуком, чтобы свести к минимуму отвлекающие факторы в Интернете и сэкономить пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="3706e-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="3706e-107">Пользователи могут настраивать поведение мультимедиа с помощью глобальных и индивидуальных элементов управления автоза воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="3706e-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span>  <span data-ttu-id="3706e-108">Кроме того, Microsoft Edge автоматически подавляет автозапок мультимедиа на фоновых вкладок.</span><span class="sxs-lookup"><span data-stu-id="3706e-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="3706e-109">Подробные [сведения и](./browser-features/autoplay-policies.md) практические методики для обеспечения хорошего взаимодействия с пользователем с мультимедиа, который находится на сайте, можно найти в политиках автозахва.</span><span class="sxs-lookup"><span data-stu-id="3706e-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>  

## <span data-ttu-id="3706e-110">Flash</span><span class="sxs-lookup"><span data-stu-id="3706e-110">Flash</span></span>  

<span data-ttu-id="3706e-111">Если на вашей странице используется Flash, но пользователь не включил его, Microsoft Edge обычно показывает значок фрагмента задачи в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="3706e-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span>  <span data-ttu-id="3706e-112">Если вы динамически добавляете контроль flash после загрузки страницы, значок задачи может не [](./browser-features/flash.md) отображаться. В этом случае вам нужно будет проверить, загружена ли flash, и обеспечить корректный режим отката, если он не отображается.</span><span class="sxs-lookup"><span data-stu-id="3706e-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>  

## <span data-ttu-id="3706e-113">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="3706e-113">Reading view</span></span>  

<span data-ttu-id="3706e-114">Microsoft Edge [](./browser-features/reading-view.md) предоставляет представление чтения для более упрощенного и похожего на книгу чтения веб-страниц, не отвлекая внимание от несвязанных или другого дополнительного содержимого на странице.</span><span class="sxs-lookup"><span data-stu-id="3706e-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="3706e-115">Ниже указаны советы по обеспечению отличного просмотра для чтения на сайте, а также инструкции по выбору сайта из представления чтения.</span><span class="sxs-lookup"><span data-stu-id="3706e-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>  

## <span data-ttu-id="3706e-116">Обнаружение службы поиска</span><span class="sxs-lookup"><span data-stu-id="3706e-116">Search provider discovery</span></span>  

<span data-ttu-id="3706e-117">Интеграция с богатым поиском встроена в адресную планку Microsoft Edge, включая предложения поиска, результаты из Интернета, историю браузера и избранное.</span><span class="sxs-lookup"><span data-stu-id="3706e-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="3706e-118">[Вот дополнительные сведения для поставщиков поиска,](./browser-features/search-provider-discovery.md) которые ищут поддержку Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3706e-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>  
