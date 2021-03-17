---
description: Отображение и редактирование файлов, создание фрагментов, отладка JavaScript и настройка рабочих пространств в панели Источников Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7ce7ae32b4bf91419512ec9e387cdf75549552a5
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439607"
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

# <a name="sources-panel-overview"></a>Обзор панели источников  

Для выполнения следующих действий используйте панель Microsoft Edge DevTools **Sources.**  

*   [Отображение файлов.](#display-files)  
*   [Изменение CSS и JavaScript](#edit-css-and-javascript).  
*   [Создание и сохранение **фрагментов** JavaScript,](#create-save-and-run-snippets)которые можно запустить на любой веб-странице.  **Фрагменты похожи** на закладки.  
*   [Отламывка JavaScript](#debug-javascript).  
*   [Настройка рабочего пространства,](#set-up-a-workspace)чтобы изменения, внесенные в DevTools, были сохранены в коде файловой системы.  
    
## <a name="display-files"></a>Отображение файлов  

Используйте **панель Page;** отображение всех ресурсов, загруженных на странице.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Панель Page" lightbox="../media/sources-page-pane.msft.png":::
   Панель **Page**  
:::image-end:::  

Порядок **** организации области Страницы:  
*   Верхний уровень, например `top` на предыдущем рисунке, представляет [htmL-кадр.][W3CHtml4Frames]  Найдите `top` на каждой странице, которую вы посещаете.  `top` представляет основную рамку документа.  
*   Второй уровень, например `docs.microsoft.com` на предыдущем рисунке, представляет [происхождение][HtmlstandardOrigin].  
*   На третьем, четвертом уровнях и так далее представлены каталоги и ресурсы, загруженные из этого происхождения.  Например, на предыдущем рисунке полный путь к `devtools-guide-chromium` ресурсу `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Выберите файл на панели **Страницы,** чтобы отобразить содержимое в **области редактора.**  Вы можете отображать любой тип файла.  Для изображений отображается предварительный просмотр изображения.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Отображение содержимого a4d10f71.index-docs.js в области редактора" lightbox="../media/sources-editor-pane.msft.png":::
   Отображение содержимого `a4d10f71.index-docs.js` панели **редактора**  
:::image-end:::  

## <a name="edit-css-and-javascript"></a>Изменение CSS и JavaScript  

Используйте области **редактора** для редактирования CSS и JavaScript.  DevTools обновляет страницу для запуска нового кода.  Например, если изменить CSS-файл, добавив правило стиля ниже:

```css
.metadata.page-metadata {
    color: red;
}
```

Это изменение должно вступает в силу немедленно.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Изменение CSS в области редактора, чтобы изменить текстовый цвет субтитра на красный" lightbox="../media/edit-css.msft.png":::
   Изменение CSS в **области редактора,** чтобы изменить текстовый цвет субтитра на красный  
:::image-end:::  

Изменения CSS вступает в силу немедленно, без сохранения.  Чтобы изменения JavaScript вступили в силу, выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\).  DevTools не выполняет повторного запуска скрипта, поэтому только изменения JavaScript, которые вступает в силу, это те, которые вы делаете внутри функций.  Например, на следующем рисунке обратите внимание, как `console.log('A')` не запустить, в то время как `console.log('B')` делает.  Если DevTools повторно запускает весь скрипт после внося изменения, то текст регистрируется `A` в **консоли**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Редактирование JavaScript в области редактора" lightbox="../media/edit-js.msft.png":::
   Редактирование JavaScript в **панели редактора**  
:::image-end:::  

DevTools стирает изменения CSS и JavaScript при обновлении страницы.  Перейдите [к настройкам рабочего пространства,](#set-up-a-workspace) чтобы узнать, как сохранить изменения в файловой системе.  

## <a name="create-save-and-run-snippets"></a>Создание, сохранение и запуск фрагментов  

Фрагменты — это скрипты, которые можно выполнить на любой странице.  Представьте, что вы несколько раз введите следующий код в **консоли,** чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли.**  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Вместо этого вы можете сохранить **** этот код в фрагменте и запустить его с помощью нескольких нажатий кнопки в любое время.  DevTools сохраняет **фрагмент файла** в файловой системе.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Фрагмент, который вставляет библиотеку jQuery на страницу" lightbox="../media/snippet.msft.png":::
   Фрагмент, **который** вставляет библиотеку jQuery на страницу  
:::image-end:::  

Для запуска **фрагмента:**

*   Откройте файл с помощью **панели фрагментов** и выберите **Выполнить** \. ![ Кнопка Запуск ](../media/run-snippet-icon.msft.png) \).  
*   Откройте [командное меню,][DevtoolsGuideChromiumCommandMenuIndex]удалите символ, введите, введите имя `>` фрагмента, а затем выберите `!` **** `Enter` .  
    
Перейдите [к запуску фрагментов кода с любой страницы,][DevtoolsGuideChromiumJavascriptSnippets] чтобы узнать больше.

## <a name="debug-javascript"></a>Отламывка JavaScript  

Вместо того, чтобы использовать для того, чтобы сделать вывод о неправильном использовании JavaScript, следует использовать средства отладки `console.log()` Microsoft Edge DevTools.  Общая идея состоит в том, чтобы установить точку остановки, которая является преднамеренным местом остановки в коде, а затем выполнить время работы кода по одной строке за раз.  При прошаговке кода можно отобразить и изменить значения всех задаваемых в настоящее время свойств и переменных, запустить JavaScript в консоли **и**другие.

Перейдите [к началу отладки JavaScript,][DevtoolsGuideChromiumJavascriptIndex] чтобы узнать основы отладки в DevTools.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Отламывка JavaScript" lightbox="../media/debugging.msft.png":::
   Отламывка JavaScript  
:::image-end:::  

## <a name="set-up-a-workspace"></a>Настройка рабочего пространства  

По умолчанию при редактировании файла в средстве **Sources** эти изменения теряются при обновлении страницы.  **Рабочей области позволяют** сохранять изменения, внесенные в DevTools, в файловую систему.  По сути, DevTools может использоваться в качестве редактора кода.

Перейдите [к редактированию файлов с помощью рабочей области,][DevtoolsGuideChromiumWorkspacesIndex] чтобы начать работу.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Запустите фрагменты JavaScript на любой странице с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Изменение файлов с помощью рабочей области | Документы Майкрософт"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin | СТАНДАРТ HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/sources) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
