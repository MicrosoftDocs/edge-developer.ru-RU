---
description: Узнайте о некоторых полезных советах и советах относительно расширений Microsoft Edge
title: Советы и рекомендации | Расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик, расширения
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235348"
---
# <span data-ttu-id="7cf73-104">Советы и рекомендации</span><span class="sxs-lookup"><span data-stu-id="7cf73-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="7cf73-105">Независимо от того, работаете ли вы в настоящее время над расширением Microsoft Edge или уже опубликовали его, вам могут пригодиться следующие советы и рекомендации.</span><span class="sxs-lookup"><span data-stu-id="7cf73-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="7cf73-106">Получите прямую ссылку на расширение в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7cf73-106">Get a direct link to your extension in the Microsoft Store</span></span>

<span data-ttu-id="7cf73-107">На информационной панели Центра разработчиков для Windows можно найти прямую ссылку на расширение в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7cf73-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="7cf73-108">Эта ссылка может быть полезна для рекламы и общего доступа к расширению.</span><span class="sxs-lookup"><span data-stu-id="7cf73-108">This link can be useful for advertising and sharing out your extension.</span></span>

<span data-ttu-id="7cf73-109">После входа в Центр разработчиков Для Windows и переходов к расширению через информационную панель на странице удостоверения приложения вы найдете ссылку в строке ссылки протокола **Магазина:**</span><span class="sxs-lookup"><span data-stu-id="7cf73-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![ссылка на протокол store](./media/store-link.png)
 
## <span data-ttu-id="7cf73-111">Убедитесь, что вы следуете политике Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7cf73-111">Make sure you’re following the Microsoft Store Policy</span></span>

<span data-ttu-id="7cf73-112">При создании расширения обязательно помните о рекомендациях по отправке в Microsoft Store, которые выделены в политике [Microsoft Store.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cf73-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="7cf73-113">Расширения Microsoft Edge также имеют дополнительный набор политик, которые следует соблюдать [здесь.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)</span><span class="sxs-lookup"><span data-stu-id="7cf73-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="7cf73-114">Улучшение возможности обнаружения расширения в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7cf73-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="7cf73-115">Вы можете добавить ключевые слова в отправку расширения, чтобы улучшить его обнаружение с помощью поиска.</span><span class="sxs-lookup"><span data-stu-id="7cf73-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span> <span data-ttu-id="7cf73-116">Например, "Расширения Microsoft Edge" и "имя расширения".</span><span class="sxs-lookup"><span data-stu-id="7cf73-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="7cf73-117">Это можно сделать в Центре разработчиков Windows в разделе описания расширения.</span><span class="sxs-lookup"><span data-stu-id="7cf73-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="7cf73-118">Эти ключевые слова необходимо добавить для каждого языка, поддерживаемого расширением.</span><span class="sxs-lookup"><span data-stu-id="7cf73-118">These keywords will need to be added for every language your extension supports.</span></span>

![Отправка ответа на отзыв — ключевые слова](./media/keywords.png)

## <span data-ttu-id="7cf73-120">Автоматизация отправки в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7cf73-120">Automate your submission to the Microsoft Store</span></span>

<span data-ttu-id="7cf73-121">Вы можете автоматизировать и оптимизировать отправки в Microsoft Store с помощью нового API отправки в Microsoft Store, который позволяет обновлять приложения и игры, надстройки (покупки из приложения) и пакеты с помощью REST API.</span><span class="sxs-lookup"><span data-stu-id="7cf73-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="7cf73-122">Ознакомьтесь с [документацией и примерами или](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) воспользуйтесь расширением [VSTS для отправки](https://github.com/Microsoft/windows-dev-center-vsts-extension) с открытым исходным кодом, чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="7cf73-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="7cf73-123">Сбор отзывов, отзывов и запросов функций с помощью Центра отзывов Windows</span><span class="sxs-lookup"><span data-stu-id="7cf73-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="7cf73-124">Вы можете направлять пользователей в подкатегорию Центра отзывов Windows для расширения, встраив ссылку на нее.</span><span class="sxs-lookup"><span data-stu-id="7cf73-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="7cf73-125">Эту ссылку необходимо создать в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="7cf73-125">This link will need to be created using the following format:</span></span> 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="7cf73-126">Вам потребуется заменить `<PFN>` имя семейства пакетов расширения.</span><span class="sxs-lookup"><span data-stu-id="7cf73-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="7cf73-127">Это можно найти в разделе **удостоверения приложения** для расширения в Центре разработчиков для Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf73-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="7cf73-128">Ознакомьтесь со своими оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="7cf73-128">Check out your ratings and reviews</span></span>

<span data-ttu-id="7cf73-129">Регулярно войдите в систему, чтобы проверить отзывы и оценки пользователей.</span><span class="sxs-lookup"><span data-stu-id="7cf73-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="7cf73-130">Хотя приложение UWP будет иметь сведения только о текущем пользовательском рынке, при входе в Центр разработчиков Для Windows будет отображаться средняя оценка на всех рынках.</span><span class="sxs-lookup"><span data-stu-id="7cf73-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="7cf73-131">Ответ на отзывы пользователей</span><span class="sxs-lookup"><span data-stu-id="7cf73-131">Respond to user reviews</span></span>

<span data-ttu-id="7cf73-132">Вы можете отвечать на отзывы пользователей в Microsoft Store с помощью информационной панели Центра разработчиков для Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf73-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="7cf73-133">Перейдите к расширению и в области "Аналитика" выберите **"Отзывы".**</span><span class="sxs-lookup"><span data-stu-id="7cf73-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="7cf73-134">Под каждым отзывом будет отображаться ссылка, которая позволит вам реагировать непосредственно на клиента.</span><span class="sxs-lookup"><span data-stu-id="7cf73-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="7cf73-135">Этот канал общения позволяет вам отправлять отзывы, решения и благодарить вас за отзыв!</span><span class="sxs-lookup"><span data-stu-id="7cf73-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Отправка ответа на отзыв](./media/reviews.png)
