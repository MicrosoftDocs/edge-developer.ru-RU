---
description: Ссылка на протокол DevTools Версии 0.2 (EdgeHTML) для домена Схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — версия протокола DevTools 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398149"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a>Домен схемы — версия протокола DevTools 0.2 (EdgeHTML)  

Предоставляет сведения о схеме протокола.  

| Категория | Участники |  
|:--- |:--- |  
| [Методы](#methods) | [getDomains](#getdomains) |  
| [Типы](#types) | [Объект Domain](#domain) |  

## <a name="methods"></a>Методы  

### <a name="getdomains"></a>getDomains  

Возвращает поддерживаемые домены.  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| домены | [Домен[]](#domain) | Список поддерживаемых доменов. |  

---  

## <a name="types"></a>Типы  

### <a name="domain-object"></a>Объект Domain  

<a name="domain"></a>  

Описание домена протокола.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| name | `string` | Доменное имя. |  
| version | `string` | Версия домена. |  

---  
