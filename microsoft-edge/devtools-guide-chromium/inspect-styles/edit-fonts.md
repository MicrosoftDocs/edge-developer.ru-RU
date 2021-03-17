---
description: Узнайте, как изменить стили и параметры шрифтов CSS с помощью области стилей в Microsoft Edge DevTools.
title: Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439495"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a>Изменение стилей и параметров шрифтов CSS в области Стилей  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

Типография в Интернете является важной частью пользовательского интерфейса.  Необходимо убедиться, что вы соответствуете корпоративным рекомендациям по бренду, а содержимое отображается как ожидалось на различных устройствах.  Текст должен быть простым для чтения с помощью размера и высоты строки.  Пользователи могут повторно размеры шрифтов для удовлетворения индивидуальных потребностей.  В ситуациях, когда конкретные шрифты недоступны на устройстве пользователя, необходимо предоставить параметры откатных шрифтов.  

CSS обеспечивает лучшую поддержку типографии в последние годы.  Для определения размера текста доступны десятки различных подразделений CSS.  Кроме того, у вас есть несколько свойств CSS, которые влияют на размер шрифта, интервалы, высоту строки и другие типографические функции.  

Чтобы упростить работу с типографией, визуальный **** редактор шрифтов теперь находится в области **Стилей.**  Вы можете изменить параметры шрифта, и изменения будут немедленно отрисовки в браузере.  Все без глубоких знаний о CSS.  

В настоящее время эта функция является экспериментальной, и ее необходимо **Enable new font editor tool within the Styles pane** включить для Microsoft Edge Developer [Tools.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Любой CSS в области **Стилей,** определения шрифтов или стили в линию, автоматически отображает значок, открываю визуальный **редактор шрифта.**  Чтобы открыть визуальный **редактор шрифта,** выберите **значок Редактор шрифта.**  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Значок в области Стилей для редактирования параметров шрифта" lightbox="../media/font-editor-icon.msft.png":::
         Значок в области **Стилей** для редактирования параметров шрифта  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей" lightbox="../media/font-editor-open.msft.png":::
         Редактор **шрифта,** открытый поверх области **Стилей**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Все поля в редакторе **визуальных шрифтов** заполняются из значений в CSS в области **Стилей.**  Например, определение установлено в области Стилей, поэтому текстовое поле высоты строки отображает и отобразит отсев `line-height` `160%` **** `160` `%` единицы.  Кроме того, ползунок автоматически устанавливается в соответствие со значениями текстового поля.  

Редактор **шрифта** состоит из двух частей: селектора семейства шрифтов и редактора свойств CSS.  

## <a name="the-font-family-selector"></a>Селектор семейства шрифтов  

Селектор семейства шрифтов — верхняя часть визуального **редактора шрифтов.**  Чтобы выбрать шрифты правила CSS, в редакторе CSS используйте селектор **семейства** шрифтов.  Для каждого правила CSS можно выбрать основные и откатные шрифты.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенным селектором семейства шрифтов" lightbox="../media/font-editor-font-family.msft.png":::
   Редактор **шрифта,** открытый поверх области **Стилей** с выделенным селектором **семейства** шрифтов  
:::image-end:::  

Используйте **отсев семейства** шрифтов, чтобы выбрать из списка шрифтов.  Шрифты организованы в четыре группы.  

1.  Вычислительные шрифты, которые являются шрифтами, доступными в таблице стилей в области **Стилей.**  
1.  Системные шрифты, которые являются шрифтами, доступными в текущей операционной системе.  
1.  Общие семейства шрифтов, например `serif` или `sans-serif` .  
1.  Глобальные значения, такие как `inherit` `initial` , и `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенным селектором семейства шрифтов" lightbox="../media/font-editor-font-family-list.msft.png":::
   Редактор **шрифта,** открытый поверх области **Стилей** с выделенным селектором **семейства** шрифтов  
:::image-end:::  

После выбора шрифта отображается еще одно выпадение меню для выбора откатных шрифтов.  Вы можете выбрать до восьми откатных шрифтов.  Чтобы удалить шрифт, выберите **значок Delete Font Family.**  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Если вы выбираете глобальное значение для семейства шрифтов, вы не получите еще одного отката, так как в CSS нет отката для него.  

## <a name="the-css-properties-editor"></a>Редактор CSS Properties  

Свойства шрифта CSS можно изменить в нижней части визуального **редактора шрифтов.**  Можно изменить размер шрифта, высоту строки, вес шрифта и интервал между буквами с помощью любого из элементов управления пользовательским интерфейсом.  Изменения применяются немедленно в браузере.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Редактор шрифта, открытый поверх области Стилей с выделенными свойствами CSS" lightbox="../media/font-editor-css-properties.msft.png":::
   Редактор **шрифта,** открытый поверх области **Стилей** с выделенными свойствами CSS  
:::image-end:::  

Кроме того, можно преобразовать подразделения CSS с помощью визуального **редактора шрифтов.**  Например, вы можете использовать средство в правиле CSS, в котором изначально установлен ползунок **размер** шрифта `16 pixels` .  Теперь используйте выпадаемую единицу и выберите значение `em` .  `1 em`Отображаемая равна `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Изменение размера шрифта до 16 пикселей" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Изменение размера шрифта на `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Откройте выпадаемую единицу для преобразования в em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Откройте выпадаемую единицу для преобразования в `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

В отсеве единицы доступны все доступные числимые единицы CSS.  Размер шрифта, высота строки, вес шрифта и интервалы использования различных единиц.  Если в текстовых полях фокусируется, можно выбрать клавиши и клавиши для настройки `arrow up` `arrow down` параметров.  Чтобы использовать ползунки с клавиатурой, выберите `arrow left` клавиши и `arrow down` клавиши.  

Редактор CSS Properties также содержит заранее.  Чтобы использовать заранее задатки ключевых слов, справа выберите `Toggle Input Type` значок.  Отображаются изменения пользовательского интерфейса и отсев предустановленных ключевых слов.  Чтобы вернуться к пользовательскому интерфейсу с помощью ползунок и других элементов управления пользовательским интерфейсом, выберите `Toggle Input Type` значок снова.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Откройте предустановленный интерфейс ключевого слова" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Откройте предустановленный интерфейс ключевого слова  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
