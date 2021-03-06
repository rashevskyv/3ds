---
title: Завершение установки
permalink:  finalizing-setup.html
---

{% include toc title="Разделы" %}

## Описание шагов

Файл `boot.firm` - это то, что boot9strap запускает после загрузки из NAND, и этот файл может быть любым arm9-приложением. Этот файл может быть заменён когда угодно, однако Luma3DS позволяет запускать другие arm9 приложения в FIRM формате, используя свой загрузчик.

Мы используем Luma3DS от [AuroraWright](https://github.com/AuroraWright/){:target="_blank"}, чтобы запускать пропатченный SysNAND напрямую, поэтому необходимость в каком-либо виде EmuNAND полностью пропадает, что значительно упрощает использование взломанной 3DS и экономит место на SD-карте.

В процессе мы установим и настроим следующие программы:    

+ **FBI** *(установка	 приложений и игр в формате CIA)*
+ **Anemone3DS** *(установка пользовательских тем)*
+ **Checkpoint** *(резервное копирование и восстановление сохранений для игр 3DS и DS)*
+ **GodMode9** *(многофункциональная утилита для работы с NAND и картриджами)*
+ **Homerew Launcher Loader** *(запускает Homebrew Launcher в качестве обычного приложения благодаря магии Rosalina)*
+ **ftpd** *(просто ftp-клиент для простого доступа к карте памяти без разбора приставки)*
+ **Luma3DS Updater** *(удобное обновление CFW)*
+ **ctr-no-timeoffset** *(программа, убирающая смещение между часами системы приставки и RTC)*

## Что понадобится

* Свежая версия {% include /inc/files/3dssdfiles.txt %}

## Инструкция

### Часть I - Настройка Luma3DS

Если вы уже конфигурировали Luma3DS, то повторно этого делать не нужно
{: .notice--info}

{% include /inc/luma_setup.txt %}

### Часть II - Подготовительные работы

Если в предыдущих пунктах вы скидывали на карту 3DSSDFiles, то переходите к следующей части. Повторно скидывать не нужно
{: .notice--info}

1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

{% capture browserhax %}

#### Восстановление DNS

1. Включите консоль
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Интернет-настройки**" (Internet Settings) -> "**Настройки подключения**" (Connection Settings)
1. Нажмите на вашем активном интернет-соединении (если такового нет, добавьте) и нажмите "**Изменить настройки**" (Change Settings) -> пролистайте вправо, нажав на стрелку в правой части экрана -> "**DNS**"
1. Выберите "**Да**" ("Yes")
1. Нажмите "**ОК**", затем "**Сохранить**" (Save)
	* Тест должен пройти успешно

{% endcapture %}
<div class="hidden" id="browserhax">{{ browserhax | markdownify }}</div>

{% capture fredtool %}

#### Восстановление работы меню Подключения Nintendo DS

1. Отключите приставку, если она включена
1. Вставьте карту памяти в ПК 
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении *movable.sed*
1. Скопируйте файл `42383841.bin`, находящийся в архиве `fredtool_output.zip` по пути `output/clean/` в папку `Nintendo DSiWare` с заменой
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Управление данными**" (Data Management) -> "**DSiWare**"
1. Выберите "**Карта SD**" (SD Card) и нажмите на "**Nintendo DSi™**"
1. Выберите "**Копировать**", затем нажмите "**ОК**"

{% endcapture %}
<div class="hidden" id="fredtool">{{ fredtool | markdownify }}</div>

### Часть III - Обновление системы

Если текущий регион вашей приставки вас не устраивает, сейчас лучшее время для того, чтобы его [сменить](region-changing){:target="_blank"}. После того, как поменяете регион, вернитесь к этому руководству, чтобы продолжить дальше.
{: .notice--warning}

{% include /inc/sys_update.txt %}

### Часть IV - Запуск HBL

{% include /inc/hbl.txt content='**Загружаемая игра (Download Play)**' icon=', нажав на <img src="/images/icons/download-play-icon.png" alt="соответствующую иконку" height="24px" width="24px">' %}

### Часть V - Дополнительные настройки

1. Выберите из списка "**ctr-no-timeoffset**" и запустите его
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы выставить смещение между RTC и системными часами в 0
  + Благодаря этому мы синхронизируем часы на приставке с аппаратными часами реального времени, что в будущем нам пригодится
1. Нажмите {% include inc/btn.txt btn="START" %} для возвращения в **Homebrew Launcher**

### Часть VI - Установка необходимых программ

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите "**\<current directory>**"
1. Выберите "**Install and delete all CIAs**" и нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Нажмите {% include inc/btn.txt btn="HOME" %} для возврата в меню Home

### Часть VII - Настройка Homebrew Launcher

{% include /inc/hbl.txt content='**the homebrew launcher**' icon=', нажав на <img src="/images/icons/hbl-icon.png" alt="соответствующую иконку" height="24px" width="24px">' %}
1. Выберите **slotTool**
1. Выберите "**RESTORE original wifi slots 1,2,3**", приставка перезагрузится

### Часть VIII - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

### Часть IX - Создание резервной копии (бекап) SysNAND

{% include /inc/sysnand_backup.txt %}

### Часть X - Дополнительные материалы

{% include /inc/finalize_addons.txt %}

___

{% include /inc/finalize_footer.md %}

<script>
	bh = localStorage.getItem('browserhax')
	ft = localStorage.getItem('fredtool')

	if (bh == "1") {
		document.querySelector('#browserhax').classList.remove("hidden")
	}

	if (ft == "1") {
		document.querySelector('#fredtool').classList.remove("hidden")
	}

	localStorage.clear();
</script>