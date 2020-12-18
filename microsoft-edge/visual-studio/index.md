---
description: Microsoft Edge (Chromium) и Visual Studio
title: VisualStudio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, vs, visual studio, отладка
ms.openlocfilehash: f3796a040fe6c658211b4009445b5c179ab9b077
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231211"
---
# VisualStudio

Microsoft [Visual Studio](https://visualstudio.microsoft.com/vs/) — это интегрированная среда разработки (IDE), которую можно использовать для редактирования, отлаки, построения и публикации веб-приложений. Это программа с множеством функций, которую можно использовать для многих аспектов веб-разработки. Над стандартным редактором и отладчиком, который предоставляет большинство IDEs, Visual Studio компиляторы, средства завершения кода, графические дизайнеры и многие другие функции для упростить процесс разработки. На этой [странице](https://visualstudio.microsoft.com/downloads/) можно скачать Visual Studio если вы еще не используете его.

В настоящее время Visual Studio 2019 поддерживает отладку JavaScript в Microsoft Edge для приложений ASP\.NET Framework и ASP\.NET Core. Выполните следующие действия для отлаки Microsoft Edge из Visual Studio.

## Запуск Microsoft Edge
Visual Studio создает приложение ASP\.NET и ASP\.NET Core, запускает веб-сервер, запускает Microsoft Edge и подключает отладчий отладок Visual Studio одним нажатием одной кнопки. Это позволяет вам отлаголать JavaScript, запущенный в Microsoft Edge, непосредственно из IDE!

### Создание нового веб-приложения ASP.NET Core

Откройте Visual Studio 2019 и выберите **"Создать новый проект".** На следующем экране выберите **веб-приложение ASP\.NET Core** и нажмите кнопку **"Далее".**

> ##### Рис. 1  
> Создание нового ASP.NET core Web Application ![ Create a new ASP.NET Core Web Application](./media/create-new-project.png)  

**Укажайте имя проекта** для нового проекта и нажмите кнопку **"Создать".** В этом примере выберите **** React.jsв качестве шаблона, в котором показано, как интегрировать React.js с приложением ASP.NET Core, и нажмите кнопку **"Создать".**

### Запуск Microsoft Edge из Visual Studio

После создания проекта откройте **ClientApp/src/components/Counter.js. ** Теперь сообщите Visual Studio javaScript, выбрав в этом выпадающий поток **** рядом с зеленой кнопкой "Play" и **IIS Express.** 

> ##### Рисунок 2  
> В dropdown рядом с зеленой кнопкой **"Play"** и **IIS Express** 
> ![ the dropdown next to the green Play button and IIS Express](./media/vs-dropdown.png)  

Выберите **"Отладка сценариев"** и нажмите кнопку **"Включено".**

> ##### Рисунок3  
> Включить отладку сценариев в Visual Studio включить отладку ![ сценариев в Visual Studio](./media/enable-script-debugging.png)  

В том же dropdown выберите веб-браузер и щелкните канал предварительного просмотра Microsoft Edge, который вы хотите запустить Visual Studio: Microsoft Edge Canary, Dev или Beta. **** Если вы еще не сделали этого, перенайтесь на эту [страницу,](https://www.microsoftedgeinsider.com/download) чтобы установить каналы предварительного просмотра Microsoft Edge.

> ##### Рисунок4  
> Выберите канал предварительного просмотра Microsoft Edge, который Visual Studio запустить, выберите канал предварительного просмотра Microsoft Edge, который Visual Studio ![ запустить](./media/set-web-browser.png)  

> [!NOTE]
> Если вы выберете Microsoft Edge (EdgeHTML), Visual Studio будет запускать его вместо Microsoft Edge (Chromium). [Установите каналы предварительного](https://www.microsoftedgeinsider.com/download) просмотра Microsoft Edge и выберите их или убедитесь, что на вашем компьютере установлена версия Microsoft Edge (Chromium), а не Microsoft Edge (EdgeHTML).

Теперь, Visual Studio настроены правильно, нажмите зеленую кнопку **"Play".** Visual Studio построит приложение, запустит веб-сервер, запустит Microsoft Edge и перейдите к порту, указанному в `https://localhost:44362/` **launchSettings.js.**

> ##### Рисунок 5  
> Microsoft Edge, запущенный из Visual Studio ![ Microsoft Edge, запущенный из Visual Studio](./media/edge-launch.png)  

### Отлажите JavaScript, запущенный в Microsoft Edge

Переключиться на Visual Studio. В **Counter.js**установите точку останова в строке 13, щелкнув в переборе рядом с этой строкой.

> ##### Рисунок6
> Установка точки останова в Visual Studio, щелкнув перебор рядом с строкой 13 в **Counter.js**Установка точки останова в Visual Studio, щелкнув перебор рядом с строкой 13 в Counter.js
> ![](./media/set-breakpoint.png)  

Теперь снова переключиться на экземпляр Microsoft Edge, Visual Studio запущен. Щелкните **"Счетчик"** в NavMenu слева от страницы. Теперь нажмите **кнопку "Приращение".**

> ##### Рисунок7
> Страница счетчика в нашем ASP.NET веб-приложении ![ "Счетчик" в веб-приложении ASP.NET Core](./media/edge-counter.png)  

Отладник JavaScript в Visual Studio будет нажать точку останова, установленную ** в **Counter.js. Visual Studio приостановил выполнение JavaScript, запущенного в Microsoft Edge, и вы можете пошаговую

> ##### Рисунок8
> Visual Studio JavaScript, запущенный в Microsoft Edge, Visual Studio прио в Microsoft ![ Edge](./media/hit-breakpoint.png)  

В этом примере была лишь небольшая демонстрация функциональных возможностей, доступных в Visual Studio. Узнайте больше обо всех том, что можно сделать в Visual Studio 2019 г., прочитав их [документацию.](/visualstudio/windows/?view=vs-2019&preserve-view=true)

## Присоединение к Microsoft Edge
В предыдущем рабочий процесс Visual Studio Microsoft Edge. С помощью этого рабочего процесса вы сможете прикрепить отладку Visual Studio к уже запущенным экземплярам Microsoft Edge. 

Во-первых, убедитесь, что нет запущенных экземпляров Microsoft Edge. Теперь в терминале запустите следующую команду:

```console
start msedge –remote-debugging-port=9222
```

В Visual Studio откройте меню **"Отлажать"** и выберите "Присоединение **к процессу"** или нажмите `Ctrl`  +  `Alt`  +  `P` .

> ##### Рисунок9
> Selecting **Attach to Process** in Visual Studio ![ Selecting **Attach to Process** in Visual Studio](./media/attach-to-process.png)  

В **диалоговом** окне **** "Присоединение к процессу" установите тип подключения к **websocket протокола разработки Chrome (без проверки подлинности).** В **текстовом ящике цели** подключения введите и `http://localhost:9222/` нажмите `Enter` . Вы увидите список открытых вкладок в Microsoft Edge, указанный в диалоговом окте "Присоединение к **процессу".**

> ##### Рисунок 10
> Настройка диалоговое окно **"Присоединение** к процессу" в Visual Studio настройки диалоговое окно "Присоединение к ![ процессу" в Visual Studio](./media/attach-to-process-dialog.png)  

Нажмите **кнопку "Выбрать"...** и проверьте **JavaScript (Microsoft Edge — Chromium).** Вы можете добавлять вкладки, переходить на новые вкладки, закрывать вкладки и видеть изменения, отраженные в диалоговом окке "Присоединение к процессу", нажав кнопку "Обновить". **** **** Выберите вкладку, отлажаемую, и нажмите кнопку **"Присоединить".**

Отлад Visual Studio теперь подключен к Microsoft Edge! Вы можете приостановить выполнение JavaScript, установить точки останова и увидеть их непосредственно в окне "Отлагивание выходных `console.log()` данных" Visual Studio.

## Знакомство с командой Microsoft Visual Studio Microsoft  

Мы с нетерпением стремимся узнать больше о том, как вы работаете с JavaScript в Visual Studio!  Отправьте нам отзыв, щелкнув значок "Обратная связь" в Visual Studio или нажав на твит [ **** @VisualStudio and @EdgeDevTools](https://twitter.com/intent/tweet?text= @VisualStudio+@EdgeDevTools).  

> ##### Рисунок11
> Значок **"Обратная** связь" Visual Studio ![ значок "Обратная связь" в Visual Studio](./media/feedback-icon.png)  
