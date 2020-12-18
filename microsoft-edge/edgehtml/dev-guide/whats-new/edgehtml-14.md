---
description: На этой странице представлен обзор новых функций EdgeHTML 14.
title: Новые функции и API в EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c99dcb4efb253959d55d96a13ca2249eb5164b68
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235473"
---
# Новые возможности EdgeHTML 14  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот изменения, внесенные в EdgeHTML 14 с момента юбилейного обновления [Windows 10](https://blogs.windows.com/windowsexperience/2016/06/29) \(08/2016, сборка 14393\).  Общие сведения об изменениях браузера Microsoft Edge см. в обзоре [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04)с юбилейным обновлением Windows 10.  

Ниже приводится permalink для следующего списка изменений: [https://aka.ms/devguide_edgehtml_14](./edgehtml-14.md) .  

## Новые возможности  

### Расширения  

Расширения — это небольшие программы, которые можно использовать для добавления новых функций в Microsoft Edge или изменения существующих функций.  Расширения предназначены для улучшения ежедневного просмотра пользователем за счет предоставления функций ниш, которые важны для целевой аудитории.  Microsoft Edge поддерживает новую модель расширения на основе HTML, JavaScript и CSS.  Эта новая модель совместима с Chrome, что означает, что существующие разработчики расширений Chrome смогут перенести свои расширения в Microsoft Edge с минимальными изменениями.  Дополнительные сведения можно получить в документы разработчика расширений [Microsoft Edge.](../../extensions/index.md)  

### Fetch API  
API [fetch](https://fetch.spec.whatwg.org#fetch-api) использует метод `fetch` для извлечения ресурсов.  В прошлом это было достигнуто с `XMLHttpRequest` помощью .  Это не только простой в использовании способ получения, но и более низкий уровень доступа к запросам и ответам.  Узнайте больше об API fetch в записи блога Microsoft Edge, Fetch (или ограничения [XHR).](https://blogs.windows.com/msedgedev/2016/05/24)  

### JavaScript  

EdgeHTML 14 обеспечивает ряд новых и экспериментальных функций в Chakra, ядра JavaScript на платформе Microsoft Edge:  

#### Новые возможности  

Включено по умолчанию  

*   [Параметры по умолчанию](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) \(ES2015\)
*   [Оператор Exponentiation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) \(ES2016\)
*   [Array.prototype.includes](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) \(ES2016\)
*   [Object.values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) and [object.entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) \(ES2017\)  

#### Экспериментальные функции JavaScript  

Включено с `about:flags`  

*   [Modules](https://blogs.windows.com/msedgedev/2016/05/17) \(ES2015\)  
*   [Async/await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) \(ES2017\)  
*   [Символы Regex](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) \(ES2015\)  

Дополнительные сведения можно найти в предварительных версиях модулей ES6 и т. д. в [ES2015, ES2016](https://blogs.windows.com/msedgedev/2016/05/17) и более новых версиях, а асинхронный код упрощается с поддержкой асинхронной функции [ES2016 в Chakra](https://blogs.windows.com/msedgedev/2015/09/30)и Microsoft Edge.  

### API веб-проверки подлинности  

Веб-API FIDO 2.0  

API веб-проверки подлинности \(ранее FIDO 2.0\) в Microsoft Edge позволяет веб-приложениям использовать биометрические данные [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) для проверки подлинности пользователей, чтобы вы и ваши пользователи могли избежать всех трудностей и рисков управления паролями, включая угадать пароль, фишинг и атаки с использованием ключей.  Текущая реализация Microsoft Edge \( с префиксом\) основана на более ранней черновике спецификации веб-проверки подлинности и, скорее всего, изменится `ms-` в будущем.  Узнайте больше о веб-проверке подлинности: [веб-проверка подлинности и Windows Hello.](../windows-integration/web-authentication.md)

### Веб-уведомления
Веб-уведомления позволяют сайтам отображать уведомления для оповещения пользователей вне контекста веб-страницы и браузера, информируя пользователей о новых сообщениях или оповещениях и позволяя сайтам повысить вовлеченность пользователей.  Веб-уведомления в Microsoft Edge полностью интегрированы с платформой уведомлений и центром уведомлений в Windows 10, обеспечивая единообразие работы с другими приложениями в системе, а также простые средства управления разрешениями и тихий часы.  Дополнительные [сведения можно узнать в веб-уведомлениях в Microsoft Edge.](https://blogs.windows.com/msedgedev/2016/05/16)  

### API веб-речи
[API веб-речи](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) — это API JavaScript, который состоит из двух частей: распознавания речи и синтеза речи \(или текста в речь\).  В настоящее время Microsoft Edge поддерживает только синтез речи.  Синтез речи включает преобразование текста в речь, которое пользователь слышит через своих динамиков.  Дополнительные сведения можно узнать в статье "Web [Speech: Speech Synthesis](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) Developer Guide" (Веб-речь: руководство разработчика по синтезу речи).  

## Новые API в EdgeHTML 14

Ниже полный список новых API в EdgeHTML 14.  Они перечислены в формате `[interface name].[api name]` .  

<iframe height='585' scrolling='no' title='Новые API в EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. API-код для новых перьев в <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> EdgeHTML 14 от </a> MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>  
