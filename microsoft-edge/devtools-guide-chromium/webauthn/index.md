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
# Эмуляция аутентификаций и отладка WebAuthn в Microsoft Edge DevTools  

Вместо отладки веб-проверки подлинности на веб-сайте или в приложении с помощью физических средств проверки подлинности используйте средство **WebAuthn** в Microsoft Edge DevTools для создания виртуальных средств проверки подлинности на основе программного обеспечения и взаимодействия с ними.  

## Перед началом работы  

Отличное место для начала работы с веб-проверкой подлинности — спецификация [API веб-проверки подлинности.][GithubW3cWebauthn]  

## Настройка средства WebAuthn  

1.  Перейдите на веб-страницу, использующую WebAuthn, например на следующем демонстрационном веб-сайте.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Во sign into the website.  
1.  [Откройте DevTools.][DevtoolsGuideChromiumOpen]  
1.  Чтобы открыть **средство WebAuthn,** выберите значок "Настройка и управление **DevTools** \( \) > Другие средства `...` ****  >  **WebAuthn.**  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Средство WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **Средство WebAuthn**  
    :::image-end:::  
    
1.  В **средстве WebAuthn** включите проверку подлинности виртуальной **среды** проверки подлинности.  
1.  После включения отображается новый раздел с именем **New authenticator.**  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Включить виртуальную среду проверки подлинности" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Включить виртуальную среду проверки подлинности**  
    :::image-end:::  
    
1.  В разделе **"Новый аутентификация"** настройте следующие параметры.  
    
    | Параметр | Значение | Сведения |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] или [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Протокол, который виртуальный аутентификация использует для кодировки и декодирования |  
    | `Transport` |   `usb`, `nfc` , `ble` , или `internal` | Виртуальный аутентификация имитирует выбранный транспорт для связи с клиентами, чтобы получить утверждение для определенных учетных данных.  Для получения дополнительных сведений перейдите к [transport Enumeration Authenticator][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Включите (или выключите\) с помощью этого контрольного списка | Включите, если ваше веб-приложение использует ключи-резиденты \(также известные как клиентские учетные данные для обнаружения\).  Для получения дополнительных сведений перейдите к [resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Включите (или выключите\) с помощью этого контрольного списка | Включите, если в веб-приложении используется локальная авторизация с помощью таких модальностей жестов, как сенсорный ввод и код пин-кода, ввод пароля или биометрическое распознавание.  Для получения дополнительных сведений перейдите к [процедуре проверки пользователей][GithubW3cWebauthnEnumUserverification] |  
    
1.  Выберите **кнопку** "Добавить".  
1.  Отобразит новый раздел созданного аутентификацию.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
Раздел **Authenticator** содержит таблицу **учетных данных.**  Таблица пуста до тех пор, пока учетные данные не будут зарегистрированы в аутентификацию.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Без учетных данных" lightbox="../media/webauthn-no-cred.msft.png":::
   Без учетных данных  
:::image-end:::  

## Регистрация новых учетных данных  

Чтобы зарегистрировать новые учетные данные, выполните следующие действия.  Дополнительные сведения о том, что [делает API][GithubW3cWebauthn] веб-проверки подлинности при регистрации новых учетных данных, перейдите к странице ["Создание новых учетных данных".][GithubW3cWebauthnSctnCreatecredential]  

1.  На демонстрационных веб-сайтах выберите **"Регистрация новых учетных данных".**  
1.  Новые учетные данные теперь добавляются в таблицу **Credentials** средства WebAuthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Просмотр учетных данных" lightbox="../media/webauthn-view-cred.msft.png":::
       Просмотр учетных данных  
    :::image-end:::  
    
На демонстрационных веб-сайтах выберите кнопку **"Проверка** подлинности".  Убедитесь, [что][GithubW3cWebauthnSctnSignCounter] число подписей учетных данных в таблице **учетных** данных увеличено на 1, что пометит успешную операцию [authenticatorGetAssertion.][GithubW3cWebauthnAuthenticatorgetassertion]  

## Экспорт и удаление учетных данных  

Чтобы экспортировать или удалить учетные данные, выберите кнопку **"Экспорт"** или **"Удалить".**  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Экспорт или удаление учетных данных" lightbox="../media/webauthn-export-remove.msft.png":::
   Экспорт или удаление учетных данных  
:::image-end:::  

## Переименование аутентификации  

Чтобы переименовать аутентификацию, выполните следующие действия.  

1.  Рядом с именем аутентификации выберите кнопку **"Изменить".**  
1.  Отредактируем имя, а затем выберите **ввод,** чтобы сохранить изменения.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Переименование аутентификации" lightbox="../media/webauthn-rename.msft.png":::
   Переименование аутентификации  
:::image-end:::  

## Настройка активного аутентификации  

Автоматически активируется только что созданный аутентификация.  Чтобы использовать другой виртуальный аутентификацию, выберите **активную** кнопку радио рядом с аутентификацией.  

> [!NOTE]
> DevTools поддерживает только один активный виртуальный аутентификация в любой момент времени.  Если удалить активный аутентификацию, другой аутентификация не активируется автоматически.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Настройка активного аутентификации" lightbox="../media/webauthn-set-active.msft.png":::
   Настройка активного аутентификации  
:::image-end:::  

## Удаление виртуального аутентификации  

Чтобы удалить виртуальный аутентификацию, рядом **** с аутентификацией выберите кнопку "Удалить".  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Удаление аутентификации" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Удаление аутентификации  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/webauthn/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
