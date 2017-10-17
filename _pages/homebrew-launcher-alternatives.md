---
title: "Homebrew Launcher (альтернативные методы запуска)"
permalink: /homebrew-launcher-alternatives.html
author_profile: true
---

{% include toc title="Разделы" %}

Homebrew Launcher имеет множество точек входа, или методов запуска.

**Убедитесь, что у вас есть рабочее активное подключение к интернету.**

Если вы не можете использовать browserhax (см. таблицу ниже), у вас нет одной из этих игр и другой 3DS с доступом к Homebrew Launcher, самый дешевый вариант это купить "Nintendo Selects" версию [Ocarina of Time 3D](https://amzn.to/2fkaKdp) (убедитесь, что покупаете картридж своего региона) и [Powersaves](https://amzn.to/2fb3VY7) (совместим со всеми регионами), затем использовать oot3dhax из таблицы ниже.

Убедитесь, что Беспроводной режим (Wireless Communication) включен, так как udsploit (используется на следующей странице) потребует активный беспроводной модуль для своей работы, и некоторые консоли (New 3DS, New 2DS и Old 2DS) не могут включить Беспроводной режим, находясь в Homebrew Launcher. Достаточно включить Беспроводной режим (Wireless Communication); наличие соединения с точкой доступа не обязательно.

## Что понадобится

* Свежая версия [OCS](https://github.com/Pirater12/ocs/releases/latest)
* [otherapp payload](https://smealum.github.io/3ds/#otherapp) *(для вашей версии ПО и региона приставки; если версия вашего браузера меньше, чем -7, попробуйте использовать otherapp для версии -7)*

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Скопируйте otherapp payload в корень вашей SD-карты и переименуйте его в `otherapp.bin`
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

## Альтернативные точки входа

1. Используйте одну из следующих точек входа для запуска Homebrew launcher

	| <sub> | <sub>Что понадобится | <sub>Издания | <sub>Устройства | <sub>Регионы | <sub>Версии игры | <sub>Версии прошивки |
	|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
    | <sub>[browserhax](https://yls8.mtheall.com/3dsbrowserhax.php) | <sub>Ничего | <sub>Предустановленный браузер | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>All | <sub>от 9.0.0-2 до 11.0.0-33 включительно |
	| <sub>[oot3dhax](https://github.com/yellows8/oot3dhax) | <sub>[*Ocarina of Time 3D*](https://amzn.to/2fkaKdp), <br> Powersaves или другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до 11.6.0-X включительно |
	| <sub>[smashbroshax](https://gbatemp.net/threads/397194/) | <sub>[*Super Smash Bros*](https://amzn.to/2ftGA72) | <sub>Картридж, eShop | <sub>New  | <sub>EUR, JPN, USA | <sub><1.1.3, <br> Картриджи с "amiibo" на обложке идут с версией 1.1.4 | <sub>от 9.0.0-X до 11.3.0-X включительно |
	| <sub>[supermysterychunkhax](https://smd.salthax.org/) | <sub>[*Pokemon Super Mystery Dungeon*](https://amzn.to/2ebxZ75), <br> Другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>9.9.0-X (USA/JPN) / от 10.2.0-X (EUR) до 11.0.0-X (EUR) включительно |
	| <sub>[freakyhax](http://plutooo.github.io/freakyhax/) | <sub>[*Freakyforms Deluxe*](https://amzn.to/2f6eHO7) | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до 11.3.0-X включительно |
	| <sub>[basehaxx](http://mrnbayoh.github.io/basehaxx/) | <sub>*Pokemon [Omega Ruby](https://amzn.to/2eRILNQ)/[Alpha Sapphire](https://amzn.to/2ebGrmN)*, <br> Другая 3DS с доступом к Homebrew Launcher | <sub>Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.0, 1.4 | <sub>от 9.0.0-X до 11.3.0-X включительно |
	| <sub>[BASICSploit](https://mrnbayoh.github.io/basicsploit/) | <sub>[*SmileBASIC*](https://www.nintendo.com/games/detail/eYURHNjVdfyrnA3OJGfmlMYIrJUzgOcv) | <sub>eShop | <sub>New, Old, 2DS | <sub>USA | <sub>3.2.1 | <sub>от 9.0.0-X до 11.0.0-X включительно |
	| <sub>[smilehax](https://plutooo.github.io/smilehax/) | <sub>[*SmileBASIC*](https://www.nintendo.com/games/detail/eYURHNjVdfyrnA3OJGfmlMYIrJUzgOcv) | <sub>eShop | <sub>New, Old, 2DS | <sub>JPN, USA | <sub>3.3.1 | <sub>от 9.0.0-X до 11.0.0-X включительно |
	| <sub>[stickerhax](https://github.com/yellows8/stickerhax) | <sub>[*Paper Mario: Sticker Star*](https://amzn.to/2f6aDx8), <br> Другая 3DS с доступом к Homebrew Launcher | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, KOR, USA | <sub>Все | <sub>от 9.0.0-X до 11.3.0-X включительно |
	| <sub>[Ninjhax 2](http://smealum.github.io/ninjhax2/) | <sub>[*Cubic Ninja*](https://amzn.to/2eRI1by) | <sub>eShop, Картридж | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>Все | <sub>от 9.0.0-X до 11.6.0-X включительно |
	| <sub>[GenHax](https://github.com/svanheulen/genhax_proxy_installer) | <sub>[*Monster Hunter X*](http://amzn.to/2gsk6Tk) | <sub>eShop | <sub>New | <sub>JPN | <sub>Все | <sub>от 9.9.0-X до 11.2.0-X включительно |
    | <sub>[Notehax](https://mrnbayoh.github.io/notehax/) | <sub>[*Flipnote Studio 3D*](https://my.nintendo.com/rewards/0391c34c430369c0) | <sub>eShop | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.3.1 (JPN) / 1.0.0 (EUR/USA) | <sub>9.0.0-X и выше, включая 11.5.0-X |
    | <sub>[RPwnG](https://mrnbayoh.github.io/rpwng/) | <sub>[*RPG Maker Player*](http://www.nintendo.com/games/detail/rpg-maker-player-3ds) | <sub>eShop | <sub>New, Old, 2DS | <sub>EUR, JPN, USA | <sub>1.1.4 (EUR) / 1.1.2 (JPN/USA) | <sub>9.0.0-X и выше, включая 11.5.0-X |
    {: .notice--info}
	
1. Консоль должна загрузиться в OCS
1. Больше информации - [https://3dbrew.org/wiki/Homebrew_Exploits](https://3dbrew.org/wiki/Homebrew_Exploits)

___

Следующий шаг: [Установка boot9strap](installing-boot9strap-homebrew-launcher)
{: .notice--success}

