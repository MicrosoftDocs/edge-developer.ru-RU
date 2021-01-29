---
description: Переопределения — это функция в средстве Sources Microsoft Edge DevTools, которая позволяет копировать ресурсы веб-страницы на жесткий диск.  При обновлении веб-страницы DevTools не загружает ресурс, а заменяет его локальной копией.
title: Переопределять ресурсы веб-страницы с локальными копиями с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230966"
---
# Переопределять ресурсы веб-страницы с локальными копиями с помощью Microsoft Edge DevTools  

Иногда требуется устранить проблему на веб-странице, к которую у вас нет доступа или исправления, которая связана с медленным и сложным процессом сборки.  Вы можете отладить и устранить все виды проблем в DevTools. Но проблема заключается в том, что изменения не сохраняются.  После обновления файла все ваши трудоемкие работы не будут работать.  

Эта проблема решается [][DevToolsSourcesTool] с помощью функции "Переопределения" в средстве "Источники".  

Теперь можно взять ресурс текущей веб-страницы и сохранить его локально.  При обновлении веб-страницы браузер не загружает ресурс с сервера.  Вместо этого браузер заменяет его локальной копией ресурса.  

## Настройка локальной папки для хранения переопределения  

1.  В **средстве "Источники"** найдите несколько разделов слева.  Если параметр **"Переопределения"** не отображается, выберите параметр <code>&#x0226B;</code><!--`≫`--> значок для получения.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Средство источников с недостаточно местом для показа параметра переопределения" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Средство** источников с недостаточно местом для показа параметра переопределения  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Выбор параметра переопределения" lightbox="../media/javascript-overrides-menu.msft.png":::
             Выбор параметра переопределения  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  После выбора параметра **"Переопределения"** необходимо выбрать папку на локальном компьютере для хранения файлов ресурсов, которые необходимо заменить.  Выберите **папку +Select для переопределения** для поиска папки.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Выбор папки для переопределения" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Выбор папки для переопределения  
    :::image-end:::  
    
1.  DevTools предупреждает о том, что необходимо иметь полный доступ к папке и не раскрывать конфиденциальную информацию.  На панели предупреждений выберите **"Разрешить** предоставление доступа".  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="предоставление DevTools доступа к папке" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Предоставление DevTools доступа к папке  
    :::image-end:::  
    
1.  В области **"Переопределения"** рядом с папкой "Переопределения" должен отобразиться этот `Enable Local Overrides` почтовый ящик.  Рядом с ней отображается значок, позволяющий удалить локальные параметры переопределения.  Теперь вы закончили настройку папки и готовы заменить живые ресурсы локальными.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Успешная настройка папки переопределения" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Успешная настройка папки переопределения  
    :::image-end:::  
    
## Добавление файлов в папку Overrides  
  
Чтобы добавить файлы в папку overrides, откройте средство **"Элементы"** и проверьте веб-страницу.  Чтобы изменить, выберите имя CSS-файла в **инспекторе стилей.**  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Выбор файла в инспекторе стилей" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Выбор файла в инспекторе **стилей**  
:::image-end:::  

В **редакторе источников** наведите курсор на имя выбранного файла, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить для **переопределеев".**  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="В редакторе источников добавьте имя файла для переопределения" lightbox="../media/javascript-overrides-file-name.msft.png":::
   В **редакторе источников** добавьте имя файла для переопределения  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="В контекстное меню выберите Сохранить для переопределеения" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   В контекстное меню выберите **"Сохранить для переопределеения"**  
:::image-end:::  

Файл хранится в папке overrides.  Убедитесь, что DevTools создает папку с именем, используя URL-адрес файла с правильной структурой каталогов.  Файл хранится внутри.  Имя файла в редакторе теперь также показывает сиреневую точку, которая указывает, что файл является локальным, а не live.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Файл успешно сохранен в папке переопределения" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Файл успешно сохранен в папке переопределения  
:::image-end:::  

:::row:::
   :::column span="":::
      В следующем примере можно изменить стили веб-страницы.  Чтобы добавить красная граница вокруг файла, в редакторе стилей скопируйте следующий стиль и добавьте его в элемент body. ****  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      Файл автоматически сохранен на компьютере.  Если обновить файл, отобразится граница, и ни одна из ваших работ не будет потеряна.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Постоянное изменение стилей веб-страниц путем редактирования файла в папке overrides" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Постоянное изменение стилей веб-страниц путем редактирования файла в папке overrides  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      В **средстве "Источники"** в разделе "Страница" наведите курсор на любой файл, откройте контекстное меню \(щелкните правой кнопкой мыши\) и добавьте его в переопределения. ****  Опять же, файлы, которые уже находятся в папке переопределения, имеют сиреневую точку на значке.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Выбор файла в средстве Источники для переопределения" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Выбор файла в средстве **"Источники"** для переопределения  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Кроме того, в средстве **"Сеть"** наведите курсор на любой файл, откройте контекстное меню \(щелкните правой кнопкой мыши\) и добавьте его в переопределения.  Если переопределения имеются, файлы, расположенные на компьютере, а не с веб-страницы.  Когда переопределения вступили в силу, в средстве **"Сеть"** найдите значок предупреждения рядом с именем файла.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Выбор файла в средстве Сеть для переопределения" lightbox="../media/javascript-overrides-network.msft.png":::
         Выбор файла в средстве **"Сеть"** для переопределения  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Двухнабное взаимодействие переопределеев  

Используйте редактор, предоставленный с помощью средства **"Источники"** DevTools или любого редактора, который вы хотите изменить.  Изменения синхронизируются во всех продуктах, которые имеют доступ к файлам в папке overrides.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Обзор средства "Источники" | Документы Майкрософт"  
