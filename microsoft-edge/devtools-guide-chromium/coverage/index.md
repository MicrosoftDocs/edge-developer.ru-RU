---
description: Поиск и анализ неиспользванного кода JavaScript и CSS в Microsoft Edge DevTools.
title: Найдите неиспользванный код JavaScript и CSS с панелью покрытия в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2a2d48bda34daa95b9f500c31a12859a1cb08625
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439200"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a><span data-ttu-id="db504-104">Найдите неиспользванный код JavaScript и CSS с панелью Coverage в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="db504-104">Find unused JavaScript and CSS code with the Coverage panel in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="db504-105">Панель **coverage** в Microsoft Edge DevTools помогает найти неиспользванный код JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="db504-105">The **Coverage** panel in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="db504-106">Удаление неиспользованого кода может ускорить загрузку страницы и сохранить мобильные данные пользователей сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="db504-106">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Анализ покрытия кода" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="db504-108">Анализ покрытия кода</span><span class="sxs-lookup"><span data-stu-id="db504-108">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="db504-109">Поиск неиспользованого кода относительно прост.</span><span class="sxs-lookup"><span data-stu-id="db504-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="db504-110">Но рефакторинг базы кода таким образом, что каждая страница передает только JavaScript и CSS, что она нуждается может быть трудно.</span><span class="sxs-lookup"><span data-stu-id="db504-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="db504-111">В этом руководстве не сообщается, как рефакторировать базу кода, чтобы избежать неиспользованого кода, так как эти рефакторы сильно зависят от стека технологий.</span><span class="sxs-lookup"><span data-stu-id="db504-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <a name="overview"></a><span data-ttu-id="db504-112">Обзор</span><span class="sxs-lookup"><span data-stu-id="db504-112">Overview</span></span>  

<span data-ttu-id="db504-113">Доставка неиспользована JavaScript или CSS является распространенной проблемой в веб-разработке.</span><span class="sxs-lookup"><span data-stu-id="db504-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="db504-114">Например, предположим, что на странице необходимо использовать компонент [кнопки Bootstrap.][BootstrapButtons]</span><span class="sxs-lookup"><span data-stu-id="db504-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="db504-115">Чтобы использовать компонент кнопки, необходимо добавить ссылку на таблицу стилей Bootstrap в HTML, например:</span><span class="sxs-lookup"><span data-stu-id="db504-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="db504-116">В этом таблице стилей не только содержится код компонента кнопки.</span><span class="sxs-lookup"><span data-stu-id="db504-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="db504-117">Он содержит CSS для **всех** компонентов Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="db504-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="db504-118">Но вы не используете ни один из других компонентов Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="db504-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="db504-119">Таким образом, ваша страница скачивает кучу CSS, что она не нужна.</span><span class="sxs-lookup"><span data-stu-id="db504-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="db504-120">Этот дополнительный CSS является проблемой по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="db504-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="db504-121">Дополнительный код замедляет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="db504-121">The extra code slows down your page load.</span></span>  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="db504-122">Если пользователь получает доступ к странице на мобильном устройстве, дополнительный код использует данные сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="db504-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a><span data-ttu-id="db504-123">Откройте панель Coverage</span><span class="sxs-lookup"><span data-stu-id="db504-123">Open the Coverage panel</span></span>  

1.  <span data-ttu-id="db504-124">[Откройте командное меню.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="db504-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="db504-125">Начните `coverage` печатать, выберите команду **Show Coverage,** а затем `Enter` выберите для запуска команды.</span><span class="sxs-lookup"><span data-stu-id="db504-125">Start typing `coverage`, select the **Show Coverage** command, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="db504-126">Панель **Coverage** открывается в **ящике**.</span><span class="sxs-lookup"><span data-stu-id="db504-126">The **Coverage** panel opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Панель Coverage" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="db504-128">Панель **Coverage**</span><span class="sxs-lookup"><span data-stu-id="db504-128">The **Coverage** panel</span></span>  
    :::image-end:::  
    
## <a name="record-code-coverage"></a><span data-ttu-id="db504-129">Покрытие кода записи</span><span class="sxs-lookup"><span data-stu-id="db504-129">Record code coverage</span></span>  

1.  <span data-ttu-id="db504-130">Выберите одну из следующих кнопок в панели **Coverage.**</span><span class="sxs-lookup"><span data-stu-id="db504-130">Choose one of the following buttons in the **Coverage** panel.</span></span>  
    *   <span data-ttu-id="db504-131">Если **вы хотите** просмотреть код, необходимый для загрузки страницы, выберите страницу Начните использовать средства и перезагрузить ![ страницу \. ](../media/reload-icon.msft.png)</span><span class="sxs-lookup"><span data-stu-id="db504-131">Choose **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page](../media/reload-icon.msft.png)\) if you want to review what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="db504-132">Если **вы хотите** просмотреть код, используемый после взаимодействия со страницей, выберите охват инструментов ![ ](../media/record-icon.msft.png) \.</span><span class="sxs-lookup"><span data-stu-id="db504-132">Choose **Instrument Coverage** \(![Instrument Coverage](../media/record-icon.msft.png)\) if you want to review what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="db504-133">Выберите **stop Instrumenting Coverage and Show Results** \( Stop Instrumenting Coverage and Show Results \) при остановке записи ![ ](../media/stop-icon.msft.png) кода.</span><span class="sxs-lookup"><span data-stu-id="db504-133">Choose **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results](../media/stop-icon.msft.png)\) when you want to stop recording code coverage.</span></span>  
    
## <a name="analyze-code-coverage"></a><span data-ttu-id="db504-134">Анализ покрытия кода</span><span class="sxs-lookup"><span data-stu-id="db504-134">Analyze code coverage</span></span>  

<span data-ttu-id="db504-135">В таблице панели **Coverage** отображаются проанализированые ресурсы и объем кода, используемый в каждом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="db504-135">The table in the **Coverage** panel displays the resources that were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="db504-136">Выберите строку, чтобы открыть этот ресурс в панели **Источники** и просмотреть строковую разбивку используемого кода и неиспользованого кода.</span><span class="sxs-lookup"><span data-stu-id="db504-136">Choose a row to open that resource in the **Sources** panel and review a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Отчет о покрытии кода" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="db504-138">Отчет о покрытии кода</span><span class="sxs-lookup"><span data-stu-id="db504-138">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="db504-139">**Url-адрес** — это URL-адрес проанализированого ресурса.</span><span class="sxs-lookup"><span data-stu-id="db504-139">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="db504-140">В **столбце Тип** говорится, содержит ли ресурс CSS, JavaScript или оба.</span><span class="sxs-lookup"><span data-stu-id="db504-140">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="db504-141">Столбец **Total Bytes** — это общий размер ресурса в bytes.</span><span class="sxs-lookup"><span data-stu-id="db504-141">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="db504-142">**Неиспользованный** столбец Bytes — это число неиспользованых bytes.</span><span class="sxs-lookup"><span data-stu-id="db504-142">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="db504-143">Последний неназванный столбец — это визуализация столбцов **Total Bytes** и **Unused Bytes.**</span><span class="sxs-lookup"><span data-stu-id="db504-143">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="db504-144">Красный раздел панели неиспользован bytes.</span><span class="sxs-lookup"><span data-stu-id="db504-144">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="db504-145">Зеленый раздел используется bytes.</span><span class="sxs-lookup"><span data-stu-id="db504-145">The green section is used bytes.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="db504-146">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="db504-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Кнопки — Bootstrap"  

> [!NOTE]
> <span data-ttu-id="db504-149">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db504-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="db504-150">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/coverage/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="db504-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="db504-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db504-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
