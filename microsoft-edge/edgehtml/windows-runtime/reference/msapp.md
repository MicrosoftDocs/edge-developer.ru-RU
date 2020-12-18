---
title: Справочник по API MSApp
description: Предоставляет дополнительные функции, позволяющие создавать объекты BLOB и MSStream.  Объекты и члены MSApp поддерживаются в приложениях для Windows с помощью JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, отправка файлов, блог, MSStream, приложения для Windows 10, uwp, edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a3ad670f61bfafa4480c538dd8f28c7013b7d7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235422"
---
# MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Объект MSApp и его члены поддерживаются только для приложений для Windows с помощью JavaScript \(включая PWAs, которые имеют доступ к функциям API Windows\).  Объект MSApp существует только в локальном контексте HTML-документа в приложении для Windows, загружаемом с помощью схемы URI ms-appx; в противном случае объект не существует (и, следовательно, ни один из его методов и свойств не доступен).  

Он предоставляет дополнительные функции, позволяющие создавать [объекты BLOB](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Методы](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Константы](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [current](#current), [high](#high), [idle](#idle), [normal](#normal).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Интерфейс MSAppAsyncOperation](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## Методы MSApp  

### clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Очищает кэш и данные indexedDB для приложения или [WebView.](../../hosting/webview/index.md)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Этот метод не имеет параметров.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Тип: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Представляет асинхронное действие.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Создает большой объект [из](https://developer.mozilla.org/docs/Web/API/Blob) объекта [IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Этот метод следует использовать при работе с объектами в приложениях, чтобы создать объект на основе `IRandomAccessStream` W3C из потока.  После создания BLOB-файл можно использовать с [FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API URL](https://developer.mozilla.org/docs/Web/API/URL)и [XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `type` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Строка | Тип контента данных.  Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.  |  
      
      `stream` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) для хранения в BLOB-хранилище.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | BLOB | Новый объект BLOB, содержащий поток.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      | Исключение | Ошибка |  
      |:---- |:--- |  
      | TypeMismatchError | Тип узла несовместим с ожидаемым типом параметра.  Для версий, более ранних Internet Explorer 10, TYPE_MISMATCH_ERR возвращается.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Создает большой объект на основе типов времени запуска Windows через пространство имен MSApp в объекте window.  Этот метод создает большой объект, который, по сути, является оболочкой света для предоставленного ему объекта [RandomAccessStream.](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference)  Этот BLOB-бизнес владеет жизненным сроком существования этого потока, и поток будет закрыт при его уничтожении.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackage  

:::row:::
   :::column span="":::
      Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, к который можно получить общий доступ.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `object` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Этот диапазон можно создать либо из объекта выделения, например: `window.selection.getRangeAt(0)` или вручную.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит разметку HTML для указанного диапазона.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод поддерживает только [диапазон doM,](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)  Возвращенный пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.  
      
      Для возвращенного пакета данных недоступны свойства.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Преобразует выбор пользователя или приложения в фрагмент HTML, к который можно получить общий доступ.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Этот метод не имеет параметров.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит разметку HTML для указанного диапазона.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Возвращенный пакет данных для выбора содержит HTML-разметку в формате буфера обмена.  Если в пользовательском интерфейсе приложения нет выбора пользователя, `createDataPackageFromSelection` `null` возвращается.  
      
      Для возвращенного пакета данных недоступны свойства.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### createFileFromStorageFile  

:::row:::
   :::column span="":::
      Преобразует [Файл Хранилища WinRT](/uwp/api/) [в](/uwp/api/windows.storage.storagefile) стандартный объект W3C [File.](https://developer.mozilla.org/docs/Web/API/File)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `storageFile` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит файл хранилища.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      | Исключение | Ошибка |  
      |:---- |:--- |  
      | TypeMismatchError | Указанная ссылка на файл W3C недействительна.  Для версий, более ранних Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createStreamFromInputStream  

:::row:::
   :::column span="":::
      Создает [MSStream](https://msdn.microsoft.com/library/hh772328) из [InputStream.](https://msdn.microsoft.com/library/hh772327)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `type` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Тип контента данных.  Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.  \([См. типы MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` `text/html` например, `image/jpeg` и `image/png` так `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` далее\).  
      
      `inputStream` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | [IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) который будет храниться в `MSStream` .  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод принимает тип контента и `IInputStream` ссылку.  Затем метод проверяет, является ли переданная ссылка потока экземпляром типа, и если `IInputStream` нет, выдает `DOMException TYPE_MISMATCH_ERR` .  Если ошибка не возникает, `createStreamFromInputStream` `MSStream` создается \(из его входных данных\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      An `IInputStream` can be used to create an `MSStream` .  Как и объекты, которые используются один раз, все созданные URL-адреса отзываются при первом их использовании `MSStreams` `URL.createObjectURL` элементом изображения.  Кроме того, запросы второго URL-адреса для этого объекта после использования потока будут неудались.  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAsyncAtPriority  

:::row:::
   :::column span="":::
      Запланировать выполнение вызова позже в соответствии с заданным приоритетом.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `asynchronousCallback` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Функция | Функция callback для асинхронного запуска, которая отправляется с заданным приоритетом.  |  
      
      `priority` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Значение контекстного приоритета, при котором будет запускаться асинхронный вызовCallback.  См. ["Константы MSApp"](#msapp-constants).  |  
      
      `args` [in]
      
      | Тип | Описание |  
      |:---- |:--- |   
      | Любой | Необязательный ряд аргументов, которые передаются в функцию вызова synchronousCallback \(в качестве параметров 1 и так далее\).  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Этот метод не возвращает значение.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Предоставленная `asynchronousCallback` функция вызова выполняется асинхронно позже.  `asynchronousCallback` будет отправлено в соответствии с предоставленным приоритетом.  Обычный приоритет эквивалентен существующему [методу setImmediate.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)  При выполнении этого вызова текущий контекстный приоритет устанавливается в качестве заданного значения параметра приоритета на время выполнения этого вызова.  
      
      Параметром `asynchronousCallback` callback может быть любая функция.  Если аргументы предоставляются после параметра, они все будут переданы функции `priority` вызова.  
      
      В отличие от этого, любой объект, возвращенный функцией обратного вызова, игнорируется и не возвращается `execAtPriority` `asynchronousCallback` через `execAsyncAtPriority` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAtPriority  

:::row:::
   :::column span="":::
      Запускает указанную функцию вызова с заданным контекстным приоритетом.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `synchronousCallback` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Функция | Функция вызова для синхронного запуска с заданным контекстным приоритетом приоритета.  |  
      
      `priority` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Указанное значение приоритета, для которого будет задано текущее значение контекстного приоритета при запуске функции `synchronousCallback` callback.  См. ["Константы MSApp"](#msapp-constants).  |  
      
      `args` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Необязательный ряд аргументов, которые передаются функции вызова `synchronousCallback` \(в качестве параметров 1 и так далее\).  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Возвращает возвращаемое значение обратного `synchronousCallback` вызова \(в соответствии с применимым\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Предоставленный `synchronousCallback` метод вызова выполняется синхронно.  Текущий контекстный приоритет меняется на предоставленное значение приоритета (заданное аргументом приоритета) на время действия предоставленной функции вызова.  После завершения выполнения функции обратного вызова приоритет возвращается предыдущему значению перед `execAtPriority` вызовом.  Возвращаемого значения является возвращаемого значения метода обратного `execAtPriority` вызова \(как предоставлено\).  
      
      Параметром `synchronousCallback` callback может быть любая функция.  Если какие-либо аргументы предоставляются после параметра приоритета, они будут переданы предоставленного метода вызова.  Если параметр обратного вызова возвращает значение, это значение также становится `execAtPriority` возвращаемой.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      var user = Windows.System.UserProfile.UserInformation;
      
      MSApp.execAtPriority(function () { // This callback executes synchronously.
        user.getFirstNameAsync().then(function () { // Dispatches at high priority.
          return user.getLastNameAsync();
        }).done(function () { // Dispatches at high priority.
          // USEFUL CODE HERE
        });
      }, MSApp.HIGH); // The second argument of the execAtPriority method.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getCurrentPriority  

:::row:::
   :::column span="":::
      Возвращает текущий контекстный приоритет.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Возвращаемого значения является одной из строк `MSApp.HIGH` `MSApp.NORMAL` , или `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод возвращает текущий контекстный приоритет \(см. [msApp Constants](#msapp-constants)\), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getHtmlPrintDocumentSource  

Неподготовленный синхронный API.  Для Windows 10 `getHtmlPrintDocumentSourceAsync` см. .  For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Возвращает исходный контент, который необходимо распечатать.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `htmlDoc` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Документ | HtmL-документ для печати.  Это может быть корневой документ, документ в iframe, фрагмент документа или документ SVG.  Следует помнить, что htmlDoc должен быть документом, а не элементом.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример 1**  
      
      ```javascript
      var printTask = event.request.createPrintTask(title, function (args) {
              var deferral = args.getDeferral();
              var getPrintDocumentSourceAsync;
              if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                  getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
              } else {
                  getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
              }
              getPrintDocumentSourceAsync.then(function (source) {
                  args.setSource(source);
                  deferral.complete();
              }, function (error) {
                  console.error(error);
                  deferral.complete();
              });
      });
      ```  
   :::column-end:::
   :::column span="":::
      **Пример 2**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
      }
      
      // Variable to hold the document source to print
      var gHtmlPrintDocumentSource = null;
      
      // Print event handler for printing via the PrintManager API.
      function onPrintTaskRequested(printEvent) {
          var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
              args.setSource(gHtmlPrintDocumentSource);
      
              // Register the handler for print task completion event
              printTask.oncompleted = onPrintTaskCompleted;
          });
      }
      
      // Print Task event handler is invoked when the print job is completed.
      function onPrintTaskCompleted(printTaskCompletionEvent) {
          // Notify the user about the failure
          if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
              console.log("Failed to print.", "sample", "error");
          }
      }
      
      // Executed just before printing.
      var beforePrint = function () {
          // Replace with code to be executed just before printing the current document:
      };
      
      // Executed immediately after printing.
      var afterPrint = function () {
          // Replace with code to be executed immediately after printing the current document:
      };
      
      function printButtonHandler() {
          // Optionally, functions to be executed immediately before and after printing can be configured as following:
          window.document.body.onbeforeprint = beforePrint;
          window.document.body.onafterprint = afterPrint;
          
          // Get document source to print
          MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
              gHtmlPrintDocumentSource = htmlPrintDocumentSource;
      
              // If the print contract is registered, the print experience is invoked.
              Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
          });
      }
      ```  
   :::column-end:::
:::row-end:::  

### getViewId  

:::row:::
   :::column span="":::
      Поддержка нескольких окон.  
      
      > [!NOTE] 
      > В приложениях UWP на JavaScript для Win8.1 поддерживалась поддержка нескольких окон с помощью API-API MSApp DOM, которые теперь не поддерживаются.  Для Windows 10 используйте `window.open` , `window` и новый `MSApp.getViewId` .  
      
      | Описание |Windows 10; | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Создание нового окна | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Новый объект window | [окно](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `window`
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Объект, представляющий окно, содержащее документ DOM.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      `viewId`
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Число | Можно использовать с различными [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Используйте [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) и [window](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но затем для взаимодействия с API WinRT добавьте `MSApp.getViewId` API.  Он принимает объект в качестве параметра и возвращает число, которое можно использовать с различными `window` `viewId` API [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Задержка видимости  
          
          Представления в WinRT обычно начинаются скрытыми, и конечный разработчик использует что-то вроде отображения представления `TryShowAsStandaloneAsync` после его полной подготовки.  В веб-мире сразу же отображает окно, и конечный пользователь может наблюдать за загрузкой и отрисовке `window.open` содержимого.  Чтобы ваши новые окна отображались как представления в WinRT и не отображались сразу, мы добавили `window.open` параметр.  Например:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Отличия основного окна  
          
          Основное окно, которое изначально открывается операционной операцией, действует иначе, чем открывалось дополнительное окно:  
          
          | Описание | Основной | Дополнительная |  
          |:---- |:--- |:--- |  
          | window.open | Разрешено | Disallowed |  
          | window.close | Закрыть приложение | Закрыть окно |  
          | Ограничения навигации | Только ACUR | Без ограничений |  
          
          Ограничение на запрет открытия дополнительных окон может измениться в зависимости от [отзывов.](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)  
      
      *   Ограничения связи с одинаковым происхождением  
          
          Существует сложная техническая проблема, препятствуя правильной поддержке синхронных вызовов скриптов с одинаковым и одинаковым началом.  Когда вы открываете окно того же источника, сценарий в одном окне может напрямую вызывать функции в другом окне, и некоторые из этих вызовов не будут выполняться.  `postMessage` вызовы работают нормально, и это рекомендуемый способ, если это возможно.  Работа по улучшению этой проблемы продолжается.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Возвращает boolean значение, указывающее, есть ли ожидающих работ на заданном уровне приоритета или выше.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `priority` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Значение приоритета \(см. [MSApp Constants](#msapp-constants)\), указывающее уровень приоритета и выше для запроса любых непогашенных работ в очереди.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Возвращает, есть ли в очереди какие-либо трудоемкие задачи на указанном уровне приоритета или выше, в противном `true` `false` случае.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод предоставляет коду JavaScript средства для определения того, есть ли ожидающих работ на различных уровнях приоритета \(или выше\) с целью того, чтобы вызывательный код JavaScript затем решил дать работу с более высоким `isTaskScheduledAtPriorityOrHigher` приоритетом.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      function performIdleWork(array_in) {
          var idx = 0;
          
          function performIdleWorkHelper() {
              for (; idx < array_in.length; ++idx) {
                  
                  // USEFUL CODE HERE 
                  
                  if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
                      MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
                      break;
                  } // if
              } // for
          } // performIdleWorkHelper
          
          performIdleWorkHelper();
      } // performIdleWork
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Используется для предотвращения обновления пути начала (перезагрузки страницы) перед каждым событием активации (например, щелчок уведомления или закрепленная плитка\).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Используйте, чтобы всегда пропустить обновление пути начала (перезагрузка страницы) и перейти непосредственно к `MSApp.pageHandlesAllApplicationActivations(true)` запуску `WebUIApplication` активированного события.  Требует, чтобы все страницы обрабатывали события активации отдельно.  При определении этого метода как щелкнув активированное событие `true` \(например, уведомление\) не активирует перезагрузку, что является важным условием для одно страниц приложений, желающих избежать перезагрузок страниц.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      // Without this, the app will first refresh to the start path before every activate event
      window.MSApp.pageHandlesAllApplicationActivations(true); 
      
      // This must not be deffered so that it can receive the initial `activated` event in time
      window.Windows.UI.WebUI.WebUIApplication.addEventListener(
          `activated`,
          e =>
              microsoftInterface.handleActivatedEvent(e);
          }),
          false
      );
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Управляет тем, подавляет ли приложение возможные запросы проверки подлинности во время скачивания ресурсов.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
     
      `suppress` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Значение true подавляет потенциальные запросы проверки подлинности.  Значение false не подавляет потенциальные запросы проверки подлинности от пользователя.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод управляет тем, подавляет ли приложение потенциальные запросы проверки подлинности `suppressSubdownloadCredentialPrompts` во время скачивания ресурсов.  По умолчанию запросы учетных данных не подавляются.  
      
      `suppressSubdownloadCredentialPrompts` предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, которым требуется проверка подлинности, например почтовое приложение \(которое может содержать информационный бюллетень, содержащий несколько изображений, где каждое изображение требует проверки подлинности\).  
      
      При подавлении подсказок учетных данных диалоги для проверки подлинности на серверах не будут показаны при доступе к ресурсам, которые требуют проверки подлинности, и ресурс не будет загружен.  Обратите внимание, что это не влияет на другие возможные запросы, такие как проверка подлинности прокси-сервера или диалоговое окно запроса на сертификацию клиента, и не влияет на `suppressSubdownloadCredentialPrompts` XHR.  
      
      Следует помнить, `suppressSubdownloadCredentialPrompts` что влияет на все содержимое в приложении, включая контент, который был в `webview` элементе.  
      
      > [!IMPORTANT]
      > Решения о запросах учетных данных кэшются.  Таким образом, если запросы учетных данных не будут отбираться, запросы учетных данных после их подавления вступает в силу, поэтому может потребоваться перезагрузка документа.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### terminateApp  


:::row:::
   :::column span="":::
      Завершает текущее приложение и создает отчет о сбое.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `error` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Ошибка | Объект, `Error` который можно использовать для описания ошибки, которая вызвала завершение.  Объект должен содержать число, описание и свойства стека; отчет о сбое не будет создан, если объект не содержит `Error` эти свойства.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Если проблема, о чем сообщили, становится одной из 5 главных проблем вашего приложения, она будет отдана на странице `terminateApp` "Качество" приложения.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      В этом `terminateApp` примере при вызове исключения вызывается.  Он использует `Error` объект, предоставленный при перехимовыыве исключение.  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### Константы MSApp  

:::row:::
   :::column span="":::
      Допустимые значения приоритета, связанные с `execAsyncAtPriority` `execAtPriority` , , и `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### Текущие  
      
      `current`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом \(См. также раздел\), метод будет использовать текущий контекстный приоритет при `current` выполнении запрашиваемой операции.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Высока  
      
      `high`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом \(См. также раздел\), метод будет использовать более высокий приоритет, чем обычный при выполнении запрашиваемой операции, и будет отправлять операцию перед любой существующей обычной работой `high` приоритета.  |  
   :::column-end:::
   :::column span="":::
      #### Состояние Idle (в покое)  
      
      `idle`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом \(См. также раздел\), метод будет использовать более низкий приоритет, чем обычный при выполнении запрашиваемой операции, и будет отправлять операцию после любой существующей обычной работы с `ideal` приоритетом.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Обычный  
      
      `normal`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом (см. также раздел), метод будет использовать обычный существующий приоритет при `normal` выполнении запрашиваемой операции.  |  
   :::column-end:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Требования**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### start  

:::row:::
   :::column span="":::
      Запускает `MSAppAsyncOperation` .  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Свойства**  
      
      `error` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMError | Представляет ошибку в `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для настройки обработера событий по завершении `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для настройки обработера событий при ошибке во время `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Число | Представляет состояние асинхронной операции в приложении для Windows с помощью JavaScript.  Значения: `Started[0]` , `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой |Представляет результат `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
