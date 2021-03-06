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
# Режим чтения  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge предоставляет представление чтения для более упрощенного и похожего на книгу чтения веб-страниц, не отвлекая внимание от несвязанных или другого дополнительного содержимого на странице.  В адресной панели или с помощью **** кнопки "Чтение" можно включать или отключать представление чтения (значок книги) в адресной панели или с помощью `Ctrl` + `Shift` + `R` .  В представлении чтения извлекаются следующие метаданные со страницы:  

*   Title
*   Автор
*   Дата
*   Издатель
*   Доминантное изображение\(s\)
*   Подписи доминантного изображения\(s\)
*   Дополнительные изображения
*   Основное текстовое содержимое страницы
*   Авторские права

Затем пользователи могут настраивать контрастность страниц и размер шрифта на панели параметров Microsoft **Edge.**  

## Извлечение метаданных  

Ниже даны сведения о метаданных страницы, отрисовытых при чтении.  

### Title  

Чтобы обеспечить отрисовки заголовка статьи в представлении чтения:  

*   `title`Включите элемент в загол  
*   Включить мета тег с `name="title"`  
*   Соедините текст заголовка в тексте статьи со строкой содержимого метатега.  Pipes \( `|` \) in your content string prevent the reader view from becoming active, try using hyphens \( `-` \) instead.  

### Автор  

В представлении чтения будет искаться элемент с `class = "byline-name"` .  Лучше всего разместить имя автора после заголовка и перед текстом статьи.  

```html
<div class="byline-name">Author name</div>
```  

### Дата  

В представлении чтения информация о издателе и дате будет отрисовка в одной строке, а для выделения этой информации будет выделен дополнительный стиль.  Дата публикации статьи будет отрисовка в точности так, как она отображается в строке.  Представление чтения не преобразуется в определенный формат даты.  

Если у вас есть дата в тексте статьи и вы хотите, чтобы представление чтения отрисовылось, назначьте элемент, содержащий дату с `'dateline'` классом:  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

Если у вас нет даты в тексте статьи, но вы хотите отрисовки даты в представлении чтения, используйте мета тег `name='displaydate'` :  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### Издатель  

В представлении чтения будет искать протокол Open Graph `"og:site_name"` для отображения сведений о издателе.  Он также ищет и `source_organization` атрибуты в любом html-теге в качестве дополнительного индикатора `publisher` информации издателя на странице.  Текст издателя будет гиперссылкой на URL-адрес страницы с помощью стиля гиперссылки страницы представления чтения.  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### Изображения  

Представление чтения захватывает большинство необработанных изображений с шириной >= 400px и пропорциями >= 1/3 и =< 3,0.  Изображения, которые не соответствуют этим измерениям, могут по-прежнему извлекаться, например изображения шириной менее 400px, но имеют подписи.  Первый подходящий образ становится доминантным образом статьи.  Доминантное изображение отрисовке в качестве первого фрагмента содержимого и предоставляется полная ширина столбца.  Все следующие изображения в этой статье отрисовыются в качестве готовых изображений.  

### Подписи  

Лучше всего разместить изображения в [тегах](https://developer.mozilla.org/docs/Web/HTML/Element/figure) рисунков не более чем с двумя вложенными [тегами](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) вымещения.  

### Body  

Чтобы убедиться, что весь текст страницы захвачен в представлении чтения, большинство текста статьи должны иметь одинаковый размер шрифта и глубину DOM.  Алгоритм просмотра чтения допускает некоторое отклонение от этого правила, чтобы издатели могли свободно добавлять акценты на строки или слова.  

### Авторские права  

Представление чтения извлекает и отображает информацию об авторских правах, обозначаемую метатегами, или, если метатегов нет, текстовый узел, содержащий символ `name = "copyright"` \( `©` \).  В представлении чтения отображаются сведения об авторских правах в конце основного текста статьи, стиль шрифта меньше, чем основной текст.  

```html
<meta name="copyright" content="Your copyright information">
```  

## Отказ от чтения  

Если вы считаете, что содержимое не подходит для чтения, вы можете использовать следующий метатег, чтобы отказаться от этой функции:  

```html
<meta name="IE_RM_OFF" content="true">
```  

С помощью этого **тега** кнопка просмотра чтения не будет отображаться в адресной панели, когда пользователи просматривают страницу.  
