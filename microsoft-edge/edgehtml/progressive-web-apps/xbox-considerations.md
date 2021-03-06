---
description: Убедитесь, что ваш PWA обеспечивает отличный опыт для Xbox
title: Прогрессивные веб-приложения для Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3ac4174c821f221d6d666a25880867275ca5cbd5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397673"
---
# <a name="progressive-web-apps-for-xbox-one"></a>Прогрессивные веб-приложения для Xbox One  

Вы можете расширить веб-приложение и сделать его доступным в качестве приложения Xbox One через Microsoft Store, продолжая при этом использовать существующие инфраструктуры, CDN и серверную базу данных.  Как и все приложения универсальной платформы Windows \(UWP\) прогрессивные веб-приложения \(PWAs\), работающие на Xbox One, также могут вызывать родной API Windows 10.  Для Xbox One уже доступно несколько PWAs, особенно в категории приложений воспроизведения [мультимедиа.](#media-pwas-on-xbox)  

По большей части вы можете упаковировать PWA для Xbox One так же, как и для [Windows,](./windows-features.md)с помощью средств [PWA Builder](https://www.pwabuilder.com) или [Visual Studio](https://visualstudio.microsoft.com/vs) IDE для создания файла, необходимого для запуска PWA в качестве приложения `appxmanifest` UWP.  Тем не менее, существует несколько ключевых различий, которые поможет вам пройти в этом руководстве.  

## <a name="deploying-and-testing-pwas-on-xbox"></a>Развертывание и тестирование PWAs на Xbox  

Чтобы начать работу, выполните [следующие действия, чтобы *активировать режим разработчика Xbox One.*](/windows/uwp/xbox-apps/devkit-activation)  С активацией режима разработчика установите портал [ *устройств для Xbox,* ](/windows/uwp/debug-test-perf/device-portal-xbox) чтобы получить удаленный доступ к Xbox из браузера в среде разработчиков.  

Теперь вы готовы развернуть приложение для тестирования с помощью PWA Builder или Visual Studio.  

### <a name="option-1--pwa-builder"></a>Вариант 1. Строитель PWA  

[PWA Builder](https://www.pwabuilder.com) — это Node.js приложение, которое можно установить из node диспетчер пакетов \(NPM\).  Метаданные веб-сайта используются для создания родных приложений для Android, iOS и Windows.  Если на вашем сайте уже [есть](https://developer.mozilla.org/docs/Web/Manifest)манифест веб-приложения, PWA Builder будет использовать его для создания пакетов установки, определенных для платформы.  В противном случае PWA Builder будет создавать базовый файл на основе характеристик `manifest.json` вашего сайта.  

#### <a name="requirements"></a>Требования  

*   [Node.js, ](https://nodejs.org)которая включает NPM.  

#### <a name="setup"></a>Настройка  

1.  Откройте командную подсказку узла для установки PWA Builder:  
    
    ```shell
    npm install pwabuilder --global
    ```  
    
1.  Запустите PWA Builder на URL-адресе веб-сайта:  
    
    ```shell
    pwabuilder https://example.com/ -windows10
    ```  
    
    Флаг *Windows10 ограничивает* генерацию пакета Windows 10 \(UWP\).  Его можно опустить для создания пакетов на всех поддерживаемых платформах, включая iOS и Android.  Дополнительные сведения см. в документы [PWA Builder.](https://docs.pwabuilder.com)  
    
1.  С портала устройств для **** [Xbox](/windows/uwp/debug-test-perf/device-portal-xbox)перейдите в home My games & приложения Добавить, выберите вариант для загрузки свободных файлов и выберите папку манифеста приложения  >  ****  >  **** Windows 10, **** созданную разработчиком PWA в текущем каталоге.  
1.  Пройдесь по мастеру, чтобы завершить процесс установки.  После установки.  Вы сможете увидеть и запустить PWA с панели мониторинга Xbox One.  
    
### <a name="option-2--visual-studio"></a>Вариант 2: Visual Studio  

Бесплатный полноразмерный [Visual Studio Community 2017](https://visualstudio.microsoft.com/vs/community) включает средства разработчика Windows 10, универсальные шаблоны приложений, редактор кода, мощный отладчик, эмуляторы Windows Mobile, богатую языковую поддержку и многое другое — все готово к использованию в производстве.  Версии [Профессиональный и Корпоративный](https://visualstudio.microsoft.com/vs/compare) предоставляют еще больше функций.  

#### <a name="requirements"></a>Требования  

*   [Visual Studio 2017](https://visualstudio.microsoft.com/vs): Любая версия, включая бесплатное издание Community.  
*   [Windows 10 SDK.](/windows/uwp/xbox-apps/development-environment-setup)Выберите этот необязательный компонент в Visual Studio 2017.  

#### <a name="setup"></a>Настройка  

1.  Выполните действия по настройкам и [запуску PWA в качестве универсального приложения Для Windows.](./windows-features.md#set-up-and-run-your-universal-windows-app)  Благодаря этому у вас будет полностью функционируют приложения Windows 10, которые могут получать доступ к универсальным API Windows.  
1.  Теперь вы можете развернуть и отладить PWA \(как приложение UWP\) на Xbox One \(как и любое другое удаленное устройство Windows 10\) с помощью Visual Studio удаленного [отладки](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017&preserve-view=true
).  Поочередно можно установить PWA с помощью портала устройств [для Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) с помощью следующих действий.  
1.  С портала устройств для **** Xbox перейдите в Home My games \& приложения Добавить , выберите вариант для загрузки пакета приложений и  >  ****  >  **** **зависимостей**.  
1.  Перейдите в папку пакета, созданную для приложения на шаге 1, и выберите `.appx` файл для отправки.  Файл [.appx —](/windows/uwp/packaging/packaging-uwp-apps) это файл пакета приложений UWP, который может быть загружен на любом устройстве для тестирования.  
1.  Затем нажмите **кнопку Зависимостей** и выберите папку для приложения и `dependencies` загрузите каждую из них.  Этот шаг необходим только для развертывания приложений с портала устройств для Xbox.  Visual Studio обеспечивает зависимость при удаленной отладке, и машина пользователя уже будет устанавливать их при доставке из Microsoft Store.  
1.  С пакетом приложения и загруженными зависимостями нажмите кнопку **Перейти** в разделе *Развертывание,* и приложение будет установлено.  Вы готовы запустить приложение из Xbox!  

## <a name="ux-considerations-for-pwas-on-xbox"></a>Соображения UX для PWAs на Xbox  

### <a name="design-for-the-10-foot-experience"></a>Дизайн для "10-футовый опыт"  

Xbox One считается "10-футовый опыт", что означает, что ваши пользователи, скорее всего, будет сидеть как минимум в 10 футов от экрана.  Таким образом, рассмотрите, как ваше приложение может использоваться на этом расстоянии, в отличие от традиционного рабочего стола веб-браузера с помощью мыши и клавиатуры.  Для разработки и руководства по UX ознакомьтесь [с разработкой для Xbox и ТЕЛЕВИЗОРА.](/windows/uwp/design/devices/designing-for-tv)  

### <a name="understand-the-tv-safezone"></a>Понимание "TV SafeZone"  

Производители телевизоров будут применять [безопасную зону](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) вокруг контента, который может обрезать ваше приложение.  По умолчанию мы применяем безопасную границу вокруг приложения для учета этого, однако вы можете убедиться, что ваше приложение принимает полный размер экрана, позвонив [setDesiredBoundsMode](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) и указав [useCoreWindow:](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode)  

```javascript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```  

Дополнительные дополнительные документы можно просмотреть в документации по пространствам имен [Windows.UI.ViewManagement.](/uwp/api/windows.ui.viewmanagement)  

### <a name="manage-xy-focus-and-navigation"></a>Управление фокусом xY и навигацией  

Методы ввода пользователя для Xbox — это игровые панели или пульт дистанционного управления, которые используют [систему навигации XY,](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)что позволяет пользователю переключать фокус с управления на управление, перемещаясь вверх, вниз, влево и вправо.  

Поэтому необходимо убедиться, что приложение хорошо работает с навигацией XY.  Кроме того, обязательно отключите режим [мыши,](/windows/uwp/xbox-apps/how-to-disable-mouse-mode)который по умолчанию включается для приложений UWP \(и, вероятно, не применим к приложению Xbox\).  

Следующий код отключается в режиме и включает входные данные для создания `mouse` событий клавиатуры DOM:  

```javascript
navigator.gamepadInputEmulation = "keyboard";
```  

Поочередно можно указать, что также отключается мышь, не генерирует события клавиатуры DOM и позволяет использовать стандартные API для веб-и/или игровых планшетов `gamepad` WinRT.  

Чтобы включить направление навигации, ознакомьтесь с [библиотекой TVJS,](#tvjs)которая будет рассмотрена далее.  

### <a name="tvjs"></a>TVJS  

[TVJS — это коллекция библиотек-помощников,](https://github.com/Microsoft/TVHelpers) которые упрощают создание веб-приложений для телевизора.  Если вы строите хост-приложение, которое также будет работать на Xbox, ** TVJS может помочь добавить поддержку для навигации по направлению, а также предоставить несколько элементов управления, которые упрощают взаимодействие с контентом на телевизоре.  

[Направленная навигация](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) — это функция TVJS, которая обеспечивает автоматическую двухмерную навигацию на страницах приложения телевизора.  С его помощью нет необходимости ловушки и обработки навигации на страницах вашего приложения, или явно указать все допустимые целевые объекты фокуса для каждого элемента в пользовательском интерфейсе.  Автоматическая обработка фокуса позволяет пользователям перемещаться интуитивно и надежно.  

Когда пользователь перемещает пользовательский интерфейс приложения с помощью кнопок направления контроллера, автоматический алгоритм фокуса смотрит на набор потенциальных целевых объектов фокуса, определяет следующий элемент, чтобы перейти к этому элементу, а затем автоматически задает фокус на этот элемент.  Чтобы определить следующий элемент, алгоритм сочетает в себе направление ввода, прошлой истории фокуса и физическое расположение элементов пользовательского интерфейса на странице.  

Чтобы включить навигацию по направлению, включаем следующую ссылку на сценарий:  

```html
<script src="directionalnavigation-1.0.0.0.js"></script>
```  

По умолчанию фокусируемыми являются только , `<a>` `<button>` , и `<input>` `<select>` `<textarea>` элементы.  Чтобы включить фокус на других элементах, назначьте им допустимый [tabindex.](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)  

```html
<div tabindex="0″>This div is eligible for focus</div>
```  

Ознакомьтесь с документацией [DirectionalNavigation,](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) чтобы узнать, как изменить корневой элемент, уделяйте начальное внимание, переопределяйте следующий фокус, оптимизируйте элементы управления для фокусиации, настраивайте входные данные.  Существует также ряд других полезных примеров.

## <a name="media-pwas-on-xbox"></a>Media PWAs on Xbox  

Если вы строите воспроизведение мультимедиа для Xbox One, следует учитывать следующие соображения.  

### <a name="encrypted-media-extensions-eme-in-the-browser"></a>Зашифрованные расширения мультимедиа (EME) в браузере  

Браузер Microsoft Edge на Xbox One не поддерживает [зашифрованные](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) расширения мультимедиа \(EME\).  Если ваш медиа-PWA использует его для управления цифровыми правами \(DRM\), вы не сможете запустить его из браузера на Xbox.  Вместо этого, прототип и проверить его в качестве приложения Xbox One с помощью [PWABuilder или Visual Studio](#deploying-and-testing-pwas-on-xbox), как описано выше.  Вы также можете запустить его в браузере Microsoft Edge в Windows, где emE полностью поддерживается.  

### <a name="integrating-with-system-media-transport-controls"></a>Интеграция с системой управления транспортным транспортом мультимедиа  

Если ваше приложение является приложением мультимедиа, важно, чтобы ваше приложение отвечало на элементы управления мультимедиа, инициированные пользователем [](/windows/uwp/audio-video-camera/system-media-transport-controls) с помощью экранных кнопок, голосовых команд [Кортаны,](https://support.xbox.com/xbox-one/console/cortana-voice-commands)системных средств управления транспортными средствами в области nav или приложений [SmartGlass Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) и [Xbox One](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) на других устройствах.  Посмотрите на элемент управления [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) из [библиотеки TVJS,](#tvjs)который автоматически интегрируется с этими средствами управления.  Поочередно можно вручную [интегрироваться с системой управления](/windows/uwp/audio-video-camera/system-media-transport-controls)транспортными средствами мультимедиа.  

### <a name="playready-content-encryption"></a>Шифрование контента PlayReady  

На момент написания этой статьи поддержка коди-кодинга [cbcs](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) ограничивается клиентом PlayReady для XBox One \(версия 1709 или выше\).  Если средства массовой информации для вашего PWA поддерживают шифрование **cbcs,** следует помнить, что возможности приложения будут ограничены \(или полностью недоступны\) в Windows.  

## <a name="see-also"></a>См. также  

[Видео South Ridge :](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video)пример видео приложения для Xbox, построенного с React.js и размещенного на веб-сервере.  

[Проектирование для Xbox и телевизора:](/windows/uwp/design/devices/designing-for-tv)разработка приложения Универсальной платформы Windows \(UWP\) таким образом, чтобы оно хорошо выглядело и хорошо функционирует на экранах Xbox One и телевизоров.  

[Лучшие практики Xbox.](/windows/uwp/xbox-apps/tailoring-for-xbox)Следуйте этим лучшим практикам, чтобы адаптировать приложение для Xbox One.  

[PWAs в Microsoft Store:](./microsoft-store.md)Вот как \(и почему?\) отправить PWA в Microsoft Store.  

[UWP на Xbox One:](/windows/uwp/xbox-apps/index)полное руководство по разработке приложений UWP для Xbox One.  
