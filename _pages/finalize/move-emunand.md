---
title: Перенос EmuNAND в SysNAND
permalink: /move-emunand.html
author_profile: true
---
{% include toc title="Разделы" %}

Этот дополнительный раздел содержит информацию о переносе содержимого EmuNAND в новый SysNAND с кастомной прошивкой, с последующим удалением раздела, содержащего EmuNAND. Помните, что RedNAND и EmuNAND - немного разные реализации [одного и того же](http://3dbrew.org/wiki/NAND_Redirection){:target="_blank"}.

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки {% include inc/btn.txt btn="START" %} при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку {% include inc/btn.txt btn="A" %} для выбора "GodMode9" при выполнении этих инструкций.

**Для продолжения, у вас уже ДОЛЖНА быть установлена Luma3DS и boot9strap**
{: .notice--danger}

## Что понадобится

* Существующий EmuNAND
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"}
* Свежая версия [FBI](fbi){:target="_blank"}

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Вставьте SD-карту обратно в консоль

### Часть II - Бэкап сохранений DSiWare из SysNAND

Если у вас нет игр DSiWare или важных для вас сохранений, пропустите эту часть.

{% include inc/launch_godmode9.txt console="на **исходной 3DS**" %}
1. Перейдите в `[2:] SYSNAND TWLN` -> `title`
1. Удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать папку `00030004`, затем выберите "Copy to 0:/gm9/out"
  + Этот процесс может занять некоторое время, если у вас много DSiWare игр
1. Дважды нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню

### Часть III - Бэкап сохранений GBA VC

Если у вас нет игр GBA VC или важных для вас сохранений, пропустите эту часть.
{: .notice--info}

Обратите внимание, что эти действия не требуется выполнять для любых других типов Virtual Console (GBC, NES и т. д.)
{: .notice--info}

Сохранение будет скопировано в папку `/gm9/out/` на SD-карте с именем `<TitleID>.gbavc.sav`.
{: .notice--info}

Чтобы идентифицировать Title ID в имени файла `<TitleID>.gbavc.sav`, вы можете посмотреть список всех установленных игр и соответствующих им Title ID. Выделите диск `[A:] SYSNAND SD`, затем удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %} и выберите "Search for titles".
{: .notice--info}

Выполните действия ниже для каждой игры GBA VC, для сохранений которых вы хотите создать бэкап:
1. Запустите игру GBA VC
1.  Выйдите из игры GBA VC

{% include inc/launch_godmode9.txt console="на **исходной 3DS**" %}
1. Перейдите в `[S:] SYSNAND VIRTUAL`
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `agbsave.bin`
1. Выберите "AGBSAVE options..."
1. Выберите "Dump GBA VC save"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки

### Часть IV - Копирование EmuNAND в SysNAND

{% include inc/launch_godmode9.txt console="на **исходной 3DS**" %}
1. Перейдите в `[E:] EMUNAND VIRTUAL`
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `nand.bin`, затем выберите "NAND image options...", затем "Restore SysNAND (safe)"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND и введите указанную комбинацию кнопок
  + Это действие не перезапишет установленный boot9strap
1. Введите указанную комбинацию кнопок чтобы разрешить запись в SysNAND (lvl1)
  + Этот процесс займет некоторое время
1. Когда процесс завершится, нажмите {% include inc/btn.txt btn="A" %} для продолжения
1. Нажмите {% include inc/btn.txt btn="B" %}, если появится запрос, чтобы не восстанавливать запрет на запись в раздел
1. Нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню

### Часть V - Восстановление сохранений DSiWare

Если вы не создавали бэкап сохранений DSiWare ранее, пропустите эту часть.
{: .notice--info}

1. Перейдите в `[0:] SDCARD` -> `gm9` -> `out`
1. Нажмите {% include inc/btn.txt btn="Y" %}, выбрав папку `00030004` чтобы скопировать ее
1. Дважды нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню
1. Перейдите в `[2:] SYSNAND TWLN` -> `title`
1. Нажмите {% include inc/btn.txt btn="Y" %} чтобы вставить папку `00030004`
1. Выберите "Copy path(s)"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Выберите "Overwrite file(s)"
  + Этот процесс может занять некоторое время, если у вас много DSiWare игр
1. Нажмите {% include inc/btn.txt btn="B" %}, если появится запрос, чтобы не восстанавливать запрет на запись в раздел
1. Дважды нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню

### Часть VI - Восстановление сохранений GBA VC

Если вы не создавали бэкап сохранений GBA VC ранее, пропустите эту часть.
{: .notice--info}

Чтобы идентифицировать Title ID в имени файла `<TitleID>.gbavc.sav`, вы можете посмотреть список всех установленных игр и соответствующих им Title ID. Удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %} в главном меню GodeMode9, затем выберите "Search for titles".
{: .notice--info}

1. Удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="START" %} чтобы выключить консоль
1. Загрузитесь в SysNAND консоли
1. Выполните нижеуказанные действия для каждой игры GBA VC, для которой вы хотите восстановить сохранения из резервной копии:
	+ Запустите игру GBA VC
	+ Выйдите из игры GBA VC
	+ Включите консоль кнопкой питания, держа нажатой кнопку {% include inc/btn.txt btn="START" %}, чтобы запустить меню Luma3DS chainloader
	+ Запустите GodMode9, нажав кнопку {% include inc/btn.txt btn="A" %}
	+ Перейдите в `[0:] SDCARD` -> `gm9`
	+ Нажмите {% include inc/btn.txt btn="Y" %} чтобы скопировать файл сохранения `<TitleID>.gbavc.sav`, который вы хотите восстановить
	+ Нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню
	+ Перейдите в `[S:] SYSNAND VIRTUAL`
	+ Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `agbsave.bin`
	+ Выберите "AGBSAVE options..."
	+ Выберите "Inject GBA VC save"
	+ Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
	+ Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки
	+ Запустите игру GBA VC
	+ Выйдите из игры GBA VC
1. Запустите GodMode9, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки

### Часть VII - Создание резервной копии (бекап) SysNAND

{% include /inc/sysnand_backup.txt %}
1. **Сделайте резервную копию всех файлов на SD-карте, поскольку в следующих шагах карта будет отформатирована.**

### Часть VIII - Форматирование SD-карты

1. Вставьте SD-карту обратно в консоль
1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для вызова меню
1. Выберите "More..."
1. Выберите "SD format menu"
1. Нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Выберите "No EmuNAND"
1. Выберите "Auto"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы подтвердить метку `GM9SD`
  + При желании вы можете ввести другую метку для SD-карты
1. При появлении запроса, введите указанную комбинацию кнопок
1. Удерживая {% include inc/btn.txt btn="R" %} нажмите {% include inc/btn.txt btn="B" %} для того, чтобы извлечь SD-карту
1. Вставьте SD-карту в компьютер
1. Скопируйте на нее файлы, которые вы сохранили несколько шагов назад
  + Убедитесь, что вы заменили `boot.firm` его версией из сохраненных ранее файлов
1. Вставьте SD-карту обратно в консоль
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы смонтировать SD-карту
1. Нажмите {% include inc/btn.txt btn="START" %}, чтобы перезагрузиться

Если после включения экран остаётся чёрным, перейдите к разделу с [проблемами и их решениями](troubleshooting#Черный-экран-при-загрузке-sysnand){:target="_blank"}
{: .notice--info}

Если у вас пропали все игры, но в настройках они есть, подсвеченные серым цветом - у вас поломались тикеты. Починить можно обратившись к разделу [Проблемы и их решения](https://3ds.customfw.xyz/troubleshooting#игры-пропали-из-меню-home-и-в-настройках-они-серые){:target="_blank"}
{: .notice--info}

___

## [Завершение установки](finalizing-setup).
{: .notice--success}