---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Узнайте, как упаковить расширение Microsoft Edge в оснастку с помощью ManifoldJS, Node.js с открытым исходным кодом.
title: Использование ManifoldJS для расширений пакетов
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 151a8b2ababb25e0964a6fbc2696b5fdc059d084
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235697"
---
# Использование ManifoldJS для создания пакетов AppX расширения  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS — это средство с открытым исходным кодом Node.js, которое позволяет быстро и безболезненно создать пакет, который затем можно использовать для отправки в Microsoft Store.  

Если в расширении используется собственный обмен сообщениями, следует пропустить указанную ниже статью и перейти к инструктативу упаковки сообщений [Native в Microsoft Edge.](../native-messaging.md#creating-an-extension-with-native-messaging)  

Перед началом работы вам по-прежнему потребуется ознакомиться со следующими статьями.  

*   [Расширения в Центре разработки для Windows](./extensions-in-the-windows-dev-center.md)  
*   [Локализация пакетов расширений](./localizing-extension-packages.md)  

> [!NOTE]
> Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.  После создания, упаковки и тестирования расширения отправьте запрос на форму отправки [расширения.](https://developer.microsoft.com/microsoft-edge/extensions/requests)  

## Установка Node.js и ManifoldJS  

В первую очередь необходимо установитьNode.js [LTS.](https://nodejs.org/en/download)  
После запуска Node в командной строке (предпочтительно в PowerShell) запустите следующую команду, чтобы установить ManifoldJS.  

```shell
npm install -g manifoldjs
```  

Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки. Если manifoldJS не распознан, добавьте `%APPDATA%\npm` в переменные PATH.  

## Упаковка с помощью ManifoldJS  

Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначения для упакованного расширения.  

Например:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> Команда `manifoldjs` выводит данные в текущем каталоге и переописает содержимое.  

Теперь, когда вы находитесь в папке назначения, запустите следующую команду.  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

Команду `mainifoldjs` можно разбить на следующие части.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Изменяет уровень журнала для `debug` получения полной распечатки.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Задает единственную платформу, на которой будет запускаться `edgeextension` преобразование.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Сообщает программе, что формат манифеста является форматом и не нужно действовать, если он не `edgeextension` удается получить проверку.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      Путь к манифесту расширения, который необходимо преобразовать.  
   :::column-end:::
:::row-end:::  

После завершения работы ManifoldJS у вас будет папка со следующим содержимым.  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...
-->  

Файл generationInfo.jsэто журнал, который был выпущен с помощью ManifoldJS и не будет включен в пакет расширения. Будет упаковано только `manifest` содержимое папки. В папке манифеста папка Assets содержит изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке Extension есть содержимое расширения.  

Теперь, когда у вас есть правильные файлы, необходимо изменить созданный файл AppXManifest в `manifest` папке. Если имя файла manifest.jsрасширение содержит международное строку для поля "name", то после запуска ManifoldJS имя папки верхнего уровня не будет иметь подчеркивания и будет включать "MSG".

Например, manifest.jsфайл со следующим `"name"` полем.  

```shell
"name" : "__MSG_appName__"
```  

будет иметь папку манифеста, в которую она будет `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` вложена.  

В файле AppXManifest необходимо:  

 *   Замените необходимые поля Identity и PublisherDisplayName, как [описано здесь.](./creating-and-testing-extension-packages.md#app-identity-template-values) Обратите внимание, что если упаковка предназначена только для тестирования или корпоративного распространения, можно использовать значения-заметивы вместо регистрации для учетной записи Центра разработчиков для Windows.  
 *   Замените значки-замещания в папке Assets значками для расширения одинаковыми размерами (150x150, 50x50, 44x44) и именами. Сведения о [том,](./../design.md#icons-for-packaging) где используются эти значки, см. в руководстве по проектированию.  
 *   Если расширение локализовано, следуйте всему руководству [по локализации расширений Microsoft Edge.](./localizing-extension-packages.md) Если она не локализована, ознакомьтесь только с именем и описанием [локализации в разделе Microsoft Store.](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store)  

После `appxmanifest.xml` сортировки файла запустите следующую команду, чтобы создать пакет.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

Теперь пакет будет находится в папке **пакета,** расположенной в папке edgeextension. Дополнительные сведения о загрузке неогрузки нового пакета см. в разделе [тестирования](./creating-and-testing-extension-packages.md#testing-an-appx-package) пакета создания и тестирования расширений.  

После тестирования пакета вы можете отправить запрос на [](https://aka.ms/extension-request) форму отправки расширения, чтобы его можно было отправить на публикацию в Microsoft Store.  
