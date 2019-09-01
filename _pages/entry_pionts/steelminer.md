---
title: Steelminer
permalink: /steelminer.html
author_profile: true
---
{% include toc title="Разделы" %}

Steelhax - новая первичная точка входа для 3DS. С её помощью можно получить доступ к Homebrew Launcher и уже из него установить кастомную прошивку. Самое приятное, что использование этой уязвимости абсолютно бесплатно. 

## Инструкция 

<!--В видео показан весь процесс взлома от начала и до конца:

{% include youtube.html id="Zdi-RK3InrY" %}
{: .text-center}
{: .notice--info}-->

## Часть I - Получение ID0

{% include /inc/id0_movable.txt %}

### Часть III - BannerBomb 

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

___

## **Следующий шаг:** [Установка CFW с помощью Fredtool](fredtool)
{: .notice--success}
