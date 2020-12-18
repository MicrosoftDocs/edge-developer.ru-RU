---
description: Сделайте расширение доступным для разных языков и протестировать языковые строки с помощью руководства по международной глобализации.
title: Расширения — internationalization
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbbc847ebd2103cba2eca8a791009b4e72f93a6f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235732"
---
# Интернационализация  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Чтобы ваше расширение было доступно множеству разных людей, важно иметь в виду другие страны. Расширения Microsoft Edge позволяют добавлять в расширения разные языковые строки, чтобы их язык можно было легко изменить.

Дополнительные сведения о международной глобализации расширения можно [](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)узнать в руководстве по международной глобализации MDN.


## Тестирование языков

Чтобы протестировать языковые строки, сначала необходимо установить язык отображения Windows для языка, для который нужно протестировать.

Чтобы изменить язык отображения Windows, выполните следующие действия.

1. Откройте приложение "Параметры".

   ![приложение параметров](./../media/loc-settings.png)
2. Выберите "Время & языка".
3. Выберите "Язык & региона".
4. Выберите "+ Добавить язык", чтобы добавить язык в список возможных языков.
5. Выберите язык из списка "Языки", который нужно протестировать.
6. Выберите кнопку "По умолчанию" (может потребоваться перезапустить компьютер).
7. Откройте Microsoft Edge и убедитесь, что строки, определенные для этого региональных точки, отображаются ожидаемым.

С помощью свойства [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) можно проверить правильность языка, который Microsoft Edge определил как язык отображения Windows.

Нажмите кнопку в CodePen ниже, чтобы увидеть язык отображения браузера.

<iframe height='300' scrolling='no' title='Получить региональные органы' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> локаль получения </a> пера msEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> </a> @MSEdgeDev) на <a href='http://codepen.io'> </a> CodePen.
</iframe>
