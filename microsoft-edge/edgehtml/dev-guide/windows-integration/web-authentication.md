---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Узнайте, как API веб-проверки подлинности позволяет веб-приложениям использовать Windows Hello и FIDO2 для проверки подлинности пользователей.
title: Веб-проверка подлинности — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 07f1de47156f43ff4726e8907a123c2cb1afc337
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235392"
---
# Веб-проверка подлинности и Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

API веб-проверки подлинности в Microsoft Edge позволяет веб-приложениям использовать [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) и внешние устройства [](https://w3c.github.io/webauthn) [FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы вы и ваши пользователи могли избежать всех трудностей и рисков управления паролями, включая угадать пароль, фишинг и атаки с использованием журнала ключей.  Текущая реализация Microsoft Edge основана на рекомендации кандидата спецификации веб-проверки подлинности.  

> [!IMPORTANT]
> В этом разделе покажем, как проверить проверку подлинности Windows Hello и FIDO2 с помощью Microsoft Edge.  

С помощью веб-проверки подлинности сервер отправляет браузеру задачу с простым текстом.  После того как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подпишет задачу с помощью закрытого ключа, ранее заданной для этого пользователя, и отправит подпись обратно на сервер.  Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и проверить правильность задачи, он может безопасно проверить подлинность пользователя.  При [асимметричном](https://en.wikipedia.org/wiki/Public-key_cryptography) шифровании, таком как этот, открытый ключ не имеет значения сам по себе, а закрытый ключ никогда не является общим.  Кроме того, закрытый ключ никогда не может быть перемещен из безопасных элементов или современных систем с аппаратным обеспечением с поддержкой TPM.  

Существует два основных этапа использования API веб-проверки подлинности:  

1.  Регистрация пользователя `create`  
1.  Проверка подлинности пользователя с помощью `get`  

В следующем руководстве разработчика вы пройдете этот поток с помощью примера приложения [WebAuthn.](https://github.com/MicrosoftEdge/webauthnsample)  

## Регистрация пользователя  

Выступая в качестве поставщика удостоверений, сначала необходимо создать учетные данные веб-проверки подлинности для пользователя с помощью `navigator.credentials.create` этого метода.  Перед регистрацией этих учетных данных для пользователя на сервере необходимо подтвердить удостоверение пользователя.  Это можно сделать, отправив пользователю подтверждение по электронной почте или попросив его использовать традиционный метод входа.  

Метод `create` принимает следующие параметры:  

:::row:::
   :::column span="1":::
      **сведения о считываемой стороне**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **сведения об учетной записи пользователя**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **параметры crypto**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      pubKeyCredParams: [
          {
              //External authenticators support the ES256 algorithm
              type: "public-key",
              alg: -7                 
          }, 
          {
              //Windows Hello supports the RS256 algorithm
              type: "public-key",
              alg: -257
          }
      ],
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Параметры выбора аутентификации**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **другие параметры**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      //Select larger timeout values, as Microsoft Edge shows UI
      timeout: 50000,
      //an opaque challenge that the authenticator signs over
      challenge: challenge,
      //prevent re-registration by specifying existing credentials here
      excludeCredentials: [],
      //specifies whether you need an attestation statement
      attestation: "none" 
      ```  
   :::column-end:::
:::row-end:::  

Для настройки [учетных](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) данных, которые необходимо создать, можно использовать параметры создания учетных данных.  В частности, вы можете создать учетные данные Windows Hello, задав для них значение или перемещая учетные данные на внешнем устройстве `authenticatorAttachment` `platform` FIDO2, задав `authenticatorAttachment` значение `cross-platform` .  

При использовании этого метода Microsoft Edge сначала попросит пользователя проверить свое присутствие, сканировав лицо или отпечаток пальца, введя ПИН-код или выйдя на внешнее устройство `create` FIDO2.  После завершения этого шага аутентификация создает пару ключей publicprivate и сохраняет закрытый ключ.  Эти учетные данные создаются для каждого источника, учетной записи и не могут быть извлечены, так как они надежно хранятся на устройстве проверки подлинности.  

В результате обещание возвращает объект [аттестации,](https://w3c.github.io/webauthn#sctn-attestation) представляющий новые учетные данные.  Объект аттестации содержит открытый ключ для учетных данных.  Этот объект отправляется на сервер для проверки подлинности в будущем.  Перед отправкой обратно на сервер необходимо закодировать необработанные данные в коде base64.  

**Клиент**  

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```  

Затем сервер должен декодировать объект аттестации, выполнить проверку, извлечь открытый ключ для этих учетных данных и сохранить его для будущих проверок подлинности.  Подробный список действий можно найти в алгоритме регистрации [учетных](https://w3c.github.io/webauthn#registering-a-new-credential) данных в спецификации WebAuthn.  

**Сервер**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Проверка подлинности пользователя  

После создания учетных данных на клиенте при следующей попытке пользователя войти на сайт можно предложить ему войти с помощью учетных данных веб-проверки подлинности вместо пароля с помощью вызова `navigator.credentials.get` .  

Метод `get` принимает задачу в качестве своего единственного обязательного параметра.  Проблема заключается в непрозрачной последовательности ветвей, которые сервер отправит клиенту для подписания с помощью закрытого ключа пользователя.  Например:  

**Сервер**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

После получения запроса с сервера вызовите API get и параметры запроса [учетных данных.](https://w3c.github.io/webauthn#credentialrequestoptions-extension)  Microsoft Edge отведет запрос, который проверит личность пользователя с помощью Windows Hello или внешнего устройства FIDO2.  После проверки пользователя задача будет подписана на устройстве TPM или FIDO2, а обещание вернет объект [assertion,](https://w3c.github.io/webauthn#authenticatorassertionresponse) содержащий подпись и другие метаданные для отправки на сервер.  

**Клиент**  

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```  

После получения утверждения на сервере необходимо проверить подпись для проверки подлинности пользователя.  Ниже приводится пример кода.  Подробный список действий можно найти в алгоритме проверки утверждений [в](https://w3c.github.io/webauthn#verifying-assertion) спецификации WebAuthn.  

**Сервер**  

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```  

## Примечания по реализации  

### Поддерживаемые платформы  

*   Версию "Рекомендации кандидата" API веб-проверки подлинности можно использовать из Microsoft Edge, начиная с EdgeHTML 18 \(Windows Insider Preview версии 17713 или более новой\).  
*   Префикс [предварительной](https://blogs.windows.com/msedgedev/2016/04/12) версии API веб-проверки подлинности удален и больше не доступен.  
*   API веб-проверки подлинности пока не доступен приложениям UWP и PWAS.  
*   Internet Explorer не поддерживает API веб-проверки подлинности.  

### Поддерживаемые аутентификация  

С помощью API веб-проверки подлинности в Microsoft Edge можно проверить подлинность пользователей с помощью следующих технологий:  

*   **Windows Hello**  Включает проверку подлинности без пароля на устройстве с помощью лица, отпечатка пальца или ПИН-кода  
*   **FIDO2**  Включает проверку подлинности без пароля в роуминге со съемным устройством, отпечатком пальца или ПИН-кодом  
*   **U2F**  Включает проверку подлинности со второго фактора для веб-сайтов, которые не готовы к переходу на модель без пароля  

### Особые соображения по Windows Hello  

При использовании проверки подлинности Windows Hello следует обратить внимание на несколько моментов:  

*   Чтобы определить, доступна ли Windows Hello на компьютере, вы можете вызывать `isUserVerifyingPlatformAuthenticatorAvailable` API.  Подробнее об этом API можно узнать [здесь.](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable)  
*   При создании учетных данных для Windows Hello следует настроить для наилучшего `authenticatorAttachment` `platform` пользовательского интерфейса.
*   Windows Hello поддерживает только RS256 \(alg -257\) в качестве алгоритма открытого ключа.  Не забудьте указать этот алгоритм при создании учетных данных.  
*   Чтобы получить заявление [об attestation TPM,](https://w3c.github.io/webauthn#tpm-attestation)при вызове API установите для его получения "прямое". `create`  TPM attestation is a best effort.  Только компьютеры с TPM 2.0 будут возвращать заявление об attestation TPM, и процесс проверки может привести к сбойу по ряду причин.  
*   Windows Hello использует различные способы защиты учетных данных пользователей.  Вы можете проверить, какой метод использовался для защиты учетных данных, с помощью поля [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) в объекте аттестации, возвращаемом при создании учетных данных.  Ниже приводится список AAGUID, которые может вернуть Windows Hello:   
    *   Программные средства проверки подлинности  
        *   Средство проверки подлинности программного обеспечения Windows Hello:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Программный аутентификация Windows Hello VBS:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   Доверенный платформенного модуля \(TPM\) backed authenticators  
        *   Аппаратный аутентификация Windows Hello:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Аппаратный аутентификация Windows Hello VBS:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### Поверхность API  

*   В Microsoft Edge полностью внедрена версия "Рекомендации кандидата" основной спецификации веб-проверки подлинности.  
*   Расширение [AppID](https://w3c.github.io/webauthn#sctn-appid-extension) поддерживается.  
*   Другие расширения не поддерживаются.  

## Демонстрационные примеры  

[Пример кода клиента и сервера](https://github.com/MicrosoftEdge/webauthnsample)  

[Демонстрация тестового диска Windows Hello](https://webauthnsample.azurewebsites.net)  

## Спецификация  

[Веб-проверка подлинности: API для доступа к учетным данным открытого ключа](http://w3c.github.io/webauthn)  
