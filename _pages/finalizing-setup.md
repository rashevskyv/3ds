---
title: Завершение установки вручную #
lang: ru
permalink:  finalizing-setup.html
author_profile: true
---

{% include toc title="Разделы" %}

## Описание шагов

Файл `boot.firm` - это то, что boot9strap запускает после загрузки из NAND, и этот файл может быть любым arm9-приложением. Этот файл может быть заменён когда угодно, однако Luma3DS позволяет запускать другие arm9 приложения в FIRM формате, используя свой загрузчик.

Мы используем Luma3DS от [AuroraWright](https://github.com/AuroraWright/){:target="_blank"}, чтобы запускать пропатченный SysNAND напрямую, поэтому необходимость в каком-либо виде EmuNAND полностью пропадает, что значительно упрощает использование взломанной 3DS и экономит место на SD-карте.

В процессе мы установим и настроим следующие программы:    

+ **FBI** *(установщик приложений и игр в формате CIA)*
+ **Anemone3DS** *(установка пользовательских тем)*
+ **Checkpoint** *(резервное копирование и восстановление сохранений для игр 3DS и DS)*
+ **GodMode9** *(многофункциональная утилита для работы с NAND и картриджами)*
+ **freeshop** *(open source клон eShop, облегчающий поиск игр)*
+ **Homerew Launcher Loader** *(запускает Homebrew Launcher в качестве обычного приложения благодаря магии Rosalina)*
+ **ftpd** *(просто ftp-клиент для простого доступа к карте памяти без разбора приставки)*
+ **Luma3DS Updater** *(удобное обновление CFW)*
+ **ctr-no-timeoffset** *(программа, убирающая смещение между часами системы приставки и RTC)*

## Что понадобится

* [Homebrew Menu v2.0.0](https://github.com/fincs/new-hbmenu/releases/latest){:target="_blank"}
* Свежая версия [Checkpoint](https://github.com/BernardoGiordano/Checkpoint/releases/latest){:target="_blank"} *(`.cia`-файл)*
* Свежая версия [DSP1](https://github.com/zoogie/DSP1/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [FBI](https://github.com/Steveice10/FBI/releases/latest){:target="_blank"} *(`.cia-файл` и `.3dsx-файл`)*
* Свежая версия [freeshop](https://notabug.org/arc13/freeShop/releases){:target="_blank"} *(`.cia` файл)*
* Свежая версия [ftpd](https://github.com/mtheall/ftpd/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [ctr-no-timeoffset](https://github.com/ihaveamac/ctr-no-timeoffset/releases/latest)
* Свежая версия [Homebrew Launcher Wrapper](https://github.com/mariohackandglitch/homebrew_launcher_dummy/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [Luma3DS Update](https://github.com/KunoichiZ/lumaupdate/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [Anemone3DS](https://github.com/astronautlevel2/Anemone3DS/releases/latest){:target="_blank"} *(`.cia`-файл)*
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"} *(`.zip`-архив)*
* [`cleanmaster.gm9`]({{ "/gm9_scripts/cleanmaster.gm9" | absolute_url }}){:target="_blank"}

## Инструкция

### Часть I - Подготовительные работы

1. Отключите приставку
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` (Homebrew Menu 2.0.0) в корень SD-карты
1. Создайте папку `3ds` в корне SD-карты, если таковой нет
1. Скопируйте `FBI.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `ctr-no-timeoffset.3dsx` в папку `/3ds/` на SD-карте
1. Создайте папку `cias` в корне SD-карты, если таковой нет
1. Скопируйте `Checkpoint.cia` в папку `/cias/` на SD-карты
1. Скопируйте `DSP1.cia` в папку `/cias/` на SD-карты
1. Скопируйте `FBI.cia` в папку `/cias/` на SD-карты
1. Скопируйте `freeshop.cia` в папку `/cias/` на SD-карты
1. Скопируйте `ftpd.cia` в папку `/cias/` на SD-карты
1. Скопируйте `Homebrew_Launcher.cia` в папку `/cias/` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Скопируйте `Anemone3DS.cia` в папку `/cias/` на SD-карты

    ![]({{ "/images/screenshots/cias-file-layout.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Создайте папку `payloads` в папке `luma` на SD-карте, если таковой нет
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `cleanmaster.gm9` в папку `/gm9/scripts/` на SD-карте

    ![]({{ "/images/screenshots/finalizing-setup-file-layout.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Включите приставку

### Часть II - Обновление системы

После выхода 11.8 появились опасения того, что Nintendo сможет отслеживать пользователей freeshop и прицельно их банить. Если ваша приставка на прошивке от 11.4 и отсутствие бана для вас весомо, вы воспользовались методом прошивки [ntrboot](ntrboot){:target="_blank"}, не обновляйте приставку! В настройках подключения пропишите первичный DNS `159.203.242.044`
{: .notice--warning}

{% include /inc/if_emunand.txt %}
{% include /inc/sys_update.txt %}

### Часть III - Запуск HBL

{% include /inc/hbl.txt content="Homebrew Launcher" %}
1. Выберите из списка "ctr-no-timeoffset" и запустите его
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы выставить смещение между RTC и системными часами в 0
  + Благодаря этому мы синхронизируем часы на приставке с аппаратными часами реального времени, что в будущем нам пригодится
1. Нажмите {% include inc/btn.txt btn="START" %} для возвращения в Homebrew Launcher

### Часть IV - Установка CIA

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs" и нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Нажмите {% include inc/btn.txt btn="HOME" %} для возврата в меню Home

### Часть V - DSP Dump

1. Запустите приложение DSP1
1. После завершения работы программы, нажмите {% include inc/btn.txt btn="B" %}, чтобы автоматически удалить программу из меню Home

### Часть VI - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

### Часть VII - Создание резервной копии (бекап) SysNAND

{% include /inc/sysnand_backup.txt %}

### Часть VIII - Дополнительные материалы

{% include /inc/finalize_addons.txt %}

___

{% include /inc/finalize_footer.txt %}
