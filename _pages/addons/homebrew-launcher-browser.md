---
title: "Homebrew Launcher (используя браузер)"
permalink: /homebrew-launcher-browser.html
author_profile: true
---
{% include toc title="Разделы" %}

**Это рудиментарная инструкция! В данный момент наиболее простым способом запуска Hombrew Launcher на прошивках от 9.0.0 до 11.3 включительно, является [Soundhax](homebrew-launcher-soundhax)**
{: .notice--warning}

**Browserhax работает для приставок следующих регионов:  EUR / JPN / USA / KOR.**
{: .notice--warning}

## Что понадобится

+ The Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
+ Настроенное и рабочее интернет-соединение. 

## Инструкция

#### Подготовительные работы

1. Скопируйте _содержимое_ папки starter из архива `starter.zip` в корень вашей карты памяти.   
2. Вставьте карту памяти в приставку.

#### Блокировка conntest.nintendowifi.net

Эта часть полезна только для New 3DS с версией прошивки 10.7.0 и 11.0.0
{: .notice--info}

Описанный метод не работает на приставках японского региона!
{: .notice--warning}

[Ознакомьтесь](https://github.com/Plailect/Guide/issues/684)
{: .notice--info}

Для использования этого метода необходимо уметь добавлять адреса в блоклист своего роутера. Воспользуйтесь гуглом, если не знаете как это делать. Для каждой модели роутера инструкция может быть сугубо индивидуальной. 
{: .notice--info}

1. Если вы счастливый владелец телефона на Android
  + установите на свой смартфон приложение [AFWall+](https://play.google.com/store/apps/details?id=dev.ukanth.ufirewall&hl=ru).
  + Зайдите в меню > Set Custom Script и впишите следующую команду `$IPTABLES -A FORWARD -D 69.25.139.140 -j DROP`.
  + Нажмите `Enable Firewall`.
1. Если у вас нет телефона на Android, можете добавить адрес 69.25.139.140 в блоклист вашего роутера. Например, для роутера на DDWRT это будет выглядеть так: 
  + Зайдите в админку вашего роутера.
  + Перейдите на вкладку Administration -> Commands
  + Вставьте в поле следующую команду - `iptables -I FORWARD -d conntest.nintendowifi.net -j DROP`
  + Перезагрузите роутер
  
Если на вашей приставке еще не было уведомлений о необходимости обновить систему для работы браузера, то можете переходить к использованию browserhax. 
{: .notice--info}

1. Если при попытке зайти в браузер вам предлагают обновить систему: 
  + Отключите добавленное в фаерволл правило.
  + Отформатируйте 3DS через системное меню (Системное меню -> Прочие настройки -> Форматирование).
  + Произведите первичную настройку приставки.
  + Включите добавленное правило.
1. Скачайте [ropbin](https://smealum.github.io/3ds/#otherapp) соответствующий вашей системе и текущей прошивке. 
1. Переименуйте скачанный файл в `browserhax_hblauncher_ropbin_payload.bin` и поместите его в корень карты памяти. 

#### browserhax

1. Перейдите по ссылке `http://yls8.mtheall.com/3dsbrowserhax_auto.php`, либо его сокращенной  версии - `https://goo.gl/d0YhK9`.

	Зеркало: `http://plail.ueuo.com/3dsbrowserhax_auto.php`, либо его сокращенная  версия - `https://goo.gl/VuK851`.
	{: .notice--info}

	+ Либо можно просто сосканировать QR с помощью камеры. Нажмите одновременно (L)+(R), находясь на домашнем экране, а затем нажмите пиктограмму с изображением QR-кода на нижнем экране. Наведите камеру на это изображение:<br>
	
    ![[browserhax_auto]](http://yls8.mtheall.com/3dsbrowserhax_auto_qrcode.png)
	{: .text-center}
    {: .notice--info}

	+ Если выскочит ошибка, перейдите в раздел [проблемы и их решения](troubleshooting#ts_browser).
1. Приставка должна загрузиться в Homebrew Launcher.
	+ Если вы воспользовались способом из части III и заблокировали conntest.nintendowifi.net (или его IP), снимите блокировки сразу, как войдете в Homebrew launcher.
	
___

Следующий шаг: [Установка boot9strap (Homebrew Launcher)](installing-boot9strap-homebrew-launcher)
{: .notice--primary}

