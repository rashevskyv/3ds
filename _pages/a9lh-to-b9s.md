---
title: "Переход с A9LH на boot9strap" #
lang: ru
permalink: a9lh-to-b9s.html
author_profile: true
---
{% include toc title="Разделы" %}

Эта страница предназначена для пользователей arm9loaderhax, чтобы обновить их устройства до boot9strap.

Все будущие релизы Luma3DS будут только в формате `.firm`, который будет совместим только с boot9strap и sighax. Это означает, что для того, чтобы продолжать получать последние обновления Luma3DS, вы должны использовать эту страницу для обновления установки.

Если в Luma3DS вы используете PIN-код, то при работе SafeB9SInstaller вы получите ошибку "OTP Crypto Fail". Для решения этой проблемы временно откажитесь от использования PIN-кода (вы сможете включить его обратно после обновления).
{: .notice--warning}

Для использования [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme)-ссылок в этом руководстве необходим torrent-клиент, например [Deluge](http://dev.deluge-torrent.org/wiki/Download)
{: .notice--success}

{% capture notice-1 %}
Сообщается о волне банов, выданных Nintendo пользователям CFW. Чтобы защитить себя, выполните следующие шаги перед началом этого руководства:

1. Откройте Системные настройки (System settings), затем "Интернет-настройки" (Internet Settings), затем "SpotPass", затем "Отправка информации о системе" (Sending of System Information)
1. Отключите опцию "Отправка информации о системе" (Sending of System Information)
1. Закройте Системные настройки (System settings)
1. Откройте Список друзей (Friend's List) (значок в виде лица на верхней строчке меню Home, на нижнем экране)

    ![]({{ base_path }}/images/screenshots/friend-list.jpg)
	{: .text-center}
    {: .notice--info}

  + Если появляется ошибка и вас не пускают в меню, значит Список друзей уже отключен
1. Перейдите в настройки Списка друзей, затем "Настройки сообщений друга" (Friend Notification Settings), затем "Показать друзьям, во что вы играете" (Show friends what you're playing)
1. Отключите опцию "Показать друзьям, во что вы играете"
1. Закройте Список друзей
{% endcapture %}

<div class="notice--danger">{{ notice-1 | markdownify }}</div>

## Что понадобится

Обратите внимание, что `secret_sector.bin` необходим для отката эксплойта arm9loaderhax, поэтому он не требуется для установки на не взломанную консоль. **Если у вас не New 3DS, вам не нужен `secret_sector.bin`**й.
{: .notice--info}

Требуемый ниже файл с именем `secret_sector.bin` это тот же, что присутствовал в различных версиях архива `data_input.zip`. Если у вас уже есть этот файл где-то на диске, вы можете использовать его, вместо загрузки файла ниже.
{: .notice--info}

* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - **Только для пользователей New 3DS:** [`secret_sector.bin`](magnet:?xt=urn:btih:15a3c97acf17d67af98ae8657cc66820cc58f655&dn=secret_sector.bin&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl% 3A2710%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce)
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z-архив`)*
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(стандартный boot9strap; не `devkit-файл`, не `ntr-файл` и не `devkit-ntr-файл`)*
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest)
* Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
* Свежая версия [Luma3DS Updater](https://github.com/KunoichiZ/lumaupdate/releases/latest)
* [`setup_ctrnand_luma3ds.gm9`]({{ "/gm9_scripts/setup_ctrnand_luma3ds.gm9" | absolute_url }})
* [`cleanup_sd_card.gm9`]({{ "/gm9_scripts/cleanup_sd_card.gm9" | absolute_url }})

## Инструкция

#### Часть I - Определение версии загрузчика 

Сначала нужно определить каким методом приставка взломана. 

1. Отключите 3DS
1. Загрузите приставку с зажатой кнопкой (SELECT)
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s)
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s), если вы не знаете какая именно у вас стоит сейчас

    ![]({{ "/images/screenshots/luma.png" | absolute_url }})
	{: .text-center}
    {: .notice--info}

#### Часть II - Подготовительные работы

Для всех шагов в этой части перезаписывайте любые существующие файлы на SD-карте.
{: .notice--info}

1. Перейдите в Системные настройки (System Settings), Управление данными (Data Managment), Nintendo 3DS, Программы (Software) и удалите Luma3DS Updater
1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте _содержимое_ архива `starter.zip` в корень SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Создайте папку `cias` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Удалите все существующие `.bin` приложения в папке `/luma/payloads/` на SD-карте, так как они не будут совместимы с boot9strap-совместимыми версиями Luma3DS
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `setup_ctrnand_luma3ds.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `cleanup_sd_card.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `SafeB9SInstaller.bin` из `.zip-архива` SafeB9SInstaller в папку `/luma/payloads/` на SD-карте
1. Переименуйте`SafeB9SInstaller.bin` в папке `/luma/payloads/` на SD-карте в `start_SafeB9SInstaller.bin`
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. **Только для пользователей New 3DS:** Скопируйте `secret_sector.bin` в папку `/boot9strap/` на SD-карте

    ![]({{ base_path }}/images/screenshots/updating-to-b9s-file-layout.png)
	{: .text-center}
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль

#### Часть III - Установка boot9strap

1. Включите консоль кнопкой питания, держа нажатой кнопку (START), чтобы запустить меню Luma3DS chainloader
  + Некоторые версии Luma3DS будут напрямую запускать любое приложение, начинающееся со `start_`. Если вместо меню chainloader запускается SafeB9SInstaller, просто следуйте инструкции.
1. Запустите SafeB9SInstaller, нажав кнопку (A) на нём
  + При возникновении ошибки попробуйте использовать другую SD-карту, или отформатировать имеющуюся (предварительно сделав резервную копию всего её содержимого)
1. Дождитесь окончания всех проверок безопасности
  + Если вы получаете сообщение об ошибке "OTP Crypto Fail", скачайте <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`aeskeydb.bin`](magnet:?xt=urn:btih:d25dab06a7e127922d70ddaa4fe896709dc99a1e&dn=aeskeydb.bin&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce), поместите этот файл в папку `/boot9strap/` на SD-карте и попробуйте снова
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки.
  + Если ваше устройство выключается при загрузке, убедитесь что вы скопировали `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты

#### Часть IV - Настройка Luma3DS

Эта часть требуется только в том случае, если после перезагрузки появилось меню настроек Luma3DS.
{: .notice--info}

1. В меню настроек Luma3DS используйте кнопки (A) и D-Pad чтобы включить следующее:    
  + **"Enable game patching"**
  + **"Show NAND or user string in System Settings"**
1. Если у вас **New 3DS**, вы *также* можете включить следующие опции:
  + **"New 3DS CPU" выбрать значение "Clock+L2(x)"**
    + Это увеличит частоту кадров в множестве игр, но может отразиться на стабильности других
    + Если какие-либо игры работают некорректно, отключите эту опцию
	
    ![]({{ base_path }}/images/screenshots/luma-settings.png)
	{: .text-center}
    {: .notice--info}

1. Нажмите (START), чтобы сохранить настройки и перезагрузиться
  
#### Часть V - Обновление системы

Если прежде чем начать выполнять действия из этого руководства у вас уже был установлен EmuNAND и вы хотите перенести содержимое EmuNAND в SysNAND с кастомной прошивкой - сейчас самый подходящий момент. Выполните действия из раздела [перенос EmuNAND](move-emunand), перед выполнением этой части. Если EmuNAND у вас нет, или вы не знаете что это такое - просто следуйте руководству дальше. 
{: .notice--info}

1. Обновите прошивку консоли, зайдя в Системные настройки (System Settings), затем "Прочие настройки" (Other Settings), затем листайте ВПРАВО до конца и выберите пункт "Обновление" (System Update)
  + Обновление консоли с установленным B9S + Luma (установленых у вас) безопасно
  + При появлении ошибки, поставьте в настройках подключения, в настройках DNS "Получать DNS автоматически" в положение "Да"
  + Если вы все еще получаете ошибку [выполните CTRTransfer](ctrtransfer) и попробуйте обновиться еще раз

#### Часть VI - Установка Luma3DS Updater

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите `lumaupdater.cia`
1. Выберите "Install CIA", затем нажмите (A) для подтверждения
1. Нажмите (HOME) для выхода из FBI
  
#### Часть VII - CTRNAND Luma3DS

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки (START) при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку (A) для выбора "GodMode9" при выполнении этих инструкций.
{: .notice--info}

Если перед переходом на boot9strap у вас есть EmuNAND, данные из которого вы хотели бы сохранить, самое время воспользоваться инструкцией по [переносу EmuNAND](move-emunand) в SysNAND, а уже после выполнять данную часть.
{: .notice--info}

1. Запустите GodMode9, удерживая (START) во время включения приставки
1. Если вам предложат создать бэкап важных файлов, нажмите кнопку (A) чтобы сделать это, затем нажмите (A) чтобы продолжить после завершения
1. Если вам предложат выставить RTC дату и время, нажмите (A) чтобы сделать это, настройте дату и время, затем нажмите (A) чтобы продолжить
	+ Обратите внимание, что если вы выставили RTC дату и время, вам также придется настроить время в Системных настройках после этого руководства
1. Нажмите (HOME), чтобы попасть в меню действий
1. Выберите "Scripts..."
1. Выберите "setup_ctrnand_luma3ds"
1. Когда появится запрос, нажмите (A) для подтверждения
1. Нажмите (A), чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите (A) чтобы продолжить
1. Нажмите (A) чтобы вновь заблокировать права на запись

##### Часть VIII - Создание бэкапа SysNAND

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "Backup SysNAND"
1. Нажмите (A) для подтверждения
	+ Этот процесс займет некоторое время
1. Нажмите (A), чтобы продолжить
1. Удерживая (R) нажмите (B) для того, чтобы извлечь SD-карту
1. Вставьте SD-карту в компьютер
1. Скопируйте `<YYMMDD>_<serialnumber>_sysnand_###.bin` из папки `/gm9/out/` на SD-карте в безопасное место на вашем компьютере
	+ Сделайте несколько резервных копий в нескольких местах (например в облачном хранилище)
	+ Эти бэкапы позволят восстановить консоль, если впоследствии что-то пойдёт не так
	+ Замените ваш старый бэкап NAND с arm9loaderhax на новый с boot9strap
1. После копирования удалите `<YYMMDD>_<serialnumber>_sysnand_###.bin` из папки `/gm9/out/` на SD-карте
1. Вставьте SD-карту обратно в консоль

##### Часть IX - Очистка SD-карты

Помните, что скрипт, используемый ниже, удалит папки `/boot9strap/` и `/cias/` с SD-карты!
{: .notice--danger}

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "cleanup_sd_card"
1. При появлении запроса, нажмите (A) для продолжения
1. Нажмите (A), чтобы продолжить
1. Нажмите (START) для перезагрузки

После работы скрипта корень SD-карты будет выглядеть следующим образом: 

![]({{ base_path }}/images/screenshots/final-file-layout.png)
{: .text-center}

___

Эта версия Luma3DS Updater позволяет работать с boot9strap, путем загрузки и распаковки последнего Luma3DS `boot.firm`.
{: .notice--info}

{% capture notice-6 %} 
Для запуска конфигуратора Luma3DS включите консоль с зажатой кнопкой (SELECT). 
<br><br>
Теперь вы можете удерживать (START) при загрузке для запуска меню Luma3DS chainloader (обратите внимание, что меню Luma3DS chainloader отображается только если существует более одного приложения).
<br><br>
Теперь, с помощью зажатой комбинации клавиш (START) + (SELECT) + (X) при включении консоли, вы сможете сохранить копии ARM11 bootrom (`boot11.bin`), ARM9 bootrom (`boot9.bin`) и уникального [OTP](otp) вашей консоли (`OTP.bin`) в папку `/boot9strap/` на SD-карте (обратите внимание, что этот процесс не предусматривает отображения какого-либо оповещения).
{% endcapture %}

<div class="notice--info">{{ notice-6 | markdownify }}</div>