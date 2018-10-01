---
title: Homebrew Menu (используя Steelminer)
permalink: /steelminer.html
author_profile: true
---
{% include toc title="Разделы" %}

Steelhax - новая первичная точка входа для 3DS. С её помощью можно получить доступ к Homebrew Launcher и уже из него установить кастомную прошивку. Самое приятное, что использование этой уязвимости абсолютно бесплатно. 

## Что понадобится 

* [Steelhack Installer](https://github.com/VegaRoXas/vegaroxas.github.io/raw/master/files/steelhax-installer.rar){:target="_blank"}
* [otherapp payload](http://smealum.github.io/3ds/##otherapp){:target="_blank"} (для прошивки 11.8.0-41 используйте otherapp для 11.7.0-40)
* Свежая версия [Homebrew Menu](https://github.com/fincs/new-hbmenu/releases/download/v2.0.0/boot.3dsx){:target="_blank"}

## Инструкция 

{% include /inc/id0_movable.txt %}

### Часть III - Создание взломанного сохранения 

1. Перейдите на сайт [http://steelminer.jisagi.net/](http://steelminer.jisagi.net/){:target='_blank'}
1. Пролистайте вниз до "**Section III - Creating the Save File**"
1. Загрузите созданный ранее `movable.sed` на сайт
	* Не удаляйте его по завершению, он нам еще понадобится
1. Выберите регион вашей приставки в выпадающем списке 
1. Нажмите "**Start!**" и сохраните полученный `00000001.sav` в удобном месте

### Часть IV - Подготовка карты памяти и запуск Homebrew Menu

1. Создайте персонажа Mii через приложение "**Mii Maker**", если у вас его ещё нет
1. Скачайте в eShop игру **Steel Diver: Sub Wars**
	* Если версия вашей прошивки ниже, чем {% include /vars/sys_version.txt %} - обновите прошивку, иначе вы не сможете скачать необходимую для взлома игру!
	* Если не можете найти игру в eShop - проверьте ваши региональные настройки, возможно выставлена страна в которой игра недоступна (Системные настройки -> Профиль -> Региональные настройки). Игра точно есть в регионе USA и Россия 
	* Вам нужно будет создать Nintendo Network ID для того, чтобы скачать эту игру
1. Запустите игру, нажмите {% include inc/btn.txt btn="A" %} и выберите персонажа Mii, чтобы игра создала файлы сохранения
	* НЕ ОБНОВЛЯЙТЕ ИГРУ!
	* Если вы обновили игру, удалите обновление через системные настройки
1. Закройте игру и выключите приставку
1. Вставьте её карту памяти в ПК
1. Извлеките **папку** `steelhax` из архива [`steelhax-installer.rar`](https://github.com/VegaRoXas/vegaroxas.github.io/raw/master/files/steelhax-installer.rar){:target="_blank"} в корень карты памяти вашей приставки
1. Скачайте [otherapp payload](http://smealum.github.io/3ds/##otherapp){:target="_blank"} (используйте otherapp для 11.7.0-40) и сохраните его в папку `steelhax` под именем `payload.bin`
	* Не забудьте выбрать регион!
1. Скопируйте [boot.3dsx (Homebrew Menu)](https://github.com/fincs/new-hbmenu/releases/download/v2.0.0/boot.3dsx){:target="_blank"} в корень карты памяти приставки
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > title > 00040000 > regionId > data` на карте памяти приставки, где вместо **regionID** будет одно из значений ниже, соответствующее региону вашей приставки:
	* USA: `000d7d00`
	* EUR: `000d7e00`
	* JPN: `000d7c00`
1. Поместите `00000001.sav`, который вы получили в части III в эту папку с заменой
1. В корне карты памяти создайте папку `3ds`, если таковой там нет
1. Верните карту памяти обратно в консоль
1. Запустите игру **Steel Diver: Sub Wars**, вместо игры должен запуститься Homebrew Launcher

___

## [Установка CFW с помощью Frogminer](frogminer)
{: .notice--success}
