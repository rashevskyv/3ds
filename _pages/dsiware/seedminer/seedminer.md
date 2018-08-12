---
title: Установка boot9strap с помощью майнинга ключа (seedminer)
permalink: /seedminer.html
author_profile: true
---

{% include toc title="Разделы" %}

Это очень комплексный метод! Его все еще активно разрабатывают, однако уже сейчас с его помощью можно взломать 3DS на прошивке {% include /vars/sys_version.txt %} используя только одну не взломанную Nintendo 3DS и потратившись только на покупку одной единственной DSiWare-игры.  

Но это на бумаге. 

На практике же вам все равно понадобится персональный компьютер с достаточно мощной видеокартой (именно поэтому seed**miner**). Вам ничего не мешает использовать для майнинга ПК друга, или попросить помощи у сообщества - для этого есть целый сайт. 

Чем мощнее ваше железо, тем быстрее будет результат! Если у вас нет мощного железа, или времени или желания внимательно следовать инструкции - изучите этот [сайт](https://bruteforcemovable.com/){:target='_blank'} (англ.). С его помощью можно смайнить необходимые файлы используя очередь и мощности ПК других пользователей. Ниже мы подробно рассмотрим как это работает.

В процессе выполнения этого метода придётся взламывать уникальный ключ вашей приставки. Видеокарта делает это быстрее всего (от нескольких секунд до двух часов), разумеется можно вычислять и на процессоре, но это будет на порядок дольше (от 6 часов до *нескольких __дней__!!!*). Так же ничего не мешает майнить ключ через облако на компьютере волонтёров. 

# Немного теории

Ещё на заводе в процессор **каждой** приставки вшит уникальный ключ (подробнее об этом можно почитать [тут](https://arxiv.org/pdf/1802.00359.pdf){:target='_blank'} (англ.)). Именно этим ключом в консоли зашифрованы все игры и сохранения к ним (содержимое папки Nintendo 3DS). Метод DSiWare заключается в том, что на прошитой приставке мы можем получить доступ к этим файлам в расшифрованном виде, в следствии чего успешно внедрить в них эксплойт и перенести его с помощью стандартного метода переноса прошивки на не взломанную консоль (это если говорить сильно упрощая). И уже на целевой приставке, запустив эксплойт, мы можем заменить FIRM0 и FIRM1 на модифицированные (по счастливой случайности, DSiWare-игры могут адресовать куда угодно, в том числе и в защищённые области).

Чем же отличается seedminer? Мы просто подбираем ключ на основе имеющихся данных и расшифровываем купленную DSiWare-игру. Куда с помощью компьютера инжектим эксплойт, запаковываем обратно и запускаем на приставке. Вот и вся магия. 

Перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!
{: .notice--info}

# Что понадобится 

* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> [`ctcert.bin`](magnet:?xt=urn:btih:2E43EDCDE39663EC42985AD6A3757641C994B184&dn=ctcert.bin&tr=udp%3a%2f%2f9.rarbg.to%3a2710%2fannounce&tr=udp%3a%2f%2fpublic.popcorn-tracker.org%3a6969%2fannounce&tr=udp%3a%2f%2finferno.demonoid.pw%3a3418%2fannounce&tr=udp%3a%2f%2ftracker.vanitycore.co%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.open-internet.nl%3a6969%2fannounce&tr=udp%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.internetwarriors.net%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.zer0day.to%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2ftracker2.christianbro.pw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.piratepublic.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.skyts.net%3a6969%2fannounce&tr=udp%3a%2f%2ftracker4.itzmx.com%3a2710%2fannounce&tr=udp%3a%2f%2fallesanddro.de%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.xku.tv%3a6969%2fannounce&tr=udp%3a%2f%2fopen.facedatabg.net%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.safe.moe%3a){:target="_blank"}
* [seedminer](https://github.com/Mike15678/seedminer/releases/latest){:target='_blank'} для вашей платформы
* [Seedplanter](https://github.com/knight-ryu12/Seedplanter/releases/latest){:target='_blank'}
* Купленная (или уже имеющаяся) DSiWare-игра из eShop на **исходной 3DS**
  + Пиратская копия игры **НЕ** будет работать
  + Список совместимых игр ищите на странице со [списком уязвимых DSiWare-игр )](installing-boot9strap-dsiware-game-injection-list){:target="_blank"}
	+ Если ваша прошивка ниже, чем {% include /vars/sys_version.txt %}, вам придётся [обновить вашу прошивку](update-system#%D1%87%D0%B0%D1%81%D1%82%D1%8C-ii---%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B){:target="_blank"} до последней, иначе вы не сможете зайти в eShop. 
* Версия `.zip` файлов для инжекта для вашего региона:
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - [`EUR.zip`](magnet:?xt=urn:btih:fe5be30f2a2c33e5e350e099804840560cbb6626&dn=EUR.zip&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.open-internet.nl%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.skyts.net%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.piratepublic.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2f9.rarbg.to%3a2710%2fannounce&tr=udp%3a%2f%2fpublic.popcorn-tracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fwambo.club%3a1337%2fannounce&tr=udp%3a%2f%2ftrackerxyz.tk%3a1337%2fannounce&tr=udp%3a%2f%2ftracker4.itzmx.com%3a2710%2fannounce&tr=udp%3a%2f%2ftracker2.christianbro.pw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker1.wasabii.com.tw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.zer0day.to%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.xku.tv%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.vanitycore.co%3a6969%2fannounce&tr=udp%3a%2f%2finferno.demonoid.pw%3a3418%2fannounce&tr=udp%3a%2f%2fopen.facedatabg.net%3a6969%2fannounce&tr=udp%3a%2f%2fmgtracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fipv4.tracker.harry.lu%3a80%2fannounce&tr=udp%3a%2f%2ftracker.christianbro.pw%3a6969%2fannounce){:target="_blank"}
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - 
[`USA.zip`](magnet:?xt=urn:btih:ead76f1e382cad15efaf1ba87c702f7b4c16d6e0&dn=USA.zip&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.open-internet.nl%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.skyts.net%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.piratepublic.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2f9.rarbg.to%3a2710%2fannounce&tr=udp%3a%2f%2fpublic.popcorn-tracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fwambo.club%3a1337%2fannounce&tr=udp%3a%2f%2ftrackerxyz.tk%3a1337%2fannounce&tr=udp%3a%2f%2ftracker4.itzmx.com%3a2710%2fannounce&tr=udp%3a%2f%2ftracker2.christianbro.pw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker1.wasabii.com.tw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.zer0day.to%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.xku.tv%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.vanitycore.co%3a6969%2fannounce&tr=udp%3a%2f%2finferno.demonoid.pw%3a3418%2fannounce&tr=udp%3a%2f%2fopen.facedatabg.net%3a6969%2fannounce&tr=udp%3a%2f%2fmgtracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fipv4.tracker.harry.lu%3a80%2fannounce&tr=udp%3a%2f%2ftracker.christianbro.pw%3a6969%2fannounce){:target="_blank"}
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - [`JPN.zip`](magnet:?xt=urn:btih:b10e9c3289c16c6de8aefcaf3892e2efe267acb8&dn=JPN.zip&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.open-internet.nl%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.skyts.net%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.piratepublic.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2f9.rarbg.to%3a2710%2fannounce&tr=udp%3a%2f%2fpublic.popcorn-tracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fwambo.club%3a1337%2fannounce&tr=udp%3a%2f%2ftrackerxyz.tk%3a1337%2fannounce&tr=udp%3a%2f%2ftracker4.itzmx.com%3a2710%2fannounce&tr=udp%3a%2f%2ftracker2.christianbro.pw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker1.wasabii.com.tw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.zer0day.to%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.xku.tv%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.vanitycore.co%3a6969%2fannounce&tr=udp%3a%2f%2finferno.demonoid.pw%3a3418%2fannounce&tr=udp%3a%2f%2fopen.facedatabg.net%3a6969%2fannounce&tr=udp%3a%2f%2fmgtracker.org%3a6969%2fannounce&tr=udp%3a%2f%2fipv4.tracker.harry.lu%3a80%2fannounce&tr=udp%3a%2f%2ftracker.christianbro.pw%3a6969%2fannounce){:target="_blank"}
{% include /inc/dsiware/3_needed.txt %}
* Достаточно мощный ПК для расшифровки (майнинга) ключа

# Инструкция 

## Установка и проверка Python

1. Перейдите на сайт [https://www.python.org](https://www.python.org/downloads/){:target="_blank"} и скачайте свежую версию Python 3
1. Установите Python 3 на ваш ПК, затем перезагрузите компьютер
1. Убедитесь, что Python работает. Для этого запустите командную строку (`Win + R` => `cmd`) и введите в ней `py -3 --version`. В командной строке высветится текущая версия python. Она должна соответствовать той, что вы скачали и установили ранее
1. Если возникнет ошибка, удалите python из вашей системы (если у вас в системе установлена не только 3-я версия, удалите все) и установите заного

## Часть I - Переносим уязвимую DSiWare-игру на SD-карту

1. Запустите приставку, которую вы собираетесь взламывать
	* SD-карта должна находится в приставке 
	* К этому моменту [лицензионная копия уязвимой DSiWare-игры](installing-boot9strap-dsiware-game-injection-list){:target="_blank"} должна быть куплена и установлена на консоли
1. Перейдите в системные настройки (System Settings), Управление данными (Data Management), DSiWare
1. Находясь на вкладке Память системы (System Memory), выберите игру и нажмите кнопку Копировать (Copy) и нажмите OK для подтверждения 
1. После окончания копирования, выключите консоль

## Часть II - Получение ID0

1. Вставьте SD-карту консоли в компьютер
1. Перейдите в папку `Nintendo 3DS`
1. В папке `Nintendo 3DS` у вас должна быть **одна** папка с длинным 32-х символьным названием - это и есть ваш ID0
1. Скопируйте название этой папки (далее для простоты я буду называть название этой папки просто как ID0) в надёжное место. Далее нам оно понадобится

	![]({{ base_path }}/images/seedminer/ID0.png){:target="_blank"}
	{: .text-center}
	{: .notice--info}
	
	* Если в папке `Nintendo 3DS` у вас несколько папок с длинным 32-х символьным названием, нужно определить какой из ID0 использовать. Для этого: 
		1. Перейдите в корень SD-карты и переименуйте папку `Nintendo 3DS` в `Nintendo 3DS_backup`
		1. Вставьте SD-карту обратно в 3DS и включите приставку
		1. Подождите, пока сгенерируется новая структура данных на SD-карте (во время генерации на нижнем экране выскочит информационное всплывающее окно)
		1. После окончания герерации выключите приставку и вставьте SD-карту в ПК. Теперь в папке `Nintendo 3DS` будет находится одна папка с длинным 32-х символьным названием - это и есть ваш ID0
		1. Скопируйте название этой папки (далее для простоты я буду называть название этой папки просто как ID0) в надёжное место. Далее нам оно понадобится
		1. Вернитесь в корень SD-карты и удалите папку `Nintendo 3DS` (убедитесь, что сохранили свой ID0 в надёжном месте)
		1. Переименуйте папку `Nintendo 3DS_backup` в `Nintendo 3DS`
			* Для порядка можете удалить в папке `Nintendo 3DS` все папки с названием из 32-х символов, кроме той, что совпадает по значению с вашим ID0. Но это не обязательно.
1. Перейдите в папку `Nintendo 3DS/ID0/ID1 (еще одна папка с длинным 32-х символьным названием)/Nintendo DSiWare`
1. В папке вы найдёте файл с 8-ми символьным именем `XXXXXXXX.bin`, скопируйте его в надёжное место
	* Если в папке несколько файлов с такими именами, 8-значный ID вашей игры смотрите на странице [Установка boot9strap (Список уязвимых игр DSiWare)](installing-boot9strap-dsiware-game-injection-list){:target="_blank"}

Выберите один из способов, соответствующих вашей ситуации: 

___
		
# [Создание movable_part1.sed](seedminer-ms1)
{: .notice--success}