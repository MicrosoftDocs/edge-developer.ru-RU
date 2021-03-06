---
description: Узнайте, как локализовать пакет расширений Microsoft Edge, чтобы он был готов к нескольким локальным данным после выпуска.
title: Локализация пакетов расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, web development, html, css, javascript, developer
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397722"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a><span data-ttu-id="e5396-104">Локализация расширений Microsoft Edge для Windows и Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="e5396-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="e5396-105">В этом руководстве понаблизовать, как локализовать расширение Microsoft Edge, чтобы оно было готово для нескольких локалов после выпуска.</span><span class="sxs-lookup"><span data-stu-id="e5396-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span>  <span data-ttu-id="e5396-106">Чтобы полностью локализовать расширение, необходимо выполнять действия, как для Windows, так и для Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e5396-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="e5396-107">Если вы хотите локализовать ресурсы расширения для Microsoft Edge, вы можете узнать, как использовать рамки i18n в руководстве [по интернационализации.](../internationalization.md)</span><span class="sxs-lookup"><span data-stu-id="e5396-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="e5396-108">Если расширение не поддерживает несколько языков, можно перейти к локализации имени и [описания в Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="e5396-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

## <a name="the-localization-process-overview"></a><span data-ttu-id="e5396-109">Обзор процесса локализации</span><span class="sxs-lookup"><span data-stu-id="e5396-109">The localization process overview</span></span>  

<span data-ttu-id="e5396-110">Первым шагом к тому, чтобы расширение было доступно широкой аудитории, является настройка [приложения AppxManifest](#configuring-the-appxmanifest) для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="e5396-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span>  <span data-ttu-id="e5396-111">В Microsoft Store пользователи покажут, на каких языках поддерживается расширение.</span><span class="sxs-lookup"><span data-stu-id="e5396-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span>  <span data-ttu-id="e5396-112">Некоторые поля в AppxManifest также необходимо изменить, если требуется локализовать имя вашего расширения в пользовательском интерфейсе Windows и [Microsoft Store.](#localizing-extension-resources-for-windows-and-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="e5396-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>  

<span data-ttu-id="e5396-113">После настройки AppxManifest необходимо создать ресурсы [строк JSON](#creating-json-string-resources) для языков, которые были указаны как поддерживаемые.</span><span class="sxs-lookup"><span data-stu-id="e5396-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span>  <span data-ttu-id="e5396-114">Для этого необходимо создать файл для каждого языка, в котором в каждом файле есть все строки пользовательского интерфейса `.resjson` этого языка.</span><span class="sxs-lookup"><span data-stu-id="e5396-114">This requires creating a `.resjson` file for each language, where each file has all the UI strings of that language within it.</span></span>  

<span data-ttu-id="e5396-115">После создания файлов для поддерживаемых языков потребуется создать `.resjson` [файл ресурсов .pri.](#creating-the-resources-file)</span><span class="sxs-lookup"><span data-stu-id="e5396-115">After the `.resjson` files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="e5396-116">Это будет создано с помощью файла конфигурации для средства MakePRI, который поставляется с [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="e5396-116">This will be created by using a configuration file to the MakePRI tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>  

> [!NOTE]
> <span data-ttu-id="e5396-117">Если вы скачиваете SDK Windows 10 только для использования этого средства, вы можете выбрать только средства подписи Windows SDK для настольных приложений и windows SDK для функций управляемых приложений `MakePri.exe` **UWP,** чтобы сохранить зажигалку загрузки. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e5396-117">If you are only downloading the Windows 10 SDK to use the `MakePri.exe` tool, you can select only the **Windows SDK Signing Tools for Desktop Apps** and **Windows SDK for UWP Managed App** features to keep the download lighter.</span></span>  <span data-ttu-id="e5396-118">Средство `MakePri.exe` будет отображаться в подмостки `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .</span><span class="sxs-lookup"><span data-stu-id="e5396-118">The `MakePri.exe` tool will appear in subfolders of `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0`.</span></span>  

<span data-ttu-id="e5396-119">После отправки расширения последний шаг — локализовать имя и [описание в Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)</span><span class="sxs-lookup"><span data-stu-id="e5396-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

> [!NOTE]
> <span data-ttu-id="e5396-120">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="e5396-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="e5396-121">**Связаться с нами** с вашими запросами на участие в Microsoft Store, и мы рассмотрим вас для будущего обновления.</span><span class="sxs-lookup"><span data-stu-id="e5396-121">**Reach out to us** with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>  

## <a name="configuring-the-appxmanifest"></a><span data-ttu-id="e5396-122">Настройка AppXManifest</span><span class="sxs-lookup"><span data-stu-id="e5396-122">Configuring the AppXManifest</span></span>  

<span data-ttu-id="e5396-123">Список поддерживаемых языков расширения в Microsoft Store создается на основе его значений AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-123">Your extension's Supported languages list in the Microsoft Store is generated based on its AppXManifest values.</span></span>  <span data-ttu-id="e5396-124">Этот список задан с помощью `Resource` элемента.</span><span class="sxs-lookup"><span data-stu-id="e5396-124">This list is specified using the `Resource` element.</span></span>  

![Сведения о приложении](../../media/language-app-details.png)  

<span data-ttu-id="e5396-126">Чтобы указать список языков, поддерживаемых расширением, можно добавить элемент в формате, приведенном ниже \(этот элемент будет поддерживать английский, немецкий и французский языки в `Resource` `Resource` Microsoft Store\):</span><span class="sxs-lookup"><span data-stu-id="e5396-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below \(this `Resource` element will show support for English, German, and French in the Microsoft Store\):</span></span>  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

<span data-ttu-id="e5396-127">Сведения о языках и языковых кодах, поддерживаемых Microsoft Store, см. в веб-сайте [Поддерживаемые](/windows/uwp/publish/supported-languages) языки.</span><span class="sxs-lookup"><span data-stu-id="e5396-127">See [Supported languages](/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>  

<span data-ttu-id="e5396-128">Чтобы указать локализованные строки для всех общедоступных элементов в AppxManifest, необходимо использовать идентификатор ресурса в формате `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="e5396-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>  

<span data-ttu-id="e5396-129">Фрагменты ниже делают полный AppxManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="e5396-130">Следующие значения должны быть извлечены из локализованных файлов ресурсов:</span><span class="sxs-lookup"><span data-stu-id="e5396-130">The following values should be retrieved from localized resource files:</span></span>  

*   <span data-ttu-id="e5396-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5396-131">Properties\DisplayName</span></span>  
*   <span data-ttu-id="e5396-132">Свойства\Описание</span><span class="sxs-lookup"><span data-stu-id="e5396-132">Properties\Description</span></span>  
*   <span data-ttu-id="e5396-133">Свойства\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="e5396-133">Properties\PublisherDisplayName</span></span>  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   <span data-ttu-id="e5396-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5396-134">Applications\Application\VisualElements\DisplayName</span></span>  
*   <span data-ttu-id="e5396-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="e5396-135">Applications\Application\VisualElements\Description</span></span>  
*   <span data-ttu-id="e5396-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5396-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>  

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```  

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a><span data-ttu-id="e5396-137">Локализация ресурсов расширения для Windows и Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="e5396-137">Localizing extension resources for Windows and the Microsoft Store</span></span>  

<span data-ttu-id="e5396-138">Теперь, когда приложение AppxManifest настроено на несколько языков, необходимо знать некоторые ключевые различия между локализализаем пользовательского интерфейса в расширении и локализализаем расширения для Windows и Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e5396-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="e5396-139">Несмотря на то, что расширения Microsoft Edge не работают вне Microsoft Edge, управление ими может происходить в Windows.</span><span class="sxs-lookup"><span data-stu-id="e5396-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span>  <span data-ttu-id="e5396-140">Например, пользователи могут управлять своими расширениями в приложении Параметры:</span><span class="sxs-lookup"><span data-stu-id="e5396-140">For example, users can manage their extensions in the Settings app:</span></span>  

![приложение параметров](../../media/settings.png)  

<span data-ttu-id="e5396-142">Имя расширения, отображаемого в приложении Параметры в Windows, происходит от AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span>  <span data-ttu-id="e5396-143">Если это значение жестко закодированно на английском языке, английская версия имени будет показываться на устройствах Windows, не в английском языке.</span><span class="sxs-lookup"><span data-stu-id="e5396-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span>  <span data-ttu-id="e5396-144">Если брендинг вашего расширения только на английском языке, его можно оставить в жестком коде.</span><span class="sxs-lookup"><span data-stu-id="e5396-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>  

> [!NOTE]
> <span data-ttu-id="e5396-145">Если вы хотите использовать локализованные имена для расширения Microsoft Edge в [](./extensions-in-the-windows-dev-center.md#name-reservation) Windows, убедитесь, что локализованные имена также доступны и зарезервированы перед внесением изменений в файле AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span>  <span data-ttu-id="e5396-146">Если имена не зарезервированы, вы получите следующую ошибку при отправке окончательного пакета в Центр разработчиков Windows:</span><span class="sxs-lookup"><span data-stu-id="e5396-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span>  
> 
> ![ошибка языка](../../media/language-error.png)  

<span data-ttu-id="e5396-148">Инфраструктура локализации на основе i18n, которая определена для расширений JavaScript, применима только в среде Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e5396-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>  

<span data-ttu-id="e5396-149">За пределами Microsoft Edge, в Windows и Microsoft Store, единственная поддерживаемая платформа локализации основана на платформе универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="e5396-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>  

<span data-ttu-id="e5396-150">Хотя мы поддерживаем ресурсы на основе JSON для приложений Windows на основе HTML, схема для ресурсов JSON не совпадает с схемой, определенной для расширений JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e5396-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>  

<span data-ttu-id="e5396-151">Ниже ключевых различий в [HTML-приложениях Windows:](/previous-versions/windows/apps/hh465228(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e5396-151">The following are the key differences in [HTML based Windows apps](/previous-versions/windows/apps/hh465228(v=win.10)):</span></span>  

*   <span data-ttu-id="e5396-152">Ресурсы указаны в `.resjson` файлах, а не `.json` в файлах.</span><span class="sxs-lookup"><span data-stu-id="e5396-152">Resources are specified in `.resjson` files instead of `.json` files.</span></span>  
*   <span data-ttu-id="e5396-153">Поддерживаемые локали должны быть указаны в файле AppXManifest, при этом первый локаль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5396-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>  
*   <span data-ttu-id="e5396-154">Ресурсы приложений Windows на основе HTML используют следующую схему:</span><span class="sxs-lookup"><span data-stu-id="e5396-154">HTML based Windows apps resources use the following schema:</span></span>  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    <span data-ttu-id="e5396-155">Пара имя/значение, обозначаемая подчеркиваемой строкой, — это комментарии для соответствующего ресурса строки.</span><span class="sxs-lookup"><span data-stu-id="e5396-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>  
*   `.resjson` <span data-ttu-id="e5396-156">файлы скомпилироваться в `.pri` файлы, которые должны быть включены во время создания пакета AppX.</span><span class="sxs-lookup"><span data-stu-id="e5396-156">files are compiled into `.pri` files which must be included during AppX package creation.</span></span>  
    
### <a name="creating-json-string-resources"></a><span data-ttu-id="e5396-157">Создание ресурсов строкИ JSON</span><span class="sxs-lookup"><span data-stu-id="e5396-157">Creating JSON string resources</span></span>  

<span data-ttu-id="e5396-158">С помощью настраиваемой системы AppxManifest и различий между выделенными рамками локализации i18n и UWP вы готовы создавать файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5396-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>  

<span data-ttu-id="e5396-159">Только одна строка ресурса в манифесте применима к пакетам расширения Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e5396-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span>  <span data-ttu-id="e5396-160">Строка обычно локализована в расширениях JavaScript и легко может быть соедем с ожидаемой `DisplayName` `.resjson` Windows файлами.</span><span class="sxs-lookup"><span data-stu-id="e5396-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the `.resjson` files that Windows expects.</span></span>  <span data-ttu-id="e5396-161">Если предположить, что это единственный ресурс, который вы хотите локализовать, вот пример файла, `.resjson` который необходимо создать:</span><span class="sxs-lookup"><span data-stu-id="e5396-161">Assuming that this is the only resource that you would like to localize, here is a sample `.resjson` file that should be created:</span></span>  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

<span data-ttu-id="e5396-162">ИД ресурса в каждом файле должен соответствовать `.resjson` ID, используемый в AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-162">The resource ID in each `.resjson` file needs to match the ID used in the AppXManifest.</span></span>  <span data-ttu-id="e5396-163">Используя пример `.resjson` фрагмента выше, соответствующая запись AppXManifest должна быть:</span><span class="sxs-lookup"><span data-stu-id="e5396-163">Using the example `.resjson` snippet above, the corresponding AppXManifest entry should be:</span></span>  

`DisplayName="ms-resource:DisplayName"`  

<span data-ttu-id="e5396-164">Каждый язык, поддерживаемый расширением, должен иметь соответствующий файл ресурсов и размещаться в `.resjson` следующей структуре папок:</span><span class="sxs-lookup"><span data-stu-id="e5396-164">Each language that your extension supports should have a corresponding resources `.resjson` file and be placed in the following folder structure:</span></span>  

![структура языковых папок](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a><span data-ttu-id="e5396-166">Создание файла ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5396-166">Creating the resources file</span></span>  

<span data-ttu-id="e5396-167">После создания всех файлов вы будете готовы создать файл с индексом ресурсов пакета `.resjson` \(PRI\).</span><span class="sxs-lookup"><span data-stu-id="e5396-167">Once you've created all your `.resjson` files, you're ready to create your package resource index \(PRI\) file.</span></span>  <span data-ttu-id="e5396-168">Этот файл сохраняет ресурсы для всех поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="e5396-168">This file stores the resources for all your supported languages.</span></span>  <span data-ttu-id="e5396-169">Для этого можно использовать **средство MakePRI,** которое включено в SDK Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e5396-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>  

<span data-ttu-id="e5396-170">Сначала необходимо создать файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e5396-170">First you'll need to create the configuration file.</span></span>  <span data-ttu-id="e5396-171">Это определяет квалификаторы по умолчанию и платформу для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5396-171">This defines the default qualifiers and platform for the resources.</span></span>  <span data-ttu-id="e5396-172">В этом примере сделайте язык по умолчанию `English (US)` и платформу Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e5396-172">For this example, make the default language `English (US)` and the platform Windows 10.</span></span>  <span data-ttu-id="e5396-173">Для этого создайте `priconfig.xml` файл со следующим содержимым в `[Root folder]` :</span><span class="sxs-lookup"><span data-stu-id="e5396-173">To do this, create a `priconfig.xml` file with the following content in the `[Root folder]`:</span></span>  

![priconfig в папке](../../media/priconfig.png)  

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```  

<span data-ttu-id="e5396-175">Теперь вы можете использовать файл конфигурации и средство MakePRI для создания файла resources.pri.</span><span class="sxs-lookup"><span data-stu-id="e5396-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span>  <span data-ttu-id="e5396-176">В этом примере корневое расположение проекта будет `[Root folder]` .</span><span class="sxs-lookup"><span data-stu-id="e5396-176">For this example, the root location for the project will be `[Root folder]`.</span></span>  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

<span data-ttu-id="e5396-177">Теперь в корневой папке должен быть один файл resources.pri:</span><span class="sxs-lookup"><span data-stu-id="e5396-177">You should now have one resources.pri file in your root folder:</span></span>  

![папка ресурсов](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a><span data-ttu-id="e5396-179">Локализация имени и описания в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="e5396-179">Localizing name and description in the Microsoft Store</span></span>  

<span data-ttu-id="e5396-180">После отправки полного локализованного пакета Центр разработчиков Windows обнаружит, что поддерживается несколько языков, и проверит, есть ли соответствующие локализованные имена и описания для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e5396-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span>  <span data-ttu-id="e5396-181">Если какие-либо из локализованных значений отсутствуют, отправка будет заблокирована до тех пор, пока вы не предоставите значения.</span><span class="sxs-lookup"><span data-stu-id="e5396-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>  

<span data-ttu-id="e5396-182">Если вы заинтересованы только в предоставлении локализованного имени и описания для Microsoft Store (а не Windows), вы можете сделать это, за счет хранения всех локализованных имен для [вашего расширения](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="e5396-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>  

<span data-ttu-id="e5396-183">После того как вы зарезервировали дополнительные локализованные имена, можно создать обновленную отправку.</span><span class="sxs-lookup"><span data-stu-id="e5396-183">Once you've reserved additional localized names, you can create an updated submission.</span></span>  <span data-ttu-id="e5396-184">В разделе описание можно управлять дополнительными языками для списка Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="e5396-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>  

![Управление языками описаний](../../media/manage-description-languages.png)  

<span data-ttu-id="e5396-186">После выбора управления **дополнительными**языками вы сможете выбрать языки, которые необходимо добавить в список Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e5396-186">Once you've selected **Manage additional languages**, you'll get to select which languages you want to add to your Microsoft Store listing.</span></span>  <span data-ttu-id="e5396-187">Новый язык будет показываться в качестве **дополнительного языка описания** в разделе **Описание.**</span><span class="sxs-lookup"><span data-stu-id="e5396-187">The new language will show up as **Additional description language** in the **Description** section.</span></span>  

<span data-ttu-id="e5396-188">Вы можете щелкнуть по отдельной ссылке в разделе **Описание,** чтобы предоставить локализованное имя и описание, заметки о выпуске и визуальные активы для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="e5396-188">You can click on the individual link in the **Description** section to provide a localized name and description, release notes, and visual assets for each language.</span></span>  <span data-ttu-id="e5396-189">Описание магазина Майкрософт не извлекается из AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="e5396-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span>  <span data-ttu-id="e5396-190">Каждое локализованное описание должно быть вписано вручную в Центр разработчиков Windows:</span><span class="sxs-lookup"><span data-stu-id="e5396-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>  

![Описание японского приложения](../../media/japanese-app-description.png)  

<span data-ttu-id="e5396-192">После отправки локализованных описаний и публикации расширения каждый, кто получит доступ к локализованной странице расширения в Microsoft Store, увидит следующий пользовательский интерфейс:</span><span class="sxs-lookup"><span data-stu-id="e5396-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>  

![японский магазин windows](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a><span data-ttu-id="e5396-194">Примеры AppxManifest</span><span class="sxs-lookup"><span data-stu-id="e5396-194">AppxManifest samples</span></span>  

### <a name="non-localized-appxmanifest"></a><span data-ttu-id="e5396-195">Не локализованный AppxManifest</span><span class="sxs-lookup"><span data-stu-id="e5396-195">Non-localized AppxManifest</span></span>  

<span data-ttu-id="e5396-196">В следующем примере показан appxManifest, который не локализован и поддерживает только `en-us` локал.</span><span class="sxs-lookup"><span data-stu-id="e5396-196">The following example shows an AppxManifest that isn't localized, and only supports the `en-us` locale.</span></span>  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  

#### <a name="localized-appxmanifest"></a><span data-ttu-id="e5396-197">Локализованный AppxManifest</span><span class="sxs-lookup"><span data-stu-id="e5396-197">Localized AppxManifest</span></span>  

<span data-ttu-id="e5396-198">Этот пример AppxManifest локализован для восьми других локалов, кроме "en-ru".</span><span class="sxs-lookup"><span data-stu-id="e5396-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="e5396-199">Обратите внимание `ms-resource:<resource id>` на случаи:</span><span class="sxs-lookup"><span data-stu-id="e5396-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>  

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```  
