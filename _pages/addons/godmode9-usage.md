---
title: Использование GodMode9 #
permalink: /godmode9-usage.html
author_profile: true
---
{% include toc title="Разделы" %}

GodMode9 это полноценный файловый менеджер для Nintendo 3DS, который дает вам доступ к SD-карте, FAT разделам внутри SysNAND или EmuNAND и просто ко всему остальному. Среди других его функций есть возможность копировать, удалять, переименовывать файлы и создавать папки.

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки {% include inc/btn.txt btn="START" %} при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку {% include inc/btn.txt btn="A" %} для выбора "GodMode9" при выполнении этих инструкций.

GodMode9 это мощный инструмент, который имеет возможность модифицировать все что угодно на вашей консоли. Хотя многие из этих модификаций заблокированы системой разрешений, и невозможно случайно выполнить опасные действия без разблокировки разрешений, всегда тщательно следуйте инструкциям и делайте резервные копии на всякий случай.

## Установка или обновление GodMode9
 
Некоторые из инструкций ниже применимы только к последней версии GodMode9, поэтому вы должны выполнить эту часть, чтобы обновить вашу копию программы и все скрипты, прежде чем продолжить. Перезаписывайте существующие файлы.
{: .notice--info}

Установка и обновление программы выполняются одинаково! 
{: .notice--info}

### Что понадобится

* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"}

### Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` GodMode9 в корень SD-карты
1. Вставьте SD-карту обратно в консоль

## Запуск GodMode9

{% include inc/launch_godmode9.txt console="" %}

## Создание резервной копии (бекап) SysNAND

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
{% include /inc/sysnand_backup.txt %}

## Восстановление резервной копии (бекапа) SysNAND

1. [Обновите и скрипты и godmode9](https://3ds.customfw.xyz/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Удерживая {% include inc/btn.txt btn="R" %} нажмите {% include inc/btn.txt btn="B" %} для того, чтобы извлечь SD-карту
1. Вставьте SD-карту в компьютер
1. Скопируйте `<date>_<serialnumber>_sysnand_###.bin` с вашего компьютера в папку `/gm9/out/` на SD-карте, если вы удалили этот файл после создания бэкапа
1. Вставьте SD-карту обратно в консоль
1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для вызова меню
1. Выберите "**Scripts...**"
1. Выберите "**GM9Megascript**"
1. Выберите "**Restoring Options**"
1. Выберите "**SysNAND Restore (safe)**"
1. Выберите ваш бэкап NAND
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl3) и введите указанную комбинацию кнопок
	+ Это действие не перезапишет установленный boot9strap
	+ Этот процесс займет некоторое время
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="B" %}, чтобы вернуться в главное меню
1. Выберите "**Exit**"
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы восстановить запрет на запись, если появится запрос

## Инъекция приложений в "Информация о здоровье и безопасности" (Health & Safety)

В целях поддержания порядка, скопируйте файл `.cia` для инъекции в папку `/cias/` на SD-карте
{: .notice--info}

Обратите внимание, что для инъекции в приложение Информация о здоровье и безопасности (Health & Safety) невозможно использовать файлы больше, чем само приложение (включая игры и другие большие приложения)
{: .notice--info}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Перейдите в `[0:] SDCARD` -> `cias`
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать ваш файл `.cia`, затем выберите "**CIA image options...**", затем "**Mount image to drive**"
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `.app`, затем выберите "**NCCH image options**", затем "**Inject to H&S**"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="A" %}, если появится запрос, чтобы восстановить запрет на запись

## Восстановление приложения "Информация о здоровье и безопасности"

Эта инструкция сработает, только если процесс инъекции был выполнен при помощи GodMode9 (не Decrypt9 или Hourglass9).
{: .notice--info}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для вызова меню
1. Выберите "**More...**"
1. Выберите "**Restore H&S**"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы восстановить запрет на запись, если появится запрос

## Создание дампа картриджа

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. Вставьте картридж, который вы хотите сдампить, в консоль
    + дампы картриджей 3DS будут иметь формат `.cia`
    + дампы картриджей NDS будут иметь формат `.nds`, совместимый с флеш-картриджами и эмуляторами
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Перейдите в `[C:] GAMECART`
1. Выполните действия ниже, соответствующие вашему типу картриджа:
  + **3DS картридж:** Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `[TitleID].trim.3ds`, затем выберите "NCSD image options...", затем "Build CIA from file"
  + **NDS картридж:** Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `[TitleID].trim.nds`, затем выберите "Copy to 0:/gm9/out"
1. Ваш файл в формате `.cia` либо `.nds` будет помещен в папку `/gm9/out/` на SD-карте

## Создание дампа тайтла

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Выделите диск, соответствующий типу нужного вам тайтла:
	+ **Пользовательский тайтл**: `[A:] SYSNAND SD`
	+ **Системный тайтл**: `[1:] SYSNAND CTRNAND`
1. Удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %}, чтобы открыть параметры диска
1. Выберите "Search for titles"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `.tmd`, затем выберите "TMD file options...", затем "Build CIA (standard)"
1. Ваш файл в формате `.cia` будет помещен в папку `/gm9/out/` на SD-карте

## Конвертация из .3DS в .CIA

{% capture notice-7 %}
+ В целях соблюдения порядка, скопируйте каждый файл `.3ds`, который вы хотите конвертировать, в папку `/cias/` на SD-карте
    + Заметьте, что если вы хотите конвертировать файл `.3ds`, который уже записан на флеш-картридж, вам нужно следовать инструкции [Создание дампа картриджа](#dump_cart){:target="_blank"}
+ Для успешной конвертации вам понадобится втрое больше места на SD-карте, чем весит сам оригинальный образ игры в формате 3DS
{% endcapture %}

<div class="notice--info">{{ notice-7 | markdownify }}</div>

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Перейдите в `[0:] SDCARD` -> `cias`
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать ваш файл `.3ds`, затем выберите "NCSD image options...", затем "Build CIA from file"
1. Ваш файл в формате `.cia` будет помещен в папку `/gm9/out/` на SD-карте

## Бэкап сохранений GBA VC

Сохранение будет скопировано в папку `/gm9/out/` на SD-карте с именем `<TitleID>.gbavc.sav`.
{: .notice--info}

Чтобы идентифицировать Title ID в имени файла `<TitleID>.gbavc.sav`, вы можете посмотреть список всех установленных игр и соответствующих им Title ID. Выделите диск `[A:] SYSNAND SD`, затем удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %} и выберите "Search for titles".
{: .notice--info}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. Выполните нижеуказанные действия для каждой игры GBA VC, для которой вы хотите сделать резервные копии сохранений:
+ Запустите игру GBA VC
+ Выйдите из игры GBA VC
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
+ Перейдите в `[S:] SYSNAND VIRTUAL`
+ Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `agbsave.bin`
+ Выберите "**AGBSAVE options...**"
+ Выберите "**Dump GBA VC save**"
+ Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
+ Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки

## Восстановление сохранений GBA VC

Чтобы идентифицировать Title ID в имени файла `<TitleID>.gbavc.sav`, вы можете посмотреть список всех установленных игр и соответствующих им Title ID. Выделите диск `[A:] SYSNAND SD`, затем удерживая {% include inc/btn.txt btn="R" %}, нажмите {% include inc/btn.txt btn="A" %} и выберите "Search for titles".
{: .notice--info}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. Выполните нижеуказанные действия для каждой игры GBA VC, для которой вы хотите восстановить сохранения из резервной копии:
+ Запустите игру GBA VC
+ Выйдите из игры GBA VC
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
+ Перейдите в `[0:] SDCARD` -> `gm9`
+ Нажмите {% include inc/btn.txt btn="Y" %} чтобы скопировать файл сохранения `<TitleID>.gbavc.sav`, который вы хотите восстановить
+ Нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню
+ Перейдите в `[S:] SYSNAND VIRTUAL`
+ Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `agbsave.bin`
+ Выберите "**AGBSAVE options...**"
+ Выберите "**Inject GBA VC save**"
+ Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
+ Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки
+ Запустите игру GBA VC
+ Выйдите из игры GBA VC

## Форматирование SD-карты

**Обратите внимание, что это сотрет всё содержимое вашей SD-карты!**
{: .notice--danger}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для вызова меню
1. Выберите "**More...**"
1. Выберите "**SD format menu**"
1. Выберите любую опцию EmuNAND, подходящую вам
  + Большинству пользователей следует выбрать "**No EmuNAND**"
1. Выберите "**Auto**"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы подтвердить метку `GM9SD`
  + При необходимости вы можете ввести другую метку для SD-карты
1. При появлении запроса, введите указанную комбинацию кнопок

## Шифровка / Расшифровка файла .CIA

В целях соблюдения порядка, скопируйте каждый файл `.cia` для шифровки / расшифровки в папку `/cias/` на SD-карте
{: .notice--info}

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Перейдите в `[0:] SDCARD` -> `cias`
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы выбрать файл `.cia`, затем выберите "CIA image options..."
1. Выберите опцию для выполнения нужной функции:
    + **Encrypt to 0:/gm9out:** Создать шифрованную копию выбранного файла `.cia` в папке `/gm9/out/` на SD-карте
    + **Decrypt to 0:/gm9out:** Создать расшифрованную копию выбранного файла `.cia` в папке `/gm9/out/` на SD-карте
    + **Encrypt inplace:** Заменить выбранный файл `.cia` его шифрованной версией
    + **Decrypt inplace:** Заменить выбранный файл `.cia` его расшифрованной версией
1. Ваш шифрованный / расшифрованный файл `.cia` будет помещен в выбранную папку

## Удаление NNID без форматирования устройства

1. [Обновите и скрипты и godmode9](/godmode9-usage#установка-или-обновление-godmode9){:target="_blank"}
1. [Запустите GodMode9](/godmode9-usage#запуск-godmode9){:target="_blank"}, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для запуска меню
1. Выберите "**Scripts...**"
1. Выберите "**GM9Megascript**"
1. Выберите "**Scripts from Plailect's Guide**"
1. Выберите "**Remove NNID**"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="B" %}, чтобы вернуться в главное меню
1. Выберите "**Exit**"
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы восстановить запрет на запись, если появится запрос
1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки приставки