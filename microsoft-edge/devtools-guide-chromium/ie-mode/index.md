---
description: Режим IE и Microsoft Edge (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, ie11, internet explorer 11, ie mode
ms.openlocfilehash: e65869cd88b449dcde0aec25c77df27f99b78f8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398604"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Режим Internet Explorer и DevTools  

В этой статье описывается, как режим Internet Explorer \(IE mode\) интегрируется с Microsoft Edge \(Chromium\) DevTools.  

## <a name="understanding-ie-mode"></a>Понимание режима IE  

Режим IE позволяет предприятиям указывать список веб-сайтов, которые работают только в Internet Explorer 11.  При переходе на эти веб-сайты в Microsoft Edge \(Chromium\), экземпляр Internet Explorer 11 запускает и отрисовывает сайт на вкладке.  Функциональность позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время не совместимы с любыми современными веб-браузерами.  Поддержка следующих технологий включена в режим IE.  

*   Режимы документов IE  
*   элементы ActiveX;  
*   другие устаревшие компоненты  

В режиме IE процесс визуализации основан на Internet Explorer 11.  Диспетчер процессов Microsoft Edge \(Chromium\) обрабатывает весь срок службы процесса отрисовки.  Она ограничена сроком службы вкладки для определенного сайта \(или app\).  При отрисовке вкладки в режиме IE в панели адресов для определенной вкладки появляется значок.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Значок режима IE в панели адресов" lightbox="../media/ie-mode-badge.msft.png":::
   Значок режима IE в панели адресов  
:::image-end:::  

Режим IE в настоящее время доступен на Windows 10 Версии 1903 \(Обновление мая 2019\), но скоро появится на всех поддерживаемых платформах Windows.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Запуск DevTools на вкладке в режиме IE  

Если вы пытаетесь просмотреть режим документа веб-сайта в режиме IE, выберите значок в панели адресов.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Просмотр режима документа с помощью значка режима IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Просмотр режима документа с помощью значка режима IE  
:::image-end:::  

Если вкладка использует режим IE, devTools не работают и возникают следующие условия.

*   Если выбрать или выбрать, пустой экземпляр `F12` `Ctrl` + `Shift` + `I` запущенных DevTools Microsoft Edge \(Chromium\) отображает следующее сообщение.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Если вы откроете контекстное меню \(правой кнопкой мыши\) и выберите **View Source,** запущен блокнот.  
*   Если вы откроете контекстное меню \(правой кнопкой мыши\), элемент **Inspect** не отображается.  

Причина того, что ряд средств в DevTools **** \(как средства сети и производительности\) не работают, заключается в том, что двигатель отрисовки переключается с Chromium на Internet Explorer 11 в режиме IE. ****  Чтобы обеспечить обратную связь, перейдите к [контакту с командой Microsoft Edge DevTools.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools запущен в режиме IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools запущен в режиме IE  
:::image-end:::  

Чтобы протестировать веб-сайт Internet Explorer 11 на основе \(или app\) в режиме Internet Explorer 11 и IE, выполните следующие действия.  

1.  Откройте Internet Explorer 11.  
    *   В Windows 10 найдите ярлык для Internet Explorer 11.
        1.  **Меню пуск**  >  Аксессуары Для **Windows**  >  **Internet Explorer 11**.  
    *   В Windows 7 найдите Internet Explorer 11.
        1.  **Меню пуск**  >  **Internet Explorer 11**.  
1.  В Internet Explorer 11 откройте ту же страницу.  
1.  Запуск Internet Explorer DevTools.  
    *   Выберите `F12` .  
    *   Наведите курсор в любом месте, откройте контекстное меню \(правой кнопкой мыши\) и выберите **элемент Inspect**.  Дополнительные сведения об использовании этих средств перейдите к использованию средств [разработчика F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]  

## <a name="remote-debugging-and-ie-mode"></a>Удаленный отладка и режим IE  

Запустите Microsoft Edge \(Chromium\) с включенной удаленной отладки из интерфейса командной строки.  Microsoft Visual Studio, Microsoft Visual Studio code и другие средства разработки обычно запускают команду для запуска Microsoft Edge.  Следующая команда запускает Microsoft Edge с портом удаленной `9222` отладки.  

```shell
start msedge --remote-debugging-port=9222
```  

После запуска Microsoft Edge \(Chromium\) с помощью аргумента командной строки режим IE недоступен.  Вы по-прежнему можете перейти к веб-сайтам \(или приложениям\), которые в противном случае отображаются в режиме IE.  Содержимое веб-сайта \(или app\) отрисовывается с помощью Chromium, а не Internet Explorer 11.  Ожидается, что части веб-страниц, которые зависят от IE11, например ActiveX элементов управления, не отрисуются правильно.  Значок режима IE не появляется в панели адресов.  

Режим IE остается недоступным до полного закрытия и перезапуска Microsoft Edge \(Chromium\).  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработки F12 | Документы Майкрософт"  
