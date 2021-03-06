---
description: Сведения о том, как управлять папками данных пользователей в приложениях WebView2
title: Управление папкой "данные пользователя" в приложениях WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML EDGE, папка "данные пользователя"
ms.openlocfilehash: ff11c4e83fa931a97ed1b5c8afa4a30b5c0b5d25
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118991"
---
# Управление папкой "данные пользователя"  

Приложения WebView2 взаимодействуют с папками данных пользователей для хранения данных браузера, таких как cookie-файлы, разрешения и кэшированные ресурсы.  Каждый экземпляр элемента управления WebView2 связан с папкой данных пользователя.  Каждая папка User Data является уникальной для пользователя.  

## Рекомендации  

Папки данных пользователя создаются автоматически с помощью WebView2.  WebView2 разработчики управляют временем существования папки данных пользователя.  Если приложение повторно использует пользовательские данные из сеансов приложений, попробуйте сохранить их, в противном случае их можно удалить.  При принятии решения о том, как управлять папками с данными пользователя, учитывайте указанные ниже сценарии.  

*   Если один и тот же пользователь несколько раз использует приложение, а веб-содержимое приложения зависит от данных пользователя, сохраните папку с данными о пользователях.  Если несколько пользователей многократно используют приложение, создайте новую папку с данными для каждого нового пользователя и сохраните их в папке User Data для каждого пользователя.
*   Если ваше приложение не имеет повторяющихся пользователей, создайте новую папку данных пользователя для каждого пользователя и удалите предыдущую папку данных пользователя.  

## Создание папок с данными пользователя  

Чтобы указать расположение папки данных пользователя, включите `userDataFolder` параметр при вызове [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) или [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.NET \).  После создания данные браузера из элемента управления WebView2 хранятся во вложенной папке `userDataFolder` .  Если `userDataFolder` не указано, WebView2 создает папки данных пользователя в расположениях по умолчанию, как описано ниже.  

*   Для приложений, упакованных из Магазина Windows, папка пользователя по умолчанию является `ApplicationData\LocalFolder` вложенной папкой в папке пакета.  
*   Для существующих классических приложений Папка данных пользователя по умолчанию — это путь к исполняемому файлу приложения + `.WebView2` .  Вместо использования по умолчанию рекомендуется указать папку с данными пользователя и создать ее в той же папке, где хранятся все другие данные приложения.  

## Удаление папок с данными пользователя  

Приложению может потребоваться удалить папки данных пользователя.  

*   При удалении приложения.  Если удалить приложения из магазина для Windows, Windows автоматически удалит папки с данными пользователей.  
*   Для очистки всего журнала данных браузера.  
*   Для восстановления из повреждения данных.  
*   Для удаления предыдущих данных сеанса.  

> [!NOTE]
> Файлы в папках данных пользователя по-прежнему будут использоваться после закрытия приложения WebView2.  В этом случае дождитесь завершения процесса браузера и всех дочерних процессов, прежде чем удалять папку.  Идентификатор процесса браузера можно получить с помощью `BrowserProcessId` Свойства WebView2.  

## Общий доступ к папкам данных пользователей  

Элементы управления WebView2 могут совместно использовать одни и те же папки данных пользователя.  

*   [Оптимизируйте системные ресурсы](../concepts/process-model.md) , выполнив один процесс браузера.  
*   Предоставление общего доступа к журналу браузера и кэшированным ресурсам.  

При совместном доступе к папкам данных пользователей учитывайте следующее:  

1.  При повторном создании WebView2 элементов управления для обновления версий браузера с помощью событий [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \ (Win32 \) или [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \ (.NET \) убедитесь, что браузеры завершают работу и закрывают элементы управления WebView2, которые имеют доступ к той же папке данных пользователя.  Чтобы получить идентификатор процесса браузера, используйте `BrowserProcessId` свойство элемента управления WebView2.  

2.  Для элементов управления WebView2, использующих одну и ту же папку данных пользователя, должны использоваться одинаковые параметры для [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \ (Win32 \) или [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \ (.NET).  В противном случае создание WebView2 завершается сбоем `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  

Чтобы изолировать различные части приложения или совместное использование данных между элементами управления WebView2, вы можете выбрать использование разных папок данных пользователя.  Например, приложение может состоять из двух элементов управления WebView2, для отображения объявления и другого для отображения содержимого приложения.  В этом сценарии разработчики могут использовать различные папки данных пользователя для каждого элемента управления WebView2.  

> [!NOTE]
> Каждый процесс браузера WebView2 потребляет дополнительную память и место на диске.  Поэтому мы не рекомендуем запускать WebView2s с использованием слишком большого числа разных папок данных пользователя.  
