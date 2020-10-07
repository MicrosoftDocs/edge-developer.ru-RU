---
description: Provides a summary of high-impact changes that may impact site compatibility
title: Site compatibility-impacting changes coming to Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/02/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform
ms.openlocfilehash: 49fbedb2fe979a52b771539c7ceedce8968c2fb4
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100290"
---
# Site compatibility-impacting changes coming to Microsoft Edge  

The web is constantly evolving to improve the user experience, security, and privacy.  In some cases, changes may be significant enough to impact the functionality of existing pages.  The following table summarizes particularly high-impact changes that the Microsoft Edge team is currently tracking.  Review this article often; the Microsoft Edge team updates the following page as thinking evolves, timelines solidify, and new changes are announced.  

| Change | Stable Channel | Experimentation | Additional information |  
|:--- |:--- |:--- |:--- |
| Cookies default to `SameSite=Lax` and `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus5088147346030592].  |  
| Referrer Policy: Default to `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus6251880185331712].  |  
| Disallow synchronous `XmlHttpRequest` in page dismissal | [Chrome+1](#release-comments) \(Edge v83\) |  | This change is happening in the Chromium project, on which Microsoft Edge is based.  Matching Chrome, Microsoft Edge offers a Group Policy to turn off this change until Edge v88.  For more information, including the planned timeline by Google for this change, navigate to the [Chrome Platform Status entry][ChromePlatformStatus4664843055398912].  |  
| Display subtle prompt for notification permissions requests | Edge v84 |  | Quiet notification requests display a subtle request icon in the address bar for site notification permissions requested using the `Notifications` or `Push` API, replacing the full or standard permission flyout prompt UI.  This feature is currently enabled for all users.  To opt out of quiet notification requests, navigate to `edge://settings/content/notifications`.  In the future, the Microsoft Edge team may explore re-enabling the full flyout notification prompt in some scenarios.  |  
| Turn off TLS/1.0 and TLS/1.1 by default | Edge v84 |  | The [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] Group Policy permits re-enabling of TLS/1.0 and TLS/1.1; the policy remains available until Edge v90.  |  
| Block mixed content downloads | [Chrome+1](#release-comments) \(Edge v86\)  |  | This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, including the planned timeline by Google for this change, navigate to the [Google security blog entry][GoogleBlogSecurity20200206].  The Microsoft rollout schedule on file types to warn or block is planned for one release after Chrome.  |  
| Deprecate AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, navigate to the [WebDev documentation][WebDevAppCacheRemoval].  The Microsoft rollout schedule for deprecation is planned for one release after Chrome.  Requesting an [AppCache OriginTrial Token][AppCacheOriginTrial] allows sites to continue to use the deprecated API until Edge v90.  |  
| Removal of Adobe Flash | Edge v88  |  | This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, navigate to the [Adobe Flash Chromium Roadmap][ChromiumFlashRoadmapSupportRemoved].  | 
| Turn off and remove FTP | Edge v88  | Edge v87 | In Edge v87, FTP support is turned off by default.  In Edge v88, FTP support is removed.  This change is happening in the Chromium project, on which Microsoft Edge is based.  For more information, navigate to the [Chrome Platform Status Entry][ChromePlatformStatus6246151319715840].  |   

##### Release comments  

:::row:::
   :::column span="1":::
      Chrome+1
   :::column-end:::
   :::column span="2":::
      Based on user and developer feedback, the indicated feature or change ships one release after Chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome or Chrome+1
   :::column-end:::
   :::column span="2":::
      Based on user and developer feedback, the indicated feature or change ships at the same time or one release after Chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Policies | Microsoft Docs"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Disallow sync XHR in page dismissal JavaScript | Chrome Platform Status"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies default to SameSite=Lax | Chrome Platform Status"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Referrer Policy: Default to strict-origin-when-cross-origin | Chrome Platform Status"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Deprecate FTP support | Chrome Platform Status"

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Flash Support Removed from Chromium (Target: Chrome 88+ - Jan 2021) - Flash Roadmap | Chromium Projects"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protecting users from insecure downloads in Google Chrome - Google Online Security Blog" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "AppCache Removal"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial token"
