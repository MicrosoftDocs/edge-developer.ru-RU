---
description: Хост-сайт на веб-сервере машины разработки, а затем доступ к контенту с устройства Android.
title: Доступ к локальным серверам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 16c9927ce4548d71681d35e643aea0a6c44ec75a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398212"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="access-local-servers"></a><span data-ttu-id="ad982-104">Доступ к локальным серверам</span><span class="sxs-lookup"><span data-stu-id="ad982-104">Access local servers</span></span>  

<span data-ttu-id="ad982-105">Узел сайта на веб-сервере машины разработки, а затем доступ к контенту с устройства Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="ad982-106">С помощью USB-кабеля и Microsoft Edge DevTools запустите сайт из машины разработки, а затем просмотреть сайт на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <a name="summary"></a><span data-ttu-id="ad982-107">Сводка</span><span class="sxs-lookup"><span data-stu-id="ad982-107">Summary</span></span>  

*   <span data-ttu-id="ad982-108">Переадпорт портов позволяет просматривать контент, который находится на веб-сервере, запущенном на компьютере разработки на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="ad982-109">Если веб-сервер использует настраиваемый домен, установите устройство Android для доступа к контенту в этом домене с помощью настраиваемой сопоставления домена.</span><span class="sxs-lookup"><span data-stu-id="ad982-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <a name="set-up-port-forwarding"></a><span data-ttu-id="ad982-110">Настройка переадпорта портов</span><span class="sxs-lookup"><span data-stu-id="ad982-110">Set up port forwarding</span></span>  

<span data-ttu-id="ad982-111">Переадпорт портов позволяет устройству Android получать доступ к контенту, который находится на веб-сервере, запущенном на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="ad982-112">Перенос портов работает путем создания порта прослушивания TCP на устройстве Android, который совпадет с портом TCP на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="ad982-113">Трафик между портами проходит через подключение USB между устройством Android и машиной разработки, поэтому подключение не зависит от конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="ad982-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="ad982-114">Чтобы включить переадпорт портов:</span><span class="sxs-lookup"><span data-stu-id="ad982-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="ad982-115">Настройка [удаленного отладки между][RemoteDebuggingGettingStarted] машиной разработки и устройством Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="ad982-116">По завершению устройство Android должно отображаться в левом меню диалогового устройства **Inspect Devices** и **индикаторе подключенного** состояния.</span><span class="sxs-lookup"><span data-stu-id="ad982-116">When you are finished, your Android device should be displayed in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="ad982-117">В **диалоговом** окантовке Inspect Devices в DevTools включить **переадпорт порта.**</span><span class="sxs-lookup"><span data-stu-id="ad982-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="ad982-118">Выберите **правило Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ad982-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Добавление правила переноса порта" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="ad982-120">Добавление правила переноса порта</span><span class="sxs-lookup"><span data-stu-id="ad982-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ad982-121">В **текстовом** ящике порта устройства слева введите номер порта, с которого вы хотите получить доступ к сайту `localhost` на устройстве Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="ad982-122">Например, если вы хотите получить доступ к сайту из `localhost:5000` входа `5000` .</span><span class="sxs-lookup"><span data-stu-id="ad982-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="ad982-123">В **текстовом** ящике Локального адреса справа введите IP-адрес или имя узла, на котором ваш сайт находится на веб-сервере, запущенном в машине разработки, а затем номер порта.</span><span class="sxs-lookup"><span data-stu-id="ad982-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="ad982-124">Например, если сайт запущен в `localhost:7331` `localhost:7331` вводе.</span><span class="sxs-lookup"><span data-stu-id="ad982-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="ad982-125">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ad982-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="ad982-126">Теперь настроена переадпортка порта.</span><span class="sxs-lookup"><span data-stu-id="ad982-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="ad982-127">Просмотрите индикатор состояния для переноса вперед на вкладке на устройстве в **диалоговом** окте "Устройства проверки".</span><span class="sxs-lookup"><span data-stu-id="ad982-127">Review the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Состояние переноса порта" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="ad982-129">Состояние переноса порта</span><span class="sxs-lookup"><span data-stu-id="ad982-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="ad982-130">Чтобы просмотреть содержимое, откройте Microsoft Edge на устройстве Android и перейдите в порт, указанный в поле `localhost` **порта** устройства.</span><span class="sxs-lookup"><span data-stu-id="ad982-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="ad982-131">Например, если вы вошли `5000` в поле, посетите `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="ad982-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <a name="map-to-custom-local-domains"></a><span data-ttu-id="ad982-132">Map to custom local domains</span><span class="sxs-lookup"><span data-stu-id="ad982-132">Map to custom local domains</span></span>  

<span data-ttu-id="ad982-133">Настраиваемый сопоставление домена позволяет просматривать контент на устройстве Android с веб-сервера на компьютере разработки, использующем настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="ad982-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="ad982-134">Например, предположим, что на вашем сайте используется сторонная библиотека JavaScript, которая работает только на `microsoft-edge.devtools` домене.</span><span class="sxs-lookup"><span data-stu-id="ad982-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="ad982-135">Таким образом, вы создаете запись в файле на компьютере разработки, чтобы составить карту этого домена `hosts` `localhost` с \(например, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="ad982-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="ad982-136">После настройки настраиваемого сопоставления домена и переноса порта просматривайте сайт на устройстве Android по `microsoft-edge.devtools` URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="ad982-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <a name="set-up-port-forwarding-to-proxy-server"></a><span data-ttu-id="ad982-137">Настройка переноса порта на прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="ad982-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="ad982-138">Чтобы составить настраиваемый домен, необходимо запустить прокси-сервер на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="ad982-139">Примерами прокси-серверов [являются Charles,][CharlesWebDebuggingProxy] [Squid][SquidOptimisingWebDelivery]и [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="ad982-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="ad982-140">Настройка переноса порта в прокси-сервер:</span><span class="sxs-lookup"><span data-stu-id="ad982-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="ad982-141">Запустите прокси-сервер и зафиксировать порт, который он использует.</span><span class="sxs-lookup"><span data-stu-id="ad982-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ad982-142">Прокси-сервер и веб-сервер должны работать в разных портах.</span><span class="sxs-lookup"><span data-stu-id="ad982-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="ad982-143">Настройка [переноса порта на](#set-up-port-forwarding) устройство Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="ad982-144">В **локальном поле адресов** введите порт, на который запущен `localhost:` прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="ad982-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="ad982-145">Например, если он запущен в `8000` порту, перейдите к `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="ad982-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="ad982-146">В поле **порта устройства** введите номер, который необходимо прослушивать устройству Android, например `3333` .</span><span class="sxs-lookup"><span data-stu-id="ad982-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <a name="configure-proxy-settings-on-your-device"></a><span data-ttu-id="ad982-147">Настройка параметров прокси на устройстве</span><span class="sxs-lookup"><span data-stu-id="ad982-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="ad982-148">Далее необходимо настроить устройство Android для связи с прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="ad982-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="ad982-149">На устройстве Android перейдите к **настройкам**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="ad982-149">On your Android device, navigate to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="ad982-150">Нажатие длинного нажатия на имя сети, к которой вы подключены в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="ad982-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ad982-151">Параметры прокси применяются к сети.</span><span class="sxs-lookup"><span data-stu-id="ad982-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="ad982-152">Выберите **Изменить сеть**.</span><span class="sxs-lookup"><span data-stu-id="ad982-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="ad982-153">Выберите **расширенные параметры**.</span><span class="sxs-lookup"><span data-stu-id="ad982-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="ad982-154">Отображение параметров прокси.</span><span class="sxs-lookup"><span data-stu-id="ad982-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="ad982-155">Выберите меню **Прокси** и выберите **Руководство**.</span><span class="sxs-lookup"><span data-stu-id="ad982-155">Choose the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="ad982-156">Для поля **имя хозяина прокси** введите `localhost` .</span><span class="sxs-lookup"><span data-stu-id="ad982-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="ad982-157">Для поля **порта Прокси** введите номер порта, который был введен для порта устройств **в** предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="ad982-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="ad982-158">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ad982-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="ad982-159">С помощью этих параметров устройство передает все свои запросы прокси-серверу на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="ad982-160">Прокси-сервер делает запросы от имени устройства, поэтому запросы на настраиваемый локальный домен будут надлежащим образом разрешены.</span><span class="sxs-lookup"><span data-stu-id="ad982-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="ad982-161">Теперь доступ к пользовательским доменам на устройстве Android, как и на компьютере разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="ad982-162">Если на веб-сервере запущен нестандартный порт, не забудьте указать порт при запросе контента с устройства Android.</span><span class="sxs-lookup"><span data-stu-id="ad982-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="ad982-163">Например, если веб-сервер использует настраиваемый домен в порту, при просмотре сайта с устройства Android необходимо использовать `microsoft-edge.devtools` `7331` URL-адрес. `microsoft-edge.devtools:7331`</span><span class="sxs-lookup"><span data-stu-id="ad982-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="ad982-164">Чтобы возобновить нормальный просмотр, не забудьте восстановить параметры прокси на устройстве Android после отключения от машины разработки.</span><span class="sxs-lookup"><span data-stu-id="ad982-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ad982-165">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ad982-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Прокси-сервер веб-отладки Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "squid : Оптимизация веб-доставки"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler — бесплатный прокси-сервер отладки веб-сайтов"  

> [!NOTE]
> <span data-ttu-id="ad982-170">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ad982-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ad982-171">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="ad982-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ad982-173">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ad982-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
