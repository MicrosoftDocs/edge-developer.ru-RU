---
description: Руководство по настройке отображения кнопки показа пароля
title: Настройка кнопки раскрытия пароля
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, совместимость, веб-платформа, раскрытие пароля, значок глаза
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327725"
---
# <span data-ttu-id="87aee-104">Настройка кнопки раскрытия пароля</span><span class="sxs-lookup"><span data-stu-id="87aee-104">Customize the password reveal button</span></span>  

<span data-ttu-id="87aee-105">Тип `password` ввода в Microsoft Edge включает в себя управление **раскрытием** паролей.</span><span class="sxs-lookup"><span data-stu-id="87aee-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="87aee-106">Пользователь может нажать **кнопку ввода** пароля, чтобы отвести **поле пароля.**</span><span class="sxs-lookup"><span data-stu-id="87aee-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="87aee-107">Обнаруженное поле **пароля** помогает пользователю проверить правильность пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="87aee-108">После ввода текста в \*\*\*\* поле пароля пользователь может \*\*\*\* нажать кнопку раскрытия пароля или перевести на кнопку включения видимости `Alt` + `F8` ввода.</span><span class="sxs-lookup"><span data-stu-id="87aee-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="87aee-109">Поле **пароля** с точками, скрывающих символы, введенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="87aee-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="87aee-110">Кнопка **раскрытия** пароля отображается справа от **поля** пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="Рядом с точками, которые скрывают текст пароля, отображается значок в форме глаза" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="87aee-112">Рядом с точками, которые скрывают текст пароля, отображается значок в форме глаза</span><span class="sxs-lookup"><span data-stu-id="87aee-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="87aee-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span><span class="sxs-lookup"><span data-stu-id="87aee-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="Значок в форме глаза имеет косую черту, и отображается исходный текст пароля" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="87aee-115">Значок в форме глаза имеет косую черту, и отображается исходный текст пароля</span><span class="sxs-lookup"><span data-stu-id="87aee-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="87aee-116">По умолчанию кнопка **раскрытия** пароля вставляется в shadow DOM всех элементов HTML с установленным `input` `type` значением `"password"` .</span><span class="sxs-lookup"><span data-stu-id="87aee-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="87aee-117">Начиная с Microsoft Edge версии 87, пользователи или [предприятия][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] могут отключить эту функцию глобально.</span><span class="sxs-lookup"><span data-stu-id="87aee-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="87aee-118">Вы, веб-дизайнеры и разработчики, должны ожидать, что большинство пользователей Microsoft Edge будут работать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87aee-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <span data-ttu-id="87aee-119">Удаление управления раскрытием паролей</span><span class="sxs-lookup"><span data-stu-id="87aee-119">Remove the password reveal control</span></span>  

<span data-ttu-id="87aee-120">Вы можете полностью удалить **кнопку раскрытия пароля,** нацелив `::-ms-reveal` псевдоэлемент.</span><span class="sxs-lookup"><span data-stu-id="87aee-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="87aee-121">Однако следует рассмотреть возможность использования кнопки раскрытия **пароля.**</span><span class="sxs-lookup"><span data-stu-id="87aee-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="87aee-122">Встроенная **кнопка раскрытия** пароля имеет [важные меры безопасности,](#visibility-of-the-control) встроенные в поведение.</span><span class="sxs-lookup"><span data-stu-id="87aee-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <span data-ttu-id="87aee-123">Настройка стиля управления</span><span class="sxs-lookup"><span data-stu-id="87aee-123">Customize the control style</span></span>  

<span data-ttu-id="87aee-124">Вместо полного удаления этого средства управления можно изменить \*\*\*\* стиль кнопки раскрытия пароля, чтобы он лучше совпадал с визуальным языком веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="87aee-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="87aee-125">В следующем фрагменте кода приводится пример такого стиля.</span><span class="sxs-lookup"><span data-stu-id="87aee-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="87aee-126">При нажатии стиля кнопки раскрытия пароля следует иметь в виду **следующее.**</span><span class="sxs-lookup"><span data-stu-id="87aee-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="87aee-127">Значок глаза реализуется в качестве фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="87aee-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="87aee-128">Чтобы добавить цвет фона в **кнопку** раскрытия пароля, используйте свойство CSS вместо `background-color` `background` краткого свойства.</span><span class="sxs-lookup"><span data-stu-id="87aee-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="87aee-129">Вы можете изменить размер и масштаб кнопки **раскрытия** пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="87aee-130">Браузер скрывает переполнение вне пределов ввода пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="87aee-131">В настоящее время нет доступных средств выбора состояния для включения состояния кнопки **раскрытия** пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <span data-ttu-id="87aee-132">Видимость управления</span><span class="sxs-lookup"><span data-stu-id="87aee-132">Visibility of the control</span></span>  

<span data-ttu-id="87aee-133">Кнопка **раскрытия** пароля недоступна, пока пользователь не введите текст в **поле пароля.**</span><span class="sxs-lookup"><span data-stu-id="87aee-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="87aee-134">Чтобы обеспечить безопасность ввода пароля пользователя, браузер подавляет кнопку в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="87aee-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="87aee-135">Если фокус перемещается с поля **пароля,** браузер удаляет кнопку **раскрытия** пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="87aee-136">Если сценарии изменяют поле **пароля,** браузер удаляет кнопку **раскрытия** пароля.</span><span class="sxs-lookup"><span data-stu-id="87aee-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="87aee-137">Если пользователь удаляет кнопку показа пароля, он должен удалить \*\*\*\* содержимое поля \*\*\*\* пароля, прежде чем кнопка показа пароля снова отобразится. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="87aee-137">If a user removes the **password reveal** button, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="87aee-138">Эта функция не позволяет пользователю вносить незначительные изменения для просмотра пароля, если пользователь покиает устройство с разблокированным устройством.</span><span class="sxs-lookup"><span data-stu-id="87aee-138">This feature prevents someone from making a minor adjustment to view the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="87aee-139">Кнопка **раскрытия** пароля недоступна, если поле **пароля** автоматически заполнено с помощью диспетчера паролей.</span><span class="sxs-lookup"><span data-stu-id="87aee-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled — Microsoft Edge — политики | Документы Майкрософт"  
