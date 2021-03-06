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
# <a name="create-an-extension-tutorial-part-2"></a><span data-ttu-id="d1e9a-104">Учебник по созданию расширения, часть 2</span><span class="sxs-lookup"><span data-stu-id="d1e9a-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="d1e9a-105">Завершенный источник пакета расширения для этой части</span><span class="sxs-lookup"><span data-stu-id="d1e9a-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a><span data-ttu-id="d1e9a-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="d1e9a-106">Overview</span></span>  

<span data-ttu-id="d1e9a-107">В этом руководстве используются следующие технологии расширения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="d1e9a-108">Ввод библиотек JavaScript в расширение</span><span class="sxs-lookup"><span data-stu-id="d1e9a-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="d1e9a-109">Обнажая активы расширения для вкладок браузера</span><span class="sxs-lookup"><span data-stu-id="d1e9a-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="d1e9a-110">В том числе страницы контента в существующих вкладок браузера</span><span class="sxs-lookup"><span data-stu-id="d1e9a-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="d1e9a-111">Если страницы контента прослушивают сообщения из всплывающих папок и отвечают</span><span class="sxs-lookup"><span data-stu-id="d1e9a-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="d1e9a-112">Вы научитесь обновлять всплывающее меню, чтобы заменить статическое начало изображения заголовком и стандартной кнопкой HTML.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="d1e9a-113">Эта кнопка при выборе передает изображение звезд, встроенное в расширение, на страницу контента.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="d1e9a-114">Это изображение вставляется на вкладку активного браузера. Дополнительные сведения см. ниже.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="d1e9a-115">Удалите изображение из всплывающее и замените его кнопкой</span><span class="sxs-lookup"><span data-stu-id="d1e9a-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="d1e9a-116">Сначала обновите файл с помощью прямой разметки, которая `popup.html` отображает заголовок и кнопку.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="d1e9a-117">Вы запрограммировать эту кнопку в ближайшее время, но на данный момент просто включить ссылку на пустой файл JavaScript `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="d1e9a-118">Вот обновление HTML.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="d1e9a-119">После обновления и открытия расширения всплывающее окно открывается с помощью кнопки отображения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html после выбора значка расширения":::
   <span data-ttu-id="d1e9a-121">popup.html после выбора значка расширения</span><span class="sxs-lookup"><span data-stu-id="d1e9a-121">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="d1e9a-122">Стратегия обновления для отображения изображения в верхней части вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="d1e9a-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="d1e9a-123">После добавления кнопки следующая задача состоит в том, чтобы сделать так, чтобы файл изображения был приведен в верхней части `images/stars.jpeg` активной страницы вкладки.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="d1e9a-124">Помните, что каждая страница вкладки выполняется в своем потоке.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="d1e9a-125">Кроме того, в расширении используется другой поток.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="d1e9a-126">Сначала создайте сценарий контента, который вводится на страницу вкладки.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="d1e9a-127">Затем отправьте сообщение из всплывающее сообщение в скрипт контента, запущенный на странице вкладки.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="d1e9a-128">Скрипт контента получает сообщение, в котором описывается, какое изображение должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="d1e9a-129">Создайте всплывающее JavaScript для отправки сообщения</span><span class="sxs-lookup"><span data-stu-id="d1e9a-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="d1e9a-130">Сначала создайте и добавьте код для отправки сообщения в еще не созданный скрипт контента, который необходимо создать и ввести в `popup/popup.js` вкладку браузера.  Для этого следующий код добавляет событие в всплывающее отображение `onclick` кнопки.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="d1e9a-131">В этом `onclick` случае найдите текущую вкладку браузера.  Затем используйте `chrome.tabs.sendmessage` API расширения для отправки сообщения на эту вкладку.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="d1e9a-132">В этом сообщении необходимо включить URL-адрес изображения, которое необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="d1e9a-133">Кроме того, отправьте уникальный ID для назначения вставленного изображения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="d1e9a-134">Вы можете позволить вставки контента JavaScript создавать его, но по причинам, которые становятся очевидными позже, создайте уникальный ID здесь и передайте его еще не созданному сценарию `popup.js` контента.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="d1e9a-135">В следующем фрагменте кода описывается обновленный код `popup/popup.js` в .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="d1e9a-136">Кроме того, передай в текущем ID вкладки, который используется позже в этой статье.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="d1e9a-137">Сделать ваш stars.jpeg доступным с любой вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="d1e9a-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="d1e9a-138">Возможно, вам интересно, почему при передаче необходимо использовать API расширения chrome вместо простого передачи относительного URL-адреса без дополнительного префикса, как в предыдущем `images/stars.jpeg` `chrome.extension.getURL` разделе.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="d1e9a-139">Кстати, этот дополнительный префикс, возвращаемый с прикрепленным изображением, выглядит следующим `getUrl` образом.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="d1e9a-140">Причина в том, что вы вводите изображение с помощью атрибута элемента `src` `img` на страницу контента.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="d1e9a-141">Страница контента работает по уникальному потоку, который не то же самое, что поток с расширением.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="d1e9a-142">Необходимо выставить статичный файл изображения как веб-актив, чтобы он работал правильно.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="d1e9a-143">Добавьте еще одну запись в `manifest.json` файл, чтобы объявить, что изображение доступно для всех вкладок браузера.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="d1e9a-144">Эта запись приведена следующим образом \(вы должны увидеть ее в полном файле ниже при добавлении объявления скрипта `manifest.json` контента далее\).</span><span class="sxs-lookup"><span data-stu-id="d1e9a-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="d1e9a-145">Теперь вы написали код в файле, чтобы отправить сообщение на страницу контента, встроенную на текущей активной странице вкладки, но вы еще не создали и не ввели эту страницу `popup.js` контента.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="d1e9a-146">Сделайте это сейчас.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-146">Do that now.</span></span>  

5.  <span data-ttu-id="d1e9a-147">Обновление manifest.jsдля контента и веб-доступа</span><span class="sxs-lookup"><span data-stu-id="d1e9a-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="d1e9a-148">`manifest.json`Обновленный, который включает в себя и является следующим `content-scripts` `web_accessible_resources` образом.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="d1e9a-149">Добавленный раздел `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="d1e9a-150">Для атрибута установлено, что все файлы вводятся во все страницы вкладок браузера при загрузке `matches` `<all_urls>` каждой `content_scripts` вкладки.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="d1e9a-151">Допустимые типы файлов, которые можно вводить, это JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="d1e9a-152">Вы также `libjquery.min.js` добавили .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="d1e9a-153">Это можно включить из скачивания, упомянутого в верхней части раздела.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="d1e9a-154">Добавление jQuery и понимание связанного потока</span><span class="sxs-lookup"><span data-stu-id="d1e9a-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="d1e9a-155">В скриптах контента, которые вы вводите, запланируйте использование jQuery `$` \( \).</span><span class="sxs-lookup"><span data-stu-id="d1e9a-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="d1e9a-156">Вы добавили minified версию jQuery и положили ее в пакет расширения как `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="d1e9a-157">Эти сценарии контента работают в отдельных песочницах, что означает, что jQuery, впрыскиваемая на страницу, не передается `popup.js` содержимым.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="d1e9a-158">Имейте в виду, что даже если на вкладке браузера javaScript запущен на загруженной веб-странице, любой вводный контент не имеет к этому доступа.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="d1e9a-159">Вводимый JavaScript имеет доступ к фактическому DOM, загруженным на вкладке браузера.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="d1e9a-160">Добавление слушателя сообщения скрипта контента</span><span class="sxs-lookup"><span data-stu-id="d1e9a-160">Add the content script message listener</span></span>  

<span data-ttu-id="d1e9a-161">Вот этот файл, который вводится на каждую страницу вкладки `content-scripts\content.js` браузера на основе `manifest.json` `content-scripts` раздела.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="d1e9a-162">Обратите внимание, что все вышеперечисленные действия JavaScript — это регистрация `listener` метода `chrome.runtime.onMessage.addListener` API расширения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="d1e9a-163">Этот слушатель ждет сообщений, таких как сообщения, отправленные ранее с помощью метода `popup.js` `chrome.tabs.sendMessage` API расширения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="d1e9a-164">Первым параметром метода является функция, первый параметр которой — запрос — это сведения о `addListener` переданных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="d1e9a-165">Помните, что при использования метода эти атрибуты первого `popup.js` `sendMessage` параметра являются и `url` `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="d1e9a-166">Когда событие обрабатывается слушателем, запустится функция, которая является первым параметром.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="d1e9a-167">Первым параметром этой функции является объект, который имеет атрибуты, заданные `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="d1e9a-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="d1e9a-168">Эта функция просто обрабатывает три строки скрипта jQuery.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="d1e9a-169">Первая строка скрипта динамически вставляет в загон DOM раздел, который необходимо назначить в качестве **\<style\>** `slide-image` класса `img` элементу.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="d1e9a-170">Вторая строка скрипта добавляет элемент прямо под вкладку браузера, заданный классом, а также ID этого `img` `body` элемента `slide-image` `imageDivId` изображения.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="d1e9a-171">Третья строка скрипта добавляет событие, которое охватывает все изображение, позволяя пользователю выбирать где-либо на изображении, и это изображение удаляется со страницы \(вместе с ним является слушателем `click` событий\).</span><span class="sxs-lookup"><span data-stu-id="d1e9a-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="d1e9a-172">Добавление функций для удаления отображаемого изображения при выборе</span><span class="sxs-lookup"><span data-stu-id="d1e9a-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="d1e9a-173">Теперь при просмотре любой страницы и \*\*\*\* выборе значка расширения всплывающее меню отображается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html после выбора значка расширения":::
   <span data-ttu-id="d1e9a-175">popup.html после выбора значка расширения</span><span class="sxs-lookup"><span data-stu-id="d1e9a-175">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="d1e9a-176">При выборе кнопки `Display` вы получите то, что ниже.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="d1e9a-177">Если выбрать где-либо на изображении, этот элемент изображения удаляется, а страницы вкладок сваляются обратно к первоначально `stars.jpeg` отображаемой.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Изображение, показывающаяся в браузере":::
   <span data-ttu-id="d1e9a-179">Изображение, показывающаяся в браузере</span><span class="sxs-lookup"><span data-stu-id="d1e9a-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="d1e9a-180">Вы создали расширение, которое успешно отправляет сообщение из всплывающее всплывающее изображение значка расширения и динамически вставлено JavaScript, запущенное в виде контента на вкладке браузера.  Вводимый контент задает элемент изображения для отображения статических звезд jpeg.</span><span class="sxs-lookup"><span data-stu-id="d1e9a-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Завершенный источник пакета расширения | Документы Майкрософт"  
