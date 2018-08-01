---
title: Обновление системного ПО приставки
permalink: /update-system.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

* Установленный и рабочий [b9s](updating-b9s){:target="_blank"} последней версии (*если уже делали, то повторно делать не нужно*)
* Свежая версия [Luma3DS](update-luma3ds){:target="_blank"} *(`.7z`-архив)*

## Часть I - Проверка версии Luma3DS

1. Выключите приставку
1. Зажмите кнопку {% include inc/btn.txt btn="SELECT" %} и, удерживая её, включите консоль
1. Запустится меню конфигурации Luma3DS

    ![]({{ base_path }}/images/screenshots/luma.png){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Обратите внимание на версию Luma3DS.
1. Если версия Luma3DS ниже, чем {% include /vars/luma_version.txt %}, обновите её следуя [этой](update-luma3ds) инструкции.
	
### Часть II - Обновление системы
{% include /inc/sys_update.txt %}