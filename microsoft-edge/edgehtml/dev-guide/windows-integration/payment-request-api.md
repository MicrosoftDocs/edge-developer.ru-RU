---
description: Узнайте, как API запроса платежей позволяет Microsoft Edge действовать в качестве посредника между продавцами, потребителями и методами платежей потребителей, хранимыми в облаке.
title: API платежного запроса — руководство разработчика
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: efcad701fec73f858fa9490f12b094259cd8c793
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235393"
---
# <span data-ttu-id="7cbe5-104">API платежного запроса (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="7cbe5-105">В этой статье описывается рабочий процесс, поддерживаемый в устаревшей [версии Microsoft Edge.][MicrosoftSupport44533505]</span><span class="sxs-lookup"><span data-stu-id="7cbe5-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="7cbe5-106">Microsoft Edge \(Chromium\) поддерживает API запроса платежей с другой реализацией на основе проекта Chromium.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="7cbe5-107">Продажи в электронной коммерции продолжают быстро расти.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="7cbe5-108">Согласно [прогнозу eMarketer,](https://www.emarketer.com)к 2018 г. объем цифровых продаж увеличится на 23 % по сравнению с уровнями 2013 г.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="7cbe5-109">Хотя потребители и компании пользуются удобством продаж электронной коммерции, проблемы остаются.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="7cbe5-110">Сегодня каждый владелец веб-сайта электронной торговли должен уделять время разработке потоков и правил проверки для выверки платежей высокого качества.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="7cbe5-111">Потребители должны переходить по различным потокам выгрузки платежей и повторно вводить одинаковые сведения об оплате и доставке на каждом сайте, где они купить.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="7cbe5-112">Это может быть трудоемким и сложным для потребителей, что приводит к высокой скорости отказа от корзины и снижению продаж для продавцов.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="7cbe5-113">По оценкам [продавцов,](http://baymard.com/lists/cart-abandonment-rate) от 60% до 70% корзины будут оставлены.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="7cbe5-114">[API платежного запроса](https://w3.org/TR/payment-request) стандартизирует процесс инауки платежа.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="7cbe5-115">Этот API требует меньше настроек для веб-разработчиков и обеспечивает более быструю, согласованную и, следовательно, меньшую путаницу для потребителей.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="7cbe5-116">Поскольку потребители могут выбирать платежные инструменты и адреса доставки из своей учетной записи Майкрософт, им необходимо вводить меньше данных для завершения покупок, что сокращает время и ввод данных, необходимые для выполнения платежа.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="7cbe5-117">[API](https://w3.org/TR/payment-request) запроса оплаты — это открытый кросс браузерный стандарт, который позволяет браузерам действовать в качестве посредника между продавцами, потребителями и методами оплаты \(например, кредитными картами\), которые потребители хранили в облаке.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="7cbe5-118">Таким образом, при использовании [API запроса платежей](https://w3.org/TR/payment-request)клиенты обычно используют веб-сайты продавца.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="7cbe5-119">При готовности к оплате веб-сайт продавца \*\*\*\* вызывает **API** платежного запроса для создания платежного запроса и передает в браузер соответствующую информацию об оплате (например, поддерживаемые способы оплаты, сумму покупки, валюту и так далее).</span><span class="sxs-lookup"><span data-stu-id="7cbe5-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Конструкция платежного запроса" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="7cbe5-121">Конструкция платежного запроса</span><span class="sxs-lookup"><span data-stu-id="7cbe5-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="7cbe5-122">Браузер аутентификация пользователя, позволяет пользователю выбрать поддерживаемый способ оплаты в файле и обрабатывает сведения об оплате.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="7cbe5-123">Затем браузер отправляет сведения об оплате обратно на веб-сайт продавца, чтобы продавцу можно было завершить оплату.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="7cbe5-124">Помимо получения платежных сведений, продавц также может выбрать получение сведений о доставке в составе **платежного запроса.**</span><span class="sxs-lookup"><span data-stu-id="7cbe5-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Конструкция ответа на платежи" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="7cbe5-126">Конструкция ответа на платежи</span><span class="sxs-lookup"><span data-stu-id="7cbe5-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="7cbe5-127">Чтобы увидеть API платежного запроса в действии, а также получить обзор его использования, ознакомьтесь с этим видео.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="7cbe5-128">API платежного запроса поддерживается в Microsoft Edge сборки 14992 или более новой.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="7cbe5-129">Создание платежного запроса</span><span class="sxs-lookup"><span data-stu-id="7cbe5-129">Creating a Payment Request</span></span>  

<span data-ttu-id="7cbe5-130">Веб-страницы обычно создают **платежный** запрос, когда пользователь инициирует процесс оплаты, нажимая кнопку "купить".</span><span class="sxs-lookup"><span data-stu-id="7cbe5-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="7cbe5-131">Конструктор **платежного запроса** [включает](/previous-versions/mt790440(v=vs.85)) methodData, сведения и параметры.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="7cbe5-132">Параметр [methodData содержит](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) список методов и сетей оплаты, принятых веб-сайтом, и все связанные данные, связанные с методом оплаты.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="7cbe5-133">В Microsoft Edge этот список соотнося с поддерживаемами методами оплаты, сохраненными покупателем в его учетной записи Майкрософт, и приводит к в списке "оплата" в пользовательском интерфейсе оплаты.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Оплата со списком в пользовательском интерфейсе Microsoft Wallet" lightbox="../media/pay_with.png":::
         <span data-ttu-id="7cbe5-135">Оплата **со списком** в пользовательском интерфейсе Microsoft Wallet</span><span class="sxs-lookup"><span data-stu-id="7cbe5-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7cbe5-136">Параметр [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) содержит сведения, которые продавц хочет передать клиенту о транзакции.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="7cbe5-137">К ним относятся элементы сводки заказов, такие как общая сумма, налог, сумма отгрузки и другие элементы суммарной суммы, влияющие на сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="7cbe5-138">Они не предназначены для заказа строки.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="7cbe5-139">Параметр [сведений](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) также используется для определения вариантов доставки, доступных клиенту при необходимости.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="7cbe5-140">Дополнительные сведения см. ниже в **разделе "Платежный запрос** с доставкой".</span><span class="sxs-lookup"><span data-stu-id="7cbe5-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="7cbe5-141">Каждая [строка](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) подробностей содержит метку валюты и суммы.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cbe5-142">Платежный **запрос** не вычисляет сумму или общую сумму этих сумм.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="7cbe5-143">На веб-сайте продавца лежит ответственность за правильное соответствие строк.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Subtotal, shipping, taxes, and total details" lightbox="../media/show_details.png":::
         <span data-ttu-id="7cbe5-145">Subtotal, shipping, taxes, and total details</span><span class="sxs-lookup"><span data-stu-id="7cbe5-145">Subtotal, shipping, taxes, and total details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var details = {
          total: {
              label: 'Total (USD)',
              amount: {currency: 'USD', value: '193.98'}
          },
          displayItems: [{
                  label: 'Subtotal',
                  amount: {currency: 'USD', value: '174.99'}
              }, {
                  label: 'Taxes',
                  amount: {currency: "USD", value: '18.99'}
          }],
      };  
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7cbe5-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) не поддерживает возврат средств, поэтому суммы всегда должны быть положительными; отдельные элементы списка могут быть отрицательными, например скидками.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="7cbe5-147">Браузер будет отрисовывал метки по мере их определения и автоматически отрисовывал правильное форматирование валюты в зависимости от региональных меток клиента.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="7cbe5-148">Обратите внимание, что метки должны быть отрисовыты на том же языке, что и содержимое.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="7cbe5-149">Параметр [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) определяет данные, которые веб-страница хочет получить из **платежного запроса.**</span><span class="sxs-lookup"><span data-stu-id="7cbe5-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="7cbe5-150">Это также определяет данные, которые необходимо собрать, включая сведения о том, требуется ли доставка, адрес электронной почты, номер телефона или все они необходимы.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Dropdown email address dropdown" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="7cbe5-152">Dropdown email address dropdown</span><span class="sxs-lookup"><span data-stu-id="7cbe5-152">Email address dropdown</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7cbe5-153">Отображение платежного запроса</span><span class="sxs-lookup"><span data-stu-id="7cbe5-153">Showing the Payment Request</span></span>  

<span data-ttu-id="7cbe5-154">Метод [show()](/previous-versions/mt790448(v=vs.85)) вызван веб-страницей, чтобы разрешить пользователю взаимодействовать с пользовательским интерфейсом **платежного** запроса.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="7cbe5-155">Метод [show()](/previous-versions/mt790448(v=vs.85)) возвращает обещание, которое будет разрешено, когда пользователь авторизирует запрос на оплату.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Подтверждение и оплата сведений" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="7cbe5-157">Подтверждение и оплата сведений</span><span class="sxs-lookup"><span data-stu-id="7cbe5-157">Confirm and pay details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7cbe5-158">Прерывание платежного запроса</span><span class="sxs-lookup"><span data-stu-id="7cbe5-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="7cbe5-159">Метод [abort()](/previous-versions/mt790437(v=vs.85)) может быть вызван веб-страницей в любое время после того, как будет вызван метод [show()](/previous-versions/mt790448(v=vs.85)) вплоть до точки разрешения обещания.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="7cbe5-160">Метод [abort()](/previous-versions/mt790437(v=vs.85)) приведет к тому, что браузер оторват запрос **на** оплату и закроет пользовательский интерфейс **платежного** запроса.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="7cbe5-161">Например, веб-страница может отменить операцию, если пользователь не завершил транзакцию в течение необходимого времени.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="7cbe5-162">Ответ на платежи</span><span class="sxs-lookup"><span data-stu-id="7cbe5-162">Payment Response</span></span>  
<span data-ttu-id="7cbe5-163">Когда клиент утверждает **платежный**запрос, на веб-сайт возвращается ответ на платежи. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7cbe5-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="7cbe5-164">Ответ **на платежи** включает следующее:</span><span class="sxs-lookup"><span data-stu-id="7cbe5-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="7cbe5-165">Свойство</span><span class="sxs-lookup"><span data-stu-id="7cbe5-165">Property</span></span>      | <span data-ttu-id="7cbe5-166">Описание</span><span class="sxs-lookup"><span data-stu-id="7cbe5-166">Description</span></span> | <span data-ttu-id="7cbe5-167">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7cbe5-167">Required</span></span> | <span data-ttu-id="7cbe5-168">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7cbe5-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="7cbe5-169">methodName</span><span class="sxs-lookup"><span data-stu-id="7cbe5-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="7cbe5-170">ИД метода оплаты, выбранного пользователем</span><span class="sxs-lookup"><span data-stu-id="7cbe5-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="7cbe5-171">Y</span><span class="sxs-lookup"><span data-stu-id="7cbe5-171">Y</span></span> | |   
[<span data-ttu-id="7cbe5-172">details</span><span class="sxs-lookup"><span data-stu-id="7cbe5-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="7cbe5-173">Объект JSON, который включает все данные, необходимые продавцу для обработки транзакции с помощью выбранного метода оплаты или маркера оплаты</span><span class="sxs-lookup"><span data-stu-id="7cbe5-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="7cbe5-174">Y</span><span class="sxs-lookup"><span data-stu-id="7cbe5-174">Y</span></span> | <span data-ttu-id="7cbe5-175">[Базовая карточка](https://w3c.github.io/payment-method-basic-card) Словарь: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="7cbe5-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="7cbe5-176">shippingAddress</span><span class="sxs-lookup"><span data-stu-id="7cbe5-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="7cbe5-177">Адрес доставки, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="7cbe5-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="7cbe5-178">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-178">Optional.</span></span>  <span data-ttu-id="7cbe5-179">Требуется, если [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="7cbe5-180">Словарь адресов: страна; addressLine; регион; город; dependentLocality; postalCode; sortingCode; languageCode; организация; recipient; phone</span><span class="sxs-lookup"><span data-stu-id="7cbe5-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="7cbe5-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="7cbe5-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="7cbe5-182">ИД выбранного варианта доставки</span><span class="sxs-lookup"><span data-stu-id="7cbe5-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="7cbe5-183">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-183">Optional.</span></span>  <span data-ttu-id="7cbe5-184">Требуется, если [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="7cbe5-185">payerName</span><span class="sxs-lookup"><span data-stu-id="7cbe5-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="7cbe5-186">Имя, предоставленное пользователем</span><span class="sxs-lookup"><span data-stu-id="7cbe5-186">The name provided by the user</span></span>  | <span data-ttu-id="7cbe5-187">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-187">Optional.</span></span>  <span data-ttu-id="7cbe5-188">Требуется, когда [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="7cbe5-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="7cbe5-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="7cbe5-190">Адрес электронной почты, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="7cbe5-190">The email address selected by the user</span></span> | <span data-ttu-id="7cbe5-191">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-191">Optional.</span></span>  <span data-ttu-id="7cbe5-192">Требуется, когда [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="7cbe5-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="7cbe5-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="7cbe5-194">Номер телефона, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="7cbe5-194">The phone number selected by the user</span></span> | <span data-ttu-id="7cbe5-195">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-195">Optional.</span></span>  <span data-ttu-id="7cbe5-196">Требуется, когда [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="7cbe5-197">Объект [сведений](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON в **ответе на** платежи будет содержать платежные данные, необходимые продавцу для обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="7cbe5-198">В простейшем виде ответом будет [](https://w3c.github.io/payment-method-basic-card) простая карточка, содержащая понятные данные карты оплаты.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="7cbe5-199">Если у продавцов есть соглашения с дополнительными партнерами по шлюзам и процессорам для предоставления поддержки платежей, продавцу может потребоваться дополнительная нагрузка, с которой может справиться обработчик.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="7cbe5-200">Они могут принимать форму маркера обработчика или шлюза или зашифрованного платежного инструмента.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="7cbe5-201">Эти способы оплаты не являются частью этого документа и будут освещаться в документации для обработчика.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="7cbe5-202">Кроме того, для [](https://w3c.github.io/payment-method-basic-card) получения ответа на базовую карточку разработчик не требует дополнительной входной нагрузки на Корпорацию Майкрософт, в отличие от других методов оплаты для процессора или шлюза, для которых может потребоваться встраивка ключа шифрования или авторизация запроса \(oAuth\).</span><span class="sxs-lookup"><span data-stu-id="7cbe5-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="7cbe5-203">После получения **платежного ответа**веб-сайт передает платежные данные обработчику платежей.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="7cbe5-204">Браузер отобразит вращаемую страницу во время обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="Страница, отображаемая при обработке платежа" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="7cbe5-206">Страница, отображаемая при обработке платежа</span><span class="sxs-lookup"><span data-stu-id="7cbe5-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="7cbe5-207">После завершения оплаты веб-страница вызывает метод [complete()](/previous-versions/mt790642(v=vs.85)) и \*\*\*\* передает значение успешного или **неудачного завершения.**</span><span class="sxs-lookup"><span data-stu-id="7cbe5-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="7cbe5-208">Метод [complete()](/previous-versions/mt790642(v=vs.85)) сообщает браузеру о том, что покупка завершена и должен быть показан соответствующий завершающийся экран пользовательского интерфейса в зависимости от значения успешности или \*\*\*\* **неудачи.**</span><span class="sxs-lookup"><span data-stu-id="7cbe5-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Пользовательский интерфейс, отображаемой при успешном приобретении" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="7cbe5-210">Пользовательский интерфейс, отображаемой при успешном приобретении</span><span class="sxs-lookup"><span data-stu-id="7cbe5-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Пользовательский интерфейс, отображаемой при сбойе покупки" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="7cbe5-212">Пользовательский интерфейс, отображаемой при сбойе покупки</span><span class="sxs-lookup"><span data-stu-id="7cbe5-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7cbe5-213">Платежный запрос с доставкой</span><span class="sxs-lookup"><span data-stu-id="7cbe5-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="7cbe5-214">Адрес доставки</span><span class="sxs-lookup"><span data-stu-id="7cbe5-214">Shipping Address</span></span>  

<span data-ttu-id="7cbe5-215">Для продаж, которые требуют доставки физических товаров, требуется адрес доставки.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="7cbe5-216">Чтобы включить адрес доставки, задан `requestShipping = True` параметр [параметров](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) запроса.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="7cbe5-217">Когда пользователь выбирает или обновляет адрес доставки, будет запускаться событие [onshippingaddresschange.](/previous-versions/mt790442(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cbe5-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="7cbe5-218">Веб-сайт, использующий прослушиватель событий, будет знать об изменении и сможет проверить адрес, пересчитать стоимость доставки и налоги, а также обновить [shippingOptions,](/previous-versions/mt790440(v=vs.85)) чтобы отразить измененные затраты и параметры доставки, доступные для выбранного адреса \(если применимо\).</span><span class="sxs-lookup"><span data-stu-id="7cbe5-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="7cbe5-219">Параметры доставки</span><span class="sxs-lookup"><span data-stu-id="7cbe5-219">Shipping Options</span></span>  

<span data-ttu-id="7cbe5-220">Параметры доставки можно представить клиенту, добавив [shippingOptions](/previous-versions/mt790440(v=vs.85)) в параметр [сведений.](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params)</span><span class="sxs-lookup"><span data-stu-id="7cbe5-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="7cbe5-221">Значение по умолчанию можно установить с помощью `selected = True` параметра для одного из вариантов доставки.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="7cbe5-222">Когда пользователь выбирает или обновляет shippingOptions, будет запускаться событие [onshippingoptionchange.](/previous-versions/mt790436(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cbe5-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="7cbe5-223">Веб-сайт, использующий прослушиватель событий, будет знать об изменении и может обновить параметр [сведений,](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) используя правильный объем отгрузки.</span><span class="sxs-lookup"><span data-stu-id="7cbe5-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

```javascript
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
```  

## <span data-ttu-id="7cbe5-224">Справочник по API</span><span class="sxs-lookup"><span data-stu-id="7cbe5-224">API Reference</span></span>  

[<span data-ttu-id="7cbe5-225">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="7cbe5-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="7cbe5-226">Спецификация</span><span class="sxs-lookup"><span data-stu-id="7cbe5-226">Specification</span></span>
[<span data-ttu-id="7cbe5-227">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="7cbe5-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Что такое Microsoft Edge Legacy?"  
