---
description: Переопределения — это функция в средстве Sources Microsoft Edge DevTools, которая позволяет копировать ресурсы веб-страницы на жесткий диск.  При обновлении веб-страницы DevTools не загружает ресурс, а заменяет его локальной копией.
title: Переопределять ресурсы веб-страницы с локальными копиями с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230966"
---
# <span data-ttu-id="30cc2-105">Переопределять ресурсы веб-страницы с локальными копиями с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="30cc2-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="30cc2-106">Иногда требуется устранить проблему на веб-странице, к которую у вас нет доступа или исправления, которая связана с медленным и сложным процессом сборки.</span><span class="sxs-lookup"><span data-stu-id="30cc2-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="30cc2-107">Вы можете отладить и устранить все виды проблем в DevTools.</span><span class="sxs-lookup"><span data-stu-id="30cc2-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="30cc2-108">Но проблема заключается в том, что изменения не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="30cc2-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="30cc2-109">После обновления файла все ваши трудоемкие работы не будут работать.</span><span class="sxs-lookup"><span data-stu-id="30cc2-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="30cc2-110">Эта проблема решается [][DevToolsSourcesTool] с помощью функции "Переопределения" в средстве "Источники".</span><span class="sxs-lookup"><span data-stu-id="30cc2-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="30cc2-111">Теперь можно взять ресурс текущей веб-страницы и сохранить его локально.</span><span class="sxs-lookup"><span data-stu-id="30cc2-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="30cc2-112">При обновлении веб-страницы браузер не загружает ресурс с сервера.</span><span class="sxs-lookup"><span data-stu-id="30cc2-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="30cc2-113">Вместо этого браузер заменяет его локальной копией ресурса.</span><span class="sxs-lookup"><span data-stu-id="30cc2-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="30cc2-114">Настройка локальной папки для хранения переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="30cc2-115">В **средстве "Источники"** найдите несколько разделов слева.</span><span class="sxs-lookup"><span data-stu-id="30cc2-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="30cc2-116">Если параметр **"Переопределения"** не отображается, выберите параметр</span><span class="sxs-lookup"><span data-stu-id="30cc2-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="30cc2-117">значок для получения.</span><span class="sxs-lookup"><span data-stu-id="30cc2-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Средство источников с недостаточно местом для показа параметра переопределения" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="30cc2-119">**Средство** источников с недостаточно местом для показа параметра переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Выбор параметра переопределения" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="30cc2-121">Выбор параметра переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="30cc2-122">После выбора параметра **"Переопределения"** необходимо выбрать папку на локальном компьютере для хранения файлов ресурсов, которые необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="30cc2-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="30cc2-123">Выберите **папку +Select для переопределения** для поиска папки.</span><span class="sxs-lookup"><span data-stu-id="30cc2-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Выбор папки для переопределения" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="30cc2-125">Выбор папки для переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30cc2-126">DevTools предупреждает о том, что необходимо иметь полный доступ к папке и не раскрывать конфиденциальную информацию.</span><span class="sxs-lookup"><span data-stu-id="30cc2-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="30cc2-127">На панели предупреждений выберите **"Разрешить** предоставление доступа".</span><span class="sxs-lookup"><span data-stu-id="30cc2-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="предоставление DevTools доступа к папке" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="30cc2-129">Предоставление DevTools доступа к папке</span><span class="sxs-lookup"><span data-stu-id="30cc2-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30cc2-130">В области **"Переопределения"** рядом с папкой "Переопределения" должен отобразиться этот `Enable Local Overrides` почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="30cc2-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="30cc2-131">Рядом с ней отображается значок, позволяющий удалить локальные параметры переопределения.</span><span class="sxs-lookup"><span data-stu-id="30cc2-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="30cc2-132">Теперь вы закончили настройку папки и готовы заменить живые ресурсы локальными.</span><span class="sxs-lookup"><span data-stu-id="30cc2-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Успешная настройка папки переопределения" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="30cc2-134">Успешная настройка папки переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="30cc2-135">Добавление файлов в папку Overrides</span><span class="sxs-lookup"><span data-stu-id="30cc2-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="30cc2-136">Чтобы добавить файлы в папку overrides, откройте средство **"Элементы"** и проверьте веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="30cc2-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="30cc2-137">Чтобы изменить, выберите имя CSS-файла в **инспекторе стилей.**</span><span class="sxs-lookup"><span data-stu-id="30cc2-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Выбор файла в инспекторе стилей" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="30cc2-139">Выбор файла в инспекторе **стилей**</span><span class="sxs-lookup"><span data-stu-id="30cc2-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="30cc2-140">В **редакторе источников** наведите курсор на имя выбранного файла, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить для **переопределеев".**</span><span class="sxs-lookup"><span data-stu-id="30cc2-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="В редакторе источников добавьте имя файла для переопределения" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="30cc2-142">В **редакторе источников** добавьте имя файла для переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="В контекстное меню выберите "Сохранить для переопределеения"" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="30cc2-144">В контекстное меню выберите **"Сохранить для переопределеения"**</span><span class="sxs-lookup"><span data-stu-id="30cc2-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="30cc2-145">Файл хранится в папке overrides.</span><span class="sxs-lookup"><span data-stu-id="30cc2-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="30cc2-146">Убедитесь, что DevTools создает папку с именем, используя URL-адрес файла с правильной структурой каталогов.</span><span class="sxs-lookup"><span data-stu-id="30cc2-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="30cc2-147">Файл хранится внутри.</span><span class="sxs-lookup"><span data-stu-id="30cc2-147">The file is stored inside.</span></span>  <span data-ttu-id="30cc2-148">Имя файла в редакторе теперь также показывает сиреневую точку, которая указывает, что файл является локальным, а не live.</span><span class="sxs-lookup"><span data-stu-id="30cc2-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Файл успешно сохранен в папке переопределения" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="30cc2-150">Файл успешно сохранен в папке переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="30cc2-151">В следующем примере можно изменить стили веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="30cc2-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="30cc2-152">Чтобы добавить красная граница вокруг файла, в редакторе стилей скопируйте следующий стиль и добавьте его в элемент body. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="30cc2-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="30cc2-153">Файл автоматически сохранен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="30cc2-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="30cc2-154">Если обновить файл, отобразится граница, и ни одна из ваших работ не будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="30cc2-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Постоянное изменение стилей веб-страниц путем редактирования файла в папке overrides" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="30cc2-156">Постоянное изменение стилей веб-страниц путем редактирования файла в папке overrides</span><span class="sxs-lookup"><span data-stu-id="30cc2-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="30cc2-157">В **средстве "Источники"** в разделе "Страница" наведите курсор на любой файл, откройте контекстное меню \(щелкните правой кнопкой мыши\) и добавьте его в переопределения. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="30cc2-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="30cc2-158">Опять же, файлы, которые уже находятся в папке переопределения, имеют сиреневую точку на значке.</span><span class="sxs-lookup"><span data-stu-id="30cc2-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Выбор файла в средстве "Источники" для переопределения" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="30cc2-160">Выбор файла в средстве **"Источники"** для переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="30cc2-161">Кроме того, в средстве **"Сеть"** наведите курсор на любой файл, откройте контекстное меню \(щелкните правой кнопкой мыши\) и добавьте его в переопределения.</span><span class="sxs-lookup"><span data-stu-id="30cc2-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="30cc2-162">Если переопределения имеются, файлы, расположенные на компьютере, а не с веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="30cc2-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="30cc2-163">Когда переопределения вступили в силу, в средстве **"Сеть"** найдите значок предупреждения рядом с именем файла.</span><span class="sxs-lookup"><span data-stu-id="30cc2-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Выбор файла в средстве "Сеть" для переопределения" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="30cc2-165">Выбор файла в средстве **"Сеть"** для переопределения</span><span class="sxs-lookup"><span data-stu-id="30cc2-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="30cc2-166">Двухнабное взаимодействие переопределеев</span><span class="sxs-lookup"><span data-stu-id="30cc2-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="30cc2-167">Используйте редактор, предоставленный с помощью средства **"Источники"** DevTools или любого редактора, который вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="30cc2-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="30cc2-168">Изменения синхронизируются во всех продуктах, которые имеют доступ к файлам в папке overrides.</span><span class="sxs-lookup"><span data-stu-id="30cc2-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="30cc2-169">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="30cc2-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Обзор средства "Источники" | Документы Майкрософт"  
