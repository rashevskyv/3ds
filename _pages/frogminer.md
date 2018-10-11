---
title: Установка CFW с помощью Frogminer
permalink: /frogminer.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

* Свежая версия [b9sTool](https://github.com/zoogie/b9sTool/releases/latest){:target="_blank"}
* Свежая версия {% include /inc/luma_adress.txt %}
* Свежая версия [frogminer_beta](https://jisagi.github.io/FrogminerGuide/public/data/FROGminer_BETA.zip){:target="_blank"}

## Часть I - Подготовка карты памяти

1. Вставьте карту памяти из приставки в ПК 
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `boot.nds` ([b9sTool](https://github.com/zoogie/b9sTool/releases/latest){:target="_blank"}) в корень SD-карты 3DS
1. Скопируйте `Frogtool.3dsx` из `.zip-архива` [frogminer_beta](https://jisagi.github.io/FrogminerGuide/public/data/FROGminer_BETA.zip){:target="_blank"} в папку `3ds`
1. Скопируйте папку `private` из `.zip-архива` [frogminer_beta](https://jisagi.github.io/FrogminerGuide/public/data/FROGminer_BETA.zip){:target="_blank"} в корень вашей карты памяти
1. Вставьте карту памяти обратно в консоль

## Часть II - Замена Download Play на Flipnote Studio

1. Запустите **Steel Diver: Sub Wars**, чтобы попасть в Homebrew Menu
1. Запустите "**Frogtool**"
1. Выберите "**Export clean DS Download Play**"
1. Нажмите на нижний экран, а затем {% include inc/btn.txt btn="START" %}, чтобы вернуться в Homebrew Menu
1. Выключите приставку и вставьте карту памяти в ПК
1. Скопируйте `484E4441.bin` на ПК, он нам скоро понадобится
1. Перейдите на сайт [DSIHaxInjector](https://jenkins.nelthorya.net/job/DSIHaxInjector/build){:target="_blank"}
1. В поле "**Username**" введите имя, которое вы сможете найти в списке позже 
	* вводите латиницей без пробелов
1. В поле "**Region**" выберите регион вашей консоли
1. В поле "**DsiBin**" выберите `484E4441.bin`, который мы сохранили ранее 
1. В поле "**MovableSed**" выберите ваш [`movable.sed`](steelminer#часть-ii---подбор-уникального-ключа-приставки-movablesed){:target="_blank"}, который мы получили ранее
1. Нажмите кнопку "**Собрать**" и ожидайте результата
1. В левой части страницы, в поле "**История сборок**" введите то имя пользователя, что вы указали ранее и нажмите "*Enter*"
1. Перейдите по появившемуся номеру и скачайте ваш `484E4441.BIN.patched_%username%`, где %username% - то имя пользователя, что вы указали ранее
1. Скопируйте  `484E4441.BIN.patched_%username%` в корень карты памяти и переименуйте его в `484E4441.BIN.patched`
1. Вставьте карту памяти в приставку и включите её

## Часть III - Запуск b9sTool

1. Запустите **Steel Diver: Sub Wars**, чтобы попасть в Homebrew Menu
1. Запустите "**Frogtool**"
1. Выберите "**IMPORT patched DS Download Play**"
1. Дождитесь окончания импорта, затем нажмите на нижний экран, чтобы продолжить
1. Выберите "**Boot patched DS Download Play**"
1. Пройдите настройку приложения, пока не получите следующий экран: 

	![]({{ "/images/screenshots/flipnote.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
	{: .notice--info}
	
	* При настройке нажимайте оранжевую кнопку, если появляются две - левую
1. Нажмите на левую кнопку 
1. Нажмите на кнопку с иконкой SD-карты 
1. Нажмите на "лицо", затем на **правую** кнопку внизу экрана 
1. Нажмите на иконку с лягушкой в левой нижней части нижнего экрана
1. Нажмите на вторую сверху кнопку на нижнем экране (с изображением плёнки)
1. Перейдите на третий слайд (3/3) с помощью тачскрина
1. Нажмите на **третью** кнопку (с буквой "А")
1. Перейдите на первый слайд (1/3) с помощью тачскрина
1. Нажмите на **четвёртую** кнопку (с буквой "А"), чтобы запустить b9sTool
1. Выберите "**Install boot9strap**" кнопкой {% include inc/btn.txt btn="A" %}, подтвердите ваши действия, зажав одновременно {% include inc/btn.txt btn="START" %} и {% include inc/btn.txt btn="SELECT" %}
1. Когда увидите надпись "Done!", нажмите кнопку {% include inc/btn.txt btn="HOME" %}, затем подтвердите выход, нажав на "ОК". Приставка выключится
  + При необходимости выключите консоль принудительно, удерживая кнопку питания
1. Включите приставку
  
## Часть IV - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

___

## [Завершение установки](finalizing-setup)
{: .notice--success}