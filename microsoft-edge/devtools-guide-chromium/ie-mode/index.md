---
description: Режим IE и Microsoft Edge (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, ie11, Internet Explorer 11, режим ie
ms.openlocfilehash: c88da78e073a75a664561aba899ca5c8ada78477
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235155"
---
# Режим Internet Explorer и DevTools  

В этой статье описывается, как режим Internet Explorer \(режим IE\) интегрируется с Microsoft Edge \(Chromium\) DevTools.  

## Общее представление о режиме IE  

Режим IE позволяет предприятиям указывать список веб-сайтов, которые работают только в Internet Explorer 11.  При переходе к этим веб-сайтам в Microsoft Edge \(Chromium\) экземпляр Internet Explorer 11 запускается и отрисовка сайта на вкладке.  Эта функция позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время несовместимы с современными веб-браузерами.  Поддержка следующих технологий включена в режим IE.  

*   Режимы документов IE  
*   элементы ActiveX;  
*   другие устаревшие компоненты  

В режиме IE процесс отрисовки основан на Internet Explorer 11.  Диспетчер процессов Microsoft Edge \(Chromium\) обрабатывает время существования процесса отрисовки.  Она ограничена сроком действия вкладки для определенного сайта \(или app\).  Когда вкладка отображается в режиме IE, индикатор событий отображается в адресной панели для определенной вкладки.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Индикатор событий режима IE в адресной панели" lightbox="../media/ie-mode-badge.msft.png":::
   Индикатор событий режима IE в адресной панели  
:::image-end:::  

Режим IE в настоящее время доступен в Windows 10 версии 1903 \(обновление за май 2019 г.), но скоро появится на всех поддерживаемых платформах Windows.  

## Запуск DevTools на вкладке в режиме IE  

Если вы пытаетесь просмотреть режим документов веб-сайта в режиме IE, выберите индикатор событий в адресной панели.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Просмотр режима документов с помощью индикатора событий режима IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Просмотр режима документов с помощью индикатора событий режима IE  
:::image-end:::  

Если вкладка использует режим IE, DevTools не работает и возникают следующие условия.

*   Если выбрать или выбрать, будет запущен пустой экземпляр `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   If you open a contextual menu \(right-click\) and choose **View Source,** Notepad is launched.  
*   Если открыть контекстное меню \(щелкните правой кнопкой мыши\), элемент **Inspect не** будет виден.  

Причина, по которой ряд средств в DevTools **** \(например, средства "Сеть" и "Производительность"), не работают, заключается в том, что механизм отрисовки переключается с Chromium на Internet Explorer 11 в режиме IE. ****  Чтобы предоставить отзыв, перейдите к [контакту с командой Разработчиков Microsoft Edge.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools, запущенный в режиме IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools, запущенный в режиме IE  
:::image-end:::  

Чтобы протестировать веб-сайт на основе Internet Explorer 11 (или app\) в Internet Explorer 11 и режиме IE, выполните следующие действия.  

1.  Откройте Internet Explorer 11.  
    *   В Windows 10 найдите ярлык для Internet Explorer 11.
        1.  **Меню "Пуск"**  >  **Дополнительные возможности**  >  Windows **Internet Explorer 11**.  
    *   В Windows 7 найдите Internet Explorer 11.
        1.  **Меню "Пуск"**  >  **Internet Explorer 11**.  
1.  В Internet Explorer 11 откройте ту же веб-страницу.  
1.  Запустите Internet Explorer DevTools.  
    *   Выберите `F12` .  
    *   Наведите курсор в любом месте, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите элемент **Inspect.**  Дополнительные сведения об использовании этих средств можно найти в средстве разработчика [F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]  

## Удаленная отладка и режим IE  

Запустите Microsoft Edge \(Chromium\) с включенной удаленной отладки из интерфейса командной строки.  Visual Studio, Visual Studio Code и другие средства разработки обычно запускают команду для запуска Microsoft Edge.  Следующая команда запускает Microsoft Edge с портом удаленной отладки, установленным на `9222` ..  

```shell
start msedge --remote-debugging-port=9222
```  

После запуска Microsoft Edge \(Chromium\) с помощью аргумента командной строки режим IE недоступен.  Вы по-прежнему можете перейти на веб-сайты \(или приложения\), которые в противном случае отображаются в режиме IE.  Содержимое веб-сайта \(или app\) визуален с помощью Chromium, а не Internet Explorer 11.  Ожидается, что части веб-страниц, зависят от IE11, например ActiveX элементов управления, не будут правильно отрисовки.  Индикатор событий в режиме IE не появляется в адресной панели.  

Режим IE остается недоступным до полного закрытия и перезапуска Microsoft Edge \(Chromium\).  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработчика F12 | Документы Майкрософт"  
