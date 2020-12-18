---
description: Эмулировать аутентификацию и отладку WebAuthn в Microsoft Edge DevTools.
title: Эмуляция аутентификаций и отладка WebAuthn в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3200f22485bfd642a37a7d34ac727b8da4500d06
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231183"
---
# <span data-ttu-id="0bf9e-104">Эмуляция аутентификаций и отладка WebAuthn в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0bf9e-104">Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0bf9e-105">Вместо отладки веб-проверки подлинности на веб-сайте или в приложении с помощью физических средств проверки подлинности используйте средство **WebAuthn** в Microsoft Edge DevTools для создания виртуальных средств проверки подлинности на основе программного обеспечения и взаимодействия с ними.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-105">Instead of debugging Web Authentication in your website or app with physical authenticators, use the **WebAuthn** tool in Microsoft Edge DevTools to create and interact with software-based virtual authenticators.</span></span>  

## <span data-ttu-id="0bf9e-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0bf9e-106">Before you begin</span></span>  

<span data-ttu-id="0bf9e-107">Отличное место для начала работы с веб-проверкой подлинности — спецификация [API веб-проверки подлинности.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-107">A great place to get started with Web Authentication is the [Web Authentication API specification][GithubW3cWebauthn].</span></span>  

## <span data-ttu-id="0bf9e-108">Настройка средства WebAuthn</span><span class="sxs-lookup"><span data-stu-id="0bf9e-108">Set up the WebAuthn tool</span></span>  

1.  <span data-ttu-id="0bf9e-109">Перейдите на веб-страницу, использующую WebAuthn, например на следующем демонстрационном веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-109">Navigate to a webpage that uses WebAuthn, such as the following demo website.</span></span>  
    
    [<span data-ttu-id="0bf9e-110">webauthndemo.appspot.com</span><span class="sxs-lookup"><span data-stu-id="0bf9e-110">webauthndemo.appspot.com</span></span>][AppspotWebauthndemo]  
    
1.  <span data-ttu-id="0bf9e-111">Во sign into the website.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-111">Sign into the website.</span></span>  
1.  <span data-ttu-id="0bf9e-112">[Откройте DevTools.][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-112">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="0bf9e-113">Чтобы открыть **средство WebAuthn,** выберите значок "Настройка и управление **DevTools** \( \) > Другие средства `...` \*\*\*\*  >  **WebAuthn.**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-113">To open the **WebAuthn** tool, choose the **Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       <span data-ttu-id="0bf9e-115">**Средство WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-115">**WebAuthn** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0bf9e-116">В **средстве WebAuthn** включите проверку подлинности виртуальной **среды** проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-116">In the **WebAuthn** tool, turn on **Enable virtual authenticator environment** checkbox.</span></span>  
1.  <span data-ttu-id="0bf9e-117">После включения отображается новый раздел с именем **New authenticator.**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-117">After it is enabled, a new section named **New authenticator** is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Включить виртуальную среду проверки подлинности" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **<span data-ttu-id="0bf9e-119">Включить виртуальную среду проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="0bf9e-119">Enable virtual authenticator environment</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="0bf9e-120">В разделе **"Новый аутентификация"** настройте следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-120">In the **New authenticator** section, configure the following options.</span></span>  
    
    | <span data-ttu-id="0bf9e-121">Параметр</span><span class="sxs-lookup"><span data-stu-id="0bf9e-121">Option</span></span> | <span data-ttu-id="0bf9e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0bf9e-122">Value</span></span> | <span data-ttu-id="0bf9e-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="0bf9e-123">Details</span></span> |  
    |:--- |:--- |:--- |  
    | `Protocol` | <span data-ttu-id="0bf9e-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] или [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-124">[ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] or [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml]</span></span> | <span data-ttu-id="0bf9e-125">Протокол, который виртуальный аутентификация использует для кодировки и декодирования</span><span class="sxs-lookup"><span data-stu-id="0bf9e-125">The protocol the virtual authenticator uses for encoding and decoding</span></span> |  
    | `Transport` |   `usb`<span data-ttu-id="0bf9e-126">, `nfc` , `ble` , или</span><span class="sxs-lookup"><span data-stu-id="0bf9e-126">, `nfc`, `ble`, or</span></span> `internal` | <span data-ttu-id="0bf9e-127">Виртуальный аутентификация имитирует выбранный транспорт для связи с клиентами, чтобы получить утверждение для определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-127">The virtual authenticator simulates the selected transport for communicating with clients in order to obtain an assertion for a specific credential.</span></span>  <span data-ttu-id="0bf9e-128">Для получения дополнительных сведений перейдите к [transport Enumeration Authenticator][GithubW3cWebauthnEnumTransport]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-128">For more information, navigate to [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport]</span></span> |  
    |  `Supports resident keys` | <span data-ttu-id="0bf9e-129">Включите (или выключите\) с помощью этого контрольного списка</span><span class="sxs-lookup"><span data-stu-id="0bf9e-129">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="0bf9e-130">Включите, если ваше веб-приложение использует ключи-резиденты \(также известные как клиентские учетные данные для обнаружения\).</span><span class="sxs-lookup"><span data-stu-id="0bf9e-130">Turn on if your web app relies on resident keys \(also known as client-side discoverable credentials\).</span></span>  <span data-ttu-id="0bf9e-131">Для получения дополнительных сведений перейдите к [resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span><span class="sxs-lookup"><span data-stu-id="0bf9e-131">For more information, navigate to [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement].</span></span> |  
    | `Supports user verification` | <span data-ttu-id="0bf9e-132">Включите (или выключите\) с помощью этого контрольного списка</span><span class="sxs-lookup"><span data-stu-id="0bf9e-132">Turn on \(or off\) using the checkbox</span></span> | <span data-ttu-id="0bf9e-133">Включите, если в веб-приложении используется локальная авторизация с помощью таких модальностей жестов, как сенсорный ввод и код пин-кода, ввод пароля или биометрическое распознавание.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-133">Turn on if your web app relies on local authorization using gesture modalities like touch plus pin code, password entry, or biometric recognition.</span></span>  <span data-ttu-id="0bf9e-134">Для получения дополнительных сведений перейдите к [процедуре проверки пользователей][GithubW3cWebauthnEnumUserverification]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-134">For more information, navigate to [User Verification][GithubW3cWebauthnEnumUserverification]</span></span> |  
    
1.  <span data-ttu-id="0bf9e-135">Выберите **кнопку** "Добавить".</span><span class="sxs-lookup"><span data-stu-id="0bf9e-135">Choose the **Add** button.</span></span>  
1.  <span data-ttu-id="0bf9e-136">Отобразит новый раздел созданного аутентификацию.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-136">A new section of your newly created authenticator is displayed.</span></span>  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       <span data-ttu-id="0bf9e-138">Authenticator</span><span class="sxs-lookup"><span data-stu-id="0bf9e-138">Authenticator</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0bf9e-139">Раздел **Authenticator** содержит таблицу **учетных данных.**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-139">The **Authenticator** section includes a **Credentials** table.</span></span>  <span data-ttu-id="0bf9e-140">Таблица пуста до тех пор, пока учетные данные не будут зарегистрированы в аутентификацию.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-140">The table is empty until a credential is registered to the authenticator.</span></span>  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Без учетных данных" lightbox="../media/webauthn-no-cred.msft.png":::
   <span data-ttu-id="0bf9e-142">Без учетных данных</span><span class="sxs-lookup"><span data-stu-id="0bf9e-142">No credentials</span></span>  
:::image-end:::  

## <span data-ttu-id="0bf9e-143">Регистрация новых учетных данных</span><span class="sxs-lookup"><span data-stu-id="0bf9e-143">Register a new credential</span></span>  

<span data-ttu-id="0bf9e-144">Чтобы зарегистрировать новые учетные данные, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-144">To register a new credential, complete the following steps.</span></span>  <span data-ttu-id="0bf9e-145">Дополнительные сведения о том, что [делает API][GithubW3cWebauthn] веб-проверки подлинности при регистрации новых учетных данных, перейдите к странице ["Создание новых учетных данных".][GithubW3cWebauthnSctnCreatecredential]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-145">For more information about what the [Web Authentication API][GithubW3cWebauthn] is doing when registering a new credential, navigate to [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].</span></span>  

1.  <span data-ttu-id="0bf9e-146">На демонстрационных веб-сайтах выберите **"Регистрация новых учетных данных".**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-146">On the demo website, choose **Register new credential**.</span></span>  
1.  <span data-ttu-id="0bf9e-147">Новые учетные данные теперь добавляются в таблицу **Credentials** средства WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-147">A new credential is now added to the **Credentials** table in the WebAuthn tool.</span></span>  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Просмотр учетных данных" lightbox="../media/webauthn-view-cred.msft.png":::
       <span data-ttu-id="0bf9e-149">Просмотр учетных данных</span><span class="sxs-lookup"><span data-stu-id="0bf9e-149">View credentials</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0bf9e-150">На демонстрационных веб-сайтах выберите кнопку **"Проверка** подлинности".</span><span class="sxs-lookup"><span data-stu-id="0bf9e-150">On the demo website, choose the **Authenticate** button.</span></span>  <span data-ttu-id="0bf9e-151">Убедитесь, [что][GithubW3cWebauthnSctnSignCounter] число подписей учетных данных в таблице **учетных** данных увеличено на 1, что пометит успешную операцию [authenticatorGetAssertion.][GithubW3cWebauthnAuthenticatorgetassertion]</span><span class="sxs-lookup"><span data-stu-id="0bf9e-151">Verify that the [Sign Count][GithubW3cWebauthnSctnSignCounter] of the credential in the **Credentials** table increased by 1, which marks a successful [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] operation.</span></span>  

## <span data-ttu-id="0bf9e-152">Экспорт и удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="0bf9e-152">Export and remove credentials</span></span>  

<span data-ttu-id="0bf9e-153">Чтобы экспортировать или удалить учетные данные, выберите кнопку **"Экспорт"** или **"Удалить".**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-153">To export or remove a credential, choose the **Export** or **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Экспорт или удаление учетных данных" lightbox="../media/webauthn-export-remove.msft.png":::
   <span data-ttu-id="0bf9e-155">Экспорт или удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="0bf9e-155">Export or remove a credential</span></span>  
:::image-end:::  

## <span data-ttu-id="0bf9e-156">Переименование аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-156">Rename an authenticator</span></span>  

<span data-ttu-id="0bf9e-157">Чтобы переименовать аутентификацию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-157">To rename an authenticator, complete the following steps.</span></span>  

1.  <span data-ttu-id="0bf9e-158">Рядом с именем аутентификации выберите кнопку **"Изменить".**</span><span class="sxs-lookup"><span data-stu-id="0bf9e-158">Next to the authenticator name, choose the **Edit** button.</span></span>  
1.  <span data-ttu-id="0bf9e-159">Отредактируем имя, а затем выберите **ввод,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-159">Edit the name, then choose **Enter** to save the changes.</span></span>  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Переименование аутентификации" lightbox="../media/webauthn-rename.msft.png":::
   <span data-ttu-id="0bf9e-161">Переименование аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-161">Rename an authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="0bf9e-162">Настройка активного аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-162">Set the active authenticator</span></span>  

<span data-ttu-id="0bf9e-163">Автоматически активируется только что созданный аутентификация.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-163">A newly created authenticator is automatically activated.</span></span>  <span data-ttu-id="0bf9e-164">Чтобы использовать другой виртуальный аутентификацию, выберите **активную** кнопку радио рядом с аутентификацией.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-164">To use another virtual authenticator, choose the **Active** radio button next to the authenticator.</span></span>  

> [!NOTE]
> <span data-ttu-id="0bf9e-165">DevTools поддерживает только один активный виртуальный аутентификация в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-165">DevTools supports only one active virtual authenticator at any point of time.</span></span>  <span data-ttu-id="0bf9e-166">Если удалить активный аутентификацию, другой аутентификация не активируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-166">If you remove the active authenticator, another authenticator is not automatically activated.</span></span>  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Настройка активного аутентификации" lightbox="../media/webauthn-set-active.msft.png":::
   <span data-ttu-id="0bf9e-168">Настройка активного аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-168">Set active authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="0bf9e-169">Удаление виртуального аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-169">Remove a virtual authenticator</span></span>  

<span data-ttu-id="0bf9e-170">Чтобы удалить виртуальный аутентификацию, рядом \*\*\*\* с аутентификацией выберите кнопку "Удалить".</span><span class="sxs-lookup"><span data-stu-id="0bf9e-170">To remove a virtual authenticator, next to the authenticator, choose the **Remove** button.</span></span>  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Удаление аутентификации" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   <span data-ttu-id="0bf9e-172">Удаление аутентификации</span><span class="sxs-lookup"><span data-stu-id="0bf9e-172">Remove authenticator</span></span>  
:::image-end:::  

## <span data-ttu-id="0bf9e-173">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0bf9e-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Демонстрация веб-сайта | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Протокол CTAP | альянс fido"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Общие сведения о универсальном 2-м факторе (U2F) | альянс fido"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Операция authenticatorGetAssertion — веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeration transport Enumeration (enum AuthenticatorTransport) — веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Resident Key Requirement Enumeration (enum ResidentKeyRequirement) — веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Проверка пользователя — веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential's [[Create](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Вопросы счетчика подписей — веб-проверка подлинности: API для доступа к учетным данным открытого ключа 2 | GitHub"  

> [!NOTE]
> <span data-ttu-id="0bf9e-185">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0bf9e-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0bf9e-186">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/webauthn/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="0bf9e-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0bf9e-188">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0bf9e-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
