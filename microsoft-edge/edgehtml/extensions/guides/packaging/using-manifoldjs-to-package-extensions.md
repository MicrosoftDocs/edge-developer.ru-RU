---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Узнайте, как упаковить расширение Microsoft Edge в оснастку с помощью ManifoldJS, Node.js с открытым исходным кодом.
title: Использование ManifoldJS для расширений пакетов
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 151a8b2ababb25e0964a6fbc2696b5fdc059d084
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235697"
---
# <span data-ttu-id="dc2f6-104">Использование ManifoldJS для создания пакетов AppX расширения</span><span class="sxs-lookup"><span data-stu-id="dc2f6-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="dc2f6-105">ManifoldJS — это средство с открытым исходным кодом Node.js, которое позволяет быстро и безболезненно создать пакет, который затем можно использовать для отправки в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="dc2f6-106">Если в расширении используется собственный обмен сообщениями, следует пропустить указанную ниже статью и перейти к инструктативу упаковки сообщений [Native в Microsoft Edge.](../native-messaging.md#creating-an-extension-with-native-messaging)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="dc2f6-107">Перед началом работы вам по-прежнему потребуется ознакомиться со следующими статьями.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="dc2f6-108">Расширения в Центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="dc2f6-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="dc2f6-109">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="dc2f6-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="dc2f6-110">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="dc2f6-111">После создания, упаковки и тестирования расширения отправьте запрос на форму отправки [расширения.](https://developer.microsoft.com/microsoft-edge/extensions/requests)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="dc2f6-112">Установка Node.js и ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="dc2f6-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="dc2f6-113">В первую очередь необходимо установитьNode.js [LTS.](https://nodejs.org/en/download)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="dc2f6-114">После запуска Node в командной строке (предпочтительно в PowerShell) запустите следующую команду, чтобы установить ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="dc2f6-115">Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="dc2f6-116">Если manifoldJS не распознан, добавьте `%APPDATA%\npm` в переменные PATH.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="dc2f6-117">Упаковка с помощью ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="dc2f6-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="dc2f6-118">Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначения для упакованного расширения.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="dc2f6-119">Например:</span><span class="sxs-lookup"><span data-stu-id="dc2f6-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="dc2f6-120">Команда `manifoldjs` выводит данные в текущем каталоге и переописает содержимое.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="dc2f6-121">Теперь, когда вы находитесь в папке назначения, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="dc2f6-122">Команду `mainifoldjs` можно разбить на следующие части.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc2f6-123">Изменяет уровень журнала для `debug` получения полной распечатки.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc2f6-124">Задает единственную платформу, на которой будет запускаться `edgeextension` преобразование.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc2f6-125">Сообщает программе, что формат манифеста является форматом и не нужно действовать, если он не `edgeextension` удается получить проверку.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="dc2f6-126">Путь к манифесту расширения, который необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="dc2f6-127">После завершения работы ManifoldJS у вас будет папка со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...
-->  

<span data-ttu-id="dc2f6-128">Файл generationInfo.jsэто журнал, который был выпущен с помощью ManifoldJS и не будет включен в пакет расширения.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="dc2f6-129">Будет упаковано только `manifest` содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="dc2f6-130">В папке манифеста папка Assets содержит изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке Extension есть содержимое расширения.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="dc2f6-131">Теперь, когда у вас есть правильные файлы, необходимо изменить созданный файл AppXManifest в `manifest` папке.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="dc2f6-132">Если имя файла manifest.jsрасширение содержит международное строку для поля "name", то после запуска ManifoldJS имя папки верхнего уровня не будет иметь подчеркивания и будет включать "MSG".</span><span class="sxs-lookup"><span data-stu-id="dc2f6-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="dc2f6-133">Например, manifest.jsфайл со следующим `"name"` полем.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="dc2f6-134">будет иметь папку манифеста, в которую она будет `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` вложена.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="dc2f6-135">В файле AppXManifest необходимо:</span><span class="sxs-lookup"><span data-stu-id="dc2f6-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="dc2f6-136">Замените необходимые поля Identity и PublisherDisplayName, как [описано здесь.](./creating-and-testing-extension-packages.md#app-identity-template-values)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="dc2f6-137">Обратите внимание, что если упаковка предназначена только для тестирования или корпоративного распространения, можно использовать значения-заметивы вместо регистрации для учетной записи Центра разработчиков для Windows.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="dc2f6-138">Замените значки-замещания в папке Assets значками для расширения одинаковыми размерами (150x150, 50x50, 44x44) и именами.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="dc2f6-139">Сведения о [том,](./../design.md#icons-for-packaging) где используются эти значки, см. в руководстве по проектированию.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="dc2f6-140">Если расширение локализовано, следуйте всему руководству [по локализации расширений Microsoft Edge.](./localizing-extension-packages.md)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="dc2f6-141">Если она не локализована, ознакомьтесь только с именем и описанием [локализации в разделе Microsoft Store.](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="dc2f6-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="dc2f6-142">После `appxmanifest.xml` сортировки файла запустите следующую команду, чтобы создать пакет.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="dc2f6-143">Теперь пакет будет находится в папке **пакета,** расположенной в папке edgeextension.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="dc2f6-144">Дополнительные сведения о загрузке неогрузки нового пакета см. в разделе [тестирования](./creating-and-testing-extension-packages.md#testing-an-appx-package) пакета создания и тестирования расширений.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="dc2f6-145">После тестирования пакета вы можете отправить запрос на [](https://aka.ms/extension-request) форму отправки расширения, чтобы его можно было отправить на публикацию в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="dc2f6-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  
