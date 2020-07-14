---
description: Узнайте, как добавлять и удалять расширения, а также переместить кнопку расширения рядом с адресной строкой.
title: Добавление и удаление расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик, расширение
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: aeebc0f18d6b4a743c790571b8287a209233e73f
ms.sourcegitcommit: 1e33cd41e5afb2e6dbdc19353011ff6c2b019f9c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2020
ms.locfileid: "10866080"
---
# <span data-ttu-id="d8f5c-104">Добавление, перемещение и удаление расширений для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d8f5c-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="d8f5c-105">Служба поддержки Microsoft Edge для расширений была представлена в **Юбилейном обновлении Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="d8f5c-106">Если вы разрабатываете и хотите загрузить расширение Microsoft Edge или если оно у вас уже есть и вы хотите его удалить, ознакомьтесь с приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="d8f5c-107">Кроме того, в этой статье рассказано о том, как изменить расположение значка расширения в браузере.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="d8f5c-108">Добавление расширения</span><span class="sxs-lookup"><span data-stu-id="d8f5c-108">Adding an extension</span></span>

1. <span data-ttu-id="d8f5c-109">Откройте Microsoft Edge и напечатайте "about:flags" в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="d8f5c-110">Установите флажок в пункте **Разрешить функции для разработчиков расширения**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![about:flags — включение функций для разработчиков](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="d8f5c-112">Если у вас нет юбилейного обновления Windows10 или более поздней версии, этот параметр будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="d8f5c-113">Нажмите **Другие (...)**, чтобы открыть меню.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-113">Select **More (...)** to open the menu.</span></span>

   ![кнопка другие](./../media/morebutton.png)  

4. <span data-ttu-id="d8f5c-115">В меню щелкните пункт **Расширения**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="d8f5c-116">Нажмите кнопку **Отправить расширение**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-116">Select the **Load extension** button.</span></span>

   ![нажатие кнопки отправить расширение](./../media/sideload-load-extension.png)

6. <span data-ttu-id="d8f5c-118">Перейдите в папку вашего расширения и нажмите кнопку  **Выбрать папку**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![выбор папки расширения для отправки](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="d8f5c-120">Если при отправке расширения появляется сообщение об ошибке, см. статью [Устранение неполадок](./../troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="d8f5c-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="d8f5c-121">Готово!</span><span class="sxs-lookup"><span data-stu-id="d8f5c-121">You're all set!</span></span> <span data-ttu-id="d8f5c-122">Теперь вы увидите ваше расширение в списке в области расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![расширение в области расширений](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="d8f5c-124">Неподписанные расширения автоматически отключаются при последующих запусках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="d8f5c-125">Когда браузер переходит в состояние простоя (приблизительно после 10сек. бездействия), в нижней части окна выводится следующее уведомление.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="d8f5c-126">рискованное уведомление](./../media/riskynotification.png) Чтобы включить неподписанные расширения, щелкните "Все равно включить".</span><span class="sxs-lookup"><span data-stu-id="d8f5c-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="d8f5c-127">Перемещение кнопки расширения</span><span class="sxs-lookup"><span data-stu-id="d8f5c-127">Moving the extension button</span></span>
<span data-ttu-id="d8f5c-128">В зависимости от параметров вашего расширения оно может отобразиться в меню **Другие (...)**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![меню действий](./../media/browseraction.png)  


<span data-ttu-id="d8f5c-130">Если вы хотите для удобства переместить кнопку из этого меню, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="d8f5c-131">Щелкните кнопку расширения правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="d8f5c-132">Нажмите кнопку **Показывать кнопку рядом с адресной строкой**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-132">Select **Show button next to address bar**.</span></span>

   ![меню действий](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="d8f5c-134">Это можно сделать также на странице "Сведения о расширении".</span><span class="sxs-lookup"><span data-stu-id="d8f5c-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="d8f5c-135">Щелкните кнопку расширения.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-135">Click on the extension button.</span></span>
2. <span data-ttu-id="d8f5c-136">Поставьте переключатель **Показывать кнопку рядом с адресной строкой** в положение "Вкл.".</span><span class="sxs-lookup"><span data-stu-id="d8f5c-136">Toggle **Show button next to address bar** to on.</span></span>

   ![показать включенный переключатель для кнопки](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="d8f5c-138">Эту кнопку в любое время можно вернуть обратно в меню **Другие (...)**, щелкнув ее правой кнопкой мыши и отменив выбор элемента **Показывать рядом с адресной строкой**, или поставив в положение "Выкл." переключатель **Показывать кнопку рядом с адресной строкой** на странице сведений о расширении.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="d8f5c-139">Удаление расширения</span><span class="sxs-lookup"><span data-stu-id="d8f5c-139">Removing an extension</span></span>

1. <span data-ttu-id="d8f5c-140">Откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="d8f5c-141">Нажмите **Другие (...)**, чтобы открыть меню.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="d8f5c-142">В меню щелкните пункт **Расширения**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="d8f5c-143">Щелкните правой кнопкой мыши расширение, которое вы хотите удалить, и выберите **Удалить** или выделите расширение и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![меню действий](./../media/remove.png)  

**<span data-ttu-id="d8f5c-145">Расширение должно исчезнуть из списка в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8f5c-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
