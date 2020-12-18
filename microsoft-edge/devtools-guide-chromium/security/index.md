---
description: С помощью панели безопасности убедитесь, что страница полностью защищена протоколом HTTPS.
title: Проблемы безопасности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5bef22eae8deacc81e31cf6d1c7791e016541346
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230616"
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

# Проблемы безопасности в Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Открытие панели безопасности  

Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.  

1.  [Откройте DevTools.][DevToolsOpen]  
1.  Откройте панель **безопасности** на вкладке **"Безопасность".**  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Панель безопасности" lightbox="../media/security-security-overview-secure.msft.png":::
       Панель **безопасности**  
    :::image-end:::  
    
## Распространенные проблемы  

### Небезопасные основные источника  

Если основной источник страницы не является безопасным, в **обзоре** безопасности говорится, что эта страница **не является безопасной.**  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Небезопасная страница" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Небезопасная страница  
:::image-end:::  

Эта проблема возникает при запросе URL-адреса по протоколу HTTP.  Для обеспечения безопасности необходимо запросить его по протоколу HTTPS.  Например, если вы посмотрите на URL-адрес в адресной панели, он, вероятно, будет выглядеть примерно `http://example.com` так.  Для обеспечения безопасности URL-адрес должен быть `https://example.com` .  

Если вы уже настроили HTTPS на сервере, все, что нужно сделать, чтобы устранить эту проблему, — настроить сервер на перенаправление всех HTTP-запросов на HTTPS.  

Если вы еще не настроили ПРОТОКОЛ HTTPS на сервере, [let's Encrypt][LetsEncrypt] предоставляет бесплатный и относительно простой способ запуска процесса.  Или вы можете рассмотреть возможность размещения сайта в сети CDN.  Большинство основных узлов CDNs по умолчанию теперь находится на https.  

> [!TIP]
> Подсказка ["Использовать HTTPS"][WebhintUseHttps] в [веб-канале][Webhint] может помочь автоматизировать процесс перенаправки всех HTTP-запросов на HTTPS.  

### Смешанное содержимое  

**Смешанное** содержимое означает, что основной источник страницы является безопасным, но страница запрашивает ресурсы из небезопасных источников.  Страницы смешанного содержимого защищены только частично, так как содержимое HTTP доступно для анализаторов и уязвимо для атак "человек в середине".  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Смешанное содержимое" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Смешанное содержимое  
:::image-end:::  

На предыдущем рисунке выберите запрос "Просмотр **1"** на панели "Сеть", чтобы открыть панель "Сеть" и применить фильтр, чтобы сетевой журнал отображал только незабезопасные **** `mixed-content:displayed` ресурсы. ****  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Смешанные ресурсы в сетевом журнале" lightbox="../media/security-network-filter.msft.png":::
   Смешанные ресурсы в **сетевом журнале**  
:::image-end:::  

## Просмотреть подробные сведения  

### Просмотр сертификата основного источника  

В **обзоре безопасности**выберите **"Просмотреть сертификат",** чтобы быстро проверить сертификат для основного источника.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Сертификат основного источника" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Сертификат основного источника  
:::image-end:::  

### Просмотр сведений об источнике  

Выберите одну из записей в левой области nav, чтобы просмотреть сведения об источнике.  На странице сведений можно просмотреть сведения о подсети и сертификате.  Сведения о прозрачности сертификата также показано, когда они доступны.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Основные сведения об источнике" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Основные сведения об источнике  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[LetsEncrypt]: https://letsencrypt.org "Шифруем — бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование HTTPS | документация по webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/security/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
