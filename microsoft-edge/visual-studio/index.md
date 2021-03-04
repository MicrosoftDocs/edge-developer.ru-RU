---
description: Microsoft Edge (Chromium) и Visual Studio
title: VisualStudio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, vs, visual studio, debugger
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387276"
---
# <a name="visual-studio"></a>VisualStudio  

Microsoft [Visual Studio][MicrosoftVisualstudioVs] — это интегрированная среда разработки \(IDE\).   Используйте его для редактирования, отлаговки, сборки и публикации веб-приложений.  Это программа с богатыми функциями, которая может использоваться для многих аспектов веб-разработки.  Помимо стандартного редактора и отладки, которые предоставляют большинство IDEs, Visual Studio включает следующие функции, облегчаю процесс разработки.  

*   компиляторы  
*   Средства завершения кода  
*   графические дизайнеры  
*   многие другие  
    
Если вы еще не используете Visual Studio, перейдите по ссылке [Скачать Visual Studio,][MicrosoftVisualstudioDownloads] чтобы скачать его.  

В настоящее время Visual Studio 2019 г. поддерживает отладку JavaScript в Microsoft Edge для ASP.NET Framework и ASP.NET Core приложений.  Выполните следующие действия, чтобы использовать Visual Studio для отлаговки Microsoft Edge.  

## <a name="launch-microsoft-edge"></a>Запуск Microsoft Edge  

Visual Studio завершает следующий рабочий процесс с помощью одной кнопки.  

1.  Создает приложение ASP.NET ASP.NET Core.  
1.  Запускает веб-сервер.  
1.  Запускает Microsoft Edge.  
1.  Подключает Visual Studio отладка.  
    
Упрощенный рабочий процесс позволяет отламывать JavaScript, который работает в Microsoft Edge непосредственно из вашего IDE.  

### <a name="create-a-new-aspnet-core-web-app"></a>Создание нового ASP.NET основного веб-приложения  

Откройте Visual Studio 2019 г. и **выберите Создание нового проекта.**  На следующем экране выберите ASP.NET **Веб-приложение**  >  **Далее**.  

:::image type="complex" source="./media/create-new-project.png" alt-text="Создание нового ASP.NET основного веб-приложения" lightbox="./media/create-new-project.png":::
   Создание нового ASP.NET основного веб-приложения  
:::image-end:::  

**Укайте имя проекта** для нового проекта и выберите **Create**.  Для целей примера выберитеReact.js** в ** качестве шаблона и выберите **Create**.  Шаблон **React.js** указывает, как интегрировать React.js с приложением ASP.NET Core.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Запуск Microsoft Edge из Visual Studio  

После создания проекта откройте `ClientApp/src/components/Counter.js` .  Теперь, чтобы использовать Visual Studio для отламки JavaScript, выберите выпадаемую кнопку рядом с зеленой кнопкой **Play** и **IIS Express.**  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="Выпадаемая часть рядом с зеленой кнопкой Play и IIS Express" lightbox="./media/vs-dropdown.png":::
   Выпадаемая часть рядом с зеленой кнопкой **Play** и **IIS Express**  
:::image-end:::  

Выберите **включенную отладку**  >  **скриптов**.  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Включаем отладку скриптов в Visual Studio" lightbox="./media/enable-script-debugging.png":::
   Включаем отладку скриптов в Visual Studio  
:::image-end:::  

В одном и том **** же отсеве выберите веб-браузер > предварительного просмотра канала Microsoft Edge, который Visual Studio запускать, например Microsoft Edge Canary, Dev или Beta.  Если вы еще не используете один из каналов предварительного просмотра Microsoft Edge, перейдите к Скачать каналы предварительного просмотра Microsoft [Edge,][MicrosoftedgeinsiderDownload] чтобы скачать один из них.  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Выберите канал предварительного просмотра Microsoft Edge, который Visual Studio запустить" lightbox="./media/set-web-browser.png":::
   Выберите канал предварительного просмотра Microsoft Edge, который Visual Studio запустить  
:::image-end:::  

> [!NOTE]
> Если вы выбрали Microsoft Edge \(EdgeHTML\), Visual Studio запускает его вместо Microsoft Edge \(Chromium\).  Установите один из каналов предварительного просмотра Microsoft Edge или убедитесь, что версия Microsoft [Edge,][MicrosoftedgeinsiderDownload] установленная на вашем компьютере, является Microsoft Edge \(Chromium\) а не Microsoft Edge \(EdgeHTML\).  

Теперь, Visual Studio правильно настроена, выберите зеленую кнопку **Play.**  Visual Studio создает приложение, запустите веб-сервер, запустите Microsoft Edge и перейдите в порт или любой `https://localhost:44362/` порт, указанный в `launchSettings.json` .  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge запускается с Visual Studio" lightbox="./media/edge-launch.png":::
   Microsoft Edge запускается с Visual Studio  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Отламка JavaScript, запущенная в Microsoft Edge  

Переключение на Visual Studio.  В `Counter.js` , чтобы установить точку разрыва на строке 13, выберите желоб рядом с строкой.  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Выберите желоб рядом с строкой 13 в Counter.js, чтобы установить точку разрыва в Visual Studio" lightbox="./media/set-breakpoint.png":::
   Выберите желоб рядом с строкой 13, чтобы установить точку `Counter.js` разрыва в Visual Studio  
:::image-end:::  

Теперь переключение на экземпляр Microsoft Edge, который Visual Studio запущен.  Выберите на **счетчике** в NavMenu слева от веб-страницы.  Теперь выберите **Приращение**.  

:::image type="complex" source="./media/edge-counter.png" alt-text="Страница Счетчик в нашем ASP.NET веб-приложении Core" lightbox="./media/edge-counter.png":::
   Страница Счетчик в нашем ASP.NET веб-приложении Core  
:::image-end:::  

Отладка JavaScript в Visual Studio попадает в точку разлома, в который вы вписались. `Counter.js`  Visual Studio теперь приостанавливается время запуска JavaScript в Microsoft Edge, и вы можете ступить через строку сценария по очереди.  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio JavaScript, запущенный в Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   Visual Studio JavaScript, запущенный в Microsoft Edge  
:::image-end:::  

В этом примере была лишь небольшая демонстрация функциональных возможностей, доступных в Visual Studio.  Дополнительные сведения о функциональных возможностях Visual Studio 2019 г. перейдите Visual Studio [документации.][VisualStudioWindowsIndex]  

## <a name="attach-to-microsoft-edge"></a>Присоединение к Microsoft Edge  

Ранее необходимо было запустить Microsoft Edge из Visual Studio.  Теперь вы можете прикрепить отладку Visual Studio к уже запущенной экземпляру Microsoft Edge.  

Во-первых, убедитесь, что нет запущенных экземпляров Microsoft Edge.  Теперь из командной строки запустите следующую команду.  

```console
start msedge –remote-debugging-port=9222
```  

Из Visual Studio откройте меню **Отлаговка** и выберите **Присоединение к процессу** или выберите `Ctrl` + `Alt` + `P` .  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Выберите Присоединение к процессу в Visual Studio" lightbox="./media/attach-to-process.png":::
   Выберите **Присоединение к процессу** в Visual Studio  
:::image-end:::  

В **диалоговом** окне "Присоединение к процессу" установите тип **подключения** к веб-сайту протокола **chrome devtools (без проверки подлинности).**  В **целевом текстовом ящике Подключения** введите `http://localhost:9222/` и выберите `Enter` .  Просмотрите список открытых вкладок, указанных в диалоговом окте Microsoft Edge в диалоговом окте **"Присоединение к процессу".**  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Настройте диалоговое окно Attach to Process в Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   Настройте **диалоговое окно Attach to Process** в Visual Studio  
:::image-end:::  

Выберите **Выберите...** > рядом с **JavaScript (Microsoft Edge — Chromium).**  Чтобы добавить вкладки, перейдите на новые вкладки и закройте **** вкладки и отобразите изменения, отражающиеся в диалоговом окте "Присоединение к процессу", выберите кнопку **"Обновление".**  Выберите вкладку, которая необходимо отлагывать, и **прикрепить**.  

Теперь Visual Studio отладка присоединена к Microsoft Edge.  Можно приостановить работу JavaScript, установить точки разрыва и просмотреть заявления непосредственно в окне `console.log()` Отлаговка в Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Контакт с командой Microsoft Visual Studio  

Команды Microsoft Visual Studio Microsoft Edge хотят узнать больше о работе с JavaScript в Visual Studio.  Чтобы отправить отзыв, выберите значок **Отправка** отзывов в Visual Studio или твит @VisualStudio [и @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Значок Отправка отзывов в Visual Studio" lightbox="./media/feedback-icon.png":::
   Значок **Отправка** отзывов в Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio документации | Документы Майкрософт"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Загрузка Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Чирикать @VisualStudio и @EdgeDevTools | Twitter"  
