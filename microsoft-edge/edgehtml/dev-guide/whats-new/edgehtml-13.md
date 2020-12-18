---
description: На этой странице представлен обзор новых функций EdgeHTML 13.
title: Новые функции и API в EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235784"
---
# Новые возможности EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот изменения, внесенные с помощью EdgeHTML 13, яма, который работает с браузером Microsoft Edge в первом крупном обновлении для Windows 10 \(11/2015, сборка 10586\). [](https://blogs.windows.com/windowsexperience/2015/11/12)  Обзор изменений в общем браузере Microsoft Edge см. в обзоре [EdgeHTML 13,](https://blogs.windows.com/msedgedev/2015/11/16)нашего первого обновления платформы для Microsoft Edge.  

Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .  

## Возможности  

### CSS  

EdgeHTML 13 поддерживает новые функции CSS, в том числе:  

*   [Псевдо-классы мутируемости CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [Псевдо-классы диапазона CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   Исходные [и](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) [неустановленные](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) ключевые слова CSS  

### Зашифрованные расширения мультимедиа  

Microsoft Edge теперь поддерживает новые незашифрованные API зашифрованных [расширений](https://w3.org/TR/encrypted-media) мультимедиа.  Зашифрованные расширения мультимедиа \(EME\) расширяют видео- и звуковые элементы, чтобы включить защищенный контент управления цифровыми правами (DRM\) без использования подключаемых модульов.  Дополнительные данные о EME: [зашифрованные расширения мультимедиа.](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API)  

### Графика  

EdgeHTML 13 представляет следующие графические обновления:  

*   [Многолинейная многояпка холста](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Режимы на blending холста](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> element](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [Внешнее содержимое SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

EdgeHTML 13 включает основные улучшения и поддержку новых функций в [Chakra](https://blogs.windows.com/msedgedev/2015/09/30), обработчик JavaScript, включающий Microsoft Edge, в том числе:  

#### Новые возможности  

Включено по умолчанию  

*   [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) по умолчанию \([запись блога](https://blogs.windows.com/msedgedev/2015/11/10), [демонстрация](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)  
*   [Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)  

#### Экспериментальные функции JavaScript  

Включено с `about:flags`  

*   [А async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)  
*   [Оператор Exponentiation](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)  
*   [Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)  

### Ввод данных пользователем  

Следующие функции, введенные в EdgeHTML 13, улучшают ввод данных пользователями:  

*   [\<meter\> element](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [обработник событий oninvalid для документа и окна элемента](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Блокировка указателя  

Microsoft Edge теперь поддерживает API блокировки указателя \(ранее называлась "Блокировка мыши"), чтобы получать доступ к необработанных перемещениям мыши, блокировать цель событий мыши в одном элементе, устраняя ограничения перемещения мыши в одном направлении и удаляя курсор из представления.  

## Новые API в EdgeHTML 13  

Ниже полный список новых API в EdgeHTML 13.  Они перечислены в формате `[interface name].[api name]` .  

<iframe height='584' scrolling='no' title='Новые API в EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>См. API-код для новых перьев <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> в EdgeHTML 13 в </a> Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> @MicrosoftEdgeDocumentation) на <a href='http://codepen.io'> </a> CodePen.</iframe>  
