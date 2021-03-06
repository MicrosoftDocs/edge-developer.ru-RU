---
ms.assetid: ''
description: Безопасно экспериментируйте в течение определенного периода времени и предосмотрить отзывы о новых функций платформы.
title: Пробные версии
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, origin trials, developer
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397547"
---
# <a name="use-origin-trials-in-microsoft-edge"></a><span data-ttu-id="14721-104">Использование испытаний origin в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="14721-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="14721-105">Разработчики могут использовать Origin Trials для опробовки экспериментальных API на живых сайтах в течение ограниченного периода времени.</span><span class="sxs-lookup"><span data-stu-id="14721-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="14721-106">При использовании origin Trials пользователи Microsoft Edge, которые посещают ваш сайт, могут запускать код, использующий экспериментальные API.</span><span class="sxs-lookup"><span data-stu-id="14721-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="14721-107">Чтобы получить доступ к экспериментальным API на каждом компьютере пользователя, не нужно ходить и `edge://flags` включить флаги функций.</span><span class="sxs-lookup"><span data-stu-id="14721-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="14721-108">Дополнительные сведения перейдите к [экспериментальным API.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="14721-108">For more information, navigate to [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="14721-109">Кроме того, вы можете предоставить отзывы о разработке API, случаях использования или опыте использования API для инженеров браузера и сообщества веб-стандартов.</span><span class="sxs-lookup"><span data-stu-id="14721-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <a name="get-started-using-origin-trials"></a><span data-ttu-id="14721-110">Начало работы с использованием origin Trials</span><span class="sxs-lookup"><span data-stu-id="14721-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="14721-111">Дополнительные сведения о экспериментальных API, доступных в Microsoft Edge, перейдите на [консоль разработчиков microsoft Edge Origin Trials.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="14721-111">For more information about the experimental APIs available in Microsoft Edge, navigate to [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="14721-112">Убедитесь, что вы просмотрите минимальные требования к версии для Microsoft Edge и дату окончания пробной версии для оценки пригодности использования экспериментальных API на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="14721-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="14721-113">Эксперимент может завершиться раньше запланированного, если возникает любая из следующих ситуаций.</span><span class="sxs-lookup"><span data-stu-id="14721-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="14721-114">Серьезный инцидент с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="14721-114">A major security incident.</span></span>  
> *   <span data-ttu-id="14721-115">Если собрана достаточная обратная связь, которая указывает на необходимость серьезного редизайна для удовлетворения потребностей веб-разработчиков.</span><span class="sxs-lookup"><span data-stu-id="14721-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="14721-116">В любом случае всем разработчикам, в настоящее время зарегистрированным в эксперименте, отправляется сообщение уведомления.</span><span class="sxs-lookup"><span data-stu-id="14721-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <a name="register-for-a-trial-of-an-experimental-api"></a><span data-ttu-id="14721-117">Регистрация пробного экспериментального API</span><span class="sxs-lookup"><span data-stu-id="14721-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="14721-118">Для регистрации пробного экспериментального API используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14721-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="14721-119">Посетите [страницу консоли разработчика microsoft Edge Origin Trials.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="14721-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="14721-120">Выберите кнопку Регистрация на любом из доступных экспериментов.</span><span class="sxs-lookup"><span data-stu-id="14721-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="14721-121">Вопишитесь в консоль разработчика с помощью имени пользователя и пароля GitHub.</span><span class="sxs-lookup"><span data-stu-id="14721-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="14721-122">Выберите **авторизованный MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="14721-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="14721-123">Заполняем форму.</span><span class="sxs-lookup"><span data-stu-id="14721-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="14721-124">Чтобы зарегистрировать один или все поддомены, выберите параметр `Do you need to match all subdomains for the provided origin?` `Yes` .</span><span class="sxs-lookup"><span data-stu-id="14721-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="14721-125">Например, это один домен, и для представления всех поддоменов используется `https://dev.contoso.com` `https://*.contoso.com` подгруппа.</span><span class="sxs-lookup"><span data-stu-id="14721-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="14721-126">Не допускаются следующие форматы происхождения.</span><span class="sxs-lookup"><span data-stu-id="14721-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="14721-127">Указание подмостка по происхождению.</span><span class="sxs-lookup"><span data-stu-id="14721-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="14721-128">Например:</span><span class="sxs-lookup"><span data-stu-id="14721-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="14721-129">Использование источника с параметрами строки запроса.</span><span class="sxs-lookup"><span data-stu-id="14721-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="14721-130">Например:</span><span class="sxs-lookup"><span data-stu-id="14721-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="14721-131">Выберите **ACCEPT и REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="14721-131">Choose **ACCEPT and REGISTER**.</span></span>  
    
### <a name="apply-your-token"></a><span data-ttu-id="14721-132">Применение маркера</span><span class="sxs-lookup"><span data-stu-id="14721-132">Apply your token</span></span>  

<span data-ttu-id="14721-133">Маркер мгновенно создается и отображается на странице [Microsoft Edge Origin Trials Developer Console.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="14721-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="14721-134">Чтобы начать использовать пробную часть на веб-сайте, используйте любой из следующих методов для применения маркера на своей странице.</span><span class="sxs-lookup"><span data-stu-id="14721-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="14721-135">Добавьте значение атрибута и маркер в тег на каждой `origin-trial` `meta` странице, использующей экспериментальный API.</span><span class="sxs-lookup"><span data-stu-id="14721-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="14721-136">Добавьте `Origin-Trial` в http-заглавную головку ответа на сервере.</span><span class="sxs-lookup"><span data-stu-id="14721-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="14721-137">Маркер действителен в течение 6 недель.</span><span class="sxs-lookup"><span data-stu-id="14721-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="14721-138">Перед окончанием пробной записи вам отправляются письма-напоминания, в которых вы запросите отзывы и попросите вас рассмотреть возможность продления пробной пробной записи до истечения срока действия маркера.</span><span class="sxs-lookup"><span data-stu-id="14721-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <a name="opt-out-of-an-experiment"></a><span data-ttu-id="14721-139">Отказ от эксперимента</span><span class="sxs-lookup"><span data-stu-id="14721-139">Opt out of an experiment</span></span>  

<span data-ttu-id="14721-140">Чтобы отказаться от эксперимента, используйте один из следующих методов для удаления маркера.</span><span class="sxs-lookup"><span data-stu-id="14721-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="14721-141">Удалите `meta` тег со всех страниц, на которые использовался экспериментальный API.</span><span class="sxs-lookup"><span data-stu-id="14721-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="14721-142">Удаление `Origin-Trial` из http-загона ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="14721-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a><span data-ttu-id="14721-143">Обнаружение экспериментальных функций и предоставление отката</span><span class="sxs-lookup"><span data-stu-id="14721-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="14721-144">При использовании экспериментальных API убедитесь, что вы предоставляете рабочий опыт всем посетителям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="14721-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="14721-145">Посетители могут использовать браузеры, которые не поддерживают экспериментальные API, добавленные в код.</span><span class="sxs-lookup"><span data-stu-id="14721-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="14721-146">Кроме того, если срок действия маркера истекает до его обновления, экспериментальный API больше не доступен, что может привести к ошибкам.</span><span class="sxs-lookup"><span data-stu-id="14721-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="14721-147">Чтобы избежать этой ситуации, убедитесь, что вы обнаружите функции, доступные в браузере.</span><span class="sxs-lookup"><span data-stu-id="14721-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="14721-148">Дополнительные сведения перейдите к [реализации обнаружения функций.][MDNImplementingFeatureDetection]</span><span class="sxs-lookup"><span data-stu-id="14721-148">For more information, navigate to [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <a name="roadmap-for-allowed-origins"></a><span data-ttu-id="14721-149">Дорожная карта для разрешенных истоков</span><span class="sxs-lookup"><span data-stu-id="14721-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="14721-150">Портал Microsoft Edge Origin Trials на сегодняшний день поддерживает только службу SSL Enabled Origins, что означает, что веб-сайты должны правильно реализовать HTTPS для регистрации для эксперимента.</span><span class="sxs-lookup"><span data-stu-id="14721-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="14721-151">В будущем планируется следующее безопасное происхождение.</span><span class="sxs-lookup"><span data-stu-id="14721-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="14721-152">`http://localhost`Зарегистрируйтесь в качестве источника для экспериментов.</span><span class="sxs-lookup"><span data-stu-id="14721-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="14721-153">Чтобы использовать `http://localhost` сегодня, перейдите к `edge://flags` и установите эксперимент включен . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="14721-153">To use `http://localhost` today, navigate to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="14721-154">Для регистрации в экспериментах используйте расширения с `extensions://` предуфаксными истоками.</span><span class="sxs-lookup"><span data-stu-id="14721-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Документы Майкрософт"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Реализация функций обнаружения | MDN"  
