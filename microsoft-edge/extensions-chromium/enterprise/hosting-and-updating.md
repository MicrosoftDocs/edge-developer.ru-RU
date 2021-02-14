---
description: Раздать и публиковать расширения на предприятии для Microsoft Edge (Chromium).
title: Публикация и обновление расширений в магазине надстройки Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327689"
---
# <span data-ttu-id="22f94-104">Публикация и обновление расширений в магазине надстройки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="22f94-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="22f94-105">Большинство расширений публикуются в хранилище надстройки [Microsoft Edge][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] для защиты пользователей от вредоносных расширений.</span><span class="sxs-lookup"><span data-stu-id="22f94-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <span data-ttu-id="22f94-106">Параметры публикации расширений</span><span class="sxs-lookup"><span data-stu-id="22f94-106">Publish options for extensions</span></span>  

<span data-ttu-id="22f94-107">Все расширения распространяются пользователям в качестве специального архивного `.zip` файла \( \) с суффиксом. `.crx`</span><span class="sxs-lookup"><span data-stu-id="22f94-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="22f94-108">Расширения, опубликованные в microsoft Edge Add-ons Store, загружаются как `.zip` файлы.</span><span class="sxs-lookup"><span data-stu-id="22f94-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="22f94-109">Процесс публикации автоматически преобразует файл `.zip` в `.crx` файл.</span><span class="sxs-lookup"><span data-stu-id="22f94-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="22f94-110">В следующих двух сценариях не требуется публиковать расширение в магазине надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22f94-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="22f94-111">Расширения, распространяемых с помощью корпоративной политики.</span><span class="sxs-lookup"><span data-stu-id="22f94-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="22f94-112">Использование распакованных каталогов расширений на локальном компьютере, когда Microsoft Edge находится в режиме разработчика.</span><span class="sxs-lookup"><span data-stu-id="22f94-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <span data-ttu-id="22f94-113">Обновления расширений</span><span class="sxs-lookup"><span data-stu-id="22f94-113">Updates to extensions</span></span>

<span data-ttu-id="22f94-114">Браузер Microsoft Edge периодически проверяет наличие новых версий установленных расширений и обновляет каждую из них без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="22f94-114">The Microsoft Edge browser periodically checks for new versions of installed extensions and updates each without user intervention.</span></span>  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Расширения — надстройки программы | Майкрософт"  

> [!NOTE]
> <span data-ttu-id="22f94-116">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22f94-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="22f94-117">Здесь находится исходная [страница.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="22f94-117">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="22f94-119">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="22f94-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
