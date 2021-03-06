---
description: Ссылка На протокол DevTools Версии 0.2 (EdgeHTML) для домена Страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools Версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398849"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a>Домен страницы — протокол DevTools Версии 0.2 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.  

| Категория | Участники |  
|:--- |:--- |  
| [Методы](#methods) | [включить,](#enable) [отключить,](#disable) [перейти,](#navigate) [getFrameTree](#getframetree) |  
| [Мероприятия](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |  
| [Типы](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |  

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
| frameId \(необязательный\) | [FrameId](#frameid) | Frame id для навигации.  Если не указано, будет перемещаться на верхней странице. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Frame id, который будет перемещаться. |  

---  

### <a name="getframetree"></a>getFrameTree  

Возвращает представленную структуру дерева кадра.  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| frameTree | [FrameTree](#frametree) | Представленная структура дерева кадра. |  

---  

## <a name="events"></a>Мероприятия  

### <a name="frameattached"></a>frameAttached  

Уволено, когда кадр был присоединен к родительскому.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | Id прикрепленного кадра. |  
| parentFrameId | [FrameId](#frameid) | Идентификатор родительского кадра. |  
| stack \(необязательный\) | [Runtime.StackTrace](./runtime.md#stacktrace) | Трассировка стека JavaScript при присоединении кадра устанавливается только в том случае, если кадр инициировался из сценария. |  

---  

### <a name="framedetached"></a>frameDetached  

В случае, если кадр отсоединяется от родительского.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID отсоединяемого кадра. |  

---  

### <a name="framenavigated"></a>frameNavigated  

Уволен после завершения навигации по кадру.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| кадр | [Кадр](#frame) | Объект Frame. |  

---  

### <a name="loadeventfired"></a>loadEventFired  

Соответствует `window.onload` событию.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| timestamp | `number` | Количество миллисекунд с эпохи. |  

---  

### <a name="domcontenteventfired"></a>domContentEventFired  

Соответствует `document.onDOMContentLoaded` событию.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| timestamp | `number` | Количество миллисекунд с эпохи. |  

---  

## <a name="types"></a>Типы  

### <a name="frameid-string"></a>Строка FrameId  

<a name="frameid"></a>  

Уникальный идентификатор кадра.  

&nbsp;  

---  

### <a name="frame-object"></a>Объект Frame  

<a name="frame"></a>  

Сведения о кадре на странице.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| id | [FrameId](#frameid) | Уникальный идентификатор frame. |  
| parentId \(необязательный\) | [FrameId](#frameid) | Уникальный идентификатор родительской рамки. |  
| имя \(необязательный\) | `string` | Имя фрейма, указанное в теге. |  
| url | `string` | URL-адрес документа кадра. |  
| securityOrigin | `string` | Происхождение безопасности кадрового документа. |  
| mimeType | `string` | MimeType кадра документа, определяемого браузером. |  

---  

### <a name="frametree-object"></a>Объект FrameTree  

<a name="frametree"></a>  

Сведения об иерархии Frame.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| кадр | [Кадр](#frame) | Сведения о кадре для этого элемента дерева. |  
| childFrames \(необязательный\) | [FrameTree[]](#frametree) | Кадры для детей. |  

---  
