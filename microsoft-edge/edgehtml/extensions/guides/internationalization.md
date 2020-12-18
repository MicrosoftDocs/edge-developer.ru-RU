---
description: Сделайте расширение доступным для разных языков и протестировать языковые строки с помощью руководства по международной глобализации.
title: Расширения — internationalization
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbbc847ebd2103cba2eca8a791009b4e72f93a6f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235732"
---
# <span data-ttu-id="0c601-104">Интернационализация</span><span class="sxs-lookup"><span data-stu-id="0c601-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="0c601-105">Чтобы ваше расширение было доступно множеству разных людей, важно иметь в виду другие страны.</span><span class="sxs-lookup"><span data-stu-id="0c601-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="0c601-106">Расширения Microsoft Edge позволяют добавлять в расширения разные языковые строки, чтобы их язык можно было легко изменить.</span><span class="sxs-lookup"><span data-stu-id="0c601-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="0c601-107">Дополнительные сведения о международной глобализации расширения можно [](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)узнать в руководстве по международной глобализации MDN.</span><span class="sxs-lookup"><span data-stu-id="0c601-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="0c601-108">Тестирование языков</span><span class="sxs-lookup"><span data-stu-id="0c601-108">Testing languages</span></span>

<span data-ttu-id="0c601-109">Чтобы протестировать языковые строки, сначала необходимо установить язык отображения Windows для языка, для который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="0c601-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="0c601-110">Чтобы изменить язык отображения Windows, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0c601-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="0c601-111">Откройте приложение "Параметры".</span><span class="sxs-lookup"><span data-stu-id="0c601-111">Open the Settings app.</span></span>

   ![приложение параметров](./../media/loc-settings.png)
2. <span data-ttu-id="0c601-113">Выберите "Время & языка".</span><span class="sxs-lookup"><span data-stu-id="0c601-113">Select "Time & language".</span></span>
3. <span data-ttu-id="0c601-114">Выберите "Язык & региона".</span><span class="sxs-lookup"><span data-stu-id="0c601-114">Select "Region & language".</span></span>
4. <span data-ttu-id="0c601-115">Выберите "+ Добавить язык", чтобы добавить язык в список возможных языков.</span><span class="sxs-lookup"><span data-stu-id="0c601-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="0c601-116">Выберите язык из списка "Языки", который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="0c601-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="0c601-117">Выберите кнопку "По умолчанию" (может потребоваться перезапустить компьютер).</span><span class="sxs-lookup"><span data-stu-id="0c601-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="0c601-118">Откройте Microsoft Edge и убедитесь, что строки, определенные для этого региональных точки, отображаются ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="0c601-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="0c601-119">С помощью свойства [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) можно проверить правильность языка, который Microsoft Edge определил как язык отображения Windows.</span><span class="sxs-lookup"><span data-stu-id="0c601-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="0c601-120">Нажмите кнопку в CodePen ниже, чтобы увидеть язык отображения браузера.</span><span class="sxs-lookup"><span data-stu-id="0c601-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="0c601-121">Получить региональные органы</span><span class="sxs-lookup"><span data-stu-id="0c601-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="0c601-122">См. <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> локаль получения </a> пера msEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> </a> @MSEdgeDev) на <a href='http://codepen.io'> </a> CodePen.</span><span class="sxs-lookup"><span data-stu-id="0c601-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
