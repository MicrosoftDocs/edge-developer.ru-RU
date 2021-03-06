---
description: Используйте панель безопасности, чтобы убедиться, что страница полностью защищена HTTPS.
title: Понимание проблем безопасности с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397778"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a>Понимание проблем безопасности с помощью Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a>Откройте панель безопасности  

Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.  

1.  [Откройте DevTools][DevToolsOpen].  
1.  Выберите **вкладку Безопасность,** чтобы открыть **средство безопасности.**  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Панель безопасности" lightbox="../media/security-security-overview-secure.msft.png":::
       Панель **безопасности**  
    :::image-end:::  
    
## <a name="common-problems"></a>Распространенные проблемы  

### <a name="non-secure-main-origins"></a>Небезопасные основные истоки  

Если основное происхождение страницы не защищено, в **Обзоре** безопасности говорится, что эта **страница не является безопасной.**  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Небезопасная страница" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Небезопасная страница  
:::image-end:::  

Эта проблема возникает, когда URL-адрес, который вы посетили, был запросят по HTTP.  Чтобы обеспечить безопасность, необходимо запросить его через HTTPS.  Например, если вы посмотрите на URL-адрес в панели адресов, он, вероятно, похож на `http://example.com` .  Для обеспечения безопасности URL-адрес должен быть `https://example.com` .  

Если вы уже настроили HTTPS на сервере, все, что необходимо сделать для устранения этой проблемы, это настроить сервер, чтобы перенаправить все запросы HTTP на HTTPS.  

Если вы не настроили HTTPS на сервере, [let's Encrypt][LetsEncrypt] предоставляет бесплатный и относительно простой способ запуска процесса.  Или, вы можете рассмотреть возможность размещения вашего сайта на CDN.  Большинство основных сайтов cdNs, принимающих https по умолчанию, сейчас.  

> [!TIP]
> Подсказка [Использование HTTPS][WebhintUseHttps] в [веб-хинте][Webhint] может помочь автоматизировать процесс, чтобы убедиться, что все запросы HTTP направляются в HTTPS.  

### <a name="mixed-content"></a>Смешанный контент  

**Смешанное** содержимое означает, что основное происхождение страницы является безопасным, но страница запрашивает ресурсы из небезопасных источников.  Смешанные страницы контента защищены только частично, так как содержимое HTTP доступно для нюхателей и уязвимо для атак из-за человека в центре.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Смешанный контент" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Смешанный контент  
:::image-end:::  

На предыдущем рисунке выберите запрос **View 1** **** в панели Network, чтобы открыть средство Network и применить фильтр, чтобы журнал Сети отображал только `mixed-content:displayed` небезопасные ресурсы. ****  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Смешанные ресурсы в сетевом журнале" lightbox="../media/security-network-filter.msft.png":::
   Смешанные ресурсы в **сетевом журнале**  
:::image-end:::  

## <a name="view-details"></a>Просмотреть подробные сведения  

### <a name="view-main-origin-certificate"></a>Просмотр основного сертификата происхождения  

В **обзоре безопасности**выберите **сертификат View,** чтобы быстро проверить сертификат основного происхождения.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Сертификат основного происхождения" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Сертификат основного происхождения  
:::image-end:::  

### <a name="view-origin-details"></a>Просмотр сведений о происхождении  

Выберите одну из записей в левом nav, чтобы просмотреть сведения о происхождении.  На странице подробные сведения можно просмотреть сведения о подключении и сертификате.  Сведения о прозрачности сертификата также показано при наличии.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Основные сведения о происхождении" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Основные сведения о происхождении  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[LetsEncrypt]: https://letsencrypt.org "Шифруем — бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование https | документация по веб-сайтам"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/security/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
