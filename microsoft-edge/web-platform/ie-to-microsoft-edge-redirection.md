---
description: Перемещение пользователей в Microsoft Edge из Internet Explorer
title: Перемещение пользователей в Microsoft Edge из Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft EDGE, совместимость, веб-платформа, Internet Explorer
ms.openlocfilehash: 872bd5ec52f471e4958ef7354c046ec30f1ba72e
ms.sourcegitcommit: 62258ce0ef469948ca8af42141d02aa9719243f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168371"
---
# <span data-ttu-id="ef670-104">Перемещение пользователей в Microsoft Edge из Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ef670-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="ef670-105">У многих современных веб-сайтов есть макеты, несовместимые с Internet Explorer \ (IE).</span><span class="sxs-lookup"><span data-stu-id="ef670-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="ef670-106">Если пользователь IE посещает неподдерживаемый общедоступный веб-сайт, пользователь может получить сообщение.</span><span class="sxs-lookup"><span data-stu-id="ef670-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="ef670-107">В сообщении говорится о том, что веб-сайт несовместим с браузером.</span><span class="sxs-lookup"><span data-stu-id="ef670-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="ef670-108">После того как сообщение будет выводиться, ожидается, что пользователь вручную переключается на современный браузер.</span><span class="sxs-lookup"><span data-stu-id="ef670-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="ef670-109">Чтобы свести к минимуму перерывы, начиная с версии 84, Microsoft EDGE поддерживает новую возможность, которая автоматически перенаправляет пользователей.</span><span class="sxs-lookup"><span data-stu-id="ef670-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="ef670-110">Если пользователь IE переходит на веб-сайт, несовместимый с IE, Windows автоматически перенаправляет пользователя в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef670-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="ef670-111">Чтобы просмотреть веб-сайты в списке, перейдите к [списку необходим Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="ef670-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="ef670-112">В этой статье описаны указанные ниже принципы.</span><span class="sxs-lookup"><span data-stu-id="ef670-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="ef670-113">Почему веб-сайт добавляется в список</span><span class="sxs-lookup"><span data-stu-id="ef670-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="ef670-114">Взаимодействие с пользователем для перенаправления</span><span class="sxs-lookup"><span data-stu-id="ef670-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="ef670-115">Запрос обновления списка</span><span class="sxs-lookup"><span data-stu-id="ef670-115">Request an update to the list</span></span>  
    
## <span data-ttu-id="ef670-116">Почему веб-сайт добавлен в список совместимости IE?</span><span class="sxs-lookup"><span data-stu-id="ef670-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="ef670-117">Список совместимости IE добавляет веб-сайт только в том случае, если выполняются описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ef670-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="ef670-118">Показывает пользователю IE сообщение, предлагающее пользователю использовать другой браузер для обеспечения совместимости.</span><span class="sxs-lookup"><span data-stu-id="ef670-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="ef670-119">Владелец запрашивает добавление веб-сайта в список совместимости с IE.</span><span class="sxs-lookup"><span data-stu-id="ef670-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <span data-ttu-id="ef670-120">Интерфейс перенаправления</span><span class="sxs-lookup"><span data-stu-id="ef670-120">Redirection experience</span></span>

<span data-ttu-id="ef670-121">При перенаправлении на Microsoft Edge пользователь показывает одноразовое диалоговое окно на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="ef670-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="ef670-122">В диалоговом окне пользователю выводятся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="ef670-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="ef670-123">В этой статье объясняется, почему перенаправляется веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="ef670-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="ef670-124">Он запрашивает согласие пользователя на копирование данных браузера и параметров из IE в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef670-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ef670-125">Будут импортированы следующие данные браузера.</span><span class="sxs-lookup"><span data-stu-id="ef670-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="ef670-126">Избранное</span><span class="sxs-lookup"><span data-stu-id="ef670-126">Favorites</span></span>  
      *   <span data-ttu-id="ef670-127">Пароли</span><span class="sxs-lookup"><span data-stu-id="ef670-127">Passwords</span></span>  
      *   <span data-ttu-id="ef670-128">Поисковые системы</span><span class="sxs-lookup"><span data-stu-id="ef670-128">Search engines</span></span>  
      *   <span data-ttu-id="ef670-129">Открытые вкладки</span><span class="sxs-lookup"><span data-stu-id="ef670-129">Open tabs</span></span>  
      *   <span data-ttu-id="ef670-130">Журнал</span><span class="sxs-lookup"><span data-stu-id="ef670-130">History</span></span>  
      *   <span data-ttu-id="ef670-131">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef670-131">Settings</span></span>  
      *   <span data-ttu-id="ef670-132">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="ef670-132">Cookies</span></span>  
      *   <span data-ttu-id="ef670-133">Домашняя страница</span><span class="sxs-lookup"><span data-stu-id="ef670-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Просмотр уведомлений и запросов на импорт данных и параметров" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="ef670-135">Просмотр уведомлений и запросов на импорт данных и параметров</span><span class="sxs-lookup"><span data-stu-id="ef670-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="ef670-136">Если пользователь не допускает согласие, выбрав параметр **всегда переноситься на мои данные браузера и настройки из Internet Explorer** , пользователь может нажать кнопку **продолжить просмотр**,   чтобы продолжить сеанс просмотра.</span><span class="sxs-lookup"><span data-stu-id="ef670-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="ef670-137">Наконец, баннер несовместимости веб-сайтов отображается в адресной строке каждого перенаправления.</span><span class="sxs-lookup"><span data-stu-id="ef670-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="ef670-138">Пример объявления о несовместимости веб-сайтов показан на приведенном ниже рисунке.</span><span class="sxs-lookup"><span data-stu-id="ef670-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Уведомление о современных сайтах и запрос на установку Microsoft EDGE в качестве браузера по умолчанию или просмотр Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="ef670-140">Уведомление о современных сайтах и запрос на установку Microsoft EDGE в качестве браузера по умолчанию или просмотр Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ef670-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="ef670-141">Заголовок "несовместимость" веб-сайта предоставляет пользователю следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ef670-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="ef670-142">Рекомендует пользователю перейти на Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef670-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="ef670-143">Позволяет использовать Microsoft EDGE в качестве браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef670-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="ef670-144">Предоставляет пользователю возможность ознакомиться с Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef670-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="ef670-145">Если веб-сайт перенаправлением из Internet Explorer в Microsoft EDGE, произойдет одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="ef670-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="ef670-146">Если на вкладке "активные ОБОЗРЕВАТЕЛи" отсутствует предыдущее содержимое, оно будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="ef670-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="ef670-147">Если на вкладке "активные" есть предыдущее содержимое, откроется [страница службы поддержки Майкрософт, в которой объясняется, почему веб-сайт был перенаправлен в Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span><span class="sxs-lookup"><span data-stu-id="ef670-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="ef670-148">После перенаправления пользователи могут продолжать использовать IE для веб-сайтов, не включенных в список совместимости IE.</span><span class="sxs-lookup"><span data-stu-id="ef670-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <span data-ttu-id="ef670-149">Запрос на обновление списка совместимости с IE</span><span class="sxs-lookup"><span data-stu-id="ef670-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="ef670-150">Список совместимости IE — это XML-файл на [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="ef670-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="ef670-151">Список регулярно обновляется в ответ на запросы разработчиков для пользователей и веб-сайтов, на которых добавляются или удаляются веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="ef670-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="ef670-152">Обновления списка автоматически загружаются на компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="ef670-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="ef670-153">Напишите на веб-сайте [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] , который нужно добавить или удалить из списка СОВМЕСТИМОСТИ с IE, и попросите на него следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="ef670-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="ef670-154">Имя владельца</span><span class="sxs-lookup"><span data-stu-id="ef670-154">Owner name</span></span>  
*   <span data-ttu-id="ef670-155">Название организации</span><span class="sxs-lookup"><span data-stu-id="ef670-155">Corporate title</span></span>  
*   <span data-ttu-id="ef670-156">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="ef670-156">Email address</span></span>  
*   <span data-ttu-id="ef670-157">Название организации</span><span class="sxs-lookup"><span data-stu-id="ef670-157">Company name</span></span>  
*   <span data-ttu-id="ef670-158">Улица</span><span class="sxs-lookup"><span data-stu-id="ef670-158">Street address</span></span>  
*   <span data-ttu-id="ef670-159">Адрес веб-сайта</span><span class="sxs-lookup"><span data-stu-id="ef670-159">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="ef670-160">Список совместимости с IE предназначен для работы только с общедоступными сайтами.</span><span class="sxs-lookup"><span data-stu-id="ef670-160">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Отправка сообщения электронной почты в ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Официальная домашняя страница Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Нужен список Microsoft Edge с кодом версии v1 | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "Веб-сайт, к которому вы пытаетесь обратиться, не работает в Internet Explorer | Служба поддержки Microsoft Office"  
