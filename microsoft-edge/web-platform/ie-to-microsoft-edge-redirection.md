---
description: Перемещение пользователей в Microsoft Edge из Internet Explorer
title: Перемещение пользователей в Microsoft Edge из Internet Explorer
author: MSEdgeTeam
ms.date: 11/06/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft EDGE, совместимость, веб-платформа, Internet Explorer
ms.openlocfilehash: 2e1488359e405247e290ad8f6300c480a7e20af6
ms.sourcegitcommit: 6ef48c8cda392c6bf8217cff5f696ac620d10739
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163209"
---
# <span data-ttu-id="c742e-104">Перемещение пользователей в Microsoft Edge из Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="c742e-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="c742e-105">У многих современных веб-сайтов есть макеты, несовместимые с Internet Explorer \ (IE).</span><span class="sxs-lookup"><span data-stu-id="c742e-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="c742e-106">Если пользователь IE посещает неподдерживаемый общедоступный веб-сайт, пользователь может получить сообщение.</span><span class="sxs-lookup"><span data-stu-id="c742e-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="c742e-107">В сообщении говорится о том, что веб-сайт несовместим с браузером.</span><span class="sxs-lookup"><span data-stu-id="c742e-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="c742e-108">После того как сообщение будет выводиться, ожидается, что пользователь вручную переключается на современный браузер.</span><span class="sxs-lookup"><span data-stu-id="c742e-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="c742e-109">Чтобы свести к минимуму перерывы, начиная с версии 84, Microsoft EDGE поддерживает новую возможность, которая автоматически перенаправляет пользователей.</span><span class="sxs-lookup"><span data-stu-id="c742e-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="c742e-110">Если пользователь IE переходит на веб-сайт, несовместимый с IE, Windows автоматически перенаправляет пользователя в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c742e-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="c742e-111">Чтобы просмотреть веб-сайты в списке, перейдите к [списку необходим Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="c742e-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="c742e-112">В этой статье описаны указанные ниже принципы.</span><span class="sxs-lookup"><span data-stu-id="c742e-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="c742e-113">Взаимодействие с пользователем для перенаправления</span><span class="sxs-lookup"><span data-stu-id="c742e-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="c742e-114">Запрос обновления списка</span><span class="sxs-lookup"><span data-stu-id="c742e-114">How to request an update to the list</span></span>  
    
## <span data-ttu-id="c742e-115">Почему веб-сайт добавлен в список совместимости IE?</span><span class="sxs-lookup"><span data-stu-id="c742e-115">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="c742e-116">Список совместимости IE добавляет веб-сайт только в том случае, если выполняются описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c742e-116">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="c742e-117">Показывает пользователю IE сообщение, предлагающее пользователю использовать другой браузер для обеспечения совместимости.</span><span class="sxs-lookup"><span data-stu-id="c742e-117">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="c742e-118">Владелец запрашивает добавление веб-сайта в список совместимости с IE.</span><span class="sxs-lookup"><span data-stu-id="c742e-118">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="c742e-119">Обновление списка совместимости с IE</span><span class="sxs-lookup"><span data-stu-id="c742e-119">Update the IE compatibility list</span></span>  

<span data-ttu-id="c742e-120">Список совместимости IE — это XML-файл на [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="c742e-120">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="c742e-121">Список регулярно обновляется в ответ на запросы разработчиков для пользователей и веб-сайтов, на которых добавляются или удаляются веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="c742e-121">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="c742e-122">Обновления списка автоматически загружаются на компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="c742e-122">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="c742e-123">Напишите на веб-сайте [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] , который нужно добавить или удалить из списка СОВМЕСТИМОСТИ с IE, и попросите на него следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="c742e-123">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="c742e-124">Имя владельца</span><span class="sxs-lookup"><span data-stu-id="c742e-124">Owner name</span></span>  
*   <span data-ttu-id="c742e-125">Название организации</span><span class="sxs-lookup"><span data-stu-id="c742e-125">Corporate title</span></span>  
*   <span data-ttu-id="c742e-126">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="c742e-126">Email address</span></span>  
*   <span data-ttu-id="c742e-127">Название организации</span><span class="sxs-lookup"><span data-stu-id="c742e-127">Company name</span></span>  
*   <span data-ttu-id="c742e-128">Улица</span><span class="sxs-lookup"><span data-stu-id="c742e-128">Street address</span></span>  
*   <span data-ttu-id="c742e-129">Адрес веб-сайта</span><span class="sxs-lookup"><span data-stu-id="c742e-129">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c742e-130">Список совместимости с IE предназначен для работы только с общедоступными сайтами.</span><span class="sxs-lookup"><span data-stu-id="c742e-130">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Отправка сообщения электронной почты в ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Официальная домашняя страница Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Нужен список Microsoft Edge с кодом версии v1 | Microsoft Edge"  
