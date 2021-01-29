---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Руководства по функциям браузера в Microsoft Edge.
title: Браузер — руководство для разработчиков
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2579fad881496e2197f9f696bb2c12c47c7f723e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235667"
---
# Функции браузера  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## Политики автозапуска  

 Microsoft Edge предоставляет клиентам возможность персонализировать свои предпочтения браузера на веб-сайтах, на которые автоматически передается мультимедиа со звуком, чтобы свести к минимуму отвлекающие факторы в Интернете и сэкономить пропускную способность.  Пользователи могут настраивать поведение мультимедиа с помощью глобальных и индивидуальных элементов управления автоза воспроизведением.  Кроме того, Microsoft Edge автоматически подавляет автозапок мультимедиа на фоновых вкладок.  

Подробные [сведения и](./browser-features/autoplay-policies.md) практические методики для обеспечения хорошего взаимодействия с пользователем с мультимедиа, который находится на сайте, можно найти в политиках автозахва.  

## Flash  

Если на вашей странице используется Flash, но пользователь не включил его, Microsoft Edge обычно показывает значок фрагмента задачи в адресной панели.  Если вы динамически добавляете контроль flash после загрузки страницы, значок задачи может не [](./browser-features/flash.md) отображаться. В этом случае вам нужно будет проверить, загружена ли flash, и обеспечить корректный режим отката, если он не отображается.  

## Режим чтения  

Microsoft Edge [](./browser-features/reading-view.md) предоставляет представление чтения для более упрощенного и похожего на книгу чтения веб-страниц, не отвлекая внимание от несвязанных или другого дополнительного содержимого на странице.  Ниже указаны советы по обеспечению отличного просмотра для чтения на сайте, а также инструкции по выбору сайта из представления чтения.  

## Обнаружение службы поиска  

Интеграция с богатым поиском встроена в адресную планку Microsoft Edge, включая предложения поиска, результаты из Интернета, историю браузера и избранное.  [Вот дополнительные сведения для поставщиков поиска,](./browser-features/search-provider-discovery.md) которые ищут поддержку Microsoft Edge.  