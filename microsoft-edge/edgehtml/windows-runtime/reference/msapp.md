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
# <a name="msapp"></a><span data-ttu-id="d52e8-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="d52e8-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="d52e8-106">Объект MSApp и его члены поддерживаются только для приложений Windows с помощью JavaScript \(включая pwAs, доступ к функциям API Windows\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="d52e8-107">Объект MSApp существует только в локальном контексте HTML-документа в приложении Windows, загружаемом с помощью схемы URI ms-appx; в противном случае объект не существует (и, следовательно, ни один из его методов и свойств не доступен).</span><span class="sxs-lookup"><span data-stu-id="d52e8-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="d52e8-108">Он предоставляет дополнительные функции, которые позволяют создавать [объекты Blob](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d52e8-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="d52e8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d52e8-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d52e8-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage,](#createdatapackage) [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="d52e8-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d52e8-111">Константы</span><span class="sxs-lookup"><span data-stu-id="d52e8-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d52e8-112">[текущий,](#current) [высокий,](#high) [простой,](#idle) [нормальный](#normal).</span><span class="sxs-lookup"><span data-stu-id="d52e8-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d52e8-113">Интерфейс MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="d52e8-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="d52e8-114">start</span><span class="sxs-lookup"><span data-stu-id="d52e8-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a><span data-ttu-id="d52e8-115">Методы MSApp</span><span class="sxs-lookup"><span data-stu-id="d52e8-115">MSApp methods</span></span>  

### <a name="cleartemporarywebdataasync"></a><span data-ttu-id="d52e8-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="d52e8-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-117">Очищает кэш и индексацию данныхdb для приложения или [WebView.](../../hosting/webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="d52e8-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-118">Parameters</span></span>**  
      
      <span data-ttu-id="d52e8-119">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d52e8-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-120">Return value</span></span>**  
      
      <span data-ttu-id="d52e8-121">Тип: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="d52e8-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="d52e8-122">Представляет асинхронное действие.</span><span class="sxs-lookup"><span data-stu-id="d52e8-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-123">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-123">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-125">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-127">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a><span data-ttu-id="d52e8-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="d52e8-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-129">Создает [Blob из](https://developer.mozilla.org/docs/Web/API/Blob) [объекта IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="d52e8-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="d52e8-130">Этот метод следует использовать при работе с объектами в приложениях, чтобы создать объект на основе `IRandomAccessStream` W3C из потока.</span><span class="sxs-lookup"><span data-stu-id="d52e8-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="d52e8-131">После создания blob его можно использовать с [файлами FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API](https://developer.mozilla.org/docs/Web/API/URL)URL-адресов и [XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)</span><span class="sxs-lookup"><span data-stu-id="d52e8-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-132">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="d52e8-133">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-133">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-134">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-134">Type</span></span> | <span data-ttu-id="d52e8-135">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-136">Строка</span><span class="sxs-lookup"><span data-stu-id="d52e8-136">String</span></span> | <span data-ttu-id="d52e8-137">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="d52e8-137">Content type of the data.</span></span>  <span data-ttu-id="d52e8-138">Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="d52e8-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="d52e8-139">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-139">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-140">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-140">Type</span></span> | <span data-ttu-id="d52e8-141">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-142">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-142">Any</span></span> | <span data-ttu-id="d52e8-143">[IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) который будет храниться в Blob.</span><span class="sxs-lookup"><span data-stu-id="d52e8-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-144">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-145">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-145">Type</span></span> | <span data-ttu-id="d52e8-146">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-147">Blob</span><span class="sxs-lookup"><span data-stu-id="d52e8-147">Blob</span></span> | <span data-ttu-id="d52e8-148">Новый объект blob, содержащий поток.</span><span class="sxs-lookup"><span data-stu-id="d52e8-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-149">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="d52e8-150">Исключение</span><span class="sxs-lookup"><span data-stu-id="d52e8-150">Exception</span></span> | <span data-ttu-id="d52e8-151">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d52e8-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="d52e8-152">TypeMismatchError</span></span> | <span data-ttu-id="d52e8-153">Тип узла несовместим с ожидаемым типом параметра.</span><span class="sxs-lookup"><span data-stu-id="d52e8-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="d52e8-154">Для версий, ранее чем Internet Explorer 10, TYPE_MISMATCH_ERR возвращается.</span><span class="sxs-lookup"><span data-stu-id="d52e8-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-155">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-156">Создает Blob из типов времени запуска Windows через пространство имен MSApp на объекте окна.</span><span class="sxs-lookup"><span data-stu-id="d52e8-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="d52e8-157">Этот метод создаст blob, который по сути является световой оболочкой над объектом [RandomAccessStream,](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) предоставленным ему.</span><span class="sxs-lookup"><span data-stu-id="d52e8-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="d52e8-158">BLOB владеет сроком службы этого потока, и поток будет закрыт при уничтожении blob.</span><span class="sxs-lookup"><span data-stu-id="d52e8-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-159">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-159">Example</span></span>**  
      
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

### <a name="createdatapackage"></a><span data-ttu-id="d52e8-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="d52e8-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-161">Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, который можно совместно использовать.</span><span class="sxs-lookup"><span data-stu-id="d52e8-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="d52e8-163">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-163">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-164">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-164">Type</span></span> | <span data-ttu-id="d52e8-165">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-166">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-166">Any</span></span> | <span data-ttu-id="d52e8-167">Этот диапазон можно создать либо из объекта выбора, например: `window.selection.getRangeAt(0)` или вручную.</span><span class="sxs-lookup"><span data-stu-id="d52e8-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-168">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-168">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-169">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-169">Type</span></span> | <span data-ttu-id="d52e8-170">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-171">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-171">Any</span></span> | <span data-ttu-id="d52e8-172">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="d52e8-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-173">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-173">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-174">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-175">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-176">Этот метод поддерживает только диапазон объектной модели документа [(DOM),](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)</span><span class="sxs-lookup"><span data-stu-id="d52e8-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="d52e8-177">Возвращенный пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="d52e8-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="d52e8-178">Для возвращенного пакета данных доступных свойств нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-179">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-179">Example</span></span>**  
      
      <span data-ttu-id="d52e8-180">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a><span data-ttu-id="d52e8-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="d52e8-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-182">Преобразует выбор пользователя или приложения в фрагмент HTML, который можно совместно использовать.</span><span class="sxs-lookup"><span data-stu-id="d52e8-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-183">Parameters</span></span>**  
      
      <span data-ttu-id="d52e8-184">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d52e8-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-185">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-185">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-186">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-186">Type</span></span> | <span data-ttu-id="d52e8-187">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-188">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-188">Any</span></span> | <span data-ttu-id="d52e8-189">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="d52e8-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-190">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-190">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-191">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-192">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-193">Возвращенный пакет данных для выбора содержит HTML-разметку в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="d52e8-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="d52e8-194">Если в пользовательском интерфейсе приложения нет выбора пользователя, `createDataPackageFromSelection` возвращается `null` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="d52e8-195">Для возвращенного пакета данных доступных свойств нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-196">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a><span data-ttu-id="d52e8-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="d52e8-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-198">Преобразует [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) в стандартный объект W3C [File.](https://developer.mozilla.org/docs/Web/API/File)</span><span class="sxs-lookup"><span data-stu-id="d52e8-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-199">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="d52e8-200">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-200">[in]</span></span>
      
      | <span data-ttu-id="d52e8-201">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-201">Type</span></span> | <span data-ttu-id="d52e8-202">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-203">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-203">Any</span></span> | <span data-ttu-id="d52e8-204">Содержит файл хранения.</span><span class="sxs-lookup"><span data-stu-id="d52e8-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-205">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-205">Return value</span></span>**
      
      <span data-ttu-id="d52e8-206">Нет</span><span class="sxs-lookup"><span data-stu-id="d52e8-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-207">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="d52e8-208">Исключение</span><span class="sxs-lookup"><span data-stu-id="d52e8-208">Exception</span></span> | <span data-ttu-id="d52e8-209">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d52e8-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="d52e8-210">TypeMismatchError</span></span> | <span data-ttu-id="d52e8-211">Указанная ссылка на файл W3C недействительна.</span><span class="sxs-lookup"><span data-stu-id="d52e8-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="d52e8-212">Для версий, ранее чем Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается.</span><span class="sxs-lookup"><span data-stu-id="d52e8-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-213">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-213">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-214">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-215">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a><span data-ttu-id="d52e8-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="d52e8-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-217">Создает [MSStream](https://msdn.microsoft.com/library/hh772328) из [inputStream.](https://msdn.microsoft.com/library/hh772327)</span><span class="sxs-lookup"><span data-stu-id="d52e8-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-218">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="d52e8-219">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-219">[in]</span></span>
      
      | <span data-ttu-id="d52e8-220">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-220">Type</span></span> | <span data-ttu-id="d52e8-221">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-222">DOMString</span></span> | <span data-ttu-id="d52e8-223">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="d52e8-223">Content type of the data.</span></span>  <span data-ttu-id="d52e8-224">Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="d52e8-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="d52e8-225">\([См. типы MIME,]( например https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) , , , , , , , , , `text/plain` и `text/html` так `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` далее \).</span><span class="sxs-lookup"><span data-stu-id="d52e8-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="d52e8-226">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-226">[in]</span></span>
      
      | <span data-ttu-id="d52e8-227">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-227">Type</span></span> | <span data-ttu-id="d52e8-228">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-229">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-229">Any</span></span> | <span data-ttu-id="d52e8-230">[IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) который будет храниться в `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-231">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-231">Return value</span></span>**
      
      <span data-ttu-id="d52e8-232">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-233">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-233">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-234">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-235">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-235">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-236">Этот метод принимает тип контента и `IInputStream` ссылку.</span><span class="sxs-lookup"><span data-stu-id="d52e8-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="d52e8-237">Метод проверяет, что переданная ссылка потока является экземпляром типа, а если `IInputStream` нет, то бросает `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="d52e8-238">Если ошибки не происходит, `createStreamFromInputStream` `MSStream` создается \(из входных данных\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-239">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-239">Example</span></span>**  
      
      <span data-ttu-id="d52e8-240">An `IInputStream` можно использовать для создания `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="d52e8-241">Как и изначально одно время использования объектов, все URL-адреса, созданные отозваны при первом их использовании с помощью `MSStreams` `URL.createObjectURL` элемента изображения.</span><span class="sxs-lookup"><span data-stu-id="d52e8-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="d52e8-242">Кроме того, запросы на второй URL-адрес этого объекта после использования потока не будут.</span><span class="sxs-lookup"><span data-stu-id="d52e8-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <a name="execasyncatpriority"></a><span data-ttu-id="d52e8-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="d52e8-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-244">Расписание выполнения вызова в более позднее время в соответствии с заданным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="d52e8-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="d52e8-246">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-246">[in]</span></span>
      
      | <span data-ttu-id="d52e8-247">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-247">Type</span></span> | <span data-ttu-id="d52e8-248">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-249">Функция</span><span class="sxs-lookup"><span data-stu-id="d52e8-249">Function</span></span> | <span data-ttu-id="d52e8-250">Функция вызова, которая будет работать асинхронно, отправляется по заданному приоритету.</span><span class="sxs-lookup"><span data-stu-id="d52e8-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="d52e8-251">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-251">[in]</span></span>
      
      | <span data-ttu-id="d52e8-252">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-252">Type</span></span> | <span data-ttu-id="d52e8-253">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-254">DOMString</span></span> | <span data-ttu-id="d52e8-255">Значение контекстного приоритета, при котором запускается асинхронный вызовCallback.</span><span class="sxs-lookup"><span data-stu-id="d52e8-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="d52e8-256">См. [константы MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="d52e8-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="d52e8-257">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-257">[in]</span></span>
      
      | <span data-ttu-id="d52e8-258">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-258">Type</span></span> | <span data-ttu-id="d52e8-259">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="d52e8-260">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-260">Any</span></span> | <span data-ttu-id="d52e8-261">Необязательная серия аргументов, которые передаются функции вызова synchronousCallback \(как параметры 1 и так далее\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-262">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-262">Return value</span></span>**  
      
      <span data-ttu-id="d52e8-263">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d52e8-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-264">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-264">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-265">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-266">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-267">Предоставленная `asynchronousCallback` функция вызова выполняется асинхронно позже.</span><span class="sxs-lookup"><span data-stu-id="d52e8-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="d52e8-268">будет отправлено в соответствии с предоставленным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="d52e8-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="d52e8-269">Обычный приоритет эквивалентен существующему [методу setImmediate.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)</span><span class="sxs-lookup"><span data-stu-id="d52e8-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="d52e8-270">При выполнении вызова текущего контекстного приоритета задано приведенное значение параметра приоритета на время выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="d52e8-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="d52e8-271">Параметр `asynchronousCallback` callback может быть любой функцией.</span><span class="sxs-lookup"><span data-stu-id="d52e8-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="d52e8-272">Если после параметра будут предоставлены аргументы, все они будут переданы функции `priority` вызова.</span><span class="sxs-lookup"><span data-stu-id="d52e8-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="d52e8-273">В отличие от этого, любой объект, возвращаемый функцией обратного вызова, игнорируется `execAtPriority` `asynchronousCallback` \(и не возвращается `execAsyncAtPriority` через \).</span><span class="sxs-lookup"><span data-stu-id="d52e8-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-274">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a><span data-ttu-id="d52e8-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="d52e8-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-276">Выполняет указанную функцию вызова в данном контекстуальном приоритете.</span><span class="sxs-lookup"><span data-stu-id="d52e8-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-277">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="d52e8-278">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-278">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-279">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-279">Type</span></span> | <span data-ttu-id="d52e8-280">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-281">Функция</span><span class="sxs-lookup"><span data-stu-id="d52e8-281">Function</span></span> | <span data-ttu-id="d52e8-282">Функция вызова для синхронного запуска при данном приоритете контекстного приоритета.</span><span class="sxs-lookup"><span data-stu-id="d52e8-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="d52e8-283">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-283">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-284">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-284">Type</span></span> | <span data-ttu-id="d52e8-285">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-286">DOMString</span></span> | <span data-ttu-id="d52e8-287">Указанное значение приоритета, которому будет задано текущее значение контекстного приоритета при запуске функции `synchronousCallback` вызова.</span><span class="sxs-lookup"><span data-stu-id="d52e8-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="d52e8-288">См. [константы MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="d52e8-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="d52e8-289">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-289">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-290">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-290">Type</span></span> | <span data-ttu-id="d52e8-291">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-292">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-292">Any</span></span> | <span data-ttu-id="d52e8-293">Необязательный ряд аргументов, которые передаются функции вызова `synchronousCallback` \(в качестве параметров 1 и так далее\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-294">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-294">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-295">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-295">Type</span></span> | <span data-ttu-id="d52e8-296">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-297">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-297">Any</span></span> | <span data-ttu-id="d52e8-298">Возвращает возвращаемое значение обратного вызова `synchronousCallback` \(как применимо\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-299">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-299">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-300">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-301">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-301">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-302">Предоставленный `synchronousCallback` метод вызова выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="d52e8-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="d52e8-303">Текущий контекстный приоритет меняется на предоставленное значение приоритета (дается аргументом приоритета) на время предоставляемой функции вызова.</span><span class="sxs-lookup"><span data-stu-id="d52e8-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="d52e8-304">После завершения выполнения функции обратного вызова приоритет возвращается к предыдущему значению перед `execAtPriority` вызовом.</span><span class="sxs-lookup"><span data-stu-id="d52e8-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="d52e8-305">Возвращаемого значения из является возвращаемого значения метода обратного `execAtPriority` вызова \(как предусмотрено\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="d52e8-306">Параметр `synchronousCallback` callback может быть любой функцией.</span><span class="sxs-lookup"><span data-stu-id="d52e8-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="d52e8-307">Если после параметра приоритета будут предоставлены какие-либо аргументы, они будут переданы в предоставленный метод вызова.</span><span class="sxs-lookup"><span data-stu-id="d52e8-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="d52e8-308">Если параметр обратного вызова возвращает значение, это значение также становится `execAtPriority` возвратным.</span><span class="sxs-lookup"><span data-stu-id="d52e8-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-309">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-309">Example</span></span>**  
      
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

### <a name="getcurrentpriority"></a><span data-ttu-id="d52e8-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="d52e8-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-311">Возвращает текущий контекстуальный приоритет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-312">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-312">Parameters</span></span>**  
      
      <span data-ttu-id="d52e8-313">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-314">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-314">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-315">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-315">Type</span></span> | <span data-ttu-id="d52e8-316">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-317">DOMString</span></span> | <span data-ttu-id="d52e8-318">Возвращаемого значения является одной из строк `MSApp.HIGH` , `MSApp.NORMAL` или `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-319">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-319">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-320">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-321">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-321">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-322">Этот метод возвращает текущий контекстуальный приоритет \(см. [msApp Constants](#msapp-constants)\), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-323">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-323">Example</span></span>**  
      
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

### <a name="gethtmlprintdocumentsource"></a><span data-ttu-id="d52e8-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="d52e8-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="d52e8-325">Синхронный API, который был обесценен.</span><span class="sxs-lookup"><span data-stu-id="d52e8-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="d52e8-326">В Windows 10 `getHtmlPrintDocumentSourceAsync` см. .</span><span class="sxs-lookup"><span data-stu-id="d52e8-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="d52e8-327">Для Windows 8 и приложений 8.1 см. запись MSDN [для полученияHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="d52e8-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <a name="gethtmlprintdocumentsourceasync"></a><span data-ttu-id="d52e8-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="d52e8-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-329">Возвращает исходный контент, который должен быть напечатан.</span><span class="sxs-lookup"><span data-stu-id="d52e8-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-330">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="d52e8-331">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-331">[in]</span></span>  
      
      | <span data-ttu-id="d52e8-332">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-332">Type</span></span> | <span data-ttu-id="d52e8-333">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-334">Документ</span><span class="sxs-lookup"><span data-stu-id="d52e8-334">Document</span></span> | <span data-ttu-id="d52e8-335">Документ HTML, который будет напечатан.</span><span class="sxs-lookup"><span data-stu-id="d52e8-335">The HTML document to be printed.</span></span>  <span data-ttu-id="d52e8-336">Это может быть корневой документ, документ в iframe, фрагмент документа или документ SVG.</span><span class="sxs-lookup"><span data-stu-id="d52e8-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="d52e8-337">Следует помнить, что htmlDoc должен быть документом, а не элементом.</span><span class="sxs-lookup"><span data-stu-id="d52e8-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-338">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-338">Return value</span></span>**
      
      <span data-ttu-id="d52e8-339">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-340">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-340">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-341">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-342">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-342">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-343">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-344">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d52e8-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="d52e8-345">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d52e8-345">Example 2</span></span>**  
      
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

### <a name="getviewid"></a><span data-ttu-id="d52e8-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="d52e8-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-347">Поддержка нескольких окон.</span><span class="sxs-lookup"><span data-stu-id="d52e8-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="d52e8-348">В Win8.1 приложения JavaScript UWP поддерживали несколько окон с помощью API-API DOM MSApp, которые в настоящее время отклонились.</span><span class="sxs-lookup"><span data-stu-id="d52e8-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="d52e8-349">Для Windows 10 используйте `window.open` , `window` и новые `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="d52e8-350">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-350">Description</span></span> |<span data-ttu-id="d52e8-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d52e8-351">Windows 10</span></span> | <span data-ttu-id="d52e8-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d52e8-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="d52e8-353">Создание нового окна</span><span class="sxs-lookup"><span data-stu-id="d52e8-353">Create new window</span></span> | [<span data-ttu-id="d52e8-354">window.open</span><span class="sxs-lookup"><span data-stu-id="d52e8-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="d52e8-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="d52e8-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="d52e8-356">Объект "Новое окно"</span><span class="sxs-lookup"><span data-stu-id="d52e8-356">New window object</span></span> | [<span data-ttu-id="d52e8-357">окно</span><span class="sxs-lookup"><span data-stu-id="d52e8-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="d52e8-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="d52e8-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-359">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="d52e8-360">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-360">Type</span></span> | <span data-ttu-id="d52e8-361">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-362">DOMString</span></span> | <span data-ttu-id="d52e8-363">Объект, представляющий окно, содержащее документ DOM.</span><span class="sxs-lookup"><span data-stu-id="d52e8-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-364">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="d52e8-365">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-365">Type</span></span> | <span data-ttu-id="d52e8-366">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-367">Число</span><span class="sxs-lookup"><span data-stu-id="d52e8-367">Number</span></span> | <span data-ttu-id="d52e8-368">Можно использовать с различными [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="d52e8-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-369">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-369">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-370">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-371">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-371">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-372">Используйте [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) и [window](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но затем для взаимодействия с API WinRT добавьте `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="d52e8-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="d52e8-373">Он принимает объект в качестве параметра и возвращает номер, который можно использовать с различными `window` `viewId` [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="d52e8-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="d52e8-374">Задержка видимости</span><span class="sxs-lookup"><span data-stu-id="d52e8-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="d52e8-375">Представления в WinRT обычно начинают скрываться, и конечный разработчик использует что-то вроде отображения представления `TryShowAsStandaloneAsync` после его полной подготовки.</span><span class="sxs-lookup"><span data-stu-id="d52e8-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="d52e8-376">В веб-мире сразу показано окно, и конечный пользователь может наблюдать за загрузкой и отрисовкам `window.open` контента.</span><span class="sxs-lookup"><span data-stu-id="d52e8-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="d52e8-377">Чтобы ваши новые окна действовали как представления в WinRT и не отображались сразу, мы добавили `window.open` параметр.</span><span class="sxs-lookup"><span data-stu-id="d52e8-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="d52e8-378">Пример:</span><span class="sxs-lookup"><span data-stu-id="d52e8-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="d52e8-379">Основные различия в окне</span><span class="sxs-lookup"><span data-stu-id="d52e8-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="d52e8-380">Начальное окно, открываемое оси, действует иначе, чем открываемое дополнительное окно:</span><span class="sxs-lookup"><span data-stu-id="d52e8-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="d52e8-381">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-381">Description</span></span> | <span data-ttu-id="d52e8-382">Основной</span><span class="sxs-lookup"><span data-stu-id="d52e8-382">Primary</span></span> | <span data-ttu-id="d52e8-383">Дополнительная</span><span class="sxs-lookup"><span data-stu-id="d52e8-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="d52e8-384">window.open</span><span class="sxs-lookup"><span data-stu-id="d52e8-384">window.open</span></span> | <span data-ttu-id="d52e8-385">Разрешено</span><span class="sxs-lookup"><span data-stu-id="d52e8-385">Allowed</span></span> | <span data-ttu-id="d52e8-386">Disallowed</span><span class="sxs-lookup"><span data-stu-id="d52e8-386">Disallowed</span></span> |  
          | <span data-ttu-id="d52e8-387">window.close</span><span class="sxs-lookup"><span data-stu-id="d52e8-387">window.close</span></span> | <span data-ttu-id="d52e8-388">Закрыть приложение</span><span class="sxs-lookup"><span data-stu-id="d52e8-388">Close app</span></span> | <span data-ttu-id="d52e8-389">Закрыть окно</span><span class="sxs-lookup"><span data-stu-id="d52e8-389">Close window</span></span> |  
          | <span data-ttu-id="d52e8-390">Ограничения навигации</span><span class="sxs-lookup"><span data-stu-id="d52e8-390">Navigation restrictions</span></span> | <span data-ttu-id="d52e8-391">Только ACUR</span><span class="sxs-lookup"><span data-stu-id="d52e8-391">ACUR only</span></span> | <span data-ttu-id="d52e8-392">Нет ограничений</span><span class="sxs-lookup"><span data-stu-id="d52e8-392">No restrictions</span></span> |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   <span data-ttu-id="d52e8-393">Те же ограничения на связь происхождения</span><span class="sxs-lookup"><span data-stu-id="d52e8-393">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="d52e8-394">Существует сложная техническая проблема, предотвращая надлежащую поддержку синхронных, однополых, межкошко, вызовов скриптов.</span><span class="sxs-lookup"><span data-stu-id="d52e8-394">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="d52e8-395">При открываемом окне того же происхождения скрипту в одном окне разрешается напрямую вызывать функции в другом окне, и некоторые из этих вызовов не будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="d52e8-395">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="d52e8-396">вызовы работают нормально, и это рекомендуемый способ сделать что-то, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="d52e8-396">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="d52e8-397">Работа по улучшению этой проблемы продолжается.</span><span class="sxs-lookup"><span data-stu-id="d52e8-397">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-398">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-398">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a><span data-ttu-id="d52e8-399">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="d52e8-399">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-400">Возвращает значение Boolean, указывающее, есть ли ожидаемая работа на заданном уровне приоритета или выше.</span><span class="sxs-lookup"><span data-stu-id="d52e8-400">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-401">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-401">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="d52e8-402">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-402">[in]</span></span>
      
      | <span data-ttu-id="d52e8-403">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-403">Type</span></span> | <span data-ttu-id="d52e8-404">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-404">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-405">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-405">DOMString</span></span> | <span data-ttu-id="d52e8-406">Значение приоритета \(см. в руб. [MSApp Constants](#msapp-constants)\) с указанием уровня приоритета и выше для запроса для выполнения любой незаполнеемой работы в очереди.</span><span class="sxs-lookup"><span data-stu-id="d52e8-406">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-407">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-407">Return value</span></span>**  
      
      | <span data-ttu-id="d52e8-408">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-408">Type</span></span> | <span data-ttu-id="d52e8-409">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-409">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-410">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="d52e8-410">Boolean</span></span> | <span data-ttu-id="d52e8-411">`true`Возвращается, если есть какие-либо очереди работы на указанном уровне приоритета или выше, `false` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d52e8-411">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-412">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-412">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-413">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-413">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-414">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-414">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-415">Этот метод позволяет коду JavaScript определить, есть ли ожидаемая работа на различных уровнях приоритета \(или выше\) с целью, чтобы вызывательный код JavaScript решил уступить работе с более высоким `isTaskScheduledAtPriorityOrHigher` приоритетом.</span><span class="sxs-lookup"><span data-stu-id="d52e8-415">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-416">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-416">Example</span></span>**  
      
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

### <a name="pagehandlesallapplicationactivations"></a><span data-ttu-id="d52e8-417">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="d52e8-417">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-418">Используется для предотвращения обновления пути запуска (перезагрузки страницы) перед каждым событием активации \(например, щелкнув уведомление или закрепленную плитку\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-418">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-419">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-419">Parameters</span></span>**  
      
      | <span data-ttu-id="d52e8-420">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-420">Type</span></span> | <span data-ttu-id="d52e8-421">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-421">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-422">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="d52e8-422">Boolean</span></span> | <span data-ttu-id="d52e8-423">Используйте, чтобы всегда пропустить обновление пути запуска (перезагрузка страницы) и вместо этого перейти прямо к `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` запуску активированного события.</span><span class="sxs-lookup"><span data-stu-id="d52e8-423">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="d52e8-424">Требуется, чтобы все страницы обрабатывали события активации отдельно.</span><span class="sxs-lookup"><span data-stu-id="d52e8-424">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="d52e8-425">Определение этого метода как щелкнуть активированное событие \(например, уведомление\) не вызовет перезагрузку, необходимую для одно страницы приложений, желающих избежать перезагрузок `true` страниц.</span><span class="sxs-lookup"><span data-stu-id="d52e8-425">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-426">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-426">Return value</span></span>**
      
      <span data-ttu-id="d52e8-427">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-427">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-428">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-428">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-429">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-429">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-430">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-430">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-431">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-431">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-432">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-432">Example</span></span>**  
      
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

### <a name="suppresssubdownloadcredentialprompts"></a><span data-ttu-id="d52e8-433">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="d52e8-433">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-434">Контролирует, подавляет ли приложение возможные запросы проверки подлинности во время скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d52e8-434">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-435">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-435">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="d52e8-436">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-436">[in]</span></span>
      
      | <span data-ttu-id="d52e8-437">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-437">Type</span></span> | <span data-ttu-id="d52e8-438">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-438">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-439">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="d52e8-439">Boolean</span></span> | <span data-ttu-id="d52e8-440">Значение true подавляет потенциальные запросы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d52e8-440">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="d52e8-441">Значение false не подавляет потенциальные запросы проверки подлинности от пользователя.</span><span class="sxs-lookup"><span data-stu-id="d52e8-441">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-442">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-442">Return value</span></span>**  
      
      <span data-ttu-id="d52e8-443">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-443">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-444">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-444">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-445">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-445">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-446">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-446">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-447">Метод контролирует, подавляет ли приложение потенциальные запросы проверки подлинности во `suppressSubdownloadCredentialPrompts` время скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d52e8-447">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="d52e8-448">По умолчанию необходимо не подавлять запросы учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d52e8-448">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="d52e8-449">предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, которые требуют проверки подлинности, таких как почтовое приложение \(которое может содержать бюллетень, содержащий несколько изображений, где каждое изображение требует проверки подлинности\).</span><span class="sxs-lookup"><span data-stu-id="d52e8-449">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="d52e8-450">При подавлении подсказок учетных данных диалоги для проверки подлинности на серверах не будут показаны при доступе к ресурсам, которые требуют проверки подлинности, и ресурс не будет загружен.</span><span class="sxs-lookup"><span data-stu-id="d52e8-450">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="d52e8-451">Обратите внимание, что это не влияет на другие возможные запросы, такие как проверка подлинности прокси или диалоги запросов на сертификацию клиентов, а также на `suppressSubdownloadCredentialPrompts` XHR.</span><span class="sxs-lookup"><span data-stu-id="d52e8-451">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="d52e8-452">Следует помнить, что влияет на все содержимое в приложении, в том числе `suppressSubdownloadCredentialPrompts` на содержимое, которое было в `webview` элементе.</span><span class="sxs-lookup"><span data-stu-id="d52e8-452">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="d52e8-453">Оперативные решения учетных данных кэшются.</span><span class="sxs-lookup"><span data-stu-id="d52e8-453">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="d52e8-454">Таким образом, при подавлении подсказок учетных данных вступает в силу немедленно, что позволяет запросы учетных данных после их подавления, возможно, потребуется перезагрузка документа, чтобы в вступил в силу.</span><span class="sxs-lookup"><span data-stu-id="d52e8-454">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-455">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-455">Example</span></span>**  
      
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

### <a name="terminateapp"></a><span data-ttu-id="d52e8-456">terminateApp</span><span class="sxs-lookup"><span data-stu-id="d52e8-456">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-457">Завершает текущее приложение и создает отчет о сбое.</span><span class="sxs-lookup"><span data-stu-id="d52e8-457">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-458">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-458">Parameters</span></span>**  
      
      `error` <span data-ttu-id="d52e8-459">[in]</span><span class="sxs-lookup"><span data-stu-id="d52e8-459">[in]</span></span>
      
      | <span data-ttu-id="d52e8-460">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-460">Type</span></span> | <span data-ttu-id="d52e8-461">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-461">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-462">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d52e8-462">Error</span></span> | <span data-ttu-id="d52e8-463">Объект, `Error` который можно использовать для описания ошибки, которая вызвала прекращение.</span><span class="sxs-lookup"><span data-stu-id="d52e8-463">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="d52e8-464">Объект должен содержать свойства числа, описания и стека; отчет о сбое не будет создан, если объект не содержит `Error` этих свойств.</span><span class="sxs-lookup"><span data-stu-id="d52e8-464">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-465">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-465">Return value</span></span>**
      
      <span data-ttu-id="d52e8-466">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-466">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-467">Исключения</span><span class="sxs-lookup"><span data-stu-id="d52e8-467">Exceptions</span></span>**  
      
      <span data-ttu-id="d52e8-468">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-468">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-469">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52e8-469">Remarks</span></span>**  
      
      <span data-ttu-id="d52e8-470">Если проблема, о чем сообщается, становится одной из 5 главных проблем приложения, она будет показываться на странице `terminateApp` Качество приложения.</span><span class="sxs-lookup"><span data-stu-id="d52e8-470">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-471">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-471">Example</span></span>**  
      
      <span data-ttu-id="d52e8-472">В этом `terminateApp` примере вызывается, когда происходит исключение.</span><span class="sxs-lookup"><span data-stu-id="d52e8-472">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="d52e8-473">Он использует `Error` объект, предоставленный при улове исключения.</span><span class="sxs-lookup"><span data-stu-id="d52e8-473">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <a name="msapp-constants"></a><span data-ttu-id="d52e8-474">Константы MSApp</span><span class="sxs-lookup"><span data-stu-id="d52e8-474">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-475">Разрешенные значения приоритета, связанные `execAsyncAtPriority` с `execAtPriority` , и `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-475">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a><span data-ttu-id="d52e8-476">Текущие</span><span class="sxs-lookup"><span data-stu-id="d52e8-476">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="d52e8-477">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-477">Type</span></span> | <span data-ttu-id="d52e8-478">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-478">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-479">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-479">DOMString</span></span> | <span data-ttu-id="d52e8-480">При использовании соответствующего метода \(См. также раздел\) метод будет использовать текущий контекстный приоритет при выполнении `current` запрашиваемой операции.</span><span class="sxs-lookup"><span data-stu-id="d52e8-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a><span data-ttu-id="d52e8-481">Высока</span><span class="sxs-lookup"><span data-stu-id="d52e8-481">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="d52e8-482">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-482">Type</span></span> | <span data-ttu-id="d52e8-483">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-483">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-484">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-484">DOMString</span></span> | <span data-ttu-id="d52e8-485">При использовании соответствующего метода \(См. также раздел\), метод будет использовать более высокий, чем обычно, приоритет при выполнении запрашиваемой операции и будет отправлять операцию перед любой существующей нормальной приоритетной `high` работой.</span><span class="sxs-lookup"><span data-stu-id="d52e8-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a><span data-ttu-id="d52e8-486">Состояние Idle (в покое)</span><span class="sxs-lookup"><span data-stu-id="d52e8-486">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="d52e8-487">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-487">Type</span></span> | <span data-ttu-id="d52e8-488">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-488">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-489">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-489">DOMString</span></span> | <span data-ttu-id="d52e8-490">При использовании соответствующего метода \(См. также раздел\), метод будет использовать ниже обычного приоритета при выполнении запрашиваемой операции и будет отправлять операцию после любой существующей нормальной приоритетной `ideal` работы.</span><span class="sxs-lookup"><span data-stu-id="d52e8-490">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a><span data-ttu-id="d52e8-491">Обычный</span><span class="sxs-lookup"><span data-stu-id="d52e8-491">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="d52e8-492">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-492">Type</span></span> | <span data-ttu-id="d52e8-493">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-493">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-494">DOMString</span><span class="sxs-lookup"><span data-stu-id="d52e8-494">DOMString</span></span> | <span data-ttu-id="d52e8-495">При использовании соответствующего метода (см. также раздел), при выполнении запрашиваемой операции метод будет использовать обычный `normal` существующий приоритет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-495">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-496">Пример</span><span class="sxs-lookup"><span data-stu-id="d52e8-496">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-497">Требования</span><span class="sxs-lookup"><span data-stu-id="d52e8-497">Requirements</span></span>**  
      
      | <span data-ttu-id="d52e8-498">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-498">Type</span></span> | <span data-ttu-id="d52e8-499">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-499">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-500">IDL</span><span class="sxs-lookup"><span data-stu-id="d52e8-500">IDL</span></span> | <span data-ttu-id="d52e8-501">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="d52e8-501">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a><span data-ttu-id="d52e8-502">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="d52e8-502">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a><span data-ttu-id="d52e8-503">start</span><span class="sxs-lookup"><span data-stu-id="d52e8-503">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d52e8-504">Запускает `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-504">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="d52e8-505">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52e8-505">Parameters</span></span>**  
      
      <span data-ttu-id="d52e8-506">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-506">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="d52e8-507">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52e8-507">Return value</span></span>**
      
      <span data-ttu-id="d52e8-508">Нет.</span><span class="sxs-lookup"><span data-stu-id="d52e8-508">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="d52e8-509">Свойства</span><span class="sxs-lookup"><span data-stu-id="d52e8-509">Properties</span></span>**  
      
      `error` <span data-ttu-id="d52e8-510">свойство</span><span class="sxs-lookup"><span data-stu-id="d52e8-510">property</span></span>  
      
      | <span data-ttu-id="d52e8-511">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-511">Type</span></span> | <span data-ttu-id="d52e8-512">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-512">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-513">DOMError</span><span class="sxs-lookup"><span data-stu-id="d52e8-513">DOMError</span></span> | <span data-ttu-id="d52e8-514">Представляет ошибку `MSAppAsyncOperation` в .</span><span class="sxs-lookup"><span data-stu-id="d52e8-514">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="d52e8-515">свойство</span><span class="sxs-lookup"><span data-stu-id="d52e8-515">property</span></span>  
      
      | <span data-ttu-id="d52e8-516">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-516">Type</span></span> | <span data-ttu-id="d52e8-517">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-517">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-518">EventHandler</span><span class="sxs-lookup"><span data-stu-id="d52e8-518">EventHandler</span></span> | <span data-ttu-id="d52e8-519">Свойство для установки обработера событий по завершению `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-519">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="d52e8-520">свойство</span><span class="sxs-lookup"><span data-stu-id="d52e8-520">property</span></span>  
      
      | <span data-ttu-id="d52e8-521">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-521">Type</span></span> | <span data-ttu-id="d52e8-522">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-522">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-523">EventHandler</span><span class="sxs-lookup"><span data-stu-id="d52e8-523">EventHandler</span></span> | <span data-ttu-id="d52e8-524">Свойство для установки обработера событий при ошибке во время `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-524">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="d52e8-525">свойство</span><span class="sxs-lookup"><span data-stu-id="d52e8-525">property</span></span>  
      
      | <span data-ttu-id="d52e8-526">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-526">Type</span></span> | <span data-ttu-id="d52e8-527">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-527">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-528">Число</span><span class="sxs-lookup"><span data-stu-id="d52e8-528">Number</span></span> | <span data-ttu-id="d52e8-529">Представляет состояние асинхронной операции в приложении Windows с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d52e8-529">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="d52e8-530">Значения включают: `Started[0]` `Completed[1]` , , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-530">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="d52e8-531">свойство</span><span class="sxs-lookup"><span data-stu-id="d52e8-531">property</span></span>  
      
      | <span data-ttu-id="d52e8-532">Тип</span><span class="sxs-lookup"><span data-stu-id="d52e8-532">Type</span></span> | <span data-ttu-id="d52e8-533">Описание</span><span class="sxs-lookup"><span data-stu-id="d52e8-533">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="d52e8-534">Любой</span><span class="sxs-lookup"><span data-stu-id="d52e8-534">Any</span></span> |<span data-ttu-id="d52e8-535">Представляет результат `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="d52e8-535">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
