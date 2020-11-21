---
description: Функции, добавленные в Microsoft EDGE (Chromium) DevTools 2019 марта
title: Новые возможности Microsoft EDGE (Chromium) DevTools 2019 марта
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182514"
---
# <span data-ttu-id="128e1-104">Новые возможности Microsoft EDGE (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="128e1-104">What's new in the Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="128e1-105">Благодарим вас за попытку предварительной версии новой версии Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="128e1-105">Thank you so much for trying out a preview of the new Microsoft Edge!</span></span> <span data-ttu-id="128e1-106">В этом выпуске мы решили крупную смену на базовой веб-платформе Microsoft EDGE, принимая проект Chromium Open Source.</span><span class="sxs-lookup"><span data-stu-id="128e1-106">With this release, we've undertaken a major shift in the underlying web platform of Microsoft Edge by adopting the Chromium open source project.</span></span> <span data-ttu-id="128e1-107">Благодаря этому изменению вы сможете легко создавать и тестировать веб-сайты в Microsoft EDGE и гарантировать, что они будут работать должным образом даже в том случае, если пользователи просматривают другие браузеры на базе Chromium, например Google Chrome, Vivaldi, Opera или Brave.</span><span class="sxs-lookup"><span data-stu-id="128e1-107">With this change, it will be easier for you to build and test your web sites in Microsoft Edge and ensure they will still work as expected even if your users are browsing in a different Chromium-based browser, like Google Chrome, Vivaldi, Opera, or Brave.</span></span>

## <span data-ttu-id="128e1-108">Новый Microsoft EDGE (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="128e1-108">The new Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="128e1-109">Если вы выйдете из Microsoft EDGE и вы в основном разрабатываете в Chromium-браузере, вам нужно прямо дома.</span><span class="sxs-lookup"><span data-stu-id="128e1-109">If you are checking out Microsoft Edge and you mainly develop in a Chromium-based browser, you should feel right at home.</span></span> <span data-ttu-id="128e1-110">Средства разработчика Microsoft EDGE (Chromium) в точности похожи на средства разработчика, которые вы уже знаете и используете.</span><span class="sxs-lookup"><span data-stu-id="128e1-110">The Microsoft Edge (Chromium) Developer Tools are exactly like the developer tools you already know and use!</span></span>

![Microsoft EDGE (Chromium) DevTools](./media/devtools.png)

<span data-ttu-id="128e1-112">Если вы извлечете новый Microsoft EDGE, и вы в основном разрабатывали в Microsoft EDGE (EdgeHTML), мы получили новые средства, которые мы надеемся, чтобы упростить и быстрее создавать и тестировать веб-сайты в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="128e1-112">If you are checking out the new Microsoft Edge and you mainly developed in Microsoft Edge (EdgeHTML), we have got some great new tools that we hope will make it easier and faster for you to build and test your web sites in Microsoft Edge!</span></span> <span data-ttu-id="128e1-113">Чтобы узнать больше об этих новых средствах, ознакомьтесь [со статьей руководство по DevTools Microsoft EDGE (Chromium)](../devtools-guide-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="128e1-113">To learn more about these new tools, check out [The Microsoft Edge (Chromium) DevTools Guide](../devtools-guide-chromium.md).</span></span>

## <span data-ttu-id="128e1-114">Новые темные и легкие темы для DevTools</span><span class="sxs-lookup"><span data-stu-id="128e1-114">New dark and light themes for the DevTools</span></span>

<span data-ttu-id="128e1-115">Мы разработали новые темные и легкие темы для DevTools, которые мы будем рады тебе!</span><span class="sxs-lookup"><span data-stu-id="128e1-115">We've designed some new dark and light themes for the DevTools that we think you'll love!</span></span> <span data-ttu-id="128e1-116">По умолчанию в Microsoft EDGE (Chromium) DevTools будет использоваться темная тема.</span><span class="sxs-lookup"><span data-stu-id="128e1-116">By default, the Microsoft Edge (Chromium) DevTools will use the Dark theme.</span></span> <span data-ttu-id="128e1-117">Чтобы изменить тему DevTools, нажмите `Fn`  +  `F1` кнопку в правом верхнем углу окна DevTools на панели Windows или Mac или перейдите к пункту параметры с помощью `...` кнопки.</span><span class="sxs-lookup"><span data-stu-id="128e1-117">To change the theme of the DevTools, press `Fn` + `F1` on Windows or Mac or navigate to Settings using the `...` button in the top right corner of the DevTools.</span></span>

![Главное меню Microsoft EDGE (Chromium) DevTools](./media/devtools-main-menu.png)

<span data-ttu-id="128e1-119">Из параметров можно изменить тему DevTools.</span><span class="sxs-lookup"><span data-stu-id="128e1-119">From Settings, you can change the theme of the DevTools.</span></span> <span data-ttu-id="128e1-120">Если вы изменили способ, которым DevTools просмотрел в браузере на основе Chromium, вы можете сделать так, чтобы Microsoft EDGE (Chromium) DevTools точно так же, как и в случае выбора **темной темы (Chromium)** или **света (Chromium)** соответственно.</span><span class="sxs-lookup"><span data-stu-id="128e1-120">If you liked the way the DevTools looked in your Chromium-based browser, you can make the Microsoft Edge (Chromium) DevTools look exactly like them by selecting the **Dark (Chromium)** or **Light (Chromium)** themes respectively.</span></span> 

## <span data-ttu-id="128e1-121">Отладка Microsoft EDGE (Chromium) из кода VS</span><span class="sxs-lookup"><span data-stu-id="128e1-121">Debug Microsoft Edge (Chromium) from VS Code</span></span>

<span data-ttu-id="128e1-122">С помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS вы можете отлаживать как Microsoft EDGE (EdgeHTML), так и Microsoft EDGE (Chromium) прямо из кода VS!</span><span class="sxs-lookup"><span data-stu-id="128e1-122">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can now debug both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium) directly from VS Code!</span></span>

![Отладчик для расширения кода пограничных и других кодов](./media/vscode-debugger.png)

<span data-ttu-id="128e1-124">Чтобы запустить Microsoft EDGE (Chromium) вместо Microsoft EDGE (EdgeHTML) из кода VS, необходимо добавить `version` атрибут к существующему **launch.js** конфигурации с версией Microsoft EDGE (Chromium), которую вы хотите запустить ( `dev` `beta` или `canary` ).</span><span class="sxs-lookup"><span data-stu-id="128e1-124">To launch Microsoft Edge (Chromium) instead of Microsoft Edge (EdgeHTML) from VS Code, you need to add a `version` attribute to your existing **launch.json** configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="128e1-125">Ниже приведен пример **launch.js** конфигурации, которая запускает Канарские версию Microsoft EDGE (Chromium) до [Bing.com](https://www.bing.com/):</span><span class="sxs-lookup"><span data-stu-id="128e1-125">Here's a sample **launch.json** configuration that will launch the Canary version of Microsoft Edge (Chromium) to [bing.com](https://www.bing.com/):</span></span>

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

<span data-ttu-id="128e1-126">Дополнительные сведения [об отладке Microsoft EDGE (Chromium) из кода VS можно](../visual-studio-code/debugger-for-edge.md)найти в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="128e1-126">For more information, check out [how to debug Microsoft Edge (Chromium) from VS Code](../visual-studio-code/debugger-for-edge.md).</span></span>

## <span data-ttu-id="128e1-127">Обновление протокола пограничного DevTools</span><span class="sxs-lookup"><span data-stu-id="128e1-127">Edge DevTools Protocol update</span></span>

<span data-ttu-id="128e1-128">При смене базовой веб-платформы Microsoft Edge протокол пограничного DevTools не получит никаких обновлений.</span><span class="sxs-lookup"><span data-stu-id="128e1-128">With the shift in the underlying web platform of Microsoft Edge, the Edge DevTools Protocol will not be receiving any further updates.</span></span> <span data-ttu-id="128e1-129">DevTools Microsoft EDGE (Chromium) будет использовать протокол DevTools или CDP для Chrome.</span><span class="sxs-lookup"><span data-stu-id="128e1-129">The Microsoft Edge (Chromium) DevTools will use the Chrome DevTools Protocol or CDP.</span></span> <span data-ttu-id="128e1-130">Для получения справочной документации по доменам и методам в CDP ознакомьтесь со [средством просмотра CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span><span class="sxs-lookup"><span data-stu-id="128e1-130">To reference documentation on the domains and methods in CDP, please refer to [the CDP viewer](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span></span>

<span data-ttu-id="128e1-131">В новой Microsoft Edge все методы с префиксами, которые `ms` не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="128e1-131">In the new Microsoft Edge, any methods that are prefixed with `ms` will not be supported.</span></span> <span data-ttu-id="128e1-132">Чтобы узнать больше о том, как использовать CDP в Microsoft EDGE (Chromium), обратитесь к разделу [протокол DevTools (Chromium)](../devtools-protocol-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="128e1-132">To learn more about how to use CDP in Microsoft Edge (Chromium), please refer to [DevTools Protocol (Chromium)](../devtools-protocol-chromium.md).</span></span>

## <span data-ttu-id="128e1-133">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="128e1-133">Known issues</span></span>

<span data-ttu-id="128e1-134">Многие ссылки с веб-сайтов Microsoft EDGE (Chromium) DevTools на содержимое, размещенное на сторонних сайтах, временно удалены.</span><span class="sxs-lookup"><span data-stu-id="128e1-134">Many links from the Microsoft Edge (Chromium) DevTools to content hosted on third-party sites have been removed temporarily.</span></span> <span data-ttu-id="128e1-135">Как только мы сможем заменить эти ссылки, мы добавим их обратно в DevTools.</span><span class="sxs-lookup"><span data-stu-id="128e1-135">As soon as we can replace these links, we will add them back to the DevTools.</span></span>


<span data-ttu-id="128e1-136">При отладке веб-содержимого на устройстве Android из Microsoft EDGE (Chromium) версия DevTools, которая запускается при нажатии кнопки " **проверить** **", может** не совпадать с версией браузера на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="128e1-136">When debugging web content on an Android device from Microsoft Edge (Chromium), the version of the DevTools that launches when you click the **Inspect** button from the **Remote devices** tool may not match the version of the browser on your Android device.</span></span> <span data-ttu-id="128e1-137">В результате в DevTools могут отображаться новые возможности, которые не будут работать в браузере на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="128e1-137">As a result, you may see new features in the DevTools that will not work against the browser on your Android device.</span></span> <span data-ttu-id="128e1-138">Если вы столкнулись с вашим мнением, мы будем рады узнать о нем, чтобы получить [отзыв о файле](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="128e1-138">If this is something you encounter, we'd love to hear about it so please [file feedback](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>

<span data-ttu-id="128e1-139">Наконец, Visual Studio для Windows и Mac пока не поддерживает Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="128e1-139">Finally, Visual Studio on Windows and Mac does not yet support Microsoft Edge (Chromium).</span></span> <span data-ttu-id="128e1-140">Зарегистрируйтесь [здесь](https://visualstudio.microsoft.com/vs/preview/) , чтобы узнать, когда у нас есть ознакомительная версия Visual Studio, поддерживающая отладку JavaScript в Microsoft EDGE (Chromium) для проектов ASP.NET!</span><span class="sxs-lookup"><span data-stu-id="128e1-140">Sign up [here](https://visualstudio.microsoft.com/vs/preview/) to be the first to know when we have a preview version of Visual Studio that supports JavaScript debugging inside Microsoft Edge (Chromium) for ASP.NET projects!</span></span>  
