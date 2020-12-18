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
# <span data-ttu-id="a8ab3-104">Веб-проверка подлинности и Windows Hello</span><span class="sxs-lookup"><span data-stu-id="a8ab3-104">Web Authentication and Windows Hello</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="a8ab3-105">API веб-проверки подлинности в Microsoft Edge позволяет веб-приложениям использовать [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) и внешние устройства [](https://w3c.github.io/webauthn) [FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы вы и ваши пользователи могли избежать всех трудностей и рисков управления паролями, включая угадать пароль, фишинг и атаки с использованием журнала ключей.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span>  <span data-ttu-id="a8ab3-106">Текущая реализация Microsoft Edge основана на рекомендации кандидата спецификации веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a8ab3-107">В этом разделе покажем, как проверить проверку подлинности Windows Hello и FIDO2 с помощью Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>  

<span data-ttu-id="a8ab3-108">С помощью веб-проверки подлинности сервер отправляет браузеру задачу с простым текстом.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span>  <span data-ttu-id="a8ab3-109">После того как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подпишет задачу с помощью закрытого ключа, ранее заданной для этого пользователя, и отправит подпись обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span>  <span data-ttu-id="a8ab3-110">Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и проверить правильность задачи, он может безопасно проверить подлинность пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span>  <span data-ttu-id="a8ab3-111">При [асимметричном](https://en.wikipedia.org/wiki/Public-key_cryptography) шифровании, таком как этот, открытый ключ не имеет значения сам по себе, а закрытый ключ никогда не является общим.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span>  <span data-ttu-id="a8ab3-112">Кроме того, закрытый ключ никогда не может быть перемещен из безопасных элементов или современных систем с аппаратным обеспечением с поддержкой TPM.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>  

<span data-ttu-id="a8ab3-113">Существует два основных этапа использования API веб-проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-113">There are two basic steps to using the Web Authentication API:</span></span>  

1.  <span data-ttu-id="a8ab3-114">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="a8ab3-114">Register your user with</span></span> `create`  
1.  <span data-ttu-id="a8ab3-115">Проверка подлинности пользователя с помощью</span><span class="sxs-lookup"><span data-stu-id="a8ab3-115">Authenticate your user with</span></span> `get`  

<span data-ttu-id="a8ab3-116">В следующем руководстве разработчика вы пройдете этот поток с помощью примера приложения [WebAuthn.](https://github.com/MicrosoftEdge/webauthnsample)</span><span class="sxs-lookup"><span data-stu-id="a8ab3-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>  

## <span data-ttu-id="a8ab3-117">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="a8ab3-117">Register your user</span></span>  

<span data-ttu-id="a8ab3-118">Выступая в качестве поставщика удостоверений, сначала необходимо создать учетные данные веб-проверки подлинности для пользователя с помощью `navigator.credentials.create` этого метода.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-118">Acting as an identity provider, you will first need to create a Web Authentication credential for your user with the `navigator.credentials.create` method.</span></span>  <span data-ttu-id="a8ab3-119">Перед регистрацией этих учетных данных для пользователя на сервере необходимо подтвердить удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span>  <span data-ttu-id="a8ab3-120">Это можно сделать, отправив пользователю подтверждение по электронной почте или попросив его использовать традиционный метод входа.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>  

<span data-ttu-id="a8ab3-121">Метод `create` принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-121">The `create` method takes the following parameters:</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="a8ab3-122">сведения о считываемой стороне</span><span class="sxs-lookup"><span data-stu-id="a8ab3-122">relying party information</span></span>**  
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
      **<span data-ttu-id="a8ab3-123">сведения об учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="a8ab3-123">user account information</span></span>**  
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
      **<span data-ttu-id="a8ab3-124">параметры crypto</span><span class="sxs-lookup"><span data-stu-id="a8ab3-124">crypto parameters</span></span>**  
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
      **<span data-ttu-id="a8ab3-125">Параметры выбора аутентификации</span><span class="sxs-lookup"><span data-stu-id="a8ab3-125">authenticator selection parameters</span></span>**  
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
      **<span data-ttu-id="a8ab3-126">другие параметры</span><span class="sxs-lookup"><span data-stu-id="a8ab3-126">other options</span></span>**  
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

<span data-ttu-id="a8ab3-127">Для настройки [учетных](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) данных, которые необходимо создать, можно использовать параметры создания учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-127">You can use [credential creation parameters](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span>  <span data-ttu-id="a8ab3-128">В частности, вы можете создать учетные данные Windows Hello, задав для них значение или перемещая учетные данные на внешнем устройстве `authenticatorAttachment` `platform` FIDO2, задав `authenticatorAttachment` значение `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="a8ab3-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span>  

<span data-ttu-id="a8ab3-129">При использовании этого метода Microsoft Edge сначала попросит пользователя проверить свое присутствие, сканировав лицо или отпечаток пальца, введя ПИН-код или выйдя на внешнее устройство `create` FIDO2.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span>  <span data-ttu-id="a8ab3-130">После завершения этого шага аутентификация создает пару ключей publicprivate и сохраняет закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-130">Once this step is completed the authenticator will generate a publicprivate key pair and store the private key.</span></span>  <span data-ttu-id="a8ab3-131">Эти учетные данные создаются для каждого источника, учетной записи и не могут быть извлечены, так как они надежно хранятся на устройстве проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span>  

<span data-ttu-id="a8ab3-132">В результате обещание возвращает объект [аттестации,](https://w3c.github.io/webauthn#sctn-attestation) представляющий новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn#sctn-attestation) representing the new credential.</span></span>  <span data-ttu-id="a8ab3-133">Объект аттестации содержит открытый ключ для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-133">The attestation object contains the public key for the credential.</span></span>  <span data-ttu-id="a8ab3-134">Этот объект отправляется на сервер для проверки подлинности в будущем.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-134">You'll send this object to the server for validating future authentications.</span></span>  <span data-ttu-id="a8ab3-135">Перед отправкой обратно на сервер необходимо закодировать необработанные данные в коде base64.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>  

**<span data-ttu-id="a8ab3-136">Клиент</span><span class="sxs-lookup"><span data-stu-id="a8ab3-136">Client</span></span>**  

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

<span data-ttu-id="a8ab3-137">Затем сервер должен декодировать объект аттестации, выполнить проверку, извлечь открытый ключ для этих учетных данных и сохранить его для будущих проверок подлинности.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span>  <span data-ttu-id="a8ab3-138">Подробный список действий можно найти в алгоритме регистрации [учетных](https://w3c.github.io/webauthn#registering-a-new-credential) данных в спецификации WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn#registering-a-new-credential) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="a8ab3-139">Сервер</span><span class="sxs-lookup"><span data-stu-id="a8ab3-139">Server</span></span>**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## <span data-ttu-id="a8ab3-140">Проверка подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="a8ab3-140">Authenticate your user</span></span>  

<span data-ttu-id="a8ab3-141">После создания учетных данных на клиенте при следующей попытке пользователя войти на сайт можно предложить ему войти с помощью учетных данных веб-проверки подлинности вместо пароля с помощью вызова `navigator.credentials.get` .</span><span class="sxs-lookup"><span data-stu-id="a8ab3-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to `navigator.credentials.get`.</span></span>  

<span data-ttu-id="a8ab3-142">Метод `get` принимает задачу в качестве своего единственного обязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-142">The `get` method takes the challenge as its only required parameter.</span></span>  <span data-ttu-id="a8ab3-143">Проблема заключается в непрозрачной последовательности ветвей, которые сервер отправит клиенту для подписания с помощью закрытого ключа пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span>  <span data-ttu-id="a8ab3-144">Например:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-144">For example:</span></span>  

**<span data-ttu-id="a8ab3-145">Сервер</span><span class="sxs-lookup"><span data-stu-id="a8ab3-145">Server</span></span>**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

<span data-ttu-id="a8ab3-146">После получения запроса с сервера вызовите API get и параметры запроса [учетных данных.](https://w3c.github.io/webauthn#credentialrequestoptions-extension)</span><span class="sxs-lookup"><span data-stu-id="a8ab3-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn#credentialrequestoptions-extension).</span></span>  <span data-ttu-id="a8ab3-147">Microsoft Edge отведет запрос, который проверит личность пользователя с помощью Windows Hello или внешнего устройства FIDO2.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span>  <span data-ttu-id="a8ab3-148">После проверки пользователя задача будет подписана на устройстве TPM или FIDO2, а обещание вернет объект [assertion,](https://w3c.github.io/webauthn#authenticatorassertionresponse) содержащий подпись и другие метаданные для отправки на сервер.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>  

**<span data-ttu-id="a8ab3-149">Клиент</span><span class="sxs-lookup"><span data-stu-id="a8ab3-149">Client</span></span>**  

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

<span data-ttu-id="a8ab3-150">После получения утверждения на сервере необходимо проверить подпись для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span>  <span data-ttu-id="a8ab3-151">Ниже приводится пример кода.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-151">The following is some sample code.</span></span>  <span data-ttu-id="a8ab3-152">Подробный список действий можно найти в алгоритме проверки утверждений [в](https://w3c.github.io/webauthn#verifying-assertion) спецификации WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="a8ab3-153">Сервер</span><span class="sxs-lookup"><span data-stu-id="a8ab3-153">Server</span></span>**  

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

## <span data-ttu-id="a8ab3-154">Примечания по реализации</span><span class="sxs-lookup"><span data-stu-id="a8ab3-154">Implementation notes</span></span>  

### <span data-ttu-id="a8ab3-155">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="a8ab3-155">Supported platforms</span></span>  

*   <span data-ttu-id="a8ab3-156">Версию "Рекомендации кандидата" API веб-проверки подлинности можно использовать из Microsoft Edge, начиная с EdgeHTML 18 \(Windows Insider Preview версии 17713 или более новой\).</span><span class="sxs-lookup"><span data-stu-id="a8ab3-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 \(Windows Insider Preview version 17713 or newer\).</span></span>  
*   <span data-ttu-id="a8ab3-157">Префикс [предварительной](https://blogs.windows.com/msedgedev/2016/04/12) версии API веб-проверки подлинности удален и больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12) of the Web Authentication API has been removed and is no longer available.</span></span>  
*   <span data-ttu-id="a8ab3-158">API веб-проверки подлинности пока не доступен приложениям UWP и PWAS.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>  
*   <span data-ttu-id="a8ab3-159">Internet Explorer не поддерживает API веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-159">Internet Explorer does not support the Web Authentication API.</span></span>  

### <span data-ttu-id="a8ab3-160">Поддерживаемые аутентификация</span><span class="sxs-lookup"><span data-stu-id="a8ab3-160">Supported authenticators</span></span>  

<span data-ttu-id="a8ab3-161">С помощью API веб-проверки подлинности в Microsoft Edge можно проверить подлинность пользователей с помощью следующих технологий:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>  

*   <span data-ttu-id="a8ab3-162">**Windows Hello**  Включает проверку подлинности без пароля на устройстве с помощью лица, отпечатка пальца или ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a8ab3-162">**Windows Hello**  Enables passwordless on-device authentication with  face, fingerprint, or PIN</span></span>  
*   <span data-ttu-id="a8ab3-163">**FIDO2**  Включает проверку подлинности без пароля в роуминге со съемным устройством, отпечатком пальца или ПИН-кодом</span><span class="sxs-lookup"><span data-stu-id="a8ab3-163">**FIDO2**  Enables passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>  
*   <span data-ttu-id="a8ab3-164">**U2F**  Включает проверку подлинности со второго фактора для веб-сайтов, которые не готовы к переходу на модель без пароля</span><span class="sxs-lookup"><span data-stu-id="a8ab3-164">**U2F**  Enables strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>  

### <span data-ttu-id="a8ab3-165">Особые соображения по Windows Hello</span><span class="sxs-lookup"><span data-stu-id="a8ab3-165">Special considerations for Windows Hello</span></span>  

<span data-ttu-id="a8ab3-166">При использовании проверки подлинности Windows Hello следует обратить внимание на несколько моментов:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-166">A few things to note when using the Windows Hello authenticator:</span></span>  

*   <span data-ttu-id="a8ab3-167">Чтобы определить, доступна ли Windows Hello на компьютере, вы можете вызывать `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span>  <span data-ttu-id="a8ab3-168">Подробнее об этом API можно узнать [здесь.](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable)</span><span class="sxs-lookup"><span data-stu-id="a8ab3-168">Learn more about this API [here](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>  
*   <span data-ttu-id="a8ab3-169">При создании учетных данных для Windows Hello следует настроить для наилучшего `authenticatorAttachment` `platform` пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
*   <span data-ttu-id="a8ab3-170">Windows Hello поддерживает только RS256 \(alg -257\) в качестве алгоритма открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-170">Windows Hello only supports RS256 \(alg -257\) as its public key algorithm.</span></span>  <span data-ttu-id="a8ab3-171">Не забудьте указать этот алгоритм при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-171">Be sure to specify this algorithm when creating a credential.</span></span>  
*   <span data-ttu-id="a8ab3-172">Чтобы получить заявление [об attestation TPM,](https://w3c.github.io/webauthn#tpm-attestation)при вызове API установите для его получения "прямое". `create`</span><span class="sxs-lookup"><span data-stu-id="a8ab3-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span>  <span data-ttu-id="a8ab3-173">TPM attestation is a best effort.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-173">TPM attestation is a best effort.</span></span>  <span data-ttu-id="a8ab3-174">Только компьютеры с TPM 2.0 будут возвращать заявление об attestation TPM, и процесс проверки может привести к сбойу по ряду причин.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>  
*   <span data-ttu-id="a8ab3-175">Windows Hello использует различные способы защиты учетных данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-175">Windows Hello employs a variety of ways to protect user credentials.</span></span>  <span data-ttu-id="a8ab3-176">Вы можете проверить, какой метод использовался для защиты учетных данных, с помощью поля [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) в объекте аттестации, возвращаемом при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span>  <span data-ttu-id="a8ab3-177">Ниже приводится список AAGUID, которые может вернуть Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span>   
    *   <span data-ttu-id="a8ab3-178">Программные средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="a8ab3-178">Software backed authenticators</span></span>  
        *   <span data-ttu-id="a8ab3-179">Средство проверки подлинности программного обеспечения Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-179">Windows Hello software authenticator:</span></span>  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   <span data-ttu-id="a8ab3-180">Программный аутентификация Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-180">Windows Hello VBS software authenticator:</span></span>  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   <span data-ttu-id="a8ab3-181">Доверенный платформенного модуля \(TPM\) backed authenticators</span><span class="sxs-lookup"><span data-stu-id="a8ab3-181">Trusted Platform Module \(TPM\) backed authenticators</span></span>  
        *   <span data-ttu-id="a8ab3-182">Аппаратный аутентификация Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-182">Windows Hello hardware authenticator:</span></span>  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   <span data-ttu-id="a8ab3-183">Аппаратный аутентификация Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="a8ab3-183">Windows Hello VBS hardware authenticator:</span></span>  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### <span data-ttu-id="a8ab3-184">Поверхность API</span><span class="sxs-lookup"><span data-stu-id="a8ab3-184">API surface</span></span>  

*   <span data-ttu-id="a8ab3-185">В Microsoft Edge полностью внедрена версия "Рекомендации кандидата" основной спецификации веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>  
*   <span data-ttu-id="a8ab3-186">Расширение [AppID](https://w3c.github.io/webauthn#sctn-appid-extension) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-186">The [AppID extension](https://w3c.github.io/webauthn#sctn-appid-extension) is supported.</span></span>  
*   <span data-ttu-id="a8ab3-187">Другие расширения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a8ab3-187">No other extensions are supported.</span></span>  

## <span data-ttu-id="a8ab3-188">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="a8ab3-188">Demos</span></span>  

[<span data-ttu-id="a8ab3-189">Пример кода клиента и сервера</span><span class="sxs-lookup"><span data-stu-id="a8ab3-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)  

[<span data-ttu-id="a8ab3-190">Демонстрация тестового диска Windows Hello</span><span class="sxs-lookup"><span data-stu-id="a8ab3-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net)  

## <span data-ttu-id="a8ab3-191">Спецификация</span><span class="sxs-lookup"><span data-stu-id="a8ab3-191">Specification</span></span>  

[<span data-ttu-id="a8ab3-192">Веб-проверка подлинности: API для доступа к учетным данным открытого ключа</span><span class="sxs-lookup"><span data-stu-id="a8ab3-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn)  
