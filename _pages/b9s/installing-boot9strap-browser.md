---
title: "Установка boot9strap (Браузер)" #
lang: ru
permalink: installing-boot9strap-browser.html
author_profile: true
---
{% include toc title="Разделы" %}

Если вы взламывали ваше устройство ранее и у вас установлена кастомная прошивка на основе EmuNAND, помните, что данное руководство работает только с SysNAND и вы должны выполнять вся шаги находясь в SysNAND. Помните, что RedNAND и EmuNAND - немного разные реализации [одного и того же](http://3dbrew.org/wiki/NAND_Redirection) (англ.).

## Что понадобится

* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(стандартный boot9strap; не `dev-файл`, не `ntr-файл`)*
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z`-архив)*
* Свежая версия [OCS](https://github.com/Pirater12/ocs/releases/latest)

## Инструкция

#### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. Скопируйте `SafeB9SInstaller.dat` и `Launcher.dat` из `.zip-ахрива` SafeB9SInstaller в корень SD-карты

    ![]({{ "/images/screenshots/boot9strap-browser-file-layout.png" | absolute_url }})
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Включите консоль

#### Часть II - Запуск SafeB9SInstaller

1. Запустите браузер на консоли и перейдите по одной из следующих ссылок
	+ `https://goo.gl/Pk5IZs` или `https://dukesrg.github.io/?SafeB9SInstaller.dat`
	+ `https://goo.gl/f8GbSf` или `http://go.gateway-3ds.com/`
	+ `https://goo.gl/ASCLSV` или `http://www.reboot.ms/3ds/load.html?Launcher.dat`
	+ `https://goo.gl/etmY59` или `http://dukesrg.dynu.net/3ds/rop?GW17567.dat&Launcher.dat`
	+ **Или сосканируйте камерой QR, если QR-сканер есть в вашей версии прошивки:**

	Для того, чтобы попасть в QR-scanner, нажмите одновременно (L)+(R), находясь на домашнем экране, а затем нажмите пиктограмму с изображением QR-кода на нижнем экране.
	{: .notice--info}

	![]({{ "/images/QR/dukeGithub.png" | absolute_url }})	![]({{ "/images/QR/gateway.png" | absolute_url }})
	<br>
	![]({{ "/images/QR/goReboot.png" | absolute_url }})	![]({{ "/images/QR/dukeDynu.png" | absolute_url }})
	{: .text-center}
	{: .notice--info}
	  
	+ В случае, если первая ссылка не сработала, попробуйте все остальные (некоторое консоли не могут использовать первую ссылку, в то время как другие не могут использовать последние три)
	+ При возникновении ошибки, обратитесь к разделу [проблемы и их решения](troubleshooting#не-работает-эксплойт-на-основе-браузера)
1. Если эксплойт сработал, запустится SafeB9SInstaller

#### Часть III - Установка boot9strap

1. Подождите окончания всех проверок безопастности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки

#### Часть IV - Настройка Luma3DS

1. Устройство загрузится в меню настройки Luma3DS
  + Если после включения экран остаётся чёрным, то перейдите к разделу [проблемы и их решения](troubleshooting#черный-экран-при-загрузке-sysnand-после-установки-b9s)
1. Нажимая (A) выберите следующие пункты:    
  + **"Enable game patching"**
  + **"Show NAND or user string in System Settings"**
1. Если у вас **New 3DS**, вы *также* можете включить следующие опции:
  + **"New 3DS CPU" выбрать значение "Clock+L2(x)"**
    + Это увеличит частоту кадров в множестве игр, но может отразиться на стабильности других
    + Если какие-либо игры работают некорректно, отключите эту опцию
	
	![]({{ "/images/screenshots/luma-settings.png" | absolute_url }})
	{: .text-center}
    {: .notice--info}
	
1. Нажмите (START), чтобы сохранить настройки и перезагрузиться
  + Если появляется ошибка, просто переходите к следующей странице

___

Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}

