---
title: CTRTransfer
permalink: /ctrtransfer.html
author_profile: true
---
{% include toc title="Разделы" %}

Это дополнительный раздел, рассказывающий об установке образа 11.5.0 CTRTransfer на ваше устройство.

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки {% include inc/btn.txt btn="START" %} при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку {% include inc/btn.txt btn="A" %} для выбора "GodMode9" при выполнении этих инструкций. 

Для продолжения, у вас уже ДОЛЖНА быть установлена Luma3DS и boot9strap.

Не обращайте внимание на версию установленного системного ПО. Всё будет хорошо, даже если версия вашего ПО выше, или ниже, чем версия ПО в образе CTRTransfer.
{: .notice--danger}

## Что понадобится

* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"}
* Свежая версия [FBI](https://github.com/Steveice10/FBI/releases/latest){:target="_blank"} *(`.3dsx-файл`)*
* CTRTransfer-образ 11.5.0 для вашего устройства и региона 
*(если вашего региона нет в списке, выберите любой, подходящий типу вашего устройства)*:
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS or 2DS - 11.5.0 - EUR - CTRTransfer](magnet:?xt=urn:btih:465f1048f81e8e5c651ce2a4d9df48fec88d1099&dn=11.5.0-38E_ctrtransfer_n3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)    
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS or 2DS - 11.5.0 - JPN - CTRTransfer](magnet:?xt=urn:btih:70f641c9f2a4933a07fac49eb7ad19451c7c8c96&dn=11.5.0-38J_ctrtransfer_n3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)    
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS or 2DS - 11.5.0 - KOR - CTRTransfer](magnet:?xt=urn:btih:c9e4de20d30b80032a5dd6f675fecb6d748f71b1&dn=11.5.0-34K_ctrtransfer_n3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)    
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [New 3DS or 2DS - 11.5.0 - USA - CTRTransfer](magnet:?xt=urn:btih:2b0a71a2523328e447938fea7b4c02ebe0b72705&dn=11.5.0-38U_ctrtransfer_n3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)    
~
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [Old 3DS or 2DS - 11.5.0 - EUR - CTRTransfer](magnet:?xt=urn:btih:df0836a731778ab6ffe9a8c658400c782f0225cd&dn=11.5.0-38E_ctrtransfer_o3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)     
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [Old 3DS or 2DS - 11.5.0 - JPN - CTRTransfer](magnet:?xt=urn:btih:d8913b4c0da224e8852fa2f685c41ddbce5310bc&dn=11.5.0-38J_ctrtransfer_o3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)     
  +    <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [Old 3DS or 2DS - 11.5.0 - USA - CTRTransfer](magnet:?xt=urn:btih:2708089605ca47387fa64e996a699eedd18031e8&dn=11.5.0-38U_ctrtransfer_o3ds.zip&tr=udp%3A%2F%2F9.rarbg.to%3A2710%2Fannounce&tr=udp%3A%2F%2Fbt.xxx-tracker.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fexodus.desync.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fmgtracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fopen.demonii.si%3A1337%2Fannounce&tr=udp%3A%2F%2Fpublic.popcorn-tracker.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fthetracker.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.cypherpunks.ru%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.ds.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.mg64.net%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.port443.xyz%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.qt.is%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce&tr=udp%3A%2F%2Ftracker.vanitycore.co%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker-2.msm8916.com%3A6969%2Fannounce)    

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `3ds` в корне SD-карты, если таковой нет
1. Скопируйте `FBI.3dsx` в папку `/3ds/` на SD-карте
1. Создайте папку `/luma/payloads/` в корне SD-карты, если таковой нет
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `.bin` файл из `.zip-архива` с образом 11.5.0 CTRTransfer в папку `/gm9/in` на SD-карте
1. Вставьте SD-карту обратно в консоль

### Часть II - CTRTransfer

{% include inc/launch_godmode9.txt console="" %}
1. Выберите "**Scripts...**"
1. Выберите "**GM9Megascript**"
1. Выберите "**CTRNAND trnsfer...**"
1. Выберите из списка на нижнем экране образ, подготовленный для переноса, нажав кнопку {% include inc/btn.txt btn="A" %}
1. Нажмите {% include inc/btn.txt btn="A" %}
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы разрешить запись в SysNAND (lvl2) и введите указанную комбинацию кнопок
	+ Этот процесс займет некоторое время
1. Если появится запрос, выберите "**Transfer to SysNAND**"
	+ Этот запрос отображается только если у вас есть EmuNAND
1. По завершению процесса, нажмите {% include inc/btn.txt btn="A" %}
1. Дважды нажмите {% include inc/btn.txt btn="B" %} для возврата в главное меню
1. Выберите "**Scripts from Plailect's Guide**"
1. Выберите "**CTRTransfer Ticket Copy**"
1. При появлении запроса, нажмите {% include inc/btn.txt btn="A" %} для продолжения
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="B" %}, чтобы вернуться в главное меню
1. Выберите "**Exit**"
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы восстановить запрет на запись
1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки
1. Обновите прошивку консоли, зайдя в **Системные настройки** (System Settings), затем "**Прочие настройки**" (Other Settings), затем листайте вправо до конца и выберите пункт "**Обновление**" (System Update)
	+ Обновление консоли с установленным B9S + Luma (установлено у вас) безопасно
	+ При появлении ошибки, поставьте в настройках подключения, в настройках DNS "Получать DNS автоматически" в положение "Да"

### Часть III - Запуск Homebrew Launcher

{% include /inc/hbl.txt content="Homebrew Launcher" %}

### Часть IV - Переустановка тикетов

Если скрипт не нашел пользовательских ticket-файлов и просил вас пропустить эту часть (Skip the 'Reinstalling Tickets' section), пропустите эту часть
{: .notice--info}

1. Выберите в списке Homebrew FBI и запустите его
1. Перейдите в `SD` -> `cias`
1. Нажмите {% include inc/btn.txt btn="B" %}, чтобы вернуться в папку "SD"
1. Выберите "**gm9**"
1. Выберите "**out**"
1. Выберите "**ctrtransfer_tickets**"
1. Выполните шаги ниже либо для папки `eshop` либо для папки `unknown`, или для обоих
	+ Перейдите в папку
	+ Выберите "**\<current directory>**"
	+ Выберите "**Install and delete all tickets**"
	+ Ожидайте. Может показаться, что приставка зависла, просто дайте ей время.
	+ Нажмите {% include inc/btn.txt btn="A" %} для подтверждения
	+ Нажмите {% include inc/btn.txt btn="B" %} для отмены установки тикетов из CDN.
1. Нажмите {% include inc/btn.txt btn="HOME" %} для выхода из FBI

### Часть V - Удаление образа CTRTransfer

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки {% include inc/btn.txt btn="START" %} при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку {% include inc/btn.txt btn="A" %} для выбора "GodMode9" при выполнении этих инструкций. 
{: .notice--info}

1. Запустите GodMode9, держа нажатой кнопку {% include inc/btn.txt btn="START" %} во время загрузки
1. Перейдите в `[0:] SDCARD` -> `gm9`
1. Нажмите {% include inc/btn.txt btn="X" %}, выделив файл `.bin` CTRTransfer чтобы удалить его
1. Нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}