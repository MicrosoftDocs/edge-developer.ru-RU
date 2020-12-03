---
description: Процесс переноса расширения Chrome на Microsoft Edge.
title: Расширение Chrome для порта в Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195161"
---
# Перенос расширения  

Microsoft EDGE позволяет переносить расширение Chrome с минимальными изменениями.  API расширения и ключи манифестов, поддерживаемые хромом, совместимы с кодом Microsoft Edge.  Список API-интерфейсов, поддерживаемых Microsoft EDGE, можно найти в разделе [Поддержка API][ExtensionApiSupport].  

Чтобы перенести расширение Chrome, выполните указанные ниже действия.  

1.  Изучите API расширения Chrome, используемые в расширениях, с помощью списка [поддерживаемых интерфейсов API][ExtensionApiSupport] расширений Microsoft Edge.  
    
    > [!NOTE]
    > Если расширение использует API, которые не поддерживаются Microsoft EDGE, он может не переноситься напрямую.  
    
1.  Если имя `Chrome` используется либо в имени, либо в описании расширения, измените расширение `Microsoft Edge` .  Этот этап необходим для передачи процесса сертификации.  
1.  Протестируйте расширение, чтобы убедиться в том, что он работает в Microsoft EDGE, с помощью [неопубликованных приложений][ExtensionsGettingStartedExtensionSideloading].  
1.  Если вы сталкиваетесь с проблемами, вы можете выполнить отладку расширений в Microsoft Edge с помощью DevTools или [обратиться к нам][mailtoExtensionMicrosoft].  
1.  Следуйте [рекомендациям по публикации][ExtensionsPublishPublishExtension] , чтобы опубликовать расширение в магазине надстроек Microsoft Edge.  
    
    > [!NOTE]
    > Если расширение обменивается сообщениями с собственным приложением с помощью `chrome.runtime.connectNative` API, убедитесь в том, что вы установили `allowed_origins` для `extension://[Microsoft-Catalog-extensionID]` собственного файла манифеста узла сообщений.  Это позволяет приложению идентифицировать расширение.  
    
## Дальнейшие действия  

После того как пакет расширения будет готов к публикации в магазине надстроек Microsoft EDGE, [Создайте учетную запись разработчика][ExtensionsPublishCreateDevAccount] и [опубликуйте расширение][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Поддержка API | Документы Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Неопубликованного расширение | Документы Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Регистрация для разработчиков | Документы Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Опубликовать расширение | Документы Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовые платежи | Разработчик Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
