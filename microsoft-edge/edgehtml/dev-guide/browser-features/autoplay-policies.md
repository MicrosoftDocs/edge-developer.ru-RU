---
description: Убедитесь, что содержимое мультимедиа на сайте ведет себя по назначению
title: Политики автозахваки — руководство разработчика
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, мультимедиа, видео, звук, автозапись
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235412"
---
# <span data-ttu-id="2d93a-104">Политики автозахваки</span><span class="sxs-lookup"><span data-stu-id="2d93a-104">Autoplay Policies</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="2d93a-105">Microsoft Edge предоставляет клиентам возможность персонализировать свои предпочтения браузера на веб-сайтах, на которые автоматически передается мультимедиа со звуком, чтобы свести к минимуму отвлекающие факторы в Интернете и сэкономить пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="2d93a-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="2d93a-106">Кроме того, Microsoft Edge автоматически подавляет автозапок мультимедиа на фоновых вкладок.</span><span class="sxs-lookup"><span data-stu-id="2d93a-106">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="2d93a-107">Пользователи могут настраивать поведение мультимедиа [](#per-site-media-autoplay-settings) с помощью [глобальных](#global-media-autoplay-settings) и индивидуальных элементов управления автоза воспроизведением, которые предоставляют следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2d93a-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>  

*   `Allow`  <span data-ttu-id="2d93a-108">По умолчанию видео будет продолжаться при первом просмотре вкладки на переднем плане по усмотрению сайта.</span><span class="sxs-lookup"><span data-stu-id="2d93a-108">The default and will continue to play videos when a tab is first viewed in the foreground, at the site's discretion.</span></span>  

*   `Limit`  <span data-ttu-id="2d93a-109">Автозапись работает только при отключаемом видео, поэтому пользователи никогда не будут уверены в звуке.</span><span class="sxs-lookup"><span data-stu-id="2d93a-109">Restricts autoplay to only work when videos are muted, so users are never surprised by sound.</span></span>  <span data-ttu-id="2d93a-110">Когда пользователь нажмет кнопку в любом месте страницы, автозаигрывка будет включена повторно и будет разрешена в пределах этого домена на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="2d93a-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>  

*   `Block`  <span data-ttu-id="2d93a-111">Запретить заместь на всех сайтах, пока пользователи не будут напрямую взаимодействовать с содержимым мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2d93a-111">Prevent sautoplay on all sites until users directly interact with the media content.</span></span>  

## <span data-ttu-id="2d93a-112">Глобальные параметры автоматического воспроизведения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2d93a-112">Global media autoplay settings</span></span>  

<span data-ttu-id="2d93a-113">Пользователи могут управлять поведением автозаполнения по умолчанию для всех сайтов в режиме "Дополнительный **параметр**  >  **мультимедиа".**</span><span class="sxs-lookup"><span data-stu-id="2d93a-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Глобальные параметры автоматического воспроизведения мультимедиа" lightbox="../media/autoplay_global.png":::
   <span data-ttu-id="2d93a-115">Глобальные параметры автоматического воспроизведения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="2d93a-115">Global media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="2d93a-116">Параметры автозахваки мультимедиа на сайте</span><span class="sxs-lookup"><span data-stu-id="2d93a-116">Per-site media autoplay settings</span></span>  

<span data-ttu-id="2d93a-117">Пользователи могут управлять поведением автозахва \*\*\*\* на уровне сайта в разделе "Разрешения веб-сайта" области сведений о веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="2d93a-117">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span>  <span data-ttu-id="2d93a-118">Этот параметр можно найти, щелкнув значок сведений или значок блокировки \*\*\*\* в левой части адресной панели и щелкнув параметры автозаписи мультимедиа для начала работы.</span><span class="sxs-lookup"><span data-stu-id="2d93a-118">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on **Media autoplay settings** to get started.</span></span>  

<span data-ttu-id="2d93a-119">Параметры на уровне сайта переопределяют глобальный параметр.</span><span class="sxs-lookup"><span data-stu-id="2d93a-119">Per-site settings override the global setting.</span></span>  <span data-ttu-id="2d93a-120">Например, если у пользователя есть свой глобальный параметр, но он изменяет параметр на уровне сайта, автозаигрывка для этого `Allow` `Block` сайта будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="2d93a-120">For example, if a user has their global setting set to `Allow` but changes a per-site setting to `Block`, autoplay will be blocked for that site.</span></span>  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Параметры автозахваки мультимедиа на сайте" lightbox="../media/autoplay_per-site.png":::
   <span data-ttu-id="2d93a-122">Параметры автозахваки мультимедиа на сайте</span><span class="sxs-lookup"><span data-stu-id="2d93a-122">Per-site media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="2d93a-123">Best Practices for Web Developers</span><span class="sxs-lookup"><span data-stu-id="2d93a-123">Best Practices for Web Developers</span></span>  

<span data-ttu-id="2d93a-124">Вот как обеспечить хороший пользовательский интерфейс с мультимедиа, который находится на сайте:</span><span class="sxs-lookup"><span data-stu-id="2d93a-124">Here's how to ensure a good user experience with media hosted on your site:</span></span>  

*   <span data-ttu-id="2d93a-125">Предположим, что для каждого использования элемента мультимедиа требуется жест пользователя, чтобы начать воспроизведение (так как пользователи могут блокировать автозапок в любой момент времени)) и спланируйте его соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d93a-125">Assume each use of a media element wil require a user gesture to start the playback \(as users can block autoplay at any point in time\) and plan accordingly.</span></span>  <span data-ttu-id="2d93a-126">Глобальные политики автозахваки и политики автозахваки на уровне сайта применяются к всем элементам и элементам независимо от того, как они используются `<audio>` `<video>` на сайте</span><span class="sxs-lookup"><span data-stu-id="2d93a-126">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>  

*   <span data-ttu-id="2d93a-127">Убедитесь, что элементы управления мультимедиа всегда присутствуют как на носители сайта, так и на содержимом.</span><span class="sxs-lookup"><span data-stu-id="2d93a-127">Ensure that media controls are always present on both site media and ad content.</span></span>  <span data-ttu-id="2d93a-128">Это позволит пользователям перезапустить воспроизведение, если автозапуск заблокирован на странице.</span><span class="sxs-lookup"><span data-stu-id="2d93a-128">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>  

*   <span data-ttu-id="2d93a-129">Оцените, как автозагрузка может повлиять на работу пользователей на вашем веб-сайте, и рассмотрите возможность использования автозагрузки таким образом, чтобы свести к минимуму нежелательное воспроизведение мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2d93a-129">Evaluate how autoplay may affect users' experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span>  <span data-ttu-id="2d93a-130">Если автозагрузка является важной частью вашего интерфейса, рассмотрите возможность запуска отключенного содержимого и разрешите пользователю отключать его.</span><span class="sxs-lookup"><span data-stu-id="2d93a-130">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span>  <span data-ttu-id="2d93a-131">Для автоматического воспроизведения отключенного содержимого источник звука должен быть явно отключен или не за установлен.</span><span class="sxs-lookup"><span data-stu-id="2d93a-131">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span>  <span data-ttu-id="2d93a-132">В противном случае элемент не будет считаться отключенным.</span><span class="sxs-lookup"><span data-stu-id="2d93a-132">Otherwise the element will not be considered as muted.</span></span>  

*   <span data-ttu-id="2d93a-133">Если нет абсолютной необходимости, используйте для воспроизведения мультимедиа элементы управления браузера.</span><span class="sxs-lookup"><span data-stu-id="2d93a-133">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span>  <span data-ttu-id="2d93a-134">Это обеспечит согласованное впечатление для пользователей.</span><span class="sxs-lookup"><span data-stu-id="2d93a-134">This will ensure a consistent experience for users.</span></span>  <span data-ttu-id="2d93a-135">При создании пользовательских элементов управления убедитесь, что элементы управления мультимедиа всегда присутствуют и ваши элементы управления правильно реагируют на подавление автозахва.</span><span class="sxs-lookup"><span data-stu-id="2d93a-135">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>  

### <span data-ttu-id="2d93a-136">Делегирования Iframe</span><span class="sxs-lookup"><span data-stu-id="2d93a-136">Iframe delegation</span></span>  

<span data-ttu-id="2d93a-137">Автозапись в автозахвах наследует разрешение на автозапись `<iframe>` от родительской страницы независимо от источника контента.</span><span class="sxs-lookup"><span data-stu-id="2d93a-137">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span>  <span data-ttu-id="2d93a-138">В сценарии списка воспроизведения, где каждый файл мультимедиа находится в отдельном iframe, пользователю потребуется начать воспроизведение только один раз для всего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2d93a-138">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>  

### <span data-ttu-id="2d93a-139">Обнаружение разрешенных автозахва</span><span class="sxs-lookup"><span data-stu-id="2d93a-139">Detecting when autoplay is allowed</span></span>  

<span data-ttu-id="2d93a-140">Вы можете настроить элементы управления воспроизведением, чтобы показать правильное состояние при блокировке автозазахва, изучив обещание, возвращенные функцией в `play()` элементе мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="2d93a-140">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
