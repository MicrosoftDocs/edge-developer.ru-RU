---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Узнайте, как Microsoft Edge предоставляет представление чтения для веб-страниц, чтобы включить чтение без надстройки.
title: Представление чтения — руководство разработчика
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 30c01d61ff896cca7b0af90b345a8619307f91c0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235676"
---
# <span data-ttu-id="1e5d3-104">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="1e5d3-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="1e5d3-105">Microsoft Edge предоставляет представление чтения для более упрощенного и похожего на книгу чтения веб-страниц, не отвлекая внимание от несвязанных или другого дополнительного содержимого на странице.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="1e5d3-106">В адресной панели или с помощью \*\*\*\* кнопки "Чтение" можно включать или отключать представление чтения (значок книги) в адресной панели или с помощью `Ctrl` + `Shift` + `R` .</span><span class="sxs-lookup"><span data-stu-id="1e5d3-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="1e5d3-107">В представлении чтения извлекаются следующие метаданные со страницы:</span><span class="sxs-lookup"><span data-stu-id="1e5d3-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="1e5d3-108">Title</span><span class="sxs-lookup"><span data-stu-id="1e5d3-108">Title</span></span>
*   <span data-ttu-id="1e5d3-109">Автор</span><span class="sxs-lookup"><span data-stu-id="1e5d3-109">Author</span></span>
*   <span data-ttu-id="1e5d3-110">Дата</span><span class="sxs-lookup"><span data-stu-id="1e5d3-110">Date</span></span>
*   <span data-ttu-id="1e5d3-111">Издатель</span><span class="sxs-lookup"><span data-stu-id="1e5d3-111">Publisher</span></span>
*   <span data-ttu-id="1e5d3-112">Доминантное изображение\(s\)</span><span class="sxs-lookup"><span data-stu-id="1e5d3-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="1e5d3-113">Подписи доминантного изображения\(s\)</span><span class="sxs-lookup"><span data-stu-id="1e5d3-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="1e5d3-114">Дополнительные изображения</span><span class="sxs-lookup"><span data-stu-id="1e5d3-114">Secondary images</span></span>
*   <span data-ttu-id="1e5d3-115">Основное текстовое содержимое страницы</span><span class="sxs-lookup"><span data-stu-id="1e5d3-115">Main text content of the page</span></span>
*   <span data-ttu-id="1e5d3-116">Авторские права</span><span class="sxs-lookup"><span data-stu-id="1e5d3-116">Copyright</span></span>

<span data-ttu-id="1e5d3-117">Затем пользователи могут настраивать контрастность страниц и размер шрифта на панели параметров Microsoft **Edge.**</span><span class="sxs-lookup"><span data-stu-id="1e5d3-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="1e5d3-118">Извлечение метаданных</span><span class="sxs-lookup"><span data-stu-id="1e5d3-118">Metadata extraction</span></span>  

<span data-ttu-id="1e5d3-119">Ниже даны сведения о метаданных страницы, отрисовытых при чтении.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="1e5d3-120">Title</span><span class="sxs-lookup"><span data-stu-id="1e5d3-120">Title</span></span>  

<span data-ttu-id="1e5d3-121">Чтобы обеспечить отрисовки заголовка статьи в представлении чтения:</span><span class="sxs-lookup"><span data-stu-id="1e5d3-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="1e5d3-122">`title`Включите элемент в загол</span><span class="sxs-lookup"><span data-stu-id="1e5d3-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="1e5d3-123">Включить мета тег с</span><span class="sxs-lookup"><span data-stu-id="1e5d3-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="1e5d3-124">Соедините текст заголовка в тексте статьи со строкой содержимого метатега.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="1e5d3-125">Pipes \( `|` \) in your content string prevent the reader view from becoming active, try using hyphens \( `-` \) instead.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="1e5d3-126">Автор</span><span class="sxs-lookup"><span data-stu-id="1e5d3-126">Author</span></span>  

<span data-ttu-id="1e5d3-127">В представлении чтения будет искаться элемент с `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="1e5d3-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="1e5d3-128">Лучше всего разместить имя автора после заголовка и перед текстом статьи.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="1e5d3-129">Дата</span><span class="sxs-lookup"><span data-stu-id="1e5d3-129">Date</span></span>  

<span data-ttu-id="1e5d3-130">В представлении чтения информация о издателе и дате будет отрисовка в одной строке, а для выделения этой информации будет выделен дополнительный стиль.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="1e5d3-131">Дата публикации статьи будет отрисовка в точности так, как она отображается в строке.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="1e5d3-132">Представление чтения не преобразуется в определенный формат даты.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="1e5d3-133">Если у вас есть дата в тексте статьи и вы хотите, чтобы представление чтения отрисовылось, назначьте элемент, содержащий дату с `'dateline'` классом:</span><span class="sxs-lookup"><span data-stu-id="1e5d3-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="1e5d3-134">Если у вас нет даты в тексте статьи, но вы хотите отрисовки даты в представлении чтения, используйте мета тег `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="1e5d3-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="1e5d3-135">Издатель</span><span class="sxs-lookup"><span data-stu-id="1e5d3-135">Publisher</span></span>  

<span data-ttu-id="1e5d3-136">В представлении чтения будет искать протокол Open Graph `"og:site_name"` для отображения сведений о издателе.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="1e5d3-137">Он также ищет и `source_organization` атрибуты в любом html-теге в качестве дополнительного индикатора `publisher` информации издателя на странице.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="1e5d3-138">Текст издателя будет гиперссылкой на URL-адрес страницы с помощью стиля гиперссылки страницы представления чтения.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="1e5d3-139">Изображения</span><span class="sxs-lookup"><span data-stu-id="1e5d3-139">Images</span></span>  

<span data-ttu-id="1e5d3-140">Представление чтения захватывает большинство необработанных изображений с шириной >= 400px и пропорциями >= 1/3 и =< 3,0.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="1e5d3-141">Изображения, которые не соответствуют этим измерениям, могут по-прежнему извлекаться, например изображения шириной менее 400px, но имеют подписи.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="1e5d3-142">Первый подходящий образ становится доминантным образом статьи.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="1e5d3-143">Доминантное изображение отрисовке в качестве первого фрагмента содержимого и предоставляется полная ширина столбца.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="1e5d3-144">Все следующие изображения в этой статье отрисовыются в качестве готовых изображений.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="1e5d3-145">Подписи</span><span class="sxs-lookup"><span data-stu-id="1e5d3-145">Captions</span></span>  

<span data-ttu-id="1e5d3-146">Лучше всего разместить изображения в [тегах](https://developer.mozilla.org/docs/Web/HTML/Element/figure) рисунков не более чем с двумя вложенными [тегами](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) вымещения.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="1e5d3-147">Body</span><span class="sxs-lookup"><span data-stu-id="1e5d3-147">Body</span></span>  

<span data-ttu-id="1e5d3-148">Чтобы убедиться, что весь текст страницы захвачен в представлении чтения, большинство текста статьи должны иметь одинаковый размер шрифта и глубину DOM.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="1e5d3-149">Алгоритм просмотра чтения допускает некоторое отклонение от этого правила, чтобы издатели могли свободно добавлять акценты на строки или слова.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="1e5d3-150">Авторские права</span><span class="sxs-lookup"><span data-stu-id="1e5d3-150">Copyright</span></span>  

<span data-ttu-id="1e5d3-151">Представление чтения извлекает и отображает информацию об авторских правах, обозначаемую метатегами, или, если метатегов нет, текстовый узел, содержащий символ `name = "copyright"` \( `©` \).</span><span class="sxs-lookup"><span data-stu-id="1e5d3-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="1e5d3-152">В представлении чтения отображаются сведения об авторских правах в конце основного текста статьи, стиль шрифта меньше, чем основной текст.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="1e5d3-153">Отказ от чтения</span><span class="sxs-lookup"><span data-stu-id="1e5d3-153">Opting out of Reading View</span></span>  

<span data-ttu-id="1e5d3-154">Если вы считаете, что содержимое не подходит для чтения, вы можете использовать следующий метатег, чтобы отказаться от этой функции:</span><span class="sxs-lookup"><span data-stu-id="1e5d3-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="1e5d3-155">С помощью этого **тега** кнопка просмотра чтения не будет отображаться в адресной панели, когда пользователи просматривают страницу.</span><span class="sxs-lookup"><span data-stu-id="1e5d3-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  
