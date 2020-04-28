---
title: Установка CFW с помощью Fredtool
permalink: /fredtool.html
author_profile: true
---
{% include toc title="Разделы" %}

### Часть I - Подготовительная работа 

1. Перейдите на сайт [https://bb3.bruteforcemovable.com/](https://bb3.bruteforcemovable.com/){:target='_blank'} на вашем ПК
1. Нажмите на кнопку "**Choose File**" и выберите `movable.sed`, его мы получали ранее 
1. Нажмите на кнопку "**Start!**"
    * Вам предложат сохранить на ПК архив `tadmuffin_out.zip`, содержащий эксплойт, сделайте это
1. Отключите консоль
1. Вставьте SD-карту приставки в ПК 
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении *movable.sed*
    * Если папки *Nintendo DSiWare* нет, создайте её
    * Если в папке *Nintendo DSiWare* есть файлы, переместите их на ПК 
1. Скопируйте файл `F00D43D5.bin`, находящийся в архиве `tadmuffin_out.zip` по пути `output\Usa_Europe_Japan_Korea\` в папку `Nintendo DSiWare`
    * В консоли в папке `Nintendo DSiWare` должен оказаться файл `F00D43D5.bin`, а не папки его содержащие

### Часть II - BannerBomb 

1. Верните SD-карту обратно в консоль
1. Включите приставку 
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Управление данными**" (Data Management) -> "**DSiWare**"
1. Выберите "**Карта SD**" (SD Card)
    * Экраны должны замигать <span style="color: magenta">пурпурным</span>, после чего приставка вылетит с ошибкой, что значит, что эксплойт сработал
1. Выключите приставку 
    * Удерживая кнопку {% include inc/btn.txt btn="POWER" %} при необходимости 
1. Вставьте карту памяти в ПК 
1. В корне карты памяти появится файл `42383841.bin`, который мы будем использовать в дальнейшем 
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении *movable.sed*
1. Удалите файл `F00D43D5.bin`

## Часть III - Fredtool

1. Перейдите на сайт [https://fredtool.bruteforcemovable.com](https://fredtool.bruteforcemovable.com){:target='_blank'} на вашем ПК
1. Нажмите на кнопку "**Choose File**" под пунктом "**Your movable.sed**" и выберите `movable.sed`, его мы получали ранее 
1. Нажмите на кнопку "**Choose File**" под пунктом "**Your dsiware.bin**" и выберите `42383841.bin` в корне вашей карты памяти
1. Пройдите капчу и нажмите "**Start!**"
1. После окончания работы программы, вам предложат скачать архив с модифицированной игрой 
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении *movable.sed*
    * Если папки *Nintendo DSiWare* нет, создайте её
1. Скопируйте файл `42383841.bin`, находящийся в архиве `fredtool_output.zip` по пути `output/hax/` в папку `Nintendo DSiWare`
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
1. Верните SD-карту обратно в консоль
1. Включите приставку 
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Управление данными**" (Data Management) -> "**DSiWare**"
1. Выберите "**Карта SD**" (SD Card) и нажмите на "**Haxxxxxxxxx!**"
 * Если рожица не появляется, перезакиньте {% include /inc/files/3dssdfiles.txt %} на карту памяти
1. Выберите "**Копировать**", затем нажмите "**ОК**"
1. Вернитесь на первую страницу Системных настроек 
1. Перейдите в "**Интернет-настройки**" (Internet Settings) -> "**Подключения Nintendo DS**" (Nintendo DS Connections) и нажмите "**ОК**"
1. Если всё сделано верно, запустится японская версия Flipnote Studio

**Возможные ошибки:**
* Чёрный экран вместо запуска Flipnote Studio может свидетельствовать о том, что приставка уже прошита. Чтобы проверить, нажмите одновременно {% include inc/btn.txt btn="L" %} + {% include inc/btn.txt btn="DOWN" %} + {% include inc/btn.txt btn="SELECT" %}. Если откроется меню Rosalina, то приставка прошита, можете сразу следовать к [завершению установки](finalizing-setup)
* Бирюзовый экран возникает при проблемах с картой памяти. Отформатируйте карту памяти через [SDFormatter](https://www.sdcard.org/downloads/formatter/eula_windows/SDCardFormatterv5_WinEN.zip){:target='_blank'}. Не забудьте перед этим скопировать содержимое карты памяти на ПК, а после форматирования вернуть обратно

## Часть IV - Flipnote Studio

1. Следуйте [это инструкции](https://zoogie.github.io/web/flipnote_directions/){:target='_blank'} для того, чтобы запустить b9stool
1. Выберите "**Install boot9strap**" кнопкой {% include inc/btn.txt btn="A" %}, подтвердите ваши действия, зажав одновременно {% include inc/btn.txt btn="START" %} и {% include inc/btn.txt btn="SELECT" %}
1. Когда увидите надпись "Done!", нажмите кнопку {% include inc/btn.txt btn="HOME" %}, затем подтвердите выход, нажав на "ОК". Приставка выключится
  + При необходимости выключите консоль принудительно, удерживая кнопку питания
  
### Часть V - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

### Часть VI - Восстановление работы меню Подключения Nintendo DS

1. Отключите приставку, если она включена
1. Вставьте карту памяти в ПК 
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении *movable.sed*
1. Скопируйте файл `42383841.bin`, находящийся в архиве `fredtool_output.zip` по пути `output/clean/` в папку `Nintendo DSiWare` с заменой
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Управление данными**" (Data Management) -> "**DSiWare**"
1. Выберите "**Карта SD**" (SD Card) и нажмите на "**Nintendo DSi™**"
1. Выберите "**Копировать**", затем нажмите "**ОК**"

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}