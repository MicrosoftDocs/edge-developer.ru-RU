---
description: Ссылка на протокол DevTools Версии 0.1 (EdgeHTML) для домена Страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools Версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399150"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a>Домен страницы — Протокол DevTools Версии 0.1 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.  

| Категория | Участники |  
|:--- |:--- |  
| [**Методы**](#methods) | [включить,](#enable) [отключить,](#disable) [перейти](#navigate) |  
| [**Типы**](#types) | [FrameId](#frameid) |  

## <a name="methods"></a>Методы  

### <a name="enable"></a>"Включить"  

Включает уведомления домена страницы.  

&nbsp;  

---  

### <a name="disable"></a>"Отключить"   

Отключение уведомлений домена страницы.  

&nbsp;  

---  

### <a name="navigate"></a>переход  

Перемещает текущую страницу на данный URL-адрес.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| url | `string` | URL-адрес для навигации по странице. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | **Экспериментальные**.  Frame ID, который будет перемещаться. |  

---  

## <a name="types"></a>Типы  

### <a name="frameid-string"></a>Строка FrameId  

<a name="frameid"></a>  

Уникальный идентификатор кадра.  

&nbsp;  

---  
