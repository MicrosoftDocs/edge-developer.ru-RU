---
description: Список ссылок на поддерживаемые домены в Microsoft Edge DevTools Protocol версии 0.2.
title: Домены протокола DevTools — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 03688ff2a1757205cc1c83d23a13d205e38011c7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235564"
---
# Домены протокола DevTools — протокол DevTools версии 0.2 (EdgeHTML)  

## [CSS](css.md)  

Этот домен предоставляет операции чтения и записи CSS. Все объекты CSS (таблицы стилей, правила и стили) связаны с последующими операциями с `id` этим объектом. Каждый тип объекта имеет определенную структуру, и они не являются взаимозаменяемыми `id` между объектами разных типов. Объекты CSS можно загружать с помощью вызовов (которые принимают ид `get*ForNode()` узла DOM). Клиент также может отслеживать таблицы стилей с помощью событий, а затем загружать необходимое содержимое таблиц стилей `styleSheetAdded` / `styleSheetRemoved` с помощью `getStyleSheet[Text]()` методов.
## [DOM](dom.md)
Этот домен предоставляет операции чтения и записи DOM. Каждый узел DOM представлен своим зеркальным объектом с объектом `id` . Это `id` можно использовать для получения дополнительных сведений об узле, ее разрешения в оболочку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Тыловой узел отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Сбор сведений о узлах, отправленных клиенту, несет ответственность клиент.<p>Обратите `iframe` внимание, что элементы-владельцы возвращают соответствующие элементы документа в качестве их узлы.</p>
## [DOMDebugger](domdebugger.md)
Отладка DOM позволяет устанавливать точки останова для определенных операций и событий DOM. Выполнение JavaScript остановится для этих операций, как если бы был установлен обычный набор точек останова.
## [Отладчик](debugger.md)
Домен отлада предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.
## [Наложение](overlay.md)
Домен наложения предоставляет визуальные эффекты и взаимодействие при выборе узла
## [Page](page.md)
Действия и события, связанные с проверенной страницей, относятся к домену страницы.
## [Время выполнения](runtime.md)
Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не отпущены явным образом.
## [Схема](schema.md)
Предоставляет сведения о схеме протокола.
