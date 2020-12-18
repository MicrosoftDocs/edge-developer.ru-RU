---
description: Протокол Microsoft Edge DevTools версии 0.1 поддерживает следующие клиенты инструментов.
title: Клиенты протокола DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb7355524ec6dab5cf0275538c5b0c030891d4a9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235203"
---
# Клиенты протокола DevTools версии 0.1 (EdgeHTML)  

> [!NOTE]
> Протокол Microsoft Edge DevTools работает только в сборках Windows 10 с обновлением за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)

**Протокол DevTools 0.1** поддерживает следующие клиенты инструментов.

[ ![ Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Microsoft Visual Studio 15.7 Preview 2](../media/visual-studio-2017.png)](#microsoft-visual-studio-preview)

## Предварительный просмотр средств разработчика в Microsoft Edge

Вы можете использовать приложение [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) для Windows 10 из Microsoft Store для удаленной отладки хост-устройства под управлением Microsoft Edge[(EdgeHTML 17](../../dev-guide/index.md) или более поздней версии).

Этот предварительный выпуск протокола DevTools версии 0.1 предоставляет основные функции отладки, такие как установка точек останова, пошаговое изучение кода и изучение трассировок стека. В пользовательском интерфейсе Edge DevTools это преобразуется [****](../../devtools-guide/debugger.md) в функциональные возможности, доступные на панели отладки, за вычетом проверки кэша (для веб-хранилища, рабочих служб, API кэша и IndexedDB). В настоящее время удаленная отладка Microsoft Edge ограничена настольными компьютерами, и поддержка других устройств с Windows 10 будет поддерживаться в будущих выпусках.

Вот как настроить удаленную отладку с помощью приложения Microsoft Edge DevTools Preview. Протокол DevTools находится в предварительной версии и требует обновления Windows 10 за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. или более поздней сборки Windows Insider Preview на хост-компьютере (отладке). Приложение Edge DevTools Preview (используемая на компьютере отладчика) будет работать в fall Creators Update (версия 1709) и сборках Windows Insider Preview.

**На хост-компьютере (отладке) ...**

1. Если вы в сети Wi-Fi, убедитесь, что сеть помечена как **"Домен"** или **"Частная".** Это можно проверить, открыв приложение Защитник Windows Security [**Center,**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) **** щелкнув брандмауэр & защиты сети и ** проверив, указана ли ваша сеть как сеть домена или частная *сеть.* 

    Если она указана *как*"Общедоступный", перейдите в & **** сети Wi-Fi в Интернете, щелкните сеть и перейдите к кнопке "Сетевой профиль" в  >  ****  >  **** **"Частное".** **

2. Откройте панель **управления "Для разработчиков"** в ** *параметрах* Windows (найдите разработчика и щелкните *"Использовать функции разработчика")* и: 

    а. Перегуют в **режиме разработчика.** При этом будет *устанавливаться* пакет режима разработчика, включающий удаленные инструменты для настольных компьютеров.

    б. [**Включите**](/windows/uwp/debug-test-perf/device-portal) портал устройств**(включите удаленную диагностику по подключениям к локальной сети) и обнаружение устройств **(** сделайте устройство видимым для USB-подключений и*локальной сети).*

    в. **Включит проверку подлинности** и включит имя пользователя или пароль.

    г. Обратите внимание на IP-адрес компьютера и порт подключения (50443).

3. Откройте в Microsoft Edge вкладки, которые нужно отлалать с клиентского компьютера.

**На компьютере клиента (отладчике) ...**

1.  Установите и запустите приложение [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) из Microsoft Store.

2. Откройте **удаленную панель** и введите сетевое расположение (URL-адрес и порт) хост-компьютера и нажмите кнопку **"Подключиться".**

3. **Установите** сертификат хост-компьютера из диалогового окно "Неверная сертификация". **

4. Укавите имя пользователя или пароль, назначенные для проверки подлинности портала устройств.

5. *Удаленная* панель загрузит список целевых объектов страницы для отладки на хост-компьютере. Выберите один из них, чтобы начать отладку.

6. Используйте **кнопку** "Обновить", чтобы обновить и перезагрузить список целевых объектов удаленных страниц на хост-компьютере. Нажмите **кнопку** "Отключить", чтобы вернуться к экрану подключения к удаленному устройству и подключиться к другому хосту. **

## Microsoft Visual Studio Preview

С помощью последней сборки [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (Visual Studio 15.7 Preview 1 или более поздней версии) можно запустить и отлалать Microsoft Edge из IDE в любом проекте ASP.NET или .NET Core. Протокол DevTools в настоящее время находится в предварительной версии и требует запуска сборки [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)

Вот как настроить отладку Microsoft Edge с помощью Visual Studio:

1.  Установите и запустите последнюю [**сборку Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (Visual Studio 15.7 Preview 1 или более поздней версии).

2. Откройте существующий проект ASP.NET или .NET Core или создайте **новый проект...** с помощью одного из шаблонов **Visual C#** .NET.

3. В **обозревателе**решений проекта откройте файлы JavaScript, которые нужно отлалать, и установите точки останова в IDE так же, как с серверным кодом.

4. Нажмите, `F5` чтобы запустить Microsoft Edge, на сервере DevTools Server. При наступии точки останова вы разберется в Visual Studio сможете дополнительно проверить код и пошаговую проверку кода.
