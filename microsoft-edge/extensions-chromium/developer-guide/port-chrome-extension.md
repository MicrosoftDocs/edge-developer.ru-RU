---
description: Процесс переноса расширения Chrome в Microsoft Edge.
title: Перенос расширения Chrome в Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: 64a92927b9fe7658562f87f326bb9ac148991031
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327696"
---
# Перенос расширения  

Microsoft Edge позволяет переносить расширение Chrome с минимальными изменениями.  API расширения и ключи манифеста, поддерживаемые Chrome, совместимы с Кодом и Microsoft Edge.  Список API, поддерживаемых Microsoft Edge, можно найти в [службе поддержки API.][ExtensionApiSupport]  

Чтобы выполнить перенос расширения Chrome, выполните следующие действия.  

1.  Просмотрите API расширений Chrome, используемые в ваших расширениях, в списке поддерживаемых [API][ExtensionApiSupport] расширений Microsoft Edge.  
    
    > [!NOTE]
    > Если расширение использует API, не поддерживаемые Microsoft Edge, оно может не переносим напрямую.  
    
1.  В файле манифеста установите `update_URL` для поля `https://edge.microsoft.com/extensionwebstorebase/v1/crx` ".  Значение указывает на файл расширения в магазине надстройки Microsoft Edge и позволяет Microsoft Edge проверять обновления `.crx` расширений.  
1.  Если используется в имени или описании расширения, повторно задайте для расширения `Chrome` `Microsoft Edge` название.  Чтобы пройти процесс сертификации, необходимо внести изменения.  
1.  Проверьте расширение, чтобы проверить, работает ли оно в Microsoft Edge, [выгрузив расширение нео][ExtensionsGettingStartedExtensionSideloading]том же.  
1.  Если у вас возникнут проблемы, вы можете отладить расширения в Microsoft Edge с помощью DevTools или связаться [с нами.][mailtoExtensionMicrosoft]  
1.  Следуйте [рекомендациям по публикации,][ExtensionsPublishPublishExtension] чтобы опубликовать расширение в магазине надстройки Microsoft Edge.  
    
    > [!NOTE]
    > Если расширение обменивается сообщениями с использованием вашего приложения, убедитесь, что вы установили его в файле манифеста ведущего приложения для обмена `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` сообщениями.  Этот параметр позволяет приложению идентифицировать расширение.  
    
## Дальнейшие действия  

После того как пакет расширения будет готов к публикации в магазине надстройки Microsoft [Edge,][ExtensionsPublishCreateDevAccount] создайте учетную запись разработчика и [опубликуйте расширение.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Поддержка API | Документы Майкрософт"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Загрузка нео sideload расширения | Документы Майкрософт"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Регистрация разработчиков | Документы Майкрософт"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Опубликуйте расширение | Документы Майкрософт"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовая оплата | Разработчик Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
