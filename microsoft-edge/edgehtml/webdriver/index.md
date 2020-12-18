---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Узнайте, как начать работу с WebDriver, проводным протоколом, который позволяет программам и сценариям управлять поведением веб-браузера.
title: WebDriver (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: edge, веб-разработка, html, css, javascript, разработчик, webdriver, selenium, тестирование
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab26931c09ecbae41ae88734b25038d21c93c0f6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235483"
---
# WebDriver (EdgeHTML)

API-интерфейс [W3C WebDriver](https://www.w3.org/TR/webdriver/) — это неотвеязающий от языка интерфейс и протокол провода, позволяющий программам или сценариям управлять поведением веб-браузера.

WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие с пользователем. Это отличается от unit tests JavaScript, так как WebDriver имеет доступ к функциям и сведениям, которые JavaScript, запущенный в браузере, не имеет, и он может более точно имитировать события пользователя или события на уровне ОС. WebDriver также может управлять тестированием в нескольких окнах, вкладок и веб-страницы в одном тестовом сеансе.

Вот как начать работу с WebDriver для Microsoft Edge (EdgeHTML).

Реализация [WebDriver](https://www.w3.org/TR/webdriver/) в Microsoft Edge (EdgeHTML) поддерживает спецификацию W3C WebDriver и [протокол JSON Wire для](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) обратной совместимости с существующими тестами.

## Начало работы с WebDriver для Microsoft Edge (EdgeHTML)
* Установите Windows 10.
* Скачайте [соответствующий сервер Microsoft WebDriver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) для сборки Windows и Microsoft Edge (EdgeHTML).
* Скачайте языковую привязку WebDriver по вашему выбору. [Все привязки языков Selenium поддерживают Microsoft Edge (EdgeHTML).](https://docs.seleniumhq.org/download/)

> [!NOTE]
> Справку, отчеты о проблемах и запросы на функции файлов можно найти на веб-сайте [Microsoft Edge (EdgeHTML) Feedback & Support.](https://developer.microsoft.com/microsoft-edge/support/)


## Использование WebDriver
Чтобы начать использовать WebDriver с Microsoft Edge (EdgeHTML), ознакомьтесь с этими примерами:

* [Пример кода на C\#](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) для открытия окна браузера, bing.com поиска "webdriver" (GitHub Gist).

## Флаги командной строки сервера WebDriver
Список флагов командной строки для сервера WebDriver.

| Имя    | Описание                                                                                                      | Доступный выпуск |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| host    | IP-адрес сервера WebDriver (по умолчанию: localhost)                                                     | 14393             |
| порт    | Порт для сервера WebDriver (по умолчанию: 17556)                                                            | 14393             |
| пакет | ApplicationUserModelId (AUMID) для запуска приложения сервером WebDriver                        | 14393             |
| подробный | Вывод полученных запросов и ответов, отправленных сервером WebDriver                                             | 14393             |
| silent  | Вывод ничего не выводит                                                                                                  | 15063             |
| version | Вывод версии MicrosoftWebDriver.exe                                                                    | 17763             |
| w3c     | Использование протокола W3C WebDriver (параметр по умолчанию)                                                                      | 17763             |
| jwp     | Использование протокола JSON Wire                                                                                           | 17763             |
| cleanup | Очистка временных данных и ключей реестра, установленных сервером WebDriver для --package. Другие параметры игнорируются | 17763             |

## W3C WebDriver
Поддержка по команде для спецификации [W3C WebDriver.](https://www.w3.org/TR/webdriver/)

### Возможности
| Возможность                       | Раздел                       | Состояние                   | Доступный выпуск |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Имя браузера                     | "browserName"             | Поддерживается                | 17763             |
| Версия браузера                  | "browserVersion"          | Поддерживается                | 17763             |
| Имя платформы                    | "platformName"            | Поддерживается                | 17763             |
| Принятие небезопасных сертификатов TLS | "acceptInsecureCerts"     | Не &nbsp; поддерживается       | Н/Д               |
| Стратегия загрузки страницы               | "pageLoadStrategy"        | Поддерживается                | 17763             |
| Настройка прокси-сервера              | "proxy"                   | Не &nbsp; поддерживается       | Н/Д               |
| Измерение и позиционирование окна  | "setWindowRect"           | Поддерживается                | 17763             |
| Конфигурация времени и времени сеанса   | "timeouts"                | Поддерживается                | 17763             |
| Необязченное поведение запроса        | "unhandledPromptBehavior" | Частично &nbsp; поддерживаемая | 17763             |
| InPrivate                        | "ms:inPrivate"            | Поддерживается                | 17763             |
| Пути расширения                  | "ms:extensionPaths"       | Поддерживается                | 17763             |
| Начальная страница                       | "ms:startPage"            | Поддерживается                | 17763             |

### Стратегии локатора
| Стратегия локатора                                                        | Состояние    | Доступный выпуск |
|:------------------------------------------------------------------------|:----------|:------------------|
| [Селекторы CSS](https://www.w3.org/TR/webdriver/#css-selectors)         | Поддерживается | 17763             |
| [Текст ссылки](https://www.w3.org/TR/webdriver/#link-text)                 | Поддерживается | 17763             |
| [Текст частичной ссылки](https://www.w3.org/TR/webdriver/#partial-link-text) | Поддерживается | 17763             |
| [Имя тега](https://www.w3.org/TR/webdriver/#tag-name)                   | Поддерживается | 17763             |
| [XPath](https://www.w3.org/TR/webdriver/#xpath)                         | Поддерживается | 17763             |

### Команды
| Метод HTTP | Шаблон URI                                                   | Команда                                                                                   | Состояние             | Доступный выпуск |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Новый сеанс](https://www.w3.org/TR/webdriver/#new-session)                               | Поддерживается          | 17763             |
| DELETE      | /session/{session id}                                          | [Удаление сеанса](https://www.w3.org/TR/webdriver/#delete-session)                         | Поддерживается          | 17763             |
| GET         | /status                                                        | [Состояние](https://www.w3.org/TR/webdriver/#status)                                         | Поддерживается          | 17763             |
| GET         | /session/{session id}/timeouts                                 | [Get Timeouts](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Поддерживается          | 17763             |
| POST        | /session/{session id}/timeouts                                 | [Set Timeouts](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Поддерживается          | 17763             |
| POST        | /session/{session id}/url                                      | [Перейти к](https://www.w3.org/TR/webdriver/#navigate-to)                               | Поддерживается          | 17763             |
| GET         | /session/{session id}/url                                      | [Получить текущий URL-адрес](https://www.w3.org/TR/webdriver/#get-current-url)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/back                                     | [Back](https://www.w3.org/TR/webdriver/#back)                                             | Поддерживается          | 17763             |
| POST        | /session/{session id}/forward                                  | [Forward](https://www.w3.org/TR/webdriver/#forward)                                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/refresh                                  | [Обновить](https://www.w3.org/TR/webdriver/#refresh)                                       | Поддерживается          | 17763             |
| GET         | /session/{session id}/title                                    | [Получить заголовок](https://www.w3.org/TR/webdriver/#get-title)                                   | Поддерживается          | 17763             |
| GET         | /session/{session id}/window                                   | [Get Window Handle](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Поддерживается          | 17763             |
| DELETE      | /session/{session id}/window                                   | [Закрыть окно](https://www.w3.org/TR/webdriver/#close-window)                             | Поддерживается          | 17763             |
| POST        | /session/{session id}/window                                   | [Переключение в окно](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Поддерживается          | 17763             |
| GET         | /session/{session id}/window/handles                           | [Get Window Handles](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Поддерживается          | 17763             |
| POST        | /session/{session id}/frame                                    | [Переключение на фрейм](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/frame/parent                             | [Переключение на родительский кадр](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Поддерживается          | 17763             |
| GET         | /session/{session id}/window/rect                              | [Get Window Rect](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/window/rect                              | [Set Window Rect](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/window/maximize                          | [Максимальное окно](https://www.w3.org/TR/webdriver/#maximize-window)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/window/minimize                          | [Свернуть окно](https://www.w3.org/TR/webdriver/#minimize-window)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/window/fullscreen                        | [Полноэкранное окно](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | Не &nbsp; поддерживается | Н/Д               |
| GET         | /session/{session id}/element/active                           | [Получить активный элемент](https://www.w3.org/TR/webdriver/#get-active-element)                 | Поддерживается          | 17763             |
| POST        | /session/{session id}/element                                  | [Элемент Find](https://www.w3.org/TR/webdriver/#find-element)                             | Поддерживается          | 17763             |
| POST        | /session/{session id}/elements                                 | [Поиск элементов](https://www.w3.org/TR/webdriver/#find-elements)                           | Поддерживается          | 17763             |
| POST        | /session/{session id}/element/{element id}/element             | [Элемент Find From](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Поддерживается          | 17763             |
| POST        | /session/{session id}/element/{element id}/elements            | [Поиск элементов из элемента](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/selected            | [Элемент Is Selected](https://www.w3.org/TR/webdriver/#is-element-selected)               | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/attribute/{name}    | [Получить атрибут элемента](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/property/{name}     | [Get Element Property](https://www.w3.org/TR/webdriver/#get-element-property)             | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/css/{property name} | [Получить значение CSS элемента](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/text                | [Получить текст элемента](https://www.w3.org/TR/webdriver/#get-element-text)                     | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/name                | [Get Element Tag Name](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/rect                | [Get Element Rect](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Поддерживается          | 17763             |
| GET         | /session/{session id}/element/{element id}/enabled             | [Включен элемент Is](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Поддерживается          | 17763             |
| POST        | /session/{session id}/element/{element id}/click               | [Элемент Click](https://www.w3.org/TR/webdriver/#element-click)                           | Поддерживается          | 17763             |
| POST        | /session/{session id}/element/{element id}/clear               | [Элемент Clear](https://www.w3.org/TR/webdriver/#element-clear)                           | Поддерживается          | 17763             |
| POST        | /session/{session id}/element/{element id}/sendKeys            | [Клавиши отправки элементов](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Поддерживается          | 17763             |
| GET         | /session/{session id}/source                                   | [Получить источник страницы](https://www.w3.org/TR/webdriver/#get-page-source)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/execute/sync                             | [Выполнение скрипта](https://www.w3.org/TR/webdriver/#execute-script)                         | Поддерживается          | 17763             |
| POST        | /session/{session id}/execute/async                            | [Выполнение а async Script](https://www.w3.org/TR/webdriver/#execute-async-script)             | Поддерживается          | 17763             |
| GET         | /session/{session id}/cookie                                   | [Получить все файлы cookie](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Поддерживается          | 17763             |
| GET         | /session/{session id}/cookie/{name}                            | [Get Named Cookie](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Поддерживается          | 17763             |
| POST        | /session/{session id}/cookie                                   | [Добавление файла cookie](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Поддерживается          | 17763             |
| DELETE      | /session/{session id}/cookie/{name}                            | [Удаление файла cookie](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Поддерживается          | 17763             |
| DELETE      | /session/{session id}/cookie                                   | [Удаление всех файлов cookie](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Поддерживается          | 17763             |
| POST        | /session/{session id}/actions                                  | [Выполнение действий](https://www.w3.org/TR/webdriver/#perform-actions)                       | Поддерживается          | 17763             |
| DELETE      | /session/{session id}/actions                                  | [Действия по выпуску](https://www.w3.org/TR/webdriver/#release-actions)                       | Поддерживается          | 17763             |
| POST        | /session/{session id}/alert/dismiss                            | [Оповещение об отклонении](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Поддерживается          | 17763             |
| POST        | /session/{session id}/alert/accept                             | [Принять оповещение](https://www.w3.org/TR/webdriver/#accept-alert)                             | Поддерживается          | 17763             |
| GET         | /session/{session id}/alert/text                               | [Получить текст оповещения](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Поддерживается          | 17763             |
| POST        | /session/{session id}/alert/text                               | [Отправка текста оповещения](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Поддерживается          | 17763             |
| GET         | /session/{session id}/screenshot                               | [Снимок экрана](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Поддерживается          | 17763             |
| GET         | /session/{session id}/screenshot/{element id}                  | [Снимок экрана элемента](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Поддерживается          | 17763             |

## JSON Wire Protocol
Поддержка по команде для протокола [JSON Wire Protocol.](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol)

### Команды
| Метод HTTP | Путь                                                                                                                                                         | Состояние             | Доступный выпуск |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Поддерживается          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Поддерживается          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Поддерживается          | 10240             |
| GET         | [/session/:sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Поддерживается          | 10240             |
| DELETE      | [/session/:sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/timeouts](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/timeouts/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/timeouts/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/url](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/url](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/back](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/refresh](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/execute](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/screenshot](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/ime/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/ime/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/ime/activated](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/ime/deactivate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/ime/activate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/frame/parent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/window/:windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/window/:windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/window/:windowHandle/position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/window/:windowHandle/position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/window/:windowHandle/maximize](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10240             |
| DELETE      | [/session/:sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/cookie/:name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/source](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Поддерживается          | 10586             |
| GET         | [/session/:sessionId}/title](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/element/active](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/element/:id/element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/element/:id/elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/element/:id/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/element/:id/submit](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/element/:id/value](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/keys](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/element/:id/clear](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/element/:id/selected](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/element/:id/enabled](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/element/:id/attribute/:name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/element/:id/equals/:other](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/displayed](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/element/:id/location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/element/:id/css/:p ropertyName](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Поддерживается          | 10240             |
| GET         | [/session/:sessionId/orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/moveto](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Поддерживается          | 10240             |
| POST        | [/session/:sessionId/buttondown](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/buttonup](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/doubleclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/touch/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/down](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/move](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/doubleclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/flick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | Не &nbsp; поддерживается | Н/Д               |
| POST        | [/session/:sessionId/touch/flick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/local_storage/key/:key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/local_storage/key/:key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/local_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| POST        | [/session/:sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/session_storage/key/:key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Поддерживается          | 10586             |
| DELETE      | [/session/:sessionId/session_storage/key/:key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/session_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Поддерживается          | 10586             |
| GET         | [/session/:sessionId/log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/log/types](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | Не &nbsp; поддерживается | Н/Д               |
| GET         | [/session/:sessionId/application_cache/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Поддерживается          | 10586             |  
