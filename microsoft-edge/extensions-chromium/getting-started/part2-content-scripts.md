---
description: Динамически вставьте изображение НАСА под тегом тела страницы с помощью скриптов контента
title: Учебник по созданию расширения, часть 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions
ms.openlocfilehash: 48af14c33a368a3449acb88b4dfb875ad5398e7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397918"
---
# <a name="create-an-extension-tutorial-part-2"></a>Учебник по созданию расширения, часть 2  
  
[Завершенный источник пакета расширения для этой части][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a>Обзор  

В этом руководстве используются следующие технологии расширения.
*   Ввод библиотек JavaScript в расширение  
*   Обнажая активы расширения для вкладок браузера  
*   В том числе страницы контента в существующих вкладок браузера  
*   Если страницы контента прослушивают сообщения из всплывающих папок и отвечают  

Вы научитесь обновлять всплывающее меню, чтобы заменить статическое начало изображения заголовком и стандартной кнопкой HTML.  Эта кнопка при выборе передает изображение звезд, встроенное в расширение, на страницу контента.  Это изображение вставляется на вкладку активного браузера. Дополнительные сведения см. ниже.

1.  Удалите изображение из всплывающее и замените его кнопкой  

Сначала обновите файл с помощью прямой разметки, которая `popup.html` отображает заголовок и кнопку.  Вы запрограммировать эту кнопку в ближайшее время, но на данный момент просто включить ссылку на пустой файл JavaScript `popup.js` .  Вот обновление HTML.  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

После обновления и открытия расширения всплывающее окно открывается с помощью кнопки отображения.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html после выбора значка расширения":::
   popup.html после выбора значка расширения
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  Стратегия обновления для отображения изображения в верхней части вкладки браузера  

После добавления кнопки следующая задача состоит в том, чтобы сделать так, чтобы файл изображения был приведен в верхней части `images/stars.jpeg` активной страницы вкладки.  

Помните, что каждая страница вкладки выполняется в своем потоке. Кроме того, в расширении используется другой поток.  Сначала создайте сценарий контента, который вводится на страницу вкладки.  Затем отправьте сообщение из всплывающее сообщение в скрипт контента, запущенный на странице вкладки. Скрипт контента получает сообщение, в котором описывается, какое изображение должно отображаться.  

3. Создайте всплывающее JavaScript для отправки сообщения  

Сначала создайте и добавьте код для отправки сообщения в еще не созданный скрипт контента, который необходимо создать и ввести в `popup/popup.js` вкладку браузера.  Для этого следующий код добавляет событие в всплывающее отображение `onclick` кнопки.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

В этом `onclick` случае найдите текущую вкладку браузера.  Затем используйте `chrome.tabs.sendmessage` API расширения для отправки сообщения на эту вкладку.  

В этом сообщении необходимо включить URL-адрес изображения, которое необходимо отобразить. Кроме того, отправьте уникальный ID для назначения вставленного изображения.  Вы можете позволить вставки контента JavaScript создавать его, но по причинам, которые становятся очевидными позже, создайте уникальный ID здесь и передайте его еще не созданному сценарию `popup.js` контента.  

В следующем фрагменте кода описывается обновленный код `popup/popup.js` в .  Кроме того, передай в текущем ID вкладки, который используется позже в этой статье.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

4. Сделать ваш stars.jpeg доступным с любой вкладки браузера  

Возможно, вам интересно, почему при передаче необходимо использовать API расширения chrome вместо простого передачи относительного URL-адреса без дополнительного префикса, как в предыдущем `images/stars.jpeg` `chrome.extension.getURL` разделе.  Кстати, этот дополнительный префикс, возвращаемый с прикрепленным изображением, выглядит следующим `getUrl` образом.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

Причина в том, что вы вводите изображение с помощью атрибута элемента `src` `img` на страницу контента.  Страница контента работает по уникальному потоку, который не то же самое, что поток с расширением.  Необходимо выставить статичный файл изображения как веб-актив, чтобы он работал правильно.  

Добавьте еще одну запись в `manifest.json` файл, чтобы объявить, что изображение доступно для всех вкладок браузера.  Эта запись приведена следующим образом \(вы должны увидеть ее в полном файле ниже при добавлении объявления скрипта `manifest.json` контента далее\).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Теперь вы написали код в файле, чтобы отправить сообщение на страницу контента, встроенную на текущей активной странице вкладки, но вы еще не создали и не ввели эту страницу `popup.js` контента.  Сделайте это сейчас.  

5.  Обновление manifest.jsдля контента и веб-доступа  

`manifest.json`Обновленный, который включает в себя и является следующим `content-scripts` `web_accessible_resources` образом.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

Добавленный раздел `content_scripts` .  Для атрибута установлено, что все файлы вводятся во все страницы вкладок браузера при загрузке `matches` `<all_urls>` каждой `content_scripts` вкладки.  Допустимые типы файлов, которые можно вводить, это JavaScript и CSS.  Вы также `libjquery.min.js` добавили .  Это можно включить из скачивания, упомянутого в верхней части раздела.  

6. Добавление jQuery и понимание связанного потока  

В скриптах контента, которые вы вводите, запланируйте использование jQuery `$` \( \).  Вы добавили minified версию jQuery и положили ее в пакет расширения как `lib\jquery.min.js` .  Эти сценарии контента работают в отдельных песочницах, что означает, что jQuery, впрыскиваемая на страницу, не передается `popup.js` содержимым.  

Имейте в виду, что даже если на вкладке браузера javaScript запущен на загруженной веб-странице, любой вводный контент не имеет к этому доступа.  Вводимый JavaScript имеет доступ к фактическому DOM, загруженным на вкладке браузера.  

7. Добавление слушателя сообщения скрипта контента  

Вот этот файл, который вводится на каждую страницу вкладки `content-scripts\content.js` браузера на основе `manifest.json` `content-scripts` раздела.  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

Обратите внимание, что все вышеперечисленные действия JavaScript — это регистрация `listener` метода `chrome.runtime.onMessage.addListener` API расширения.  Этот слушатель ждет сообщений, таких как сообщения, отправленные ранее с помощью метода `popup.js` `chrome.tabs.sendMessage` API расширения.  

Первым параметром метода является функция, первый параметр которой — запрос — это сведения о `addListener` переданных сообщениях.  Помните, что при использования метода эти атрибуты первого `popup.js` `sendMessage` параметра являются и `url` `imageDivId` .  

Когда событие обрабатывается слушателем, запустится функция, которая является первым параметром.  Первым параметром этой функции является объект, который имеет атрибуты, заданные `sendMessage` .  Эта функция просто обрабатывает три строки скрипта jQuery.  

*   Первая строка скрипта динамически вставляет в загон DOM раздел, который необходимо назначить в качестве **\<style\>** `slide-image` класса `img` элементу.  
*   Вторая строка скрипта добавляет элемент прямо под вкладку браузера, заданный классом, а также ID этого `img` `body` элемента `slide-image` `imageDivId` изображения.  
*   Третья строка скрипта добавляет событие, которое охватывает все изображение, позволяя пользователю выбирать где-либо на изображении, и это изображение удаляется со страницы \(вместе с ним является слушателем `click` событий\).  

8. Добавление функций для удаления отображаемого изображения при выборе  

Теперь при просмотре любой страницы и **** выборе значка расширения всплывающее меню отображается следующим образом.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html после выбора значка расширения":::
   popup.html после выбора значка расширения
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

При выборе кнопки `Display` вы получите то, что ниже.  Если выбрать где-либо на изображении, этот элемент изображения удаляется, а страницы вкладок сваляются обратно к первоначально `stars.jpeg` отображаемой.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Изображение, показывающаяся в браузере":::
   Изображение, показывающаяся в браузере
:::image-end:::

Вы создали расширение, которое успешно отправляет сообщение из всплывающее всплывающее изображение значка расширения и динамически вставлено JavaScript, запущенное в виде контента на вкладке браузера.  Вводимый контент задает элемент изображения для отображения статических звезд jpeg.  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Завершенный источник пакета расширения | Документы Майкрософт"  
