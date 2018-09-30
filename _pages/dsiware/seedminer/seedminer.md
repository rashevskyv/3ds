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

# Инструкция 

{% include /inc/id0_movable.txt %}

## Часть III - Переносим уязвимую DSiWare-игру на SD-карту

1. Запустите приставку, которую вы собираетесь взламывать
	* SD-карта должна находится в приставке 
	* К этому моменту [лицензионная копия уязвимой DSiWare-игры](installing-boot9strap-dsiware-game-injection-list){:target="_blank"} должна быть куплена и установлена на консоли
1. Перейдите в системные настройки (System Settings), Управление данными (Data Management), DSiWare
1. Находясь на вкладке Память системы (System Memory), выберите игру и нажмите кнопку Копировать (Copy) и нажмите OK для подтверждения 
1. После окончания копирования, выключите консоль

## Часть IV - Внедрение эксплойта в DSIWare-игру

1. На вашем ПК откройте сайт [https://jisagi.github.io/](https://jisagi.github.io/TADpole-Online/){:target='_blank'}
	* Если сайт не работает, воспользуйтесь [зеркалом](https://jenkins.nelthorya.net/job/DSIHaxInjector/build){:target='_blank'}
1. В поле "DSiWare.bin" (в зеркале - "DsiBin") выберите файл с бекапом DSiWare-игры, с 8-ми символьным именем `XXXXXXXX.bin`, который мы копировали ранее
1. В поле "movable.sed" выберите `movable.sed` (в зеркале - "MovableSed"), который мы сгенерировали ранее
1. В поле "ctsert.bin" выберите `ctsert.bin`, скачанный ранее
1. Разархивируйте скачанные ранее файлы для инжекта (`USA/EUR/JPN.zip`) в удобную для вас папку 
1. В поле "game_XXX.app" выберите `app`-файл из архива, что вы распаковали выше (на сайте-зеркале просто выберите регион вашей приставки)
1. В поле "public_XXX.sav" выберите `sav`-файл из архива, что вы распаковали выше (на сайте-зеркале просто выберите регион вашей приставки)
1. Нажмите "Start" и подождите результата
1. Скачайте полученный файл и назовите его точно так же, как называется ваша DSiWare-игра (8-ми символьным именем `XXXXXXXX.bin`), затем сохраните его в удобном месте.
1. Переместите этот файл в папку `Nintendo 3DS/ID0/ID1/Nintendo DSiWare`, где ID0 и ID1 - разные значения из 32-х символов
1. Согласитесь на замену 
	* Убедитесь, что заменили файл с непропатченной игрой, файлом с пропатченной - тем, что получили с сайта!
  
## Часть V - Перенос инфицированной игры на консоль

1. Вставьте SD-карту обратно в приставку и включите её
1. Перейдите в системные настройки (System Settings), Управление данными (Data Management), DSiWare
1. Находясь на вкладке Карта SD (microSD Card), выберите игру и нажмите кнопку Копировать (Copy) и нажмите OK для подтверждения 
1. После окончания копирования, выйдите в меню Home
1. Запустите DSiWare-игру с внедрённым эксплойтом
1. Нажмите на экран, либо на какую-либо кнопку, чтобы запустить игру и проверить, работает ли сохранение
  + Если игра завершается с ошибкой, касающейся `boot.nds`, или зависает на белом\цветном экране, **значит эксплойт работает и все в порядке!**
  + Если игра работает нормально безо всяких ошибок, значит вам следует остановится и выяснить на каком этапе вы допустили оплошность

## Часть VI - Прошивка FIRM целевой 3DS

1. Вставьте SD-карту приставки в компьютер
1. Скопируйте `boot.3dsx` (Homebrew Menu 2.0.0) в корень SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `boot.nds` (B9STool) в корень SD-карты 3DS
1. Верните SD-карту обратно в приставку
1. Откройте b9sTool, запустив DSiWare-игру с эксплойтом
	+ Если не видите игру, попробуйте пролистать все экраны.
1. Кнопкой {% include inc/btn.txt btn="A" %} выберите 'Install boot9strap' и нажмите одновременно {% include inc/btn.txt btn="START" %} + {% include inc/btn.txt btn="SELECT" %}
1. Когда увидите надпись "Done!", нажмите кнопку {% include inc/btn.txt btn="HOME" %}, затем подтвердите выход, нажав на "ОК". Приставка выключится
  + При необходимости выключите консоль принудительно, удерживая кнопку питания
  
## Часть VII - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
		
___
		
## [Завершение установки](finalizing-setup)
{: .notice--success}