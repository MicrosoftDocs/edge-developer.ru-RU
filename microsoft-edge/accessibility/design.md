---
description: Ознакомьтесь с ресурсами для инклюзивного проектирования и практическими методиками.
title: Accessibility - Design
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 8468f8e1-9f4a-426c-a969-76eab9419137
keywords: accessibility, accessibility for developers, accessible websites, edge, web development, ARIA, developer, UIA, UI Automation
ms.openlocfilehash: 8d31f7b32cb92794ff8592c239436f3b101a3859
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230819"
---
# <span data-ttu-id="233af-104">Разработка доступных веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="233af-104">Designing Accessible Websites</span></span>  

<span data-ttu-id="233af-105">Создание инклюзивного дизайна делает технологию можной для всех людей независимо от их возраста, образования, географического расположения, языка или ограниченных возможностей.</span><span class="sxs-lookup"><span data-stu-id="233af-105">Creating an inclusive design makes technology usable by all people no matter their age, education, geographic location, language, or disability.</span></span>  <span data-ttu-id="233af-106">Пользователи, использующие технологии и просмотр в Интернете, имеют широкий спектр возможностей и предпочтений.</span><span class="sxs-lookup"><span data-stu-id="233af-106">People using technology and browsing the web have a wide range of abilities and preferences.</span></span>  <span data-ttu-id="233af-107">При разработке веб-сайта следует помнить о следующих ключевых сценариях с учетом ключевых возможностей.</span><span class="sxs-lookup"><span data-stu-id="233af-107">As you design your website, keep in mind the following key accessibility scenarios:</span></span>

*   <span data-ttu-id="233af-108">Устройства чтения с экрана — пользователи с нарушениями зрения или незрячие пользователи используют устройства чтения с экрана для интерпретации пользовательского интерфейса приложения и взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="233af-108">Screen readers—Users who are blind or visually impaired rely on screen readers to interpret and interact with the UI of your app.</span></span>  <span data-ttu-id="233af-109">Интерпретация подразумевает чтение имен элементов пользовательского интерфейса, ролей, значений и так далее, а взаимодействие с пользовательским интерфейсом подразумевает перемещение фокуса от одного элемента к другому и создание функций.</span><span class="sxs-lookup"><span data-stu-id="233af-109">Interpreting involves reading the UI element names, roles, values, and so on, and interacting with the UI involves moving the focus from one element to another and invoking functionality.</span></span>
*   <span data-ttu-id="233af-110">Доступность клавиатуры — многие пользователи с специальными интерфейсами используют клавиатуру для навигации и работы с пользовательским интерфейсом с помощью:</span><span class="sxs-lookup"><span data-stu-id="233af-110">Keyboard accessibility—Many accessibility users rely on the keyboard to navigate and operate the UI by:</span></span>
    *   <span data-ttu-id="233af-111">Перемещение фокуса между элементами с помощью клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="233af-111">Moving focus among elements by using the Tab key.</span></span>
    *   <span data-ttu-id="233af-112">Навигация в элементах контейнера, таких как списки, сетки и представления дерева, с помощью клавиш со стрелками.</span><span class="sxs-lookup"><span data-stu-id="233af-112">Navigating in container elements such as lists, grids, and tree views by using the arrow keys.</span></span>
    *   <span data-ttu-id="233af-113">Активация функций \(с помощью действий\) с помощью клавиши ВВОД или ПРОБЕЛ.</span><span class="sxs-lookup"><span data-stu-id="233af-113">Activating functionality \(invoking actions\) by using the Enter or Space key.</span></span>
    *   <span data-ttu-id="233af-114">Использование сочетания клавиш для эффективного доступа к другим функциям приложения.</span><span class="sxs-lookup"><span data-stu-id="233af-114">Using shortcut keys to efficiently access other app functionality.</span></span>
*   <span data-ttu-id="233af-115">Доступные визуальные эффекты — пользователям с нарушениями зрения требуется достаточный коэффициент контрастности текста для текстового содержимого и хороший визуальный эффект с высококонтравтными темами в целом.</span><span class="sxs-lookup"><span data-stu-id="233af-115">Accessible visual experience—Users who are visually impaired need a sufficient text contrast ratio for text content, and a good visual experience with high contrast themes overall.</span></span>  <span data-ttu-id="233af-116">Пользователи с дальтонией должны передавать информацию не цветом, а другими способами.</span><span class="sxs-lookup"><span data-stu-id="233af-116">Users who are color blind need information to be conveyed in ways other than through color.</span></span>

<span data-ttu-id="233af-117">Многие распространенные проблемы с доступностью в Интернете можно решить с помощью хорошего кода.</span><span class="sxs-lookup"><span data-stu-id="233af-117">Many common accessibility issues on the web can be solved through good coding practice.</span></span>  <span data-ttu-id="233af-118">Документация по [WCAG 2.0](https://www.w3.org/TR/WCAG20) содержит методики и рекомендации по разработке более доступных динамических веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="233af-118">The [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG20) documentation provides techniques and best practices to help you design more accessible dynamic web applications.</span></span>  <span data-ttu-id="233af-119">Дополнительные сведения о создании доступных веб-сайтов можно найти на сайте ["Создание доступных веб-сайтов".](./build/index.md)</span><span class="sxs-lookup"><span data-stu-id="233af-119">For more information on building accessible websites, navigate to [Building Accessible Websites](./build/index.md) .</span></span>

## <span data-ttu-id="233af-120">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="233af-120">Resources</span></span>  

#### [<span data-ttu-id="233af-121">Проектирование для включения</span><span class="sxs-lookup"><span data-stu-id="233af-121">Designing for Inclusion</span></span>](https://w3.org/WAI/users/Overview.html)  

<span data-ttu-id="233af-122">Проект по включению в проект в рамках инициативы по веб-специальным возможностям W3C предоставляет ресурсы, которые помогут вам лучше понять пользователей с ограниченными возможностями и как спроектировать веб-сайт с учетом этих возможностей.</span><span class="sxs-lookup"><span data-stu-id="233af-122">Designing for Inclusion by the W3C Web Accessibility Initiative provides resources to help you better understand users with disabilities and how to design your website with them in mind.</span></span>

#### [<span data-ttu-id="233af-123">Проектирование инклюзивного программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="233af-123">Designing inclusive software</span></span>](https://msdn.microsoft.com/windows/uwp/accessibility/designing-inclusive-software)  

<span data-ttu-id="233af-124">При разработке инклюзивного программного обеспечения обсуждаются принципы и методики разработки корпорации Майкрософт для универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="233af-124">Designing inclusive software discusses Microsoft design principles and practices for the Universal Windows Platform (UWP).</span></span>

#### [<span data-ttu-id="233af-125">Использование Интернета для людей с ограниченными возможностями</span><span class="sxs-lookup"><span data-stu-id="233af-125">How People with Disabilities Use the Web</span></span>](https://www.w3.org/WAI/intro/people-use-web/Overview.html)  

<span data-ttu-id="233af-126">Этот ресурс W3C представляет, как люди с ограниченными возможностями, в том числе люди с нарушениями возраста, используют Интернет.</span><span class="sxs-lookup"><span data-stu-id="233af-126">This resource by the W3C introduces how people with disabilities, including people with age-related impairments, use the Web.</span></span>

#### [<span data-ttu-id="233af-127">Инклюзивное набор средств</span><span class="sxs-lookup"><span data-stu-id="233af-127">Inclusive Design Toolkit</span></span>](https://www.microsoft.com/design/practice#howwemake-section)  

<span data-ttu-id="233af-128">Корпорация Майкрософт разработала проект инклюзивного набор средств, чтобы показать, как разнообразие людей может создать более широкие ограничения проектирования и как подключиться к более широким рынкам, на первый взгляд, нишевые решения.</span><span class="sxs-lookup"><span data-stu-id="233af-128">Microsoft developed the Inclusive Design Toolkit to show how human diversity can create better design constraints and how to connect seemingly niche solutions to broader markets.</span></span>
