---
description: Содержит сводку о существенных изменениях, которые могут повлиять на совместимость сайтов
title: 'Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, совместимость, веб-платформа
ms.openlocfilehash: 64cdb417e6bd0aa648c7e1225bb6dc522f3873ce
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327507"
---
# Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge  

Интернет постоянно развивается, чтобы улучшить взаимодействие с пользователями, безопасность и конфиденциальность.  В некоторых случаях изменения могут быть достаточно значительными, чтобы повлиять на функциональность существующих страниц.  В следующей таблице водятся особенно опасные изменения, которые команда Microsoft Edge отслеживает в настоящее время.  Часто просматривая эту статью; Команда Microsoft Edge обновляет следующую страницу по мере развития мышлении, укрепляются временные шкалы и объявляются новые изменения.  

| Изменение | Канал Stable | Эксперименты | Дополнительные сведения |  
|:--- |:--- |:--- |:--- |
| Файлы cookie по умолчанию `SameSite=Lax` и `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Для получения дополнительных сведений, включая запланированную временную шкалу Google для этого изменения, перейдите к записи "Состояние платформы [Chrome".][ChromePlatformStatus5088147346030592]  |  
| Политика ссылок: значение по умолчанию `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Для получения дополнительных сведений, включая запланированную временную шкалу Google для этого изменения, перейдите к записи "Состояние платформы [Chrome".][ChromePlatformStatus6251880185331712]  |  
| Не синхронное `XmlHttpRequest` отклонение страницы | [Chrome+1](#release-comments) \(Edge v83\) |  | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  В Microsoft Edge, совпадающих с Chrome, предлагается групповая политика, которая отключит это изменение до Edge 88.  Для получения дополнительных сведений, включая запланированную временную шкалу Google для этого изменения, перейдите к записи "Состояние платформы [Chrome".][ChromePlatformStatus4664843055398912]  |  
| Отображение неявных запросов на уведомления о разрешениях | Edge v84 |  | В запросах на уведомления без уведомлений в адресной панели отображается тонкий значок запроса на разрешения уведомлений сайта, запрашиваемого с помощью API или API, заменяющий полный или стандартный пользовательский интерфейс запроса на `Notifications` `Push` разрешение.  В настоящее время эта функция включена для всех пользователей.  Чтобы отказаться от запросов на уведомления без уведомлений, перейдите к `edge://settings/content/notifications` .  В будущем команда Microsoft Edge может изучить возможность повторного включения полноразвивного уведомления в некоторых сценариях.  |  
| Отключение TLS/1.0 и TLS/1.1 по умолчанию | Edge v84 |  | Групповая политика [SSLMinVersion][DeployedgeMicrosoftEdgePoliciesSslversionmin] разрешает повторное включение TLS/1.0 и TLS/1.1; политика остается доступной до edge v90.  |  
| Блокировка скачивания смешанного содержимого | [Chrome+1](#release-comments) \(Edge v86\)  |  | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Дополнительные сведения, включая запланированную временную шкалу Google для этого изменения, перейдите к записи блога [о безопасности Google.][GoogleBlogSecurity20200206]  Расписание выпуска майкрософт для типов файлов, которые необходимо предупредить или заблокировать, планируется для одного выпуска после Chrome.  |  
| Амортизации AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Дополнительные сведения можно найти в [документации WebDev.][WebDevAppCacheRemoval]  Расписание выпуска Корпорации Майкрософт для амортизации планируется на один выпуск после Chrome.  Запрос [маркера AppCache OriginTrial][ChromeDevelopersOrigintrialsAppCacheOriginTrial] позволяет сайтам продолжать использовать неподготовленный API до Edge v90.  |  
| Удаление Adobe Flash | Edge v88  |  | Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Для получения дополнительных сведений перейдите к [плану Adobe Flash Chromium.][ChromiumFlashRoadmapSupportRemoved]  | 
| Отключение и удаление FTP | Edge v88  | Edge Beta v87 | В бета-версии 87 edge поддержка FTP по умолчанию отключена; В Edge Stable v87 он остается включенным.  В Edge v88 поддержка FTP полностью удалена.  Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge.  Дополнительные сведения можно найти в записи состояния [платформы Chrome.][ChromePlatformStatus6246151319715840]  Предприятия с сайтами, которые по-прежнему требуют поддержки FTP, могут продолжать использовать FTP, настроив сайт для использования [режима IE.][DeployedgeEdgeIeMode]  | 
| Автоматическое разбивание изображений смешанного содержимого | Edge v88  |  | Небезопасные ссылки на изображения (HTTP\) автоматически обновляются до HTTPS; Если изображение не доступно по протоколу HTTPS, скачивание изображения не удастся. Для [управления этой][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] функцией доступна групповая политика. Это изменение происходит в проекте Chromium, на котором основан Microsoft Edge. Дополнительные сведения можно найти в [записи "Состояние платформы Chrome".][ChromePlatformStatus4926989725073408]  | 
| Http authentication disallowed when third-party cookies are blocked  | Edge v87  |  | Начиная с Edge v87, когда файлы cookie блокированы для сторонних запросов с помощью политики [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] или через страницу параметров edge, http-проверка подлинности также блокируется. Это изменение может повлиять на загрузку списка сайтов в режиме предприятия для [режима Internet Explorer,][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] если для конечной точки, в которая размещен список, требуется проверка подлинности HTTP.  Чтобы разрешить использование файлов cookie и проверки подлинности HTTP для загрузки списка сайтов в режиме предприятия, добавьте шаблон совпадающих URL-адресов в политику [CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |   

##### Комментарии о выпуске  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанная функция или изменение предлагает один выпуск после Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome или Chrome+1  
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанная функция или изменение предлагается одновременно или один выпуск после Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "О режиме IE | Документы Майкрософт"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Настройка с помощью политики списка веб-сайтов IE в режиме предприятия — настройка политик режима IE | Документы Майкрософт"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies — Microsoft Edge — политики | Документы Майкрософт"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls — Microsoft Edge — политики | Документы Майкрософт"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls — Microsoft Edge — политики | Документы Майкрософт"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin — Microsoft Edge — политики | Документы Майкрософт"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Disallow sync XHR in page dismissal JavaScript | Состояние платформы Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Состояние платформы Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Файлы cookie по умолчанию— SameSite=Lax | Состояние платформы Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Неподдержка поддержки FTP | Состояние платформы Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Политика ссылок: по умолчанию для стандарта strict-origin-when-cross-origin | Состояние платформы Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Поддержка flash удалена из Chromium (цель: Chrome 88+ — январь 2021 г.) — план flash | Проекты Chromium"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial token | Разработчики Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Защита пользователей от небезопасных загрузок в Google Chrome — блог Google Online Security" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Подготовка к удалению AppCache | web.dev"  

<!--todo:  cleanup links  -->  
