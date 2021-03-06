---
description: Ссылка на протокол DevTools Версии 0.1 (EdgeHTML) для домена Схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — Версия протокола DevTools 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398863"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a>Домен схемы — Версия протокола DevTools 0.1 (EdgeHTML)  

Предоставляет сведения о схеме протокола.  

| Категория | Участники |  
|:--- |:--- |  
| [Методы](#methods) | [getDomains](#getdomains) |  
| [Типы](#types) | [Домен](#domain) |  

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
