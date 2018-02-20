---
title: "Установка и обновление freeshop" #
lang: ru
permalink:  freeshop.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

{% include /inc/olx_vk.txt %}
{: .notice--info}

* Прошитая приставка 
* Установленный и рабочий [FBI](fbi){:target="_blank"}
* Свежая версия [freeshop](https://notabug.org/evi/freeShop/releases){:target="_blank"} *(`.cia` файл)*

Действия для обновления и установки freeshop идентичны

## Часть I - Установка freeshop

1. [Установите freeshop](games){:target="_blank"} любым удобным методом
	+ Отсканируйте QR-код, если решите воспользоваться методом установки через QR
	
    ![]({{"/images/QR/freeshop.jpg" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

## Часть II - Настройка freeshop

Приложение работает только при включенном интернете!
{: .notice--info}

1. Запустите консоль
1. Запустите приложение freeshop из меню Home
1. Дождитесь пока программа обновится
1. Перейдите в настройки программы. Для этого на нижнем экране нажмите ![]({{"/images/fs/settings.png" | absolute_url }}){:target="_blank"}
1. Перейдите во вкладку "Обновление" (Update)
1. Поставьте галочку напротив первого пункта - "Авто-обновление ключей приложения через URL" (Auto-update title keys from URL)
	+ Если галочка уже стоит и там вписан URL-адрес, нажмите на ![]({{"/images/fs/trash.png" | absolute_url }}){:target="_blank"}, чтобы его удалить
1. Нажмите на ![]({{"/images/fs/qr.png" | absolute_url }}){:target="_blank"} и отсканируйте QR 

    ![]({{"/images/QR/freeshop_keys.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

	+ Если у вас не работает камера, нажмите на ![]({{"/images/fs/kb.png" | absolute_url }}){:target="_blank"} и вручную введите `http://3ds.titlekeys.gq/downloadenc`

1. Нажмите кнопку "Обновить кэш"
1. Перезагрузите freeshop

Русский язык крашит freeshop. Не выбирайте его. Если выбрали - удалите config.json из папки 3ds/freeshop и больше не включай русский
{: .notice--danger}

freeshop может некорректно работать, если в имени wifi сети есть точки, пробелы, кириллица, прочее. Желательно, чтобы имя точки доступа состояло только из латинских символов, цифр и знаков подчеркивания. Старайтесь избегать другие символы.
{: .notice--warning}

Если у вас freeshop ругается на неверные или отсутствующие ключи, скачайте предложенный [`zip-архив`](files/freeShop_data.zip){:target="_blank"} и распакуйте его содержимое с заменой в папку `/3ds` на вашей SD-карте (должно получится так: `/3ds/freeshop/файлы`).
{: .notice--warning}

Установка приложений из freeshop происходит с помощью кнопки {% include inc/btn.txt btn="X" %}. Приложение умеет устанавливать игры в режиме ожидания. Для этого нужно выбрать желаемую игру в списке кнопкой {% include inc/btn.txt btn="Y" %}, выйти из freeshop и перевести приставку в режим ожидания. Через время игра будет загружена. 

freeshop практически всегда крашится при выходе с помощью кнопки {% include inc/btn.txt btn="START" %}. Для корректного закрытия программы выйдите в меню Home с помощью кнопки {% include inc/btn.txt btn="HOME" %} и нажмите {% include inc/btn.txt btn="X" %} на тайле freeshop, чтобы закрыть его. 
{: .notice--warning}