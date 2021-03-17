---
title: Ссылка на API MSApp
description: Предоставляет дополнительные функции, позволяющие создавать объекты Blob и MSStream.  Объекты и члены MSApp поддерживаются для приложений Windows с помощью JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, отправка файлов, блог, MSStream, windows 10 apps, uwp, edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439726"
---
# <a name="msapp"></a>MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Объект MSApp и его члены поддерживаются только для приложений Windows с помощью JavaScript \(включая pwAs, доступ к функциям API Windows\).  Объект MSApp существует только в локальном контексте HTML-документа в приложении Windows, загружаемом с помощью схемы URI ms-appx; в противном случае объект не существует (и, следовательно, ни один из его методов и свойств не доступен).  

Он предоставляет дополнительные функции, которые позволяют создавать [объекты Blob](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Методы](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage,](#createdatapackage) [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Константы](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [текущий,](#current) [высокий,](#high) [простой,](#idle) [нормальный](#normal).  
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

## <a name="msapp-methods"></a>Методы MSApp  

### <a name="cleartemporarywebdataasync"></a>clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Очищает кэш и индексацию данныхdb для приложения или [WebView.](../../hosting/webview/index.md)  
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
      **Пример**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a>createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Создает [Blob из](https://developer.mozilla.org/docs/Web/API/Blob) [объекта IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Этот метод следует использовать при работе с объектами в приложениях, чтобы создать объект на основе `IRandomAccessStream` W3C из потока.  После создания blob его можно использовать с [файлами FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API](https://developer.mozilla.org/docs/Web/API/URL)URL-адресов и [XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)  
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
      | Любой | [IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) который будет храниться в Blob.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Blob | Новый объект blob, содержащий поток.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      | Исключение | Ошибка |  
      |:---- |:--- |  
      | TypeMismatchError | Тип узла несовместим с ожидаемым типом параметра.  Для версий, ранее чем Internet Explorer 10, TYPE_MISMATCH_ERR возвращается.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Создает Blob из типов времени запуска Windows через пространство имен MSApp на объекте окна.  Этот метод создаст blob, который по сути является световой оболочкой над объектом [RandomAccessStream,](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) предоставленным ему.  BLOB владеет сроком службы этого потока, и поток будет закрыт при уничтожении blob.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
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

### <a name="createdatapackage"></a>createDataPackage  

:::row:::
   :::column span="":::
      Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, который можно совместно использовать.  
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
      | Любой | Этот диапазон можно создать либо из объекта выбора, например: `window.selection.getRangeAt(0)` или вручную.  |  
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
      
      Этот метод поддерживает только диапазон объектной модели документа [(DOM),](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)  Возвращенный пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.  
      
      Для возвращенного пакета данных доступных свойств нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a>createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Преобразует выбор пользователя или приложения в фрагмент HTML, который можно совместно использовать.  
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
      
      Возвращенный пакет данных для выбора содержит HTML-разметку в формате буфера обмена.  Если в пользовательском интерфейсе приложения нет выбора пользователя, `createDataPackageFromSelection` возвращается `null` .  
      
      Для возвращенного пакета данных доступных свойств нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a>createFileFromStorageFile  

:::row:::
   :::column span="":::
      Преобразует [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) в стандартный объект W3C [File.](https://developer.mozilla.org/docs/Web/API/File)  
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
      | Любой | Содержит файл хранения.  |  
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
      | TypeMismatchError | Указанная ссылка на файл W3C недействительна.  Для версий, ранее чем Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a>createStreamFromInputStream  

:::row:::
   :::column span="":::
      Создает [MSStream](https://msdn.microsoft.com/library/hh772328) из [inputStream.](https://msdn.microsoft.com/library/hh772327)  
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
      | DOMString | Тип контента данных.  Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.  \([См. типы MIME,]( например https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) , , , , , , , , , `text/plain` и `text/html` так `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` далее \).  
      
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
      
      Этот метод принимает тип контента и `IInputStream` ссылку.  Метод проверяет, что переданная ссылка потока является экземпляром типа, а если `IInputStream` нет, то бросает `DOMException TYPE_MISMATCH_ERR` .  Если ошибки не происходит, `createStreamFromInputStream` `MSStream` создается \(из входных данных\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      An `IInputStream` можно использовать для создания `MSStream` .  Как и изначально одно время использования объектов, все URL-адреса, созданные отозваны при первом их использовании с помощью `MSStreams` `URL.createObjectURL` элемента изображения.  Кроме того, запросы на второй URL-адрес этого объекта после использования потока не будут.  
      
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

### <a name="execasyncatpriority"></a>execAsyncAtPriority  

:::row:::
   :::column span="":::
      Расписание выполнения вызова в более позднее время в соответствии с заданным приоритетом.  
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
      | Функция | Функция вызова, которая будет работать асинхронно, отправляется по заданному приоритету.  |  
      
      `priority` [in]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Значение контекстного приоритета, при котором запускается асинхронный вызовCallback.  См. [константы MSApp.](#msapp-constants)  |  
      
      `args` [in]
      
      | Тип | Описание |  
      |:---- |:--- |   
      | Любой | Необязательная серия аргументов, которые передаются функции вызова synchronousCallback \(как параметры 1 и так далее\).  |  
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
      
      Предоставленная `asynchronousCallback` функция вызова выполняется асинхронно позже.  `asynchronousCallback` будет отправлено в соответствии с предоставленным приоритетом.  Обычный приоритет эквивалентен существующему [методу setImmediate.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)  При выполнении вызова текущего контекстного приоритета задано приведенное значение параметра приоритета на время выполнения вызова.  
      
      Параметр `asynchronousCallback` callback может быть любой функцией.  Если после параметра будут предоставлены аргументы, все они будут переданы функции `priority` вызова.  
      
      В отличие от этого, любой объект, возвращаемый функцией обратного вызова, игнорируется `execAtPriority` `asynchronousCallback` \(и не возвращается `execAsyncAtPriority` через \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a>execAtPriority  

:::row:::
   :::column span="":::
      Выполняет указанную функцию вызова в данном контекстуальном приоритете.  
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
      | Функция | Функция вызова для синхронного запуска при данном приоритете контекстного приоритета.  |  
      
      `priority` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Указанное значение приоритета, которому будет задано текущее значение контекстного приоритета при запуске функции `synchronousCallback` вызова.  См. [константы MSApp.](#msapp-constants)  |  
      
      `args` [in]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Необязательный ряд аргументов, которые передаются функции вызова `synchronousCallback` \(в качестве параметров 1 и так далее\).  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Возвращает возвращаемое значение обратного вызова `synchronousCallback` \(как применимо\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Предоставленный `synchronousCallback` метод вызова выполняется синхронно.  Текущий контекстный приоритет меняется на предоставленное значение приоритета (дается аргументом приоритета) на время предоставляемой функции вызова.  После завершения выполнения функции обратного вызова приоритет возвращается к предыдущему значению перед `execAtPriority` вызовом.  Возвращаемого значения из является возвращаемого значения метода обратного `execAtPriority` вызова \(как предусмотрено\).  
      
      Параметр `synchronousCallback` callback может быть любой функцией.  Если после параметра приоритета будут предоставлены какие-либо аргументы, они будут переданы в предоставленный метод вызова.  Если параметр обратного вызова возвращает значение, это значение также становится `execAtPriority` возвратным.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
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

### <a name="getcurrentpriority"></a>getCurrentPriority  

:::row:::
   :::column span="":::
      Возвращает текущий контекстуальный приоритет.  

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
      | DOMString | Возвращаемого значения является одной из строк `MSApp.HIGH` , `MSApp.NORMAL` или `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод возвращает текущий контекстуальный приоритет \(см. [msApp Constants](#msapp-constants)\), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
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

### <a name="gethtmlprintdocumentsource"></a>getHtmlPrintDocumentSource  

Синхронный API, который был обесценен.  В Windows 10 `getHtmlPrintDocumentSourceAsync` см. .  Для Windows 8 и приложений 8.1 см. запись MSDN [для полученияHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### <a name="gethtmlprintdocumentsourceasync"></a>getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Возвращает исходный контент, который должен быть напечатан.  
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
      | Документ | Документ HTML, который будет напечатан.  Это может быть корневой документ, документ в iframe, фрагмент документа или документ SVG.  Следует помнить, что htmlDoc должен быть документом, а не элементом.  |  
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

### <a name="getviewid"></a>getViewId  

:::row:::
   :::column span="":::
      Поддержка нескольких окон.  
      
      > [!NOTE] 
      > В Win8.1 приложения JavaScript UWP поддерживали несколько окон с помощью API-API DOM MSApp, которые в настоящее время отклонились.  Для Windows 10 используйте `window.open` , `window` и новые `MSApp.getViewId` .  
      
      | Описание |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Создание нового окна | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Объект "Новое окно" | [окно](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
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
      
      Используйте [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) и [window](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но затем для взаимодействия с API WinRT добавьте `MSApp.getViewId` API.  Он принимает объект в качестве параметра и возвращает номер, который можно использовать с различными `window` `viewId` [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Задержка видимости  
          
          Представления в WinRT обычно начинают скрываться, и конечный разработчик использует что-то вроде отображения представления `TryShowAsStandaloneAsync` после его полной подготовки.  В веб-мире сразу показано окно, и конечный пользователь может наблюдать за загрузкой и отрисовкам `window.open` контента.  Чтобы ваши новые окна действовали как представления в WinRT и не отображались сразу, мы добавили `window.open` параметр.  Пример:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Основные различия в окне  
          
          Начальное окно, открываемое оси, действует иначе, чем открываемое дополнительное окно:  
          
          | Описание | Основной | Дополнительная |  
          |:---- |:--- |:--- |  
          | window.open | Разрешено | Disallowed |  
          | window.close | Закрыть приложение | Закрыть окно |  
          | Ограничения навигации | Только ACUR | Нет ограничений |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   Те же ограничения на связь происхождения  
          
          Существует сложная техническая проблема, предотвращая надлежащую поддержку синхронных, однополых, межкошко, вызовов скриптов.  При открываемом окне того же происхождения скрипту в одном окне разрешается напрямую вызывать функции в другом окне, и некоторые из этих вызовов не будут выполняться.  `postMessage` вызовы работают нормально, и это рекомендуемый способ сделать что-то, если это возможно.  Работа по улучшению этой проблемы продолжается.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a>isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Возвращает значение Boolean, указывающее, есть ли ожидаемая работа на заданном уровне приоритета или выше.  
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
      | DOMString | Значение приоритета \(см. в руб. [MSApp Constants](#msapp-constants)\) с указанием уровня приоритета и выше для запроса для выполнения любой незаполнеемой работы в очереди.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | `true`Возвращается, если есть какие-либо очереди работы на указанном уровне приоритета или выше, `false` в противном случае.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод позволяет коду JavaScript определить, есть ли ожидаемая работа на различных уровнях приоритета \(или выше\) с целью, чтобы вызывательный код JavaScript решил уступить работе с более высоким `isTaskScheduledAtPriorityOrHigher` приоритетом.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
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

### <a name="pagehandlesallapplicationactivations"></a>pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Используется для предотвращения обновления пути запуска (перезагрузки страницы) перед каждым событием активации \(например, щелкнув уведомление или закрепленную плитку\).  
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
      | Boolean (Логическое) | Используйте, чтобы всегда пропустить обновление пути запуска (перезагрузка страницы) и вместо этого перейти прямо к `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` запуску активированного события.  Требуется, чтобы все страницы обрабатывали события активации отдельно.  Определение этого метода как щелкнуть активированное событие \(например, уведомление\) не вызовет перезагрузку, необходимую для одно страницы приложений, желающих избежать перезагрузок `true` страниц.  |  
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
      **Пример**  
      
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

### <a name="suppresssubdownloadcredentialprompts"></a>suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Контролирует, подавляет ли приложение возможные запросы проверки подлинности во время скачивания ресурсов.  
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
      
      Метод контролирует, подавляет ли приложение потенциальные запросы проверки подлинности во `suppressSubdownloadCredentialPrompts` время скачивания ресурсов.  По умолчанию необходимо не подавлять запросы учетных данных.  
      
      `suppressSubdownloadCredentialPrompts` предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, которые требуют проверки подлинности, таких как почтовое приложение \(которое может содержать бюллетень, содержащий несколько изображений, где каждое изображение требует проверки подлинности\).  
      
      При подавлении подсказок учетных данных диалоги для проверки подлинности на серверах не будут показаны при доступе к ресурсам, которые требуют проверки подлинности, и ресурс не будет загружен.  Обратите внимание, что это не влияет на другие возможные запросы, такие как проверка подлинности прокси или диалоги запросов на сертификацию клиентов, а также на `suppressSubdownloadCredentialPrompts` XHR.  
      
      Следует помнить, что влияет на все содержимое в приложении, в том числе `suppressSubdownloadCredentialPrompts` на содержимое, которое было в `webview` элементе.  
      
      > [!IMPORTANT]
      > Оперативные решения учетных данных кэшются.  Таким образом, при подавлении подсказок учетных данных вступает в силу немедленно, что позволяет запросы учетных данных после их подавления, возможно, потребуется перезагрузка документа, чтобы в вступил в силу.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
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

### <a name="terminateapp"></a>terminateApp  


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
      | Ошибка | Объект, `Error` который можно использовать для описания ошибки, которая вызвала прекращение.  Объект должен содержать свойства числа, описания и стека; отчет о сбое не будет создан, если объект не содержит `Error` этих свойств.  |  
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
      
      Если проблема, о чем сообщается, становится одной из 5 главных проблем приложения, она будет показываться на странице `terminateApp` Качество приложения.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример**  
      
      В этом `terminateApp` примере вызывается, когда происходит исключение.  Он использует `Error` объект, предоставленный при улове исключения.  
      
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

### <a name="msapp-constants"></a>Константы MSApp  

:::row:::
   :::column span="":::
      Разрешенные значения приоритета, связанные `execAsyncAtPriority` с `execAtPriority` , и `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a>Текущие  
      
      `current`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании соответствующего метода \(См. также раздел\) метод будет использовать текущий контекстный приоритет при выполнении `current` запрашиваемой операции.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a>Высока  
      
      `high`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании соответствующего метода \(См. также раздел\), метод будет использовать более высокий, чем обычно, приоритет при выполнении запрашиваемой операции и будет отправлять операцию перед любой существующей нормальной приоритетной `high` работой.  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a>Состояние Idle (в покое)  
      
      `idle`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании соответствующего метода \(См. также раздел\), метод будет использовать ниже обычного приоритета при выполнении запрашиваемой операции и будет отправлять операцию после любой существующей нормальной приоритетной `ideal` работы.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a>Обычный  
      
      `normal`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании соответствующего метода (см. также раздел), при выполнении запрашиваемой операции метод будет использовать обычный `normal` существующий приоритет.  |  
   :::column-end:::
   :::column span="":::
      **Пример**  
      
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

## <a name="msappasyncoperation"></a>MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a>start  

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
      | DOMError | Представляет ошибку `MSAppAsyncOperation` в .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для установки обработера событий по завершению `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для установки обработера событий при ошибке во время `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Число | Представляет состояние асинхронной операции в приложении Windows с помощью JavaScript.  Значения включают: `Started[0]` `Completed[1]` , , `Error[2]` .  |  
      
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
