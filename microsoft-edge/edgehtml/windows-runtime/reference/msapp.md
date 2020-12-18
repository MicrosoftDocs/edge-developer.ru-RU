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
# <span data-ttu-id="cb456-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="cb456-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="cb456-106">Объект MSApp и его члены поддерживаются только для приложений для Windows с помощью JavaScript \(включая PWAs, которые имеют доступ к функциям API Windows\).</span><span class="sxs-lookup"><span data-stu-id="cb456-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="cb456-107">Объект MSApp существует только в локальном контексте HTML-документа в приложении для Windows, загружаемом с помощью схемы URI ms-appx; в противном случае объект не существует (и, следовательно, ни один из его методов и свойств не доступен).</span><span class="sxs-lookup"><span data-stu-id="cb456-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="cb456-108">Он предоставляет дополнительные функции, позволяющие создавать [объекты BLOB](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="cb456-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="cb456-109">Методы</span><span class="sxs-lookup"><span data-stu-id="cb456-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cb456-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="cb456-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cb456-111">Константы</span><span class="sxs-lookup"><span data-stu-id="cb456-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cb456-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="cb456-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cb456-113">Интерфейс MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="cb456-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="cb456-114">start</span><span class="sxs-lookup"><span data-stu-id="cb456-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="cb456-115">Методы MSApp</span><span class="sxs-lookup"><span data-stu-id="cb456-115">MSApp methods</span></span>  

### <span data-ttu-id="cb456-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="cb456-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-117">Очищает кэш и данные indexedDB для приложения или [WebView.](../../hosting/webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="cb456-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-118">Parameters</span></span>**  
      
      <span data-ttu-id="cb456-119">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb456-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-120">Return value</span></span>**  
      
      <span data-ttu-id="cb456-121">Тип: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="cb456-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="cb456-122">Представляет асинхронное действие.</span><span class="sxs-lookup"><span data-stu-id="cb456-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-123">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-123">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-125">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-127">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cb456-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="cb456-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-129">Создает большой объект [из](https://developer.mozilla.org/docs/Web/API/Blob) объекта [IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="cb456-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="cb456-130">Этот метод следует использовать при работе с объектами в приложениях, чтобы создать объект на основе `IRandomAccessStream` W3C из потока.</span><span class="sxs-lookup"><span data-stu-id="cb456-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="cb456-131">После создания BLOB-файл можно использовать с [FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API URL](https://developer.mozilla.org/docs/Web/API/URL)и [XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)</span><span class="sxs-lookup"><span data-stu-id="cb456-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-132">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="cb456-133">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-133">[in]</span></span>  
      
      | <span data-ttu-id="cb456-134">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-134">Type</span></span> | <span data-ttu-id="cb456-135">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-136">Строка</span><span class="sxs-lookup"><span data-stu-id="cb456-136">String</span></span> | <span data-ttu-id="cb456-137">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="cb456-137">Content type of the data.</span></span>  <span data-ttu-id="cb456-138">Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="cb456-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="cb456-139">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-139">[in]</span></span>  
      
      | <span data-ttu-id="cb456-140">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-140">Type</span></span> | <span data-ttu-id="cb456-141">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-142">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-142">Any</span></span> | <span data-ttu-id="cb456-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) для хранения в BLOB-хранилище.</span><span class="sxs-lookup"><span data-stu-id="cb456-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-144">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-145">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-145">Type</span></span> | <span data-ttu-id="cb456-146">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-147">BLOB</span><span class="sxs-lookup"><span data-stu-id="cb456-147">Blob</span></span> | <span data-ttu-id="cb456-148">Новый объект BLOB, содержащий поток.</span><span class="sxs-lookup"><span data-stu-id="cb456-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-149">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="cb456-150">Исключение</span><span class="sxs-lookup"><span data-stu-id="cb456-150">Exception</span></span> | <span data-ttu-id="cb456-151">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cb456-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="cb456-152">TypeMismatchError</span></span> | <span data-ttu-id="cb456-153">Тип узла несовместим с ожидаемым типом параметра.</span><span class="sxs-lookup"><span data-stu-id="cb456-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="cb456-154">Для версий, более ранних Internet Explorer 10, TYPE_MISMATCH_ERR возвращается.</span><span class="sxs-lookup"><span data-stu-id="cb456-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-155">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-156">Создает большой объект на основе типов времени запуска Windows через пространство имен MSApp в объекте window.</span><span class="sxs-lookup"><span data-stu-id="cb456-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="cb456-157">Этот метод создает большой объект, который, по сути, является оболочкой света для предоставленного ему объекта [RandomAccessStream.](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference)</span><span class="sxs-lookup"><span data-stu-id="cb456-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="cb456-158">Этот BLOB-бизнес владеет жизненным сроком существования этого потока, и поток будет закрыт при его уничтожении.</span><span class="sxs-lookup"><span data-stu-id="cb456-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-159">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-159">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="cb456-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-161">Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, к который можно получить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="cb456-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="cb456-163">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-163">[in]</span></span>  
      
      | <span data-ttu-id="cb456-164">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-164">Type</span></span> | <span data-ttu-id="cb456-165">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-166">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-166">Any</span></span> | <span data-ttu-id="cb456-167">Этот диапазон можно создать либо из объекта выделения, например: `window.selection.getRangeAt(0)` или вручную.</span><span class="sxs-lookup"><span data-stu-id="cb456-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-168">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-168">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-169">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-169">Type</span></span> | <span data-ttu-id="cb456-170">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-171">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-171">Any</span></span> | <span data-ttu-id="cb456-172">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="cb456-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-173">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-173">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-174">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-175">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-176">Этот метод поддерживает только [диапазон doM,](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)</span><span class="sxs-lookup"><span data-stu-id="cb456-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="cb456-177">Возвращенный пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="cb456-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="cb456-178">Для возвращенного пакета данных недоступны свойства.</span><span class="sxs-lookup"><span data-stu-id="cb456-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-179">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-179">Example</span></span>**  
      
      <span data-ttu-id="cb456-180">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cb456-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="cb456-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-182">Преобразует выбор пользователя или приложения в фрагмент HTML, к который можно получить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="cb456-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-183">Parameters</span></span>**  
      
      <span data-ttu-id="cb456-184">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb456-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-185">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-185">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-186">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-186">Type</span></span> | <span data-ttu-id="cb456-187">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-188">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-188">Any</span></span> | <span data-ttu-id="cb456-189">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="cb456-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-190">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-190">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-191">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-192">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-193">Возвращенный пакет данных для выбора содержит HTML-разметку в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="cb456-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="cb456-194">Если в пользовательском интерфейсе приложения нет выбора пользователя, `createDataPackageFromSelection` `null` возвращается.</span><span class="sxs-lookup"><span data-stu-id="cb456-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="cb456-195">Для возвращенного пакета данных недоступны свойства.</span><span class="sxs-lookup"><span data-stu-id="cb456-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-196">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="cb456-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="cb456-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-198">Преобразует [Файл Хранилища WinRT](/uwp/api/) [в](/uwp/api/windows.storage.storagefile) стандартный объект W3C [File.](https://developer.mozilla.org/docs/Web/API/File)</span><span class="sxs-lookup"><span data-stu-id="cb456-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-199">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="cb456-200">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-200">[in]</span></span>
      
      | <span data-ttu-id="cb456-201">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-201">Type</span></span> | <span data-ttu-id="cb456-202">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-203">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-203">Any</span></span> | <span data-ttu-id="cb456-204">Содержит файл хранилища.</span><span class="sxs-lookup"><span data-stu-id="cb456-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-205">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-205">Return value</span></span>**
      
      <span data-ttu-id="cb456-206">Нет</span><span class="sxs-lookup"><span data-stu-id="cb456-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-207">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="cb456-208">Исключение</span><span class="sxs-lookup"><span data-stu-id="cb456-208">Exception</span></span> | <span data-ttu-id="cb456-209">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cb456-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="cb456-210">TypeMismatchError</span></span> | <span data-ttu-id="cb456-211">Указанная ссылка на файл W3C недействительна.</span><span class="sxs-lookup"><span data-stu-id="cb456-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="cb456-212">Для версий, более ранних Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается.</span><span class="sxs-lookup"><span data-stu-id="cb456-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-213">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-213">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-214">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-215">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cb456-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="cb456-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-217">Создает [MSStream](https://msdn.microsoft.com/library/hh772328) из [InputStream.](https://msdn.microsoft.com/library/hh772327)</span><span class="sxs-lookup"><span data-stu-id="cb456-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-218">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="cb456-219">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-219">[in]</span></span>
      
      | <span data-ttu-id="cb456-220">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-220">Type</span></span> | <span data-ttu-id="cb456-221">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-222">DOMString</span></span> | <span data-ttu-id="cb456-223">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="cb456-223">Content type of the data.</span></span>  <span data-ttu-id="cb456-224">Эта строка должна быть в формате, указанном в маркере типа мультимедиа, определенном в разделе 3.7 RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="cb456-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="cb456-225">\([См. типы MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` `text/html` например, `image/jpeg` и `image/png` так `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` далее\).</span><span class="sxs-lookup"><span data-stu-id="cb456-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="cb456-226">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-226">[in]</span></span>
      
      | <span data-ttu-id="cb456-227">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-227">Type</span></span> | <span data-ttu-id="cb456-228">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-229">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-229">Any</span></span> | <span data-ttu-id="cb456-230">[IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) который будет храниться в `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="cb456-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-231">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-231">Return value</span></span>**
      
      <span data-ttu-id="cb456-232">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-233">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-233">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-234">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-235">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-235">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-236">Этот метод принимает тип контента и `IInputStream` ссылку.</span><span class="sxs-lookup"><span data-stu-id="cb456-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="cb456-237">Затем метод проверяет, является ли переданная ссылка потока экземпляром типа, и если `IInputStream` нет, выдает `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="cb456-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="cb456-238">Если ошибка не возникает, `createStreamFromInputStream` `MSStream` создается \(из его входных данных\).</span><span class="sxs-lookup"><span data-stu-id="cb456-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-239">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-239">Example</span></span>**  
      
      <span data-ttu-id="cb456-240">An `IInputStream` can be used to create an `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="cb456-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="cb456-241">Как и объекты, которые используются один раз, все созданные URL-адреса отзываются при первом их использовании `MSStreams` `URL.createObjectURL` элементом изображения.</span><span class="sxs-lookup"><span data-stu-id="cb456-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="cb456-242">Кроме того, запросы второго URL-адреса для этого объекта после использования потока будут неудались.</span><span class="sxs-lookup"><span data-stu-id="cb456-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <span data-ttu-id="cb456-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="cb456-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-244">Запланировать выполнение вызова позже в соответствии с заданным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="cb456-246">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-246">[in]</span></span>
      
      | <span data-ttu-id="cb456-247">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-247">Type</span></span> | <span data-ttu-id="cb456-248">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-249">Функция</span><span class="sxs-lookup"><span data-stu-id="cb456-249">Function</span></span> | <span data-ttu-id="cb456-250">Функция callback для асинхронного запуска, которая отправляется с заданным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="cb456-251">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-251">[in]</span></span>
      
      | <span data-ttu-id="cb456-252">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-252">Type</span></span> | <span data-ttu-id="cb456-253">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-254">DOMString</span></span> | <span data-ttu-id="cb456-255">Значение контекстного приоритета, при котором будет запускаться асинхронный вызовCallback.</span><span class="sxs-lookup"><span data-stu-id="cb456-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="cb456-256">См. ["Константы MSApp"](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="cb456-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="cb456-257">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-257">[in]</span></span>
      
      | <span data-ttu-id="cb456-258">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-258">Type</span></span> | <span data-ttu-id="cb456-259">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="cb456-260">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-260">Any</span></span> | <span data-ttu-id="cb456-261">Необязательный ряд аргументов, которые передаются в функцию вызова synchronousCallback \(в качестве параметров 1 и так далее\).</span><span class="sxs-lookup"><span data-stu-id="cb456-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-262">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-262">Return value</span></span>**  
      
      <span data-ttu-id="cb456-263">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb456-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-264">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-264">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-265">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-266">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-267">Предоставленная `asynchronousCallback` функция вызова выполняется асинхронно позже.</span><span class="sxs-lookup"><span data-stu-id="cb456-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="cb456-268">будет отправлено в соответствии с предоставленным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="cb456-269">Обычный приоритет эквивалентен существующему [методу setImmediate.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)</span><span class="sxs-lookup"><span data-stu-id="cb456-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="cb456-270">При выполнении этого вызова текущий контекстный приоритет устанавливается в качестве заданного значения параметра приоритета на время выполнения этого вызова.</span><span class="sxs-lookup"><span data-stu-id="cb456-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="cb456-271">Параметром `asynchronousCallback` callback может быть любая функция.</span><span class="sxs-lookup"><span data-stu-id="cb456-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="cb456-272">Если аргументы предоставляются после параметра, они все будут переданы функции `priority` вызова.</span><span class="sxs-lookup"><span data-stu-id="cb456-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="cb456-273">В отличие от этого, любой объект, возвращенный функцией обратного вызова, игнорируется и не возвращается `execAtPriority` `asynchronousCallback` через `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="cb456-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-274">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cb456-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="cb456-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-276">Запускает указанную функцию вызова с заданным контекстным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-277">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="cb456-278">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-278">[in]</span></span>  
      
      | <span data-ttu-id="cb456-279">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-279">Type</span></span> | <span data-ttu-id="cb456-280">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-281">Функция</span><span class="sxs-lookup"><span data-stu-id="cb456-281">Function</span></span> | <span data-ttu-id="cb456-282">Функция вызова для синхронного запуска с заданным контекстным приоритетом приоритета.</span><span class="sxs-lookup"><span data-stu-id="cb456-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="cb456-283">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-283">[in]</span></span>  
      
      | <span data-ttu-id="cb456-284">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-284">Type</span></span> | <span data-ttu-id="cb456-285">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-286">DOMString</span></span> | <span data-ttu-id="cb456-287">Указанное значение приоритета, для которого будет задано текущее значение контекстного приоритета при запуске функции `synchronousCallback` callback.</span><span class="sxs-lookup"><span data-stu-id="cb456-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="cb456-288">См. ["Константы MSApp"](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="cb456-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="cb456-289">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-289">[in]</span></span>  
      
      | <span data-ttu-id="cb456-290">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-290">Type</span></span> | <span data-ttu-id="cb456-291">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-292">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-292">Any</span></span> | <span data-ttu-id="cb456-293">Необязательный ряд аргументов, которые передаются функции вызова `synchronousCallback` \(в качестве параметров 1 и так далее\).</span><span class="sxs-lookup"><span data-stu-id="cb456-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-294">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-294">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-295">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-295">Type</span></span> | <span data-ttu-id="cb456-296">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-297">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-297">Any</span></span> | <span data-ttu-id="cb456-298">Возвращает возвращаемое значение обратного `synchronousCallback` вызова \(в соответствии с применимым\).</span><span class="sxs-lookup"><span data-stu-id="cb456-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-299">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-299">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-300">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-301">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-301">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-302">Предоставленный `synchronousCallback` метод вызова выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="cb456-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="cb456-303">Текущий контекстный приоритет меняется на предоставленное значение приоритета (заданное аргументом приоритета) на время действия предоставленной функции вызова.</span><span class="sxs-lookup"><span data-stu-id="cb456-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="cb456-304">После завершения выполнения функции обратного вызова приоритет возвращается предыдущему значению перед `execAtPriority` вызовом.</span><span class="sxs-lookup"><span data-stu-id="cb456-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="cb456-305">Возвращаемого значения является возвращаемого значения метода обратного `execAtPriority` вызова \(как предоставлено\).</span><span class="sxs-lookup"><span data-stu-id="cb456-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="cb456-306">Параметром `synchronousCallback` callback может быть любая функция.</span><span class="sxs-lookup"><span data-stu-id="cb456-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="cb456-307">Если какие-либо аргументы предоставляются после параметра приоритета, они будут переданы предоставленного метода вызова.</span><span class="sxs-lookup"><span data-stu-id="cb456-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="cb456-308">Если параметр обратного вызова возвращает значение, это значение также становится `execAtPriority` возвращаемой.</span><span class="sxs-lookup"><span data-stu-id="cb456-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-309">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-309">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="cb456-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-311">Возвращает текущий контекстный приоритет.</span><span class="sxs-lookup"><span data-stu-id="cb456-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-312">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-312">Parameters</span></span>**  
      
      <span data-ttu-id="cb456-313">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-314">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-314">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-315">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-315">Type</span></span> | <span data-ttu-id="cb456-316">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-317">DOMString</span></span> | <span data-ttu-id="cb456-318">Возвращаемого значения является одной из строк `MSApp.HIGH` `MSApp.NORMAL` , или `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="cb456-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-319">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-319">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-320">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-321">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-321">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-322">Этот метод возвращает текущий контекстный приоритет \(см. [msApp Constants](#msapp-constants)\), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="cb456-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-323">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-323">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="cb456-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="cb456-325">Неподготовленный синхронный API.</span><span class="sxs-lookup"><span data-stu-id="cb456-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="cb456-326">Для Windows 10 `getHtmlPrintDocumentSourceAsync` см. .</span><span class="sxs-lookup"><span data-stu-id="cb456-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="cb456-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="cb456-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="cb456-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="cb456-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-329">Возвращает исходный контент, который необходимо распечатать.</span><span class="sxs-lookup"><span data-stu-id="cb456-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-330">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="cb456-331">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-331">[in]</span></span>  
      
      | <span data-ttu-id="cb456-332">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-332">Type</span></span> | <span data-ttu-id="cb456-333">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-334">Документ</span><span class="sxs-lookup"><span data-stu-id="cb456-334">Document</span></span> | <span data-ttu-id="cb456-335">HtmL-документ для печати.</span><span class="sxs-lookup"><span data-stu-id="cb456-335">The HTML document to be printed.</span></span>  <span data-ttu-id="cb456-336">Это может быть корневой документ, документ в iframe, фрагмент документа или документ SVG.</span><span class="sxs-lookup"><span data-stu-id="cb456-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="cb456-337">Следует помнить, что htmlDoc должен быть документом, а не элементом.</span><span class="sxs-lookup"><span data-stu-id="cb456-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-338">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-338">Return value</span></span>**
      
      <span data-ttu-id="cb456-339">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-340">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-340">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-341">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-342">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-342">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-343">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-344">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb456-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="cb456-345">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb456-345">Example 2</span></span>**  
      
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

### <span data-ttu-id="cb456-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="cb456-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-347">Поддержка нескольких окон.</span><span class="sxs-lookup"><span data-stu-id="cb456-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="cb456-348">В приложениях UWP на JavaScript для Win8.1 поддерживалась поддержка нескольких окон с помощью API-API MSApp DOM, которые теперь не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="cb456-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="cb456-349">Для Windows 10 используйте `window.open` , `window` и новый `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="cb456-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="cb456-350">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-350">Description</span></span> |<span data-ttu-id="cb456-351">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="cb456-351">Windows 10</span></span> | <span data-ttu-id="cb456-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cb456-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="cb456-353">Создание нового окна</span><span class="sxs-lookup"><span data-stu-id="cb456-353">Create new window</span></span> | [<span data-ttu-id="cb456-354">window.open</span><span class="sxs-lookup"><span data-stu-id="cb456-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="cb456-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="cb456-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="cb456-356">Новый объект window</span><span class="sxs-lookup"><span data-stu-id="cb456-356">New window object</span></span> | [<span data-ttu-id="cb456-357">окно</span><span class="sxs-lookup"><span data-stu-id="cb456-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="cb456-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="cb456-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-359">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="cb456-360">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-360">Type</span></span> | <span data-ttu-id="cb456-361">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-362">DOMString</span></span> | <span data-ttu-id="cb456-363">Объект, представляющий окно, содержащее документ DOM.</span><span class="sxs-lookup"><span data-stu-id="cb456-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-364">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="cb456-365">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-365">Type</span></span> | <span data-ttu-id="cb456-366">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-367">Число</span><span class="sxs-lookup"><span data-stu-id="cb456-367">Number</span></span> | <span data-ttu-id="cb456-368">Можно использовать с различными [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="cb456-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-369">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-369">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-370">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-371">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-371">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-372">Используйте [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) и [window](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но затем для взаимодействия с API WinRT добавьте `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="cb456-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="cb456-373">Он принимает объект в качестве параметра и возвращает число, которое можно использовать с различными `window` `viewId` API [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="cb456-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="cb456-374">Задержка видимости</span><span class="sxs-lookup"><span data-stu-id="cb456-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="cb456-375">Представления в WinRT обычно начинаются скрытыми, и конечный разработчик использует что-то вроде отображения представления `TryShowAsStandaloneAsync` после его полной подготовки.</span><span class="sxs-lookup"><span data-stu-id="cb456-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="cb456-376">В веб-мире сразу же отображает окно, и конечный пользователь может наблюдать за загрузкой и отрисовке `window.open` содержимого.</span><span class="sxs-lookup"><span data-stu-id="cb456-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="cb456-377">Чтобы ваши новые окна отображались как представления в WinRT и не отображались сразу, мы добавили `window.open` параметр.</span><span class="sxs-lookup"><span data-stu-id="cb456-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="cb456-378">Например:</span><span class="sxs-lookup"><span data-stu-id="cb456-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="cb456-379">Отличия основного окна</span><span class="sxs-lookup"><span data-stu-id="cb456-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="cb456-380">Основное окно, которое изначально открывается операционной операцией, действует иначе, чем открывалось дополнительное окно:</span><span class="sxs-lookup"><span data-stu-id="cb456-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="cb456-381">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-381">Description</span></span> | <span data-ttu-id="cb456-382">Основной</span><span class="sxs-lookup"><span data-stu-id="cb456-382">Primary</span></span> | <span data-ttu-id="cb456-383">Дополнительная</span><span class="sxs-lookup"><span data-stu-id="cb456-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="cb456-384">window.open</span><span class="sxs-lookup"><span data-stu-id="cb456-384">window.open</span></span> | <span data-ttu-id="cb456-385">Разрешено</span><span class="sxs-lookup"><span data-stu-id="cb456-385">Allowed</span></span> | <span data-ttu-id="cb456-386">Disallowed</span><span class="sxs-lookup"><span data-stu-id="cb456-386">Disallowed</span></span> |  
          | <span data-ttu-id="cb456-387">window.close</span><span class="sxs-lookup"><span data-stu-id="cb456-387">window.close</span></span> | <span data-ttu-id="cb456-388">Закрыть приложение</span><span class="sxs-lookup"><span data-stu-id="cb456-388">Close app</span></span> | <span data-ttu-id="cb456-389">Закрыть окно</span><span class="sxs-lookup"><span data-stu-id="cb456-389">Close window</span></span> |  
          | <span data-ttu-id="cb456-390">Ограничения навигации</span><span class="sxs-lookup"><span data-stu-id="cb456-390">Navigation restrictions</span></span> | <span data-ttu-id="cb456-391">Только ACUR</span><span class="sxs-lookup"><span data-stu-id="cb456-391">ACUR only</span></span> | <span data-ttu-id="cb456-392">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="cb456-392">No restrictions</span></span> |  
          
          <span data-ttu-id="cb456-393">Ограничение на запрет открытия дополнительных окон может измениться в зависимости от [отзывов.](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)</span><span class="sxs-lookup"><span data-stu-id="cb456-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="cb456-394">Ограничения связи с одинаковым происхождением</span><span class="sxs-lookup"><span data-stu-id="cb456-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="cb456-395">Существует сложная техническая проблема, препятствуя правильной поддержке синхронных вызовов скриптов с одинаковым и одинаковым началом.</span><span class="sxs-lookup"><span data-stu-id="cb456-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="cb456-396">Когда вы открываете окно того же источника, сценарий в одном окне может напрямую вызывать функции в другом окне, и некоторые из этих вызовов не будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="cb456-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="cb456-397">вызовы работают нормально, и это рекомендуемый способ, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="cb456-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="cb456-398">Работа по улучшению этой проблемы продолжается.</span><span class="sxs-lookup"><span data-stu-id="cb456-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-399">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="cb456-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="cb456-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-401">Возвращает boolean значение, указывающее, есть ли ожидающих работ на заданном уровне приоритета или выше.</span><span class="sxs-lookup"><span data-stu-id="cb456-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-402">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="cb456-403">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-403">[in]</span></span>
      
      | <span data-ttu-id="cb456-404">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-404">Type</span></span> | <span data-ttu-id="cb456-405">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-406">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-406">DOMString</span></span> | <span data-ttu-id="cb456-407">Значение приоритета \(см. [MSApp Constants](#msapp-constants)\), указывающее уровень приоритета и выше для запроса любых непогашенных работ в очереди.</span><span class="sxs-lookup"><span data-stu-id="cb456-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-408">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-408">Return value</span></span>**  
      
      | <span data-ttu-id="cb456-409">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-409">Type</span></span> | <span data-ttu-id="cb456-410">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-411">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="cb456-411">Boolean</span></span> | <span data-ttu-id="cb456-412">Возвращает, есть ли в очереди какие-либо трудоемкие задачи на указанном уровне приоритета или выше, в противном `true` `false` случае.</span><span class="sxs-lookup"><span data-stu-id="cb456-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-413">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-413">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-414">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-415">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-415">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-416">Этот метод предоставляет коду JavaScript средства для определения того, есть ли ожидающих работ на различных уровнях приоритета \(или выше\) с целью того, чтобы вызывательный код JavaScript затем решил дать работу с более высоким `isTaskScheduledAtPriorityOrHigher` приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-417">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-417">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="cb456-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-419">Используется для предотвращения обновления пути начала (перезагрузки страницы) перед каждым событием активации (например, щелчок уведомления или закрепленная плитка\).</span><span class="sxs-lookup"><span data-stu-id="cb456-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-420">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-420">Parameters</span></span>**  
      
      | <span data-ttu-id="cb456-421">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-421">Type</span></span> | <span data-ttu-id="cb456-422">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-423">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="cb456-423">Boolean</span></span> | <span data-ttu-id="cb456-424">Используйте, чтобы всегда пропустить обновление пути начала (перезагрузка страницы) и перейти непосредственно к `MSApp.pageHandlesAllApplicationActivations(true)` запуску `WebUIApplication` активированного события.</span><span class="sxs-lookup"><span data-stu-id="cb456-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="cb456-425">Требует, чтобы все страницы обрабатывали события активации отдельно.</span><span class="sxs-lookup"><span data-stu-id="cb456-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="cb456-426">При определении этого метода как щелкнув активированное событие `true` \(например, уведомление\) не активирует перезагрузку, что является важным условием для одно страниц приложений, желающих избежать перезагрузок страниц.</span><span class="sxs-lookup"><span data-stu-id="cb456-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-427">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-427">Return value</span></span>**
      
      <span data-ttu-id="cb456-428">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-429">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-429">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-430">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-431">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-431">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-432">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-433">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-433">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="cb456-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-435">Управляет тем, подавляет ли приложение возможные запросы проверки подлинности во время скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb456-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-436">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="cb456-437">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-437">[in]</span></span>
      
      | <span data-ttu-id="cb456-438">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-438">Type</span></span> | <span data-ttu-id="cb456-439">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-440">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="cb456-440">Boolean</span></span> | <span data-ttu-id="cb456-441">Значение true подавляет потенциальные запросы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cb456-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="cb456-442">Значение false не подавляет потенциальные запросы проверки подлинности от пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb456-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-443">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-443">Return value</span></span>**  
      
      <span data-ttu-id="cb456-444">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-445">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-445">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-446">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-447">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-447">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-448">Этот метод управляет тем, подавляет ли приложение потенциальные запросы проверки подлинности `suppressSubdownloadCredentialPrompts` во время скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb456-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="cb456-449">По умолчанию запросы учетных данных не подавляются.</span><span class="sxs-lookup"><span data-stu-id="cb456-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="cb456-450">предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, которым требуется проверка подлинности, например почтовое приложение \(которое может содержать информационный бюллетень, содержащий несколько изображений, где каждое изображение требует проверки подлинности\).</span><span class="sxs-lookup"><span data-stu-id="cb456-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="cb456-451">При подавлении подсказок учетных данных диалоги для проверки подлинности на серверах не будут показаны при доступе к ресурсам, которые требуют проверки подлинности, и ресурс не будет загружен.</span><span class="sxs-lookup"><span data-stu-id="cb456-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="cb456-452">Обратите внимание, что это не влияет на другие возможные запросы, такие как проверка подлинности прокси-сервера или диалоговое окно запроса на сертификацию клиента, и не влияет на `suppressSubdownloadCredentialPrompts` XHR.</span><span class="sxs-lookup"><span data-stu-id="cb456-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="cb456-453">Следует помнить, `suppressSubdownloadCredentialPrompts` что влияет на все содержимое в приложении, включая контент, который был в `webview` элементе.</span><span class="sxs-lookup"><span data-stu-id="cb456-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="cb456-454">Решения о запросах учетных данных кэшются.</span><span class="sxs-lookup"><span data-stu-id="cb456-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="cb456-455">Таким образом, если запросы учетных данных не будут отбираться, запросы учетных данных после их подавления вступает в силу, поэтому может потребоваться перезагрузка документа.</span><span class="sxs-lookup"><span data-stu-id="cb456-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-456">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-456">Example</span></span>**  
      
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

### <span data-ttu-id="cb456-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="cb456-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-458">Завершает текущее приложение и создает отчет о сбое.</span><span class="sxs-lookup"><span data-stu-id="cb456-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-459">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="cb456-460">[in]</span><span class="sxs-lookup"><span data-stu-id="cb456-460">[in]</span></span>
      
      | <span data-ttu-id="cb456-461">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-461">Type</span></span> | <span data-ttu-id="cb456-462">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-463">Ошибка</span><span class="sxs-lookup"><span data-stu-id="cb456-463">Error</span></span> | <span data-ttu-id="cb456-464">Объект, `Error` который можно использовать для описания ошибки, которая вызвала завершение.</span><span class="sxs-lookup"><span data-stu-id="cb456-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="cb456-465">Объект должен содержать число, описание и свойства стека; отчет о сбое не будет создан, если объект не содержит `Error` эти свойства.</span><span class="sxs-lookup"><span data-stu-id="cb456-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-466">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-466">Return value</span></span>**
      
      <span data-ttu-id="cb456-467">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-468">Исключения</span><span class="sxs-lookup"><span data-stu-id="cb456-468">Exceptions</span></span>**  
      
      <span data-ttu-id="cb456-469">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-470">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb456-470">Remarks</span></span>**  
      
      <span data-ttu-id="cb456-471">Если проблема, о чем сообщили, становится одной из 5 главных проблем вашего приложения, она будет отдана на странице `terminateApp` "Качество" приложения.</span><span class="sxs-lookup"><span data-stu-id="cb456-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-472">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-472">Example</span></span>**  
      
      <span data-ttu-id="cb456-473">В этом `terminateApp` примере при вызове исключения вызывается.</span><span class="sxs-lookup"><span data-stu-id="cb456-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="cb456-474">Он использует `Error` объект, предоставленный при перехимовыыве исключение.</span><span class="sxs-lookup"><span data-stu-id="cb456-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <span data-ttu-id="cb456-475">Константы MSApp</span><span class="sxs-lookup"><span data-stu-id="cb456-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-476">Допустимые значения приоритета, связанные с `execAsyncAtPriority` `execAtPriority` , , и `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="cb456-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="cb456-477">Текущие</span><span class="sxs-lookup"><span data-stu-id="cb456-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="cb456-478">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-478">Type</span></span> | <span data-ttu-id="cb456-479">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-480">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-480">DOMString</span></span> | <span data-ttu-id="cb456-481">При использовании с соответствующим методом \(См. также раздел\), метод будет использовать текущий контекстный приоритет при `current` выполнении запрашиваемой операции.</span><span class="sxs-lookup"><span data-stu-id="cb456-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="cb456-482">Высока</span><span class="sxs-lookup"><span data-stu-id="cb456-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="cb456-483">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-483">Type</span></span> | <span data-ttu-id="cb456-484">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-485">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-485">DOMString</span></span> | <span data-ttu-id="cb456-486">При использовании с соответствующим методом \(См. также раздел\), метод будет использовать более высокий приоритет, чем обычный при выполнении запрашиваемой операции, и будет отправлять операцию перед любой существующей обычной работой `high` приоритета.</span><span class="sxs-lookup"><span data-stu-id="cb456-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="cb456-487">Состояние Idle (в покое)</span><span class="sxs-lookup"><span data-stu-id="cb456-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="cb456-488">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-488">Type</span></span> | <span data-ttu-id="cb456-489">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-490">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-490">DOMString</span></span> | <span data-ttu-id="cb456-491">При использовании с соответствующим методом \(См. также раздел\), метод будет использовать более низкий приоритет, чем обычный при выполнении запрашиваемой операции, и будет отправлять операцию после любой существующей обычной работы с `ideal` приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cb456-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="cb456-492">Обычный</span><span class="sxs-lookup"><span data-stu-id="cb456-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="cb456-493">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-493">Type</span></span> | <span data-ttu-id="cb456-494">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-495">DOMString</span><span class="sxs-lookup"><span data-stu-id="cb456-495">DOMString</span></span> | <span data-ttu-id="cb456-496">При использовании с соответствующим методом (см. также раздел), метод будет использовать обычный существующий приоритет при `normal` выполнении запрашиваемой операции.</span><span class="sxs-lookup"><span data-stu-id="cb456-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-497">Пример.</span><span class="sxs-lookup"><span data-stu-id="cb456-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-498">Требования</span><span class="sxs-lookup"><span data-stu-id="cb456-498">Requirements</span></span>**  
      
      | <span data-ttu-id="cb456-499">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-499">Type</span></span> | <span data-ttu-id="cb456-500">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-501">IDL</span><span class="sxs-lookup"><span data-stu-id="cb456-501">IDL</span></span> | <span data-ttu-id="cb456-502">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="cb456-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="cb456-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="cb456-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="cb456-504">start</span><span class="sxs-lookup"><span data-stu-id="cb456-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cb456-505">Запускает `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cb456-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cb456-506">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb456-506">Parameters</span></span>**  
      
      <span data-ttu-id="cb456-507">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cb456-508">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb456-508">Return value</span></span>**
      
      <span data-ttu-id="cb456-509">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb456-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="cb456-510">Свойства</span><span class="sxs-lookup"><span data-stu-id="cb456-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="cb456-511">свойство</span><span class="sxs-lookup"><span data-stu-id="cb456-511">property</span></span>  
      
      | <span data-ttu-id="cb456-512">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-512">Type</span></span> | <span data-ttu-id="cb456-513">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="cb456-514">DOMError</span></span> | <span data-ttu-id="cb456-515">Представляет ошибку в `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cb456-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="cb456-516">свойство</span><span class="sxs-lookup"><span data-stu-id="cb456-516">property</span></span>  
      
      | <span data-ttu-id="cb456-517">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-517">Type</span></span> | <span data-ttu-id="cb456-518">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="cb456-519">EventHandler</span></span> | <span data-ttu-id="cb456-520">Свойство для настройки обработера событий по завершении `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cb456-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="cb456-521">свойство</span><span class="sxs-lookup"><span data-stu-id="cb456-521">property</span></span>  
      
      | <span data-ttu-id="cb456-522">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-522">Type</span></span> | <span data-ttu-id="cb456-523">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="cb456-524">EventHandler</span></span> | <span data-ttu-id="cb456-525">Свойство для настройки обработера событий при ошибке во время `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cb456-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="cb456-526">свойство</span><span class="sxs-lookup"><span data-stu-id="cb456-526">property</span></span>  
      
      | <span data-ttu-id="cb456-527">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-527">Type</span></span> | <span data-ttu-id="cb456-528">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-529">Число</span><span class="sxs-lookup"><span data-stu-id="cb456-529">Number</span></span> | <span data-ttu-id="cb456-530">Представляет состояние асинхронной операции в приложении для Windows с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cb456-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="cb456-531">Значения: `Started[0]` , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="cb456-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="cb456-532">свойство</span><span class="sxs-lookup"><span data-stu-id="cb456-532">property</span></span>  
      
      | <span data-ttu-id="cb456-533">Тип</span><span class="sxs-lookup"><span data-stu-id="cb456-533">Type</span></span> | <span data-ttu-id="cb456-534">Описание</span><span class="sxs-lookup"><span data-stu-id="cb456-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cb456-535">Любой</span><span class="sxs-lookup"><span data-stu-id="cb456-535">Any</span></span> |<span data-ttu-id="cb456-536">Представляет результат `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cb456-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
