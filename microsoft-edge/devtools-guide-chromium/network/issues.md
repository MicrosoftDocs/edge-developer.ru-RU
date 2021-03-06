---
description: Узнайте, как обнаруживать сетевые проблемы в сетевой панели Microsoft Edge DevTools.
title: Справочные материалы по неполадкам в сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 12cc447fa9d8ef8624e8528430eabc25ab523dd0
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398275"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="network-issues-guide"></a>Справочные материалы по неполадкам в сети  

В этом руководстве показано, как выявлять сетевые проблемы или возможности оптимизации в сетевой панели Microsoft Edge DevTools.  

Чтобы узнать основы сетевого средства, перейдите к [сайту Get Started][NetworkPerformance]. ****  

## <a name="queued-or-stalled-requests"></a>Очередные или отостановимые запросы  

**Симптомы**  

Одновременно загружаются шесть запросов.  После этого ряд запросов выстроились в очередь или застопорились.  После завершения одного из первых шести запросов начинается один из запросов в очереди.  

В **водопаде** на следующем рисунке одновременно начинаются первые шесть запросов `edge-iconx1024.msft.png` на актив.  Последующие запросы отостановятся до завершения одного из шести исходных запросов.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Пример очереди или срыва ряда в панели Network" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Пример очереди или срыва ряда в **средстве Network**  
:::image-end:::  

**Причины**  

Слишком много запросов делается в одном домене.  В подключениях HTTP/1.0 или HTTP/1.1 Microsoft Edge разрешает не более шести одновременных подключений TCP на один хост.  

**Исправление**  

*   Реализуем осколок домена, если необходимо использовать HTTP/1.0 или HTTP/1.1.  
*   Используйте HTTP/2.  Не используйте осколок домена с помощью HTTP/2.  
*   Удалите или отойте ненужные запросы, чтобы критические запросы загружались ранее.  
    
## <a name="slow-time-to-first-byte-ttfb"></a>Медленное время для первого byte (TTFB)  

**Симптомы**  

Запрос тратит много времени на ожидание получения первого byte с сервера.  

На следующем рисунке длинная зеленая **** планка водопада указывает на то, что запрос долго ждали.  Это было смоделированно с помощью профиля, чтобы ограничить скорость сети и добавить задержку.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Пример запроса с медленным временем до первого byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Пример запроса с медленным временем до первого byte  
:::image-end:::  

**Причины**  

*   Подключение между клиентом и сервером медленно.  
*   Сервер медленно реагирует.  Локализуй сервер, чтобы определить, медленно ли это подключение или сервер.  Если при доступе к локальному серверу вы все еще получаете медленное время для первого byte \(TTFB\), сервер медленно.  
    
**Исправление**  

*   Если подключение медленное, рассмотрите возможность размещения контента на CDN или изменения поставщиков хостинга.  
*   Если сервер медленный, следует оптимизировать запросы баз данных, реализовать кэш или изменить конфигурацию сервера.  
    
## <a name="slow-content-download"></a>Медленная загрузка контента  

**Симптомы**  

Загрузка запроса занимает много времени.  

На следующем рисунке длинная синяя планка в **водопаде** рядом с png означает, что загрузка заняла много времени.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Пример запроса, который занимает много времени для скачивания" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Пример запроса, который занимает много времени для скачивания  
:::image-end:::  

**Причины**  

*   Подключение между клиентом и сервером медленно.  
*   Загружается большое количество контента.  
    
**Исправление**  

*   Рассмотрите возможность размещения контента на CDN или изменения поставщиков хостинга.  
*   Отправьте меньшее количество bytes путем оптимизации запросов.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая проблема — MicrosoftDocs/edge-developer"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/issues) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Джонатан Гарби][JonathanGarbee] \(Эксперт разработчика Google для веб-технологий\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
