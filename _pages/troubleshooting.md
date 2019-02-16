---
title: Проблемы и их решения
permalink: /troubleshooting.html
author_profile: true
---
{% include toc title="Разделы" %}

Если ваша консоль не загружается, найдите раздел, соответствующий вашей проблеме, и следуйте его инструкциям. После решения возникшей проблемы, вернитесь к основному руководству
(Этот раздел весьма обширный, воспользуйтесь Ctrl+F для поиска своей проблемы)

Если решения вашей проблемы здесь не оказалось, то загрузите содержимое всех .log файлов из корня SD-карты на [Gist](https://gist.github.com/){:target="_blank"}, а затем обращайтесь за помощью, детально описав проблему и испробованные способы решения.

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки {% include inc/btn.txt btn="START" %} при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку {% include inc/btn.txt btn="A" %} для выбора "GodMode9" при выполнении этих инструкций.

## DSi/DS игры не работают на прошитой приставке

### Что понадобится:

* TWL_FIRM `.cia`, соответствующие вашему устройству
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New_3DS TWL_FIRM - v9936.cia](magnet:?xt=urn:btih:eab8558c97b18b1f329a2bfcc3c899b84c082a27&dn=New%5F3DS%20TWL%5FFIRM%20-%20v9936.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [Old_3DS TWL_FIRM - v8817.cia](magnet:?xt=urn:btih:17511eadb6e6f3ff22d04f90644e37bd2d96ca43&dn=Old%5F3DS%20TWL%5FFIRM%20-%20v8817.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [TWL Version Data - v0.cia](magnet:?xt=urn:btih:4a106681407fede5de95cc8bda635432481f6b5d&dn=TWL%20Version%20Data%20-%20v0.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [DS Internet - v2048.cia](magnet:?xt=urn:btih:2b9df8496922f2546dfb0b01220068ce53c19d3d&dn=DS%20Internet%20-%20v2048.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [DS Download Play - v1024.cia](magnet:?xt=urn:btih:b581d3c5d98f5e621fddfc1ce5704bb45bf05a8c&dn=DS%20Download%20Play%20-%20v1024.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [Nintendo DS Cart Whitelist - v11264.cia](magnet:?xt=urn:btih:7b90d506ad032a581a00035616eaa17a68c48eff&dn=Nintendo%20DS%20Cart%20Whitelist%20-%20v11264.cia&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)
 
### Инструкция

#### Часть I - Подготовительные работы

1. Отключите приставку 
1. Вставьте SD-карту консоли в ПК
1. Создайте папку `cias` в корне SD-карты, если таковой нет
1. Скопируйте `TWL Version Data - v0.cia` в папку `/cias/` на SD-карте
1. Скопируйте `DS Download Play - v1024.cia` в папку `/cias/` на SD-карте
1. Скопируйте `DS Internet - v2048.cia` в папку `/cias/` на SD-карте
1. Скопируйте `Nintendo DS Cart Whitelist - v11264.cia` в папку `/cias/` на SD-карте
1. Скопируйте `New_3DS TWL_FIRM - v9936.cia`  или `Old_3DS TWL_FIRM - v8817.cia` в папку `/cias/` на SD-карте
1. Верните SD-карту в приставку 

#### Часть II - Установка

1. Включите консоль
1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs"
1. Нажмите {% include inc/btn.txt btn="HOME" %} для выхода из FBI

## Я потерял все данные на SD-карте. Что нужно делать, чтобы восстановить работоспособность? 

Воспользуйтесь [этой](clean_sd){:target="_blank"} инструкцией

## Черный экран при загрузке SysNAND

1. Попробуйте загрузиться без SD-карты, а затем верните ее в консоль
    1. Выключите консоль
    1. Извлеките SD-карту из консоли
    1. Включите консоль
    1. Когда появится меню Home, вставьте SD-карту обратно в консоль
    1. Если это сработало, вам следует очистить данные меню Home:
        1. Отключите устройство
        1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
		1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для запуска меню
		1. Выберите "**Scripts...**"
		1. Выберите "**GM9Megascript**"
		1. Выберите "**Scripts from Plailect's Guide**"
        1. Выберите **"Remove extdata**"
		1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
		1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
		1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
		1. Нажмите {% include inc/btn.txt btn="B" %}, чтобы вернуться в главное меню
		1. Выберите "**Exit**"
		1. Нажмите {% include inc/btn.txt btn="A" %} чтобы восстановить запрет на запись, если появится запрос
		1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки приставки
1. Попробуйте включить устройство без каких-либо картриджей (включая флеш-картриджи)
1. Если у вас есть хардмод и резервная копия NAND, прошейте бэкап обратно в SysNAND
1. Попробуйте загрузиться в режим восстановления и обновить систему    
    1. Выключите консоль
    1. Зажмите {% include inc/btn.txt btn="L" %}+{% include inc/btn.txt btn="R" %}+{% include inc/btn.txt btn="A" %}+{% include inc/btn.txt btn="UP" %}
    1. Включите консоль
    1. Если вы вошли в режим восстановления, обновите консоль.
1. Ваша консоль, скорее всего, превратилась в брик. Вы можете обратиться за поддержкой [сюда](http://customfw.xyz/contacts){:target="_blank"}

## Черный экран при загрузке SysNAND после установки b9s

1. Убедитесь, что у вас установлен рабочий загрузчик
    + Проверьте, есть ли в корне SD-карты файл `boot.firm`.
1. Попробуйте сбросить настройки Luma3DS
    1. Удалите файл `/luma/config.bin` с SD-карты
    1. Выберите нужные настройки при запуске
1. Попробуйте запустить GodMode9
    + Для устройства с Luma3DS, зажмите {% include inc/btn.txt btn="START" %} при включении
1. Попробуйте очистить данные меню Home [этим способом](#черный-экран-при-загрузке-sysnand)
1. Попробуйте включить устройство без каких-либо картриджей (включая флеш-картриджи)
1. Если вы понижали прошивку через Gateway, то убедитесь, что у вас установлена самая последняя версия Luma3DS (не ниже 6.2.3)
1. Если версия вашего NAND между 3.0.0 и 4.5.0, проделайте следующие действия:
	+ Убедитесь, что используете самую свежую версию Luma 3DS (6.6, или выше)
	+ Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/00000056){:target="_blank"} и переименуйте его в `native.firm`
	+ Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/cetk){:target="_blank"}
	+ Скопируйте `native.firm` и `cetk` в папку `/luma/` на SD-карте
	+ Если у вас Luma3DS версии 7.1 или ниже, переименуйте `native.firm` в `firmware.bin`
	+ После обновления прошивки удалите оба этих файла
1. Попробуйте выполнить [CTRTransfer](ctrtransfer){:target="_blank"}
1. Вы можете обратиться за поддержкой на канал [Nintendo Homebrew в Discord](https://discord.gg/MWxPgEp){:target="_blank"} (англ.), или [группу 3DS_CFW вконтакте](http://vk.com/3ds_cfw){:target="_blank"} (рус.).

## Не запускается ни один пейлоадер. Сразу запускается консоль

+ Убедитесь, что на карте памяти лежит пейлоадер, соответствующий типу установленного взлома - .firm для b9s и .bin для a9lh
+ Для luma3ds ниже версии 7, следует в начале имени пейлоадера писать кнопку, отвечающую за его вызов. Например, переименовав decrypt9.bin в x_decrypt9.bin, вы сможете запустить Decrypt9WIP, зажав {% include inc/btn.txt btn="X" %} при включении консоли
+ Если вы уверены, что все у вас правильно, а пейлоадер все равно не запускается, сделайте резервную копию всех файлов на SD-карте и [отформатируйте](https://3ds.customfw.xyz/clean_sd#ii-форматирование-sd-карты){:target="_blank"} её, а затем верните все файлы обратно и попробуйте еще раз
+ Попробуйте другую карту памяти

## Игры выкидывает с ошибкой

![]({{ base_path }}/images/screenshots/error.png){:target="_blank"}
{: .text-center}

+ Обратите внимание на значение строки **Exception type**. `data abort` и `prefetch abort` означают что точно проблемы с SD-картой. Скопируйте всю информацию со старой карты на новую, предварительно [отформатировав](clean_sd#ii-форматирование-sd-карты){:target="_blank"} новую SD-карту. 

В иных случаях: 

+ Если такая ошибка на только что установленной игре, попробуйте следующее:
	
	1. Запустите [FBI](fbi){:target="_blank"}
	1. Перейдите в меню "**Titles**"
	1. Выберите свою игру и нажмите {% include inc/btn.txt btn="A" %}
	1. Выберите "**Import seed**"

+ Если у вас приставка линейки New, убедитесь, что в настройках Luma3DS отключен разгон: 

  1. Выключите приставку
  1. Включите консоль с зажатым {% include inc/btn.txt btn="SELECT" %}
  1. Отключите разгон:
	+ Установите значение поля **New 3DS CPU** в положение **Off**
	
+ Иногда такая ошибка может возникать при запуске игры чужого региона. Если игра работала, но вдруг перестала после очередного обновления, или установки DLC - скорее всего причина именно в не родном регионе. Можно обмануть игру, воспользовавшись [lumalocale switcher](lumalocales){:target="_blank"}

+ Если вышеперечисленное не помогло - у вас проблемы с картой. Скопируйте с неё все данные на ПК, [отформатируйте карту](clean_sd#ii-форматирование-sd-карты){:target="_blank"}, верните данные на место. Не помогло? Пробуйте с другой картой. 

## 3DS не включается после обновления через Luma3DS Updater - загорается синий диод и тухнет

Вы установили Luma3DS на несовместимый boot
Сперва попробуем определить boot какой версии прошит в приставку

#### Способ I - CTRNAND

Если прошивка выполнялась по этому гайду , то в CTRNAND приставки должны были быть скопированы файлы прошивки. Следовательно, вынув КП из приставки и запустив 3DS, вы сможете запустить Luma и увидеть её версию, из чего легко сделать вывод о том, какой загрузчик стоит в системе.
{: .notice--info}

1. Отключите 3DS
1. Достаньте КП из приставки
1. Загрузите приставку с зажатой кнопкой {% include inc/btn.txt btn="SELECT" %}
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s){:target="_blank"}
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s){:target="_blank"}, если вы не знаете какая именно у вас стоит сейчас

    ![]({{ base_path }}/images/screenshots/luma.png){:target="_blank"}
	{: .text-center}
    {: .notice--info}

#### Способ II - Перебор

Этот метод для тех, кто по каким-то причинам не стал устанавливать Luma3DS в CTRNAND, либо для тех, кто обновился до b9s 1.0 в момент его выхода и обновил Luma3DS через Luma3DS Updater
{: .notice--info}

1. Выключаем консоль
1. Вставляем SD-карту из приставки в компьютер
1. Качаем [Luma3DS 7.0.5](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.0.5){:target="_blank"}
1. Копируем `arm9loaderhax.bin` из архива `Luma3DSv7.0.5.7z` в корень карты памяти с заменой
1. Возвращаем карту памяти в консоль
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас a9lh - [перейдите на b9s актуальной версии](a9lh-to-b9s){:target="_blank"}. 
  + Если не сработало, двигаемся дальше
1. Качаем [Luma3DS 7.1](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1){:target="_blank"} 
1. Копируем `boot.firm` из архива `Luma3DSv7.1.7z` в корень карты памяти с заменой 
1. Возвращаем карту памяти в консоль 
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас b9s 1.0 и нужно обновить его до актуальной версии по инструкции (updating-b9s)
  + Если не сработало, двигаемся дальше
1. Качаем свежую версию {% include /inc/luma_adress.txt %}
1. Копируем `boot.firm` из `7z-архива` Luma3DS в корень SD-карты с заменой 
1. Возвращаем SD-карту в консоль 
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас b9s или выше и самая последняя версия Luma3DS. Можете [обновить b9s до актуальной версии](updating-b9s){:target="_blank"}, если вы не знаете какая именно у вас стоит сейчас
  + Если ничего не помогло, попробуйте выполнить [CTRTransfer](ctrtransfer){:target="_blank"}

## Голубой экран при загрузке (bootrom error)

1. У вас брик
	+ Если вы делали хардмод, попробуйте его отпаять полностью
1. Для восстановления вам понадобится хардмод или ремонт / замена устройства