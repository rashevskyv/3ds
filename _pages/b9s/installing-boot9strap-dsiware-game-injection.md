---
title: "Установка boot9strap (Инъекция в игры DSiWare)" #
lang: ru
permalink: installing-boot9strap-dsiware-game-injection.html
author_profile: true
---

{% include toc title="Разделы" %}

{% include /inc/dsiware.txt 

needed_list="* Купленная (или уже имеющаяся) DSiWare-игра из eShop на **исходной 3DS**
  + Пиратская копия игры **НЕ** будет работать
  + Список совместимых игр ищите на странице [Установка boot9strap (Список уязвимых игр DSiWare)](installing-boot9strap-dsiware-game-injection-list)
* Версия sudokuhax injection `.zip`для вашего региона:
  + <i class='fa fa-magnet' aria-hidden='true' title='Это магнитная ссылка. Используйте торрент-клиент для работы с ней.'></i> - [`DSiWare_usa_sudokuhax_injection.zip`](magnet:?xt=urn:btih:7ed7fee15c900ed02b5e2cb3c8e7a0363f4d9354&dn=DSiWare_usa_sudokuhax_injection.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce)
  + <i class='fa fa-magnet' aria-hidden='true' title='Это магнитная ссылка. Используйте торрент-клиент для работы с ней.'></i> - [`DSiWare_eur_sudokuhax_injection.zip`](magnet:?xt=urn:btih:1542dd3c2bf7785b1e7a6dda3887fc8fb2710685&dn=DSiWare_eur_sudokuhax_injection.zip&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce)
  + <i class='fa fa-magnet' aria-hidden='true' title='Это магнитная ссылка. Используйте торрент-клиент для работы с ней.'></i> - [`DSiWare_jpn_4swordshax_injection.zip`](magnet:?xt=urn:btih:1bcc90c93da91c9876671f6218084207def90db9&dn=DSiWare_jpn_4swordshax_injection.zip&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce)"

part1="1. Скопируйте `.app-файл` и папку `savedata` из `.zip-архива` с DSiWare injection, соответствующего региону консоли в корень SD-карты **исходной 3DS**"

part2="### Часть II - Инъекция игры и сохранения

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки (START) при загрузке будет запускать 'chainloader menu', где вам нужно будет использовать D-Pad и кнопку (A) для выбора 'GodMode9' при выполнении этих инструкций.
{: .notice--info}

1. Включите **исходную 3DS** кнопкой питания, держа нажатой кнопку (START), чтобы запустить GodMode9
1. Если вам предложат создать бэкап важных файлов, нажмите кнопку (A) чтобы сделать это, затем нажмите (A) чтобы продолжить после завершения
1. Если вам предложат выставить RTC дату и время, нажмите (A) чтобы сделать это, настройте дату и время, затем нажмите (A) чтобы продолжить
	+ Обратите внимание, что если вы выставили RTC дату и время, вам также придется настроить время в Системных настройках после этого руководства
1. Перейдите в `[0:] SDCARD`
1. Нажмите (Y) на `.app`-файле из архива с файлами для инжекта DSiWare, который вы скопировали на КП ранее
1. Нажмите (B) для возврата в главное меню
1. Перейдите в `[2:] SYSNAND TWLN` -> `title` -> `00030004` -> `(8-ми значный ID)`
  + 8-значный ID смотрите на странице [Установка boot9strap (Список уязвимых игр DSiWare)](installing-boot9strap-dsiware-game-injection-list)
  + Папку `[2:] SYSNAND TWLN` не будет видно, если у вас не [b9s 1.2](update-luma3ds#определение-типа-и-версии-взлома). 
1. Перейдите в папку `content`
1. Нажмите (A) на `.app-файле`, находящемся в папке
1. Выберите 'Inject data @offset'
1. Нажмите (A), чтобы выбрать смещение `00000000`
1. Нажмите (A), чтобы разрешить запись в SysNAND и введите указанную комбинацию кнопок
1. Нажмите (B) чтобы перейти на уровень выше
1. Перейдите в `data`
1. Нажмите (A) на `public.sav`
1. Выберите 'Mount as FAT image'
1. Нажмите (B), чтобы вернуться в главное меню
1. Перейдите в `[0:] SDCARD`
1. Нажмите (Y) на файле(ах) в папке `savedata`, чтобы скопировать их
  + Если в папке `savedata` есть папка `savedata` - это не ошибка. Вам следует скопировать вложенную папку `savedata`, а не файлы в ней.
1. Нажмите (B) для возврата в главное меню
1. Перейдите в `[7:] FAT IMAGE`
1. C помощью кнопки (X) удалите все содержимое папки `[7:] FAT IMAGE`
1. Нажмите (Y), чтобы вставить **скопированное содержимое** папки `savedata`в `[7:] FAT IMAGE`
1. Выберите 'Copy path(s)'
1. Нажмите (A), чтобы разрешить запись в SysNAND и введите указанную комбинацию кнопок
1. Нажмите (START) для перезагрузки **исходной 3DS**
1. Запустите DSiWare-игру на **исходной 3DS**
1. Нажмите на экран, либо на какую-либо кнопку, чтобы запустить игру и проверить, работает ли сохранение
  + Если игра завершается с ошибкой, касающейся `boot.nds`, или просто в белый экран, **значит эксплойт работает и все в порядке!**
  + Если игра жалуется на поврежденный или неверный файл сохранения (corrupted or inaccessible), убедитесь, что скопировали именно **содержимое** папки `savedata`, а не саму папку
  + Если игра работает нормально безо всяких ошибок, значит вам следует остановится и выяснить на каком этапе вы допустили оплошность
  + Если появляется черный экран, обратитесь к разделу с [проблемами и их решениями](troubleshooting#dsids-игры-не-работают-на-прошитой-приставке)"

test=""
  
%}