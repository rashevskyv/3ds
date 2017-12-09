---
title: "Использование читов в 3DS-играх" #
lang: ru
permalink:  cheats.html
author_profile: true
---

{% include toc title="Разделы" %}

Использование читов в онлайн-играх почти наверняка приведёт вас к бану.
{: .notice--warning}

## Что понадобится

{% include /inc/olx_vk.txt %}
{: .notice--info}

* Установленный и рабочий [FBI](fbi){:target="_blank"}
* Установленный и рабочий [b9s](updating-b9s){:target="_blank"} последней версии 
* Свежая версия [BootNTR Selector](https://github.com/Nanquitas/BootNTR/releases/latest){:target="_blank"} (`BootNTRSelector-FONZD-Banner.cia`)
**Для пользователей Old 3DS:** Свежая версия [BootNTR Selector Mode3](https://github.com/Nanquitas/BootNTR/releases/latest){:target="_blank"} (`BootNTRSelector-Mode3-FONZD-Banner.cia`)
**Пользователи Old 3DS должны скачать обе версии**
* Плагин `<pluginName>.plg` для выбранной игры. 

К сожалению одной определенной базы с чит-плагинами не существует. Вам придется самому найди этот файл. Для начала попробуйте поискать [здесь](http://ntrplugins.shoutwiki.com/wiki/Plugins){:target="_blank"} (англ.), [здесь](http://www.elotrolado.net/wiki/Cheats_para_NTR#Listado_de_trucos){:target="_blank"} (исп.) или [здесь](http://www.speedfly.cn/category/game/nintendo/3ds_cheat/){:target="_blank"} (кит.) и обратиться в гугл. Запрос может выглядеть следующим образом: "название_игры cheat plg 3ds".

## Часть I - Подготовительные работы

1. Установите BootNTR Selector. Как это сделать [написано здесь](games#способ-ii---fbi){:target="_blank"}
1. **Для пользователей Old 3DS:** Установите BootNTR Selector Mode3. То есть пользователи старых можелей должны установить ОБЕ версии.
1. Зайдите в FBI > Titles и найдите установленную игру к которой вы собираетесь применить читы
1. Запишите или запомните Title ID игры, к которой вы собираетесь применить читы (выделите игру и ищите Title ID на верхнем экране)

![]({{ base_path }}/images/screenshots/addons/fbi_titleid.png){:target="_blank"}
{: .text-center}

1. Отключите приставку
1. Вставьте SD-карту приставки в ПК
1. Создайте папку `plugin` в корне SD-карты 
1. Создайте папку названием которой будет Title ID выбранной игры
1. Положите в эту папку скачанный чит-плагин для выбранной игры
1. Верните SD-карту в приставку
1. Включите консоль

## Часть II - Первичная настройка BootNTR Selector

Если вы запускаете BootNTR Selector не в первый раз и уже настраивали его в прошлом, пропустите эту часть
{: .notice--info}

1. Запустите BootNTR Selector
  + Используйте BootNTR Selector Mode3, если у вас Old 3DS и игра, для которой вы хотите применить чит, использует расширенную память          
      + Проще говоря, если у вас Old 3DS и читы не работают на BootNTR Selector, попробуйте BootNTR Selector Mode3.
1. Нажмите кнопку "Use defaults"
1. Нажмите кнопку "Save Settings"
1. Выберите "3.6". Программа закроется - это нормально
1. Перезагрузите приставку

## Часть III - Запуск BootNTR Selector

1. Запустите BootNTR Selector, через несколько секунд программа закроется сама. Это значит, что все идет по плану и работает выбранная версия NTR. Проверить работает ли NTR CFW можно нажатием {% include inc/btn.txt btn="X" %} + {% include inc/btn.txt btn="Y" %}.
1. Запустите игру
1. Дождитесь геймплей
1. Нажмите {% include inc/btn.txt btn="X" %} + {% include inc/btn.txt btn="Y" %} для активации меню NTR CFW
1. Выберите пункт "Game Plugins"
1. Выберите "Activate Cheat"
1. Выберите читы и наслаждайтесь нечестной игрой

## Часть IV - Решение проблем

Если не работает:

+ Используйте BootNTR Selector Mode3, если у вас Old 3DS и игра, для которой вы хотите применить чит, использует расширенную память          
  + Проще говоря, если у вас Old 3DS и читы не работают на BootNTR Selector, попробуйте BootNTR Selector Mode3.
+ Проверьте верно ли названа папка в папке `plugins`. Название вложенной папки должно совпадать с Title ID запускаемой игры
+ Убедитесь в том, что запускаете плагин нужного региона. 
+ Часто плагины для n3ds и old3ds разные
+ Убедитесь в том, что правильно активируете чит-плагин. Часто для каждого плагина комбинация кнопок может отличаться
