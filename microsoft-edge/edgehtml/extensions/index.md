---
description: Узнайте, как разрабатывать расширения Microsoft Edge. Эти небольшие программы можно использовать для добавления новых функций в Microsoft Edge или изменения существующих функций.
title: Расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: extensions
keywords: edge, веб-разработка, html, css, javascript, разработчик, расширения
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cc54e3512cf315183ce8baa59abde3db568d1828
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235690"
---
# <span data-ttu-id="0c12b-105">Расширения Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="0c12b-105">Microsoft Edge (EdgeHTML) extensions</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="0c12b-106">Расширения — это небольшие программы, которые можно использовать для добавления новых функций в Microsoft Edge (EdgeHTML) или изменения существующих функций.</span><span class="sxs-lookup"><span data-stu-id="0c12b-106">Extensions are small programs that can be used to add new features to Microsoft Edge (EdgeHTML) or modify the existing functionality.</span></span> <span data-ttu-id="0c12b-107">Расширения предназначены для улучшения ежедневного просмотра пользователем за счет предоставления функций ниш, которые важны для целевой аудитории.</span><span class="sxs-lookup"><span data-stu-id="0c12b-107">Extensions are intended to improve a user’s day-to-day browsing experience by providing niche functionality that is important to targeted audiences.</span></span>

<span data-ttu-id="0c12b-108">Microsoft Edge (EdgeHTML) поддерживает новую модель расширения на основе HTML, JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="0c12b-108">Microsoft Edge (EdgeHTML) supports a new HTML, JavaScript and CSS based extension model.</span></span> <span data-ttu-id="0c12b-109">Эта новая модель совместима с Chrome, что означает, что существующие разработчики расширений Chrome смогут перенести свои расширения в Microsoft Edge (EdgeHTML) с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="0c12b-109">This new model is Chrome-compatible which means that existing Chrome extension developers will be able to migrate their extensions to Microsoft Edge (EdgeHTML) with minimal changes.</span></span>

<span data-ttu-id="0c12b-110">Чтобы получить общие сведения о завершении создания расширения Microsoft Edge (EdgeHTML) от разработки до публикации, ознакомьтесь с руководством по началу [работы!](./getting-started.md)</span><span class="sxs-lookup"><span data-stu-id="0c12b-110">To get an overview of the end to end journey of creating a Microsoft Edge (EdgeHTML) extension from development to publishing, check out the [Getting started guide](./getting-started.md)!</span></span>


## <span data-ttu-id="0c12b-111">Популярные статьи</span><span class="sxs-lookup"><span data-stu-id="0c12b-111">Popular articles</span></span>

<table>
  <tr>
    <td><a href = "./api-support/extension-api-roadmap.md"><span data-ttu-id="0c12b-112">Схема расширения API</span><span class="sxs-lookup"><span data-stu-id="0c12b-112">Extension API roadmap</span></span></a></td>
    <td><span data-ttu-id="0c12b-113">Узнайте, какие API поддерживаются или находятся в разработке для Windows 10 Insider Preview и общедоступных сборках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0c12b-113">Check out what APIs are supported/in development for Windows 10 Insider Preview and publicly released builds of Microsoft Edge.</span></span></td></p>
<p>  </tr>
  <tr>
    <td><a href = "./api-support/supported-apis.md"><span data-ttu-id="0c12b-114">Поддерживаемые API</span><span class="sxs-lookup"><span data-stu-id="0c12b-114">Supported APIs</span></span></a></td>
    <td><span data-ttu-id="0c12b-115">Получите сведения о поддерживаемых API, включая известные проблемы и несовместимости Chrome.</span><span class="sxs-lookup"><span data-stu-id="0c12b-115">Get info on our supported APIs including known issues and Chrome incompatibilities.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/creating-an-extension.md"><span data-ttu-id="0c12b-116">Создание расширения</span><span class="sxs-lookup"><span data-stu-id="0c12b-116">Creating an extension</span></span></a></td>
    <td><span data-ttu-id="0c12b-117">Новые возможности разработки расширений?</span><span class="sxs-lookup"><span data-stu-id="0c12b-117">New to the world of extension development?</span></span> <span data-ttu-id="0c12b-118">Попробуйте некоторые учебники, чтобы быстро приумноться.</span><span class="sxs-lookup"><span data-stu-id="0c12b-118">Try out some tutorials to get up to speed.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/packaging.md"><span data-ttu-id="0c12b-119">Создание пакетов</span><span class="sxs-lookup"><span data-stu-id="0c12b-119">Packaging</span></span></a></td>
    <td><span data-ttu-id="0c12b-120">Узнайте, как упаковировать расширение после завершения&#39;разработки.</span><span class="sxs-lookup"><span data-stu-id="0c12b-120">Learn how to package up your extension after you&#39;ve finished development.</span></span></td>

  </tr>
  <tr>
    <td><a href = "./guides/porting-chrome-extensions.md"><span data-ttu-id="0c12b-121">Перенос расширений Chrome</span><span class="sxs-lookup"><span data-stu-id="0c12b-121">Porting Chrome extensions</span></span></a></td>
    <td><span data-ttu-id="0c12b-122">Создали расширение Chrome,&#39;хотите увидеть в Microsoft Edge?</span><span class="sxs-lookup"><span data-stu-id="0c12b-122">Created a Chrome extension you&#39;d like to see on Microsoft Edge?</span></span> <span data-ttu-id="0c12b-123">Узнайте, как его перенос с помощью расширения Microsoft Edge набор средств.</span><span class="sxs-lookup"><span data-stu-id="0c12b-123">See how to port it with the Microsoft Edge Extension Toolkit.</span></span></td>

  </tr>
</table>
