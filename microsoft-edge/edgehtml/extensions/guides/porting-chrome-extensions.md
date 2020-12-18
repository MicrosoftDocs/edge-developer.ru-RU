---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Узнайте, как перенос расширения Chrome в Microsoft Edge с помощью расширения Microsoft Edge набор средств.
title: Перенос расширений Chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f226d79dbc9efdc43eb68bfb353fa12748198371
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235692"
---
# Перенос расширения из Chrome в Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Перенос расширения из Chrome в Microsoft Edge проще с помощью microsoft [Edge Extension набор средств.](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb) Это средство разработчика преобразует распакованное расширение Chrome в распакованное расширение Microsoft Edge, переверив API-интерфейсы и выявив все ошибки в `manifest.json` файле.


### Мосты API
Чтобы обеспечить беспрепятственное перенос API Chrome в поддерживаемые API Microsoft Edge, в папку расширения добавляются два сценария. Эти сценарии мост API (polyfiling при необходимости), что означает, что вам не придется беспокоиться об изменении какого-либо кода Chrome в фоновых сценариях или сценариях содержимого.

После преобразования они будут включены в файл манифеста расширения с `"-ms-preload"` ключом:

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Использование расширения Microsoft Edge набор средств

Следующие инструкции подробно о том, как преобразовать расширение Chrome для запуска в Microsoft Edge в выпуске Юбилейного обновления Windows 10:

1. Установите microsoft [Edge Extension набор средств](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Сделайте копию папки расширения Chrome для безопасного сохраняемого. Процесс преобразования переопишет код. 
3. Запустите microsoft Edge Extension набор средств и загрузите копию расширения.  
 ![кнопка расширения загрузки](./../media/save-folder.png)
4. Исправлять все ошибки, которые сообщаются в текстовом редакторе средства. Выберите "Повторно проверить", чтобы проверить ошибки после внося исправлений.  
 ![extension-toolkit finding errors](./../media/extension-toolkit.png)
5. Выберите "Сохранить файлы".

Теперь вы можете выйти из наборов инструментов и загрузить расширение в Microsoft Edge! 

Вы можете искать известные проблемы платформы с помощью отслеживания проблем [EdgeHTML.](http://issues.microsoftedge.com) Если вы считаете, что нашли что-то новое, [откройте проблему!](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)
