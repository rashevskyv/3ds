---
title: Homebrew Launcher (альтернативные методы запуска)
permalink: /homebrew-launcher-alternatives.html
author_profile: true
---

{% include toc title="Разделы" %}

Homebrew Launcher имеет множество точек входа, или методов запуска.

**Убедитесь, что у вас есть рабочее активное подключение к интернету.**

Если вы не можете использовать browserhax (см. таблицу ниже), у вас нет одной из этих игр и другой 3DS с доступом к Homebrew Launcher, самый дешевый вариант это купить "Nintendo Selects" версию [Ocarina of Time 3D](https://amzn.to/2fkaKdp){:target="_blank"} (убедитесь, что покупаете картридж своего региона) и [Powersaves](https://amzn.to/2fb3VY7){:target="_blank"} (совместим со всеми регионами), затем использовать oot3dhax из таблицы ниже.

Убедитесь, что Беспроводной режим (Wireless Communication) включен, так как udsploit и safehax (используется на следующей странице) потребует активный беспроводной модуль для своей работы, и некоторые консоли (New 3DS, New 2DS и Old 2DS) не могут включить Беспроводной режим, находясь в Homebrew Launcher. Достаточно включить Беспроводной режим (Wireless Communication); наличие соединения с точкой доступа не обязательно.

## Что понадобится

* [Homebrew Menu v2.0.0](https://github.com/fincs/new-hbmenu/releases/latest){:target="_blank"}
<!-- {% include /inc/files/ocs.txt %} -->
* [otherapp payload](https://smealum.github.io/3ds/#otherapp){:target="_blank"} *(для вашей версии ПО и региона приставки; если версия вашего браузера меньше, чем -7, попробуйте использовать otherapp для версии -7)*

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
<!-- 1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты -->
1. Скопируйте `boot.3dsx` (Homebrew Menu 2.0.0) в корень SD-карты
1. Скопируйте otherapp payload в корень вашей SD-карты и переименуйте его в `otherapp.bin`
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

## Альтернативные точки входа

Используйте одну из следующих точек входа для запуска Homebrew launcher. На этой странице представлены самые простоы для использования эксплойты. Со всеми известными эксплойтами можно ознакомиться здесь - [https://3dbrew.org/wiki/Homebrew_Exploits](https://3dbrew.org/wiki/Homebrew_Exploits){:target="_blank"}

### Первичные точки входа

Первичной точкой входа называют такую точку, для работы которой не требуется ничего, кроме самой игры. 

| <sub> | <sub>Что понадобится | <sub>Издания | <sub>Устройства | <sub>Регионы | <sub>Версии игры | <sub>Версии прошивки |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| <sub>[Steelminer](http://steelminer.jisagi.net/){:target="_blank"} | <sub>[*Steel Diver: Sub Wars
*](https://www.nintendo.com/games/detail/BSJH4AsXmM1QXZQ_oxMJjiblWuchnKEw){:target="_blank"} | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>{% include /vars/sys_version.txt %} |
| <sub>[Ninjhax 2](http://smealum.github.io/ninjhax2/){:target="_blank"} | <sub>[*Cubic Ninja*](https://amzn.to/2eRI1by){:target="_blank"} | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до {% include /vars/sys_version.txt %} |
| <sub>[freakyhax](http://plutooo.github.io/freakyhax/){:target="_blank"} | <sub>[*Freakyforms Deluxe*](https://amzn.to/2f6eHO7){:target="_blank"} | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до {% include /vars/sys_version.txt %} |
| <sub>[smilehax](https://plutooo.github.io/smilehax/){:target="_blank"} | <sub>[*SmileBASIC*](https://www.nintendo.com/games/detail/eYURHNjVdfyrnA3OJGfmlMYIrJUzgOcv){:target="_blank"} | <sub>eShop | <sub>New, Old, 2DS | <sub>JPN, USA | <sub>3.3.1 | <sub>от 9.0.0-X до 11.0.0-X включительно |
| <sub>[BASICSploit](https://mrnbayoh.github.io/basicsploit/){:target="_blank"} | <sub>[*SmileBASIC*](https://www.nintendo.com/games/detail/eYURHNjVdfyrnA3OJGfmlMYIrJUzgOcv){:target="_blank"} | <sub>eShop | <sub>New, Old, 2DS | <sub>USA | <sub>3.2.1 | <sub>от 9.0.0-X до 11.0.0-X включительно |
| <sub>[smashbroshax](https://gbatemp.net/threads/397194/){:target="_blank"} | <sub>[*Super Smash Bros*](https://amzn.to/2ftGA72){:target="_blank"} | <sub>Картридж, eShop | <sub>New  | <sub>EUR, JPN, USA | <sub><1.1.3, <br> Картриджи с "amiibo" на обложке идут с версией 1.1.4 | <sub>от 9.0.0-X до 11.3.0-X включительно |
| <sub>[browserhax](https://yls8.mtheall.com/3dsbrowserhax.php){:target="_blank"} | <sub>Ничего | <sub>Предустановленный браузер | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>All | <sub>от 9.0.0-2 до 11.0.0-33 включительно |
| <sub>[GenHax](https://github.com/svanheulen/genhax_proxy_installer){:target="_blank"} | <sub>[*Monster Hunter X*](http://amzn.to/2gsk6Tk){:target="_blank"} | <sub>eShop | <sub>New | <sub>JPN | <sub>Все | <sub>от 9.9.0-X до 11.2.0-X включительно |
| <sub>[RPwnG](https://mrnbayoh.github.io/rpwng/){:target="_blank"} | <sub>[*RPG Maker Player*](http://www.nintendo.com/games/detail/rpg-maker-player-3ds){:target="_blank"} | <sub>eShop | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.1.4 (EUR) / 1.1.2 (JPN/USA) | <sub>9.0.0-X и выше, включая {% include /vars/sys_version.txt %} |
| <sub>[Notehax](https://mrnbayoh.github.io/notehax/){:target="_blank"} | <sub>[*Flipnote Studio 3D*](https://my.nintendo.com/rewards/0391c34c430369c0){:target="_blank"} | <sub>eShop | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.3.1 (JPN) / 1.0.0 (EUR/USA) | <sub>9.0.0-X и выше, включая 11.5.0-X |
{: .notice--info}
	
### Вторичные точки входа

В отличии от первичных, для работы таких точек входа нужны дополнительные ухищрения, например, запись инфицированного сохранения в игру с помощью второй уже взломанной приставки
	
| <sub> | <sub>Что понадобится | <sub>Издания | <sub>Устройства | <sub>Регионы | <sub>Версии игры | <sub>Версии прошивки |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| <sub>[oot3dhax](https://github.com/yellows8/oot3dhax){:target="_blank"} | <sub>[*Ocarina of Time 3D*](https://amzn.to/2fkaKdp){:target="_blank"}, <br> Powersaves или другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до {% include /vars/sys_version.txt %} |
| <sub>[supermysterychunkhax](https://smd.salthax.org/){:target="_blank"} | <sub>[*Pokemon Super Mystery Dungeon*](https://amzn.to/2ebxZ75){:target="_blank"}, <br> Другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>9.9.0-X (USA/JPN) / от 10.2.0-X (EUR) до 11.0.0-X (EUR) включительно |
| <sub>[basehaxx](http://mrnbayoh.github.io/basehaxx/){:target="_blank"} | <sub>*Pokemon [Omega Ruby](https://amzn.to/2eRILNQ){:target="_blank"}/[Alpha Sapphire](https://amzn.to/2ebGrmN){:target="_blank"}*, <br> Другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.0, 1.4 | <sub>от 9.0.0-X до 11.3.0-X включительно |
| <sub>[stickerhax](https://github.com/yellows8/stickerhax){:target="_blank"} | <sub>[*Paper Mario: Sticker Star*](https://amzn.to/2f6aDx8){:target="_blank"}, <br> Другая 3DS с доступом к Homebrew Launcher | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, KOR, USA | <sub>Все | <sub>от 9.0.0-X до 11.3.0-X включительно |
{: .notice--info}
	
<!-- Консоль должна загрузиться в OCS -->
Консоль должна загрузиться в Homebrew Launcher

___

## [Установка boot9strap](installing-boot9strap-homebrew-launcher)
{: .notice--success}