---
description: Хост-сайт на веб-сервере машины разработки, а затем доступ к контенту с устройства Android.
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 16c9927ce4548d71681d35e643aea0a6c44ec75a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398212"
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

# <a name="access-local-servers"></a>Доступ к локальным серверам  

Узел сайта на веб-сервере машины разработки, а затем доступ к контенту с устройства Android.  

С помощью USB-кабеля и Microsoft Edge DevTools запустите сайт из машины разработки, а затем просмотреть сайт на устройстве Android.  

### <a name="summary"></a>Сводка  

*   Переадпорт портов позволяет просматривать контент, который находится на веб-сервере, запущенном на компьютере разработки на устройстве Android.  
*   Если веб-сервер использует настраиваемый домен, установите устройство Android для доступа к контенту в этом домене с помощью настраиваемой сопоставления домена.  

## <a name="set-up-port-forwarding"></a>Настройка переадпорта портов  

Переадпорт портов позволяет устройству Android получать доступ к контенту, который находится на веб-сервере, запущенном на компьютере разработки.  Перенос портов работает путем создания порта прослушивания TCP на устройстве Android, который совпадет с портом TCP на компьютере разработки.  Трафик между портами проходит через подключение USB между устройством Android и машиной разработки, поэтому подключение не зависит от конфигурации сети.  

Чтобы включить переадпорт портов:  

1.  Настройка [удаленного отладки между][RemoteDebuggingGettingStarted] машиной разработки и устройством Android.  По завершению устройство Android должно отображаться в левом меню диалогового устройства **Inspect Devices** и **индикаторе подключенного** состояния.  
1.  В **диалоговом** окантовке Inspect Devices в DevTools включить **переадпорт порта.**  
1.  Выберите **правило Добавить**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Добавление правила переноса порта" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Добавление правила переноса порта  
    :::image-end:::  
    
1.  В **текстовом** ящике порта устройства слева введите номер порта, с которого вы хотите получить доступ к сайту `localhost` на устройстве Android.  Например, если вы хотите получить доступ к сайту из `localhost:5000` входа `5000` .  
1.  В **текстовом** ящике Локального адреса справа введите IP-адрес или имя узла, на котором ваш сайт находится на веб-сервере, запущенном в машине разработки, а затем номер порта.  Например, если сайт запущен в `localhost:7331` `localhost:7331` вводе.  
1.  Выберите **Добавить**.  
    
Теперь настроена переадпортка порта.  Просмотрите индикатор состояния для переноса вперед на вкладке на устройстве в **диалоговом** окте "Устройства проверки".  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Состояние переноса порта" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Состояние переноса порта  
:::image-end:::  

Чтобы просмотреть содержимое, откройте Microsoft Edge на устройстве Android и перейдите в порт, указанный в поле `localhost` **порта** устройства.  Например, если вы вошли `5000` в поле, посетите `localhost:5000` .  

## <a name="map-to-custom-local-domains"></a>Map to custom local domains  

Настраиваемый сопоставление домена позволяет просматривать контент на устройстве Android с веб-сервера на компьютере разработки, использующем настраиваемый домен.  

Например, предположим, что на вашем сайте используется сторонная библиотека JavaScript, которая работает только на `microsoft-edge.devtools` домене.  Таким образом, вы создаете запись в файле на компьютере разработки, чтобы составить карту этого домена `hosts` `localhost` с \(например, `127.0.0.1 microsoft-edge.devtools` \).  После настройки настраиваемого сопоставления домена и переноса порта просматривайте сайт на устройстве Android по `microsoft-edge.devtools` URL-адресу.  

### <a name="set-up-port-forwarding-to-proxy-server"></a>Настройка переноса порта на прокси-сервер  

Чтобы составить настраиваемый домен, необходимо запустить прокси-сервер на компьютере разработки.  Примерами прокси-серверов [являются Charles,][CharlesWebDebuggingProxy] [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].  

Настройка переноса порта в прокси-сервер:  

1.  Запустите прокси-сервер и зафиксировать порт, который он использует.  
    
    > [!NOTE]
    > Прокси-сервер и веб-сервер должны работать в разных портах.  
    
1.  Настройка [переноса порта на](#set-up-port-forwarding) устройство Android.  В **локальном поле адресов** введите порт, на который запущен `localhost:` прокси-сервер.  Например, если он запущен в `8000` порту, перейдите к `localhost:8000` .  В поле **порта устройства** введите номер, который необходимо прослушивать устройству Android, например `3333` .  
    
### <a name="configure-proxy-settings-on-your-device"></a>Настройка параметров прокси на устройстве  

Далее необходимо настроить устройство Android для связи с прокси-сервером.  

1.  На устройстве Android перейдите к **настройкам**  >  **Wi-Fi**.  
1.  Нажатие длинного нажатия на имя сети, к которой вы подключены в настоящее время.  
    
    > [!NOTE]
    > Параметры прокси применяются к сети.  
    
1.  Выберите **Изменить сеть**.  
1.  Выберите **расширенные параметры**.  Отображение параметров прокси.  
1.  Выберите меню **Прокси** и выберите **Руководство**.  
1.  Для поля **имя хозяина прокси** введите `localhost` .  
1.  Для поля **порта Прокси** введите номер порта, который был введен для порта устройств **в** предыдущем разделе.  
1.  Выберите **Сохранить**.  
    
С помощью этих параметров устройство передает все свои запросы прокси-серверу на компьютере разработки.  Прокси-сервер делает запросы от имени устройства, поэтому запросы на настраиваемый локальный домен будут надлежащим образом разрешены.  

Теперь доступ к пользовательским доменам на устройстве Android, как и на компьютере разработки.  

Если на веб-сервере запущен нестандартный порт, не забудьте указать порт при запросе контента с устройства Android.  Например, если веб-сервер использует настраиваемый домен в порту, при просмотре сайта с устройства Android необходимо использовать `microsoft-edge.devtools` `7331` URL-адрес. `microsoft-edge.devtools:7331`  

> [!TIP]
> Чтобы возобновить нормальный просмотр, не забудьте восстановить параметры прокси на устройстве Android после отключения от машины разработки.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер веб-отладки Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "squid : Оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler — бесплатный прокси-сервер отладки веб-сайтов"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
