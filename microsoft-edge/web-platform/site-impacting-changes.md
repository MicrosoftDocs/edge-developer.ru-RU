---
description: Общие сведения об изменениях высокого влияния, которые могут повлиять на совместимость сайтов
title: 'Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, совместимость, веб-платформа
ms.openlocfilehash: 8c872546b29633cb22e0095fdd1a0326f89fc087
ms.sourcegitcommit: 5d3802721036dc7cd90e9e6f7ac90dc3acc24eec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191557"
---
# Совместимость сайта: влияние на изменения, которые поступают в Microsoft Edge  

Интернет постоянно развивается, чтобы улучшить взаимодействие с пользователями, безопасность и конфиденциальность.  В некоторых случаях изменения могут значительно повлиять на функциональность существующих страниц.  В следующей таблице перечислены особые изменения, которые в настоящее время отслеживаются группой Microsoft Edge.  Регулярно изучите эту статью; Группа Microsoft Edge обновляет следующую страницу в соответствии с обдумыванием эволюции, временные шкалы solidify и новые изменения объявляются.  

| Изменение | Канал Stable | Эксперименты | Дополнительные сведения |  
|:--- |:--- |:--- |:--- |
| Cookie-файлы по умолчанию `SameSite=Lax` и `SameSite=None-requires-Secure` | [Хром + 1](#release-comments) \ (Edge V86 \)  | Канарские V82, dev V82 | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, перейдите к [элементу состояние платформы Chrome][ChromePlatformStatus5088147346030592].  |  
| Политика для ссылки на источник: по умолчанию `strict-origin-when-cross-origin` | [Хром + 1](#release-comments) \ (Edge V86 \)  | Канарские V79, dev V79 | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, перейдите к [элементу состояние платформы Chrome][ChromePlatformStatus6251880185331712].  |  
| Запретить синхронность `XmlHttpRequest` при закрытии страницы | [Хром + 1](#release-comments) \ (Edge v83 \) |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Соответствующий хром Microsoft Edge предложит групповую политику, чтобы отключить это изменение до пограничного V88.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, перейдите к [элементу состояние платформы Chrome][ChromePlatformStatus4664843055398912].  |  
| Вывод неявных запросов на запросы разрешений на уведомления | Пограничный v84 |  | В ответ на запрос уведомлений в тихом окне отображается слабый значок запроса для разрешений на уведомления о сайтах, запрашиваемых с помощью интерфейса `Notifications` или `Push` API, заменяя полный или стандартный пользовательский интерфейс подсказки для всплывающих подсказок.  В настоящее время эта функция включена для всех пользователей.  Чтобы отказаться от запросов на уведомления в тихом режиме, перейдите на `edge://settings/content/notifications` .  В будущем группа Microsoft Edge может проанализировать повторное включение полного всплывающего уведомления в некоторых сценариях.  |  
| Отключение TLS/1.0 и TLS/1.1 по умолчанию | Пограничный v84 |  | Групповая политика [SSLMinVersion][DeployedgePoliciesSslversionmin] разрешает повторное включение TLS/1.0 и TLS/1.1; политика остается доступной до появления на краю V90.  |  
| Блокировка загрузки смешанного содержимого | [Хром + 1](#release-comments) \ (Edge V86 \)  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Чтобы получить дополнительные сведения, в том числе запланированную временную шкалу в Google для этого изменения, перейдите к [записи блога о безопасности Google][GoogleBlogSecurity20200206].  Расписание выпуска Microsoft для типов файлов, которые нужно предупреждать или блокировать, планируется для одного выхода после Chrome.  |  
| Устаревшие AppCache | [Хром + 1](#release-comments) \ (Edge V86 \)  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Дополнительные сведения можно найти в документации по [WebDev][WebDevAppCacheRemoval].  Расписание выпуска Microsoft для устаревшей планируется для одного выпуска после Chrome.  Запрос [маркера AppCache OriginTrial][ChromeDevelopersOrigintrialsAppCacheOriginTrial] позволяет сайтам продолжать использовать устаревший API, пока не появится Edge V90.  |  
| Удаление Adobe Flash | Пограничный V88  |  | Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Для получения дополнительных сведений перейдите к [плану Chromium Adobe Flash][ChromiumFlashRoadmapSupportRemoved].  | 
| Отключение и удаление FTP | Пограничный V88  | V87, пограничный бета-версия | В v87 бета-версии поддержка FTP отключена по умолчанию; в EDGE, v87 она остается включенной.  В V88 EDGE поддержка FTP полностью удалена.  Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge.  Для получения дополнительных сведений перейдите к [элементу Status платформы Chrome][ChromePlatformStatus6246151319715840].  Предприятия с сайтами, которые по-прежнему требуют поддержки FTP, могут продолжать использовать FTP, настроив сайт на использование [режима Internet Explorer][DeployedgeEdgeIeMode].  | 
| Автообновление смешанных изображений контента | Пограничный V88  |  | Небезопасные (HTTP) ссылки на изображения автоматически обновляются до HTTPS; Если изображение недоступно по протоколу HTTPS, загрузка изображения завершается сбоем. Для управления этой функцией доступна [Групповая политика][DeployedgePoliciesInsecurecontentallowedforurls] . Это изменение происходит в проекте Chromium, на котором основывается Microsoft Edge. Для получения дополнительных сведений перейдите к [элементу Status платформы Chrome][ChromePlatformStatus4926989725073408].  |  

##### Примечания о выпуске  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанные функции или изменения отставляются один выпуск после Chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome или Chrome + 1
   :::column-end:::
   :::column span="2":::
      На основе отзывов пользователей и разработчиков указанные функции или изменения поставляются одновременно или одним выпуском после Chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Сведения о режиме IE | Документы Microsoft"  
[DeployedgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls-Microsoft Edge-Policies | Документы Microsoft"  
[DeployedgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-Policies | Документы Microsoft"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Отключить синхронизацию XHR при закрытии страницы JavaScript | Состояние платформы Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Изображение для автообновления смешанного содержимого | Состояние платформы Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Файлы cookie по умолчанию SameSite = слабый | Состояние платформы Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Устаревшая поддержка FTP | Состояние платформы Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Политика "источник ссылки": по умолчанию используется строгое происхождение Состояние платформы Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Поддержка флэш-памяти, удаленная из Chromium (targets: Chrome 88 +-Янв 2021)-Flash-схема | Проекты Chromium"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial Token | Разработчики Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Защита пользователей от небезопасных Скачиваний в Google Chrome-блоге по безопасности Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Подготовка к удалению AppCache | Web. dev"  

<!--todo:  cleanup links  -->  
