---
description: Размещение веб-содержимого на платформе Win32, .NET и приложениях UWP с помощью элемента управления Microsoft Edge WebView2
title: Элемент управления Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, CoreWebView2, ICoreWebView2Host, HTML, Windows Forms,, WPF, .NET, WinUI, Project
ms.openlocfilehash: 9e5cc3a26f07a11c9fd5c21d62ecafc3ed5103f4
ms.sourcegitcommit: c619168deea44cdec8ebc80ef9ddf1d91d5f726d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2020
ms.locfileid: "11182185"
---
# <span data-ttu-id="88778-104">Введение в Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="88778-105">Элемент управления Microsoft Edge WebView2 позволяет внедрять в собственные приложения веб-технологии \ (HTML, CSS и JavaScript).</span><span class="sxs-lookup"><span data-stu-id="88778-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="88778-106">Элемент управления WebView2 использует [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderMain] в качестве обработчика обработки для отображения веб-содержимого в собственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="88778-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="88778-107">С помощью WebView2 вы можете внедрить веб-код в различные части собственного приложения или создать для него приложение целиком в рамках одного WebView.</span><span class="sxs-lookup"><span data-stu-id="88778-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="88778-108">Сведения о том, как приступить к созданию приложения WebView2, можно найти в разделе Начало [работы](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="88778-108">For information on how to start building a WebView2 application, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Что такое WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="88778-110">Что такое WebView</span><span class="sxs-lookup"><span data-stu-id="88778-110">What is WebView</span></span>  
:::image-end:::  

## <span data-ttu-id="88778-111">Подход к гибридным приложениям</span><span class="sxs-lookup"><span data-stu-id="88778-111">Hybrid application approach</span></span>  

<span data-ttu-id="88778-112">Разработчикам часто приходится определять создание веб-приложения или собственного приложения.</span><span class="sxs-lookup"><span data-stu-id="88778-112">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="88778-113">Решение на основе компромиссов между абонентами и возможностями.</span><span class="sxs-lookup"><span data-stu-id="88778-113">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="88778-114">Веб-приложения допускают широкий доступ к ним.</span><span class="sxs-lookup"><span data-stu-id="88778-114">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="88778-115">Как и веб-разработчик, вы можете использовать больше всего, если не все ваши коды на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="88778-115">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="88778-116">Однако в собственных приложениях используются возможности всей платформы машинного кода.</span><span class="sxs-lookup"><span data-stu-id="88778-116">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Исходный веб-сайт" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="88778-118">Исходный веб-сайт</span><span class="sxs-lookup"><span data-stu-id="88778-118">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="88778-119">Гибридные приложения позволяют разработчикам использовать преимущества обоих миров.</span><span class="sxs-lookup"><span data-stu-id="88778-119">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="88778-120">Разработчики гибридных приложений выигрывают от широкого и мощного веб-платформы, а также мощь и полную функциональность собственной платформы.</span><span class="sxs-lookup"><span data-stu-id="88778-120">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="88778-121">Преимущества WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-121">WebView2 benefits</span></span>  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Причины WebView" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="88778-123">Причины WebView</span><span class="sxs-lookup"><span data-stu-id="88778-123">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="88778-124">Веб-экосистема \ "&й навык"</span><span class="sxs-lookup"><span data-stu-id="88778-124">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="88778-125">Используйте все веб-платформы, библиотеки, Инструментарий и все, что есть в веб-экосистеме.</span><span class="sxs-lookup"><span data-stu-id="88778-125">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="88778-126">Быстрые инновации</span><span class="sxs-lookup"><span data-stu-id="88778-126">Rapid innovation</span></span>**  
      <span data-ttu-id="88778-127">Веб-разработки допускают более быстрые развертывание и итерации.</span><span class="sxs-lookup"><span data-stu-id="88778-127">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="88778-128">Поддержка Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="88778-128">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="88778-129">Поддержка согласованного взаимодействия с пользователем в Windows 7, 8 и 10.</span><span class="sxs-lookup"><span data-stu-id="88778-129">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="88778-130">Собственные возможности</span><span class="sxs-lookup"><span data-stu-id="88778-130">Native capabilities</span></span>**  
      <span data-ttu-id="88778-131">Получить доступ к полному набору API для собственных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="88778-131">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="88778-132">Совместное использование кода</span><span class="sxs-lookup"><span data-stu-id="88778-132">Code-sharing</span></span>**  
      <span data-ttu-id="88778-133">Добавление веб-кода в базу кода для более высокой повторной работы на нескольких платформах.</span><span class="sxs-lookup"><span data-stu-id="88778-133">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="88778-134">Служба поддержки Майкрософт</span><span class="sxs-lookup"><span data-stu-id="88778-134">Microsoft support</span></span>**  
      <span data-ttu-id="88778-135">Корпорация Майкрософт предоставляет поддержку и добавляет новые запросы на доступ к функциям, когда WebView2 отпущена как завершенный.</span><span class="sxs-lookup"><span data-stu-id="88778-135">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="88778-136">Распространение Evergreen</span><span class="sxs-lookup"><span data-stu-id="88778-136">Evergreen distribution</span></span>**  
      <span data-ttu-id="88778-137">Полагаться на обновленную версию Chromium с помощью регулярных обновлений платформы и исправлений для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="88778-137">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="88778-138">**Исправлено** \ (скоро)</span><span class="sxs-lookup"><span data-stu-id="88778-138">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="88778-139">Выберите, чтобы упаковать биты Chromium в приложении.</span><span class="sxs-lookup"><span data-stu-id="88778-139">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="88778-140">Добавочное внедрение</span><span class="sxs-lookup"><span data-stu-id="88778-140">Incremental adoption</span></span>**  
      <span data-ttu-id="88778-141">Добавление части веб-компонентов в приложение.</span><span class="sxs-lookup"><span data-stu-id="88778-141">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="88778-142">Начало работы</span><span class="sxs-lookup"><span data-stu-id="88778-142">Getting started</span></span>  

<span data-ttu-id="88778-143">Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderDownload] и [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] .</span><span class="sxs-lookup"><span data-stu-id="88778-143">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="88778-144">Чтобы приступить к работе, выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="88778-144">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="88778-145">Начало работы с Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="88778-145">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="88778-146">Начало работы с WPF</span><span class="sxs-lookup"><span data-stu-id="88778-146">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="88778-147">Приступая к работе с WinForms</span><span class="sxs-lookup"><span data-stu-id="88778-147">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="88778-148">Начало работы с WinUI3</span><span class="sxs-lookup"><span data-stu-id="88778-148">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="88778-149">В репозитории [примеров WebView2][GithubMicrosoftedgeWebview2samples] содержатся примеры, демонстрирующие все функции SDK WebView2 и использование API.</span><span class="sxs-lookup"><span data-stu-id="88778-149">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="88778-150">По мере добавления дополнительных функций в пакет SDK для WebView2, образцы приложений будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="88778-150">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="88778-151">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="88778-151">Supported platforms</span></span>  

<span data-ttu-id="88778-152">Общие сведения о доступности, а также о предварительной версии, можно найти в следующих средах программирования.</span><span class="sxs-lookup"><span data-stu-id="88778-152">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="88778-153">Win32 C/C++ \ (GA \)</span><span class="sxs-lookup"><span data-stu-id="88778-153">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="88778-154">Платформа .NET Framework 4.6.2 или более поздней версии (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="88778-154">.NET Framework 4.6.2 or later \(Preview\)</span></span>  
*   <span data-ttu-id="88778-155">.NET Core 3,0 или более поздняя версия (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="88778-155">.NET Core 3.0 or later \(Preview\)</span></span>  
*   <span data-ttu-id="88778-156">[WinUI 3,0][UwpToolkitsWinui3] \ (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="88778-156">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="88778-157">Вы можете запускать приложения WebView2 в следующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="88778-157">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="88778-158">Windows 10</span><span class="sxs-lookup"><span data-stu-id="88778-158">Windows 10</span></span>  
*   <span data-ttu-id="88778-159">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="88778-159">Windows 8.1</span></span>  
*   <span data-ttu-id="88778-160">Windows 7 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="88778-160">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="88778-161">WindowsServer2019</span><span class="sxs-lookup"><span data-stu-id="88778-161">Windows Server 2019</span></span>  
*   <span data-ttu-id="88778-162">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="88778-162">Windows Server 2016</span></span>  
*   <span data-ttu-id="88778-163">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88778-163">Windows Server 2012</span></span>  
*   <span data-ttu-id="88778-164">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="88778-164">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="88778-165">Windows Server 2008 R2 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="88778-165">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="88778-166">\ \* \ \* WebView2 поддержка для Windows 7 и Windows Server 2008 R2 обеспечивает один и тот же цикл поддержки в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88778-166">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="88778-167">Дополнительные сведения можно найти в разделе [Поддерживаемые операционные системы Microsoft Edge][DeployedgeMicrosoftEdgeSupportedOS].</span><span class="sxs-lookup"><span data-stu-id="88778-167">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <span data-ttu-id="88778-168">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="88778-168">Next steps</span></span>  

<span data-ttu-id="88778-169">Дополнительные сведения о том, как создавать и развертывать приложения WebView2, можно узнать в концептуальной документации и руководствах.</span><span class="sxs-lookup"><span data-stu-id="88778-169">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="88778-170">Понятия</span><span class="sxs-lookup"><span data-stu-id="88778-170">Concepts</span></span>  

*   [<span data-ttu-id="88778-171">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-171">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="88778-172">Распространение приложений с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-172">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="88778-173">Рекомендации по разработке защищенных приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-173">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="88778-174">Управление папкой "данные пользователя" в приложениях WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-174">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="88778-175">How-To направляющие</span><span class="sxs-lookup"><span data-stu-id="88778-175">How-To guides</span></span>  

*   [<span data-ttu-id="88778-176">Отладка с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="88778-176">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="88778-177">Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="88778-177">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="88778-178">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="88778-178">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Рекомендации по разработке безопасных приложений WebView2 | Документы Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Управление папкой "данные пользователя" | Документы Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Общие сведения о версиях SDK для WebView2 | Документы Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Начало работы с WebView2 | Документы Microsoft"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях для Windows Forms (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Начало работы с WebView2 в WinUI3 (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF (Предварительная версия) | Документы Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Отладка с помощью WebView2 | Документы Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge | Документы Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3 Preview (2020 июля) | Документы Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge поддерживал операционные системы | Документы Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Загрузить программу предварительной оценки Microsoft Edge"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Коллекция NuGet"  
