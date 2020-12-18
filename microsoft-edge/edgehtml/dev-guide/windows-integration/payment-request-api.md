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
# API платежного запроса (EdgeHTML)  

> [!NOTE]
> В этой статье описывается рабочий процесс, поддерживаемый в устаревшей [версии Microsoft Edge.][MicrosoftSupport44533505]  Microsoft Edge \(Chromium\) поддерживает API запроса платежей с другой реализацией на основе проекта Chromium.  

Продажи в электронной коммерции продолжают быстро расти.  Согласно [прогнозу eMarketer,](https://www.emarketer.com)к 2018 г. объем цифровых продаж увеличится на 23 % по сравнению с уровнями 2013 г.  Хотя потребители и компании пользуются удобством продаж электронной коммерции, проблемы остаются.  Сегодня каждый владелец веб-сайта электронной торговли должен уделять время разработке потоков и правил проверки для выверки платежей высокого качества.  Потребители должны переходить по различным потокам выгрузки платежей и повторно вводить одинаковые сведения об оплате и доставке на каждом сайте, где они купить.  Это может быть трудоемким и сложным для потребителей, что приводит к высокой скорости отказа от корзины и снижению продаж для продавцов.  По оценкам [продавцов,](http://baymard.com/lists/cart-abandonment-rate) от 60% до 70% корзины будут оставлены.  

[API платежного запроса](https://w3.org/TR/payment-request) стандартизирует процесс инауки платежа.  Этот API требует меньше настроек для веб-разработчиков и обеспечивает более быструю, согласованную и, следовательно, меньшую путаницу для потребителей.  Поскольку потребители могут выбирать платежные инструменты и адреса доставки из своей учетной записи Майкрософт, им необходимо вводить меньше данных для завершения покупок, что сокращает время и ввод данных, необходимые для выполнения платежа.  

[API](https://w3.org/TR/payment-request) запроса оплаты — это открытый кросс браузерный стандарт, который позволяет браузерам действовать в качестве посредника между продавцами, потребителями и методами оплаты \(например, кредитными картами\), которые потребители хранили в облаке.  
  
Таким образом, при использовании [API запроса платежей](https://w3.org/TR/payment-request)клиенты обычно используют веб-сайты продавца.  При готовности к оплате веб-сайт продавца **** вызывает **API** платежного запроса для создания платежного запроса и передает в браузер соответствующую информацию об оплате (например, поддерживаемые способы оплаты, сумму покупки, валюту и так далее).  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Конструкция платежного запроса" lightbox="../media/payment_request_construct.png":::
   Конструкция платежного запроса  
:::image-end:::  

Браузер аутентификация пользователя, позволяет пользователю выбрать поддерживаемый способ оплаты в файле и обрабатывает сведения об оплате.  Затем браузер отправляет сведения об оплате обратно на веб-сайт продавца, чтобы продавцу можно было завершить оплату.  Помимо получения платежных сведений, продавц также может выбрать получение сведений о доставке в составе **платежного запроса.**  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Конструкция ответа на платежи" lightbox="../media/payment_response_construct.png":::
   Конструкция ответа на платежи  
:::image-end:::  

Чтобы увидеть API платежного запроса в действии, а также получить обзор его использования, ознакомьтесь с этим видео.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> API платежного запроса поддерживается в Microsoft Edge сборки 14992 или более новой.  

## Создание платежного запроса  

Веб-страницы обычно создают **платежный** запрос, когда пользователь инициирует процесс оплаты, нажимая кнопку "купить".  Конструктор **платежного запроса** [включает](/previous-versions/mt790440(v=vs.85)) methodData, сведения и параметры.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

Параметр [methodData содержит](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) список методов и сетей оплаты, принятых веб-сайтом, и все связанные данные, связанные с методом оплаты.  В Microsoft Edge этот список соотнося с поддерживаемами методами оплаты, сохраненными покупателем в его учетной записи Майкрософт, и приводит к в списке "оплата" в пользовательском интерфейсе оплаты.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Оплата со списком в пользовательском интерфейсе Microsoft Wallet" lightbox="../media/pay_with.png":::
         Оплата **со списком** в пользовательском интерфейсе Microsoft Wallet  
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

Параметр [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) содержит сведения, которые продавц хочет передать клиенту о транзакции.  К ним относятся элементы сводки заказов, такие как общая сумма, налог, сумма отгрузки и другие элементы суммарной суммы, влияющие на сумму платежа.  Они не предназначены для заказа строки.  
  
Параметр [сведений](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) также используется для определения вариантов доставки, доступных клиенту при необходимости.  Дополнительные сведения см. ниже в **разделе "Платежный запрос** с доставкой".  

Каждая [строка](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) подробностей содержит метку валюты и суммы.  

> [!NOTE]
> Платежный **запрос** не вычисляет сумму или общую сумму этих сумм.  На веб-сайте продавца лежит ответственность за правильное соответствие строк.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Subtotal, shipping, taxes, and total details" lightbox="../media/show_details.png":::
         Subtotal, shipping, taxes, and total details  
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

[PaymentRequest](/previous-versions/mt790440(v=vs.85)) не поддерживает возврат средств, поэтому суммы всегда должны быть положительными; отдельные элементы списка могут быть отрицательными, например скидками.  

Браузер будет отрисовывал метки по мере их определения и автоматически отрисовывал правильное форматирование валюты в зависимости от региональных меток клиента.  Обратите внимание, что метки должны быть отрисовыты на том же языке, что и содержимое.  

Параметр [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) определяет данные, которые веб-страница хочет получить из **платежного запроса.**  Это также определяет данные, которые необходимо собрать, включая сведения о том, требуется ли доставка, адрес электронной почты, номер телефона или все они необходимы.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Dropdown email address dropdown" lightbox="../media/email_snippet.png":::
         Dropdown email address dropdown  
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

## Отображение платежного запроса  

Метод [show()](/previous-versions/mt790448(v=vs.85)) вызван веб-страницей, чтобы разрешить пользователю взаимодействовать с пользовательским интерфейсом **платежного** запроса.  Метод [show()](/previous-versions/mt790448(v=vs.85)) возвращает обещание, которое будет разрешено, когда пользователь авторизирует запрос на оплату.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Подтверждение и оплата сведений" lightbox="../media/pay_screen_default.png":::
         Подтверждение и оплата сведений  
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

## Прерывание платежного запроса  
 
Метод [abort()](/previous-versions/mt790437(v=vs.85)) может быть вызван веб-страницей в любое время после того, как будет вызван метод [show()](/previous-versions/mt790448(v=vs.85)) вплоть до точки разрешения обещания.  Метод [abort()](/previous-versions/mt790437(v=vs.85)) приведет к тому, что браузер оторват запрос **на** оплату и закроет пользовательский интерфейс **платежного** запроса.  Например, веб-страница может отменить операцию, если пользователь не завершил транзакцию в течение необходимого времени.  

```javascript
payment.abort();
```  

## Ответ на платежи  
Когда клиент утверждает **платежный**запрос, на веб-сайт возвращается ответ на платежи. ****  Ответ **на платежи** включает следующее:  

 Свойство      | Описание | Обязательный | Дополнительные сведения
|---------------|-----------------|-------|-----------------|
[methodName](/previous-versions/mt790656(v=vs.85)) | ИД метода оплаты, выбранного пользователем | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Объект JSON, который включает все данные, необходимые продавцу для обработки транзакции с помощью выбранного метода оплаты или маркера оплаты | Y | [Базовая карточка](https://w3c.github.io/payment-method-basic-card) Словарь: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
[shippingAddress](/previous-versions/mt790445(v=vs.85)) | Адрес доставки, выбранный пользователем  |  Необязательно.  Требуется, если [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True`  | Словарь адресов: страна; addressLine; регион; город; dependentLocality; postalCode; sortingCode; languageCode; организация; recipient; phone |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | ИД выбранного варианта доставки | Необязательно.  Требуется, если [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True`  | |   
[payerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Имя, предоставленное пользователем  | Необязательно.  Требуется, когда [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Адрес электронной почты, выбранный пользователем | Необязательно.  Требуется, когда [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | Номер телефона, выбранный пользователем | Необязательно.  Требуется, когда [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) `True` | |  

Объект [сведений](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON в **ответе на** платежи будет содержать платежные данные, необходимые продавцу для обработки платежа.  В простейшем виде ответом будет [](https://w3c.github.io/payment-method-basic-card) простая карточка, содержащая понятные данные карты оплаты.  Если у продавцов есть соглашения с дополнительными партнерами по шлюзам и процессорам для предоставления поддержки платежей, продавцу может потребоваться дополнительная нагрузка, с которой может справиться обработчик.  Они могут принимать форму маркера обработчика или шлюза или зашифрованного платежного инструмента.  Эти способы оплаты не являются частью этого документа и будут освещаться в документации для обработчика.  Кроме того, для [](https://w3c.github.io/payment-method-basic-card) получения ответа на базовую карточку разработчик не требует дополнительной входной нагрузки на Корпорацию Майкрософт, в отличие от других методов оплаты для процессора или шлюза, для которых может потребоваться встраивка ключа шифрования или авторизация запроса \(oAuth\).  

После получения **платежного ответа**веб-сайт передает платежные данные обработчику платежей.  Браузер отобразит вращаемую страницу во время обработки платежа.  

:::image type="complex" source="../media/loading_screen.png" alt-text="Страница, отображаемая при обработке платежа" lightbox="../media/loading_screen.png":::
   Страница, отображаемая при обработке платежа  
:::image-end:::  

После завершения оплаты веб-страница вызывает метод [complete()](/previous-versions/mt790642(v=vs.85)) и **** передает значение успешного или **неудачного завершения.**  Метод [complete()](/previous-versions/mt790642(v=vs.85)) сообщает браузеру о том, что покупка завершена и должен быть показан соответствующий завершающийся экран пользовательского интерфейса в зависимости от значения успешности или **** **неудачи.**  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Пользовательский интерфейс, отображаемой при успешном приобретении" lightbox="../media/response_payment-request_complete.png":::
         Пользовательский интерфейс, отображаемой при успешном приобретении  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Пользовательский интерфейс, отображаемой при сбойе покупки" lightbox="../media/response_payment-request_failure.png":::
         Пользовательский интерфейс, отображаемой при сбойе покупки  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Платежный запрос с доставкой  

### Адрес доставки  

Для продаж, которые требуют доставки физических товаров, требуется адрес доставки.  Чтобы включить адрес доставки, задан `requestShipping = True` параметр [параметров](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) запроса.  

Когда пользователь выбирает или обновляет адрес доставки, будет запускаться событие [onshippingaddresschange.](/previous-versions/mt790442(v=vs.85))  Веб-сайт, использующий прослушиватель событий, будет знать об изменении и сможет проверить адрес, пересчитать стоимость доставки и налоги, а также обновить [shippingOptions,](/previous-versions/mt790440(v=vs.85)) чтобы отразить измененные затраты и параметры доставки, доступные для выбранного адреса \(если применимо\).  

### Параметры доставки  

Параметры доставки можно представить клиенту, добавив [shippingOptions](/previous-versions/mt790440(v=vs.85)) в параметр [сведений.](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params)  Значение по умолчанию можно установить с помощью `selected = True` параметра для одного из вариантов доставки.  
 
Когда пользователь выбирает или обновляет shippingOptions, будет запускаться событие [onshippingoptionchange.](/previous-versions/mt790436(v=vs.85))  Веб-сайт, использующий прослушиватель событий, будет знать об изменении и может обновить параметр [сведений,](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) используя правильный объем отгрузки.  

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

## Справочник по API  

[API запроса оплаты](/previous-versions/mt790447(v=vs.85))  

## Спецификация
[API запроса оплаты](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Что такое Microsoft Edge Legacy?"  
