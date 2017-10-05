---
title: "Проблемы и их решения"
permalink: /troubleshooting.html
author_profile: true
---

Если ваша консоль не загружается, найдите раздел, соответствующий вашей проблеме, и следуйте его инструкциям. После решения возникшей проблемы, вернитесь к основному руководству
(Этот раздел весьма обширный, воспользуйтесь Ctrl+F для поиска своей проблемы)

Если решения вашей проблемы здесь не оказалось, то загрузите содержимое всех .log файлов из корня SD-карты на [Gist](https://gist.github.com/), а затем обращайтесь за помощью, детально описав проблему и испробованные способы решения.

Для использования [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme)-ссылок в этом руководстве необходим torrent-клиент, например [Deluge](http://dev.deluge-torrent.org/wiki/Download)

{% include toc title="Разделы" %}
&nbsp;

## DSi / DS игры не работают после завершения руководства
<a name="twl_broken" />

### Что понадобится:

* TWL_FIRM `.cia`, соответствующие вашему устройству
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`New_3DS TWL_FIRM - v9936.cia`](magnet:?xt=urn:btih:eab8558c97b18b1f329a2bfcc3c899b84c082a27&dn=New%5F3DS%20TWL%5FFIRM%20-%20v9936.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
    + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`Old_3DS TWL_FIRM - v8817.cia`](magnet:?xt=urn:btih:17511eadb6e6f3ff22d04f90644e37bd2d96ca43&dn=Old%5F3DS%20TWL%5FFIRM%20-%20v8817.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`TWL Version Data - v0.cia`](magnet:?xt=urn:btih:4a106681407fede5de95cc8bda635432481f6b5d&dn=TWL%20Version%20Data%20-%20v0.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`DS Internet - v2048.cia`](magnet:?xt=urn:btih:2b9df8496922f2546dfb0b01220068ce53c19d3d&dn=DS%20Internet%20-%20v2048.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`DS Download Play - v1024.cia`](magnet:?xt=urn:btih:b581d3c5d98f5e621fddfc1ce5704bb45bf05a8c&dn=DS%20Download%20Play%20-%20v1024.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`Nintendo DS Cart Whitelist - v11264.cia`](magnet:?xt=urn:btih:7b90d506ad032a581a00035616eaa17a68c48eff&dn=Nintendo%20DS%20Cart%20Whitelist%20-%20v11264.cia&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce)
 
### Инструкция

#### Часть I - Подготовительные работы

1. Создайте папку `cias` в корне SD-карты, если таковой нет
1. Скопируйте `TWL Version Data - v0.cia` в папку `/cias/` на SD-карте
1. Скопируйте `DS Download Play - v1024.cia` в папку `/cias/` на SD-карте
1. Скопируйте `DS Internet - v2048.cia` в папку `/cias/` на SD-карте
1. Скопируйте `Nintendo DS Cart Whitelist - v11264.cia` в папку `/cias/` на SD-карте
1. Скопируйте `New_3DS TWL_FIRM - v9936.cia`  или `Old_3DS TWL_FIRM - v8817.cia` в папку `/cias/` на SD-карте

#### Часть II - Установка

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs"
1. Нажмите (HOME) для выхода из FBI

## Игры высвечиваются в настройках с крестиками, но в меню Home не видны
<a name="lost_tickets" />

Нужно перекачать тикеты

1. Скачайте [tikShop](https://github.com/DanTheMan827/tikShop/releases/download/v1.0.3/tikShop.zip). 
1. Извлеките из архива с программой `.cia-файл` и положите его в удобную для вас папку на SD-карте приставки. 
1. Установите tikShop. Как это сделать [написано здесь](https://3ds.customfw.xyz/games#способ-ii---fbi)
1. Запустите программу. Программа просканирует систему и скачает недостающие тикеты, после чего автоматически запустит eShop. 
1. Закройте eShop и перезагрузите систему.

## Я потерял все данные на SD-карте. Что нужно делать, чтобы восстановить работоспособность? 
<a name="clean_sd" />

Воспользуйтесь [этой](clean_sd) инструкцией

## Не работает интеграция в Health & Safety на устройстве с пониженной прошивкой при помощи Gateway
<a name="gw_fbi" />

Это вызвано крайне некорректной процедурой понижения прошивки Gateway, которая дублирует каждое приложение в системе. Одно из них не используется, но это сбивает с толку систему интеграции в H&S, из-за чего она интегрирует FBI в неиспользуемый дубликат.

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки (START) при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку (A) для выбора "GodMode9" при выполнении этих инструкций.
{: .notice--info}

1. Запустите GodMode9, удерживая (START) во время включения приставки
1. Перейдите в `[1:] SYSNAND CTRNAND` -> `title` -> `00040010`
1. Перейдите в папку, соответствующую вашей приставке и региону:
  + **Old 3DS или Old 2DS EUR**: `00022300` -> `content`
  + **Old 3DS или Old 2DS JPN**: `00020300` -> `content`
  + **Old 3DS или Old 2DS USA**: `00021300` -> `content`
  + **New 3DS или New 2DS EUR**: `20022300` -> `content`
  + **New 3DS или New 2DS JPN**: `20020300` -> `content`
  + **New 3DS или New 2DS USA**: `20021300` -> `content`
1. Заметьте, что есть два вида app и tmp файлов, одни имеют расширение, написанное прописными буквами (`.TMD` и `.APP`), а другие строчными (`.tmd` и `.app`)
1. Удерживая (R), нажмите (Y), чтобы создать новую папку
1. Нажмите (А), чтобы подтвердить название новой папки - `newdir` (название папки не играет роли)
1. Нажмите (A), чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите (B), если появится запрос, чтобы не восстанавливать запрет на запись в раздел
1. Нажмите (L) на каждом файле, расширение которого написано прописными буквами (`.TMD` и `.APP`), чтобы отметить его
1. Нажмите (Y), чтобы скопировать эти файлы
1. Перейдите в папку `newdir`
1. Нажмите (Y), чтобы вставить скопированные ранее файлы
1. Выберите "Move path(s)"
1. Теперь файлы с расширением из прописных букв перемещены в папку `newdir`
1. Нажмите (START) для перезагрузки
1. Вернитесь к разделу [Завершение установки](finalizing-setup) и попробуйте интегрировать FBI еще раз
1. Если это не помогло, верните файлы с расширением `.TMD` и `.APP` обратно в папку `content`, а файлы с расширением `.tmd` и `.app` переместите в папку `newdir`, затем попытайтесь интегрировать FBI еще раз

## Не работает эксплойт на основе браузера
<a name="ts_browser" />

Эксплойты, базирующиеся на браузере (например, browserhax или 2xrsa), нестабильны и часто не срабатывают, но в некоторых случаях это можно исправить, следуя рекомендациям ниже
{: .notice--info}

1. Откройте браузер, затем настройки браузера (Settings)
1. Прокрутите до конца ВНИЗ и выберите "Удалить сохр. данные" (Initialize Savedata/Clear All Save Data)
1. Попробуйте запустить эксплойт еще раз

## Черный экран при загрузке SysNAND
<a name="ts_sys_down" />

1. Попробуйте загрузиться без SD-карты, а затем верните ее в консоль
    1. Выключите консоль
    1. Извлеките SD-карту из консоли
    1. Включите консоль
    1. Когда появится меню Home, вставьте SD-карту обратно в консоль
    1. Если это сработало, вам следует очистить данные меню Home, удалив соответствующую вашему региону папку, находящуюся в`/Nintendo 3DS/(32-значный ID)/(32-значный ID)/extdata/00000000/`
        + EUR регион: Удалите `00000098`
        + JPN регион: Удалите `00000082`
        + USA регион: Удалите `0000008f`
        + CHN регион: Удалите `000000A1`
        + KOR регион: Удалите `000000A9`
        + TWN регион: Удалите `000000B1`
1. Попробуйте включить устройство без каких-либо картриджей (включая флеш-картриджи)
1. Если у вас есть хардмод и резервная копия NAND, прошейте бэкап обратно в SysNAND
1. Попробуйте загрузиться в режим восстановления и обновить систему    
    1. Выключите консоль
    1. Зажмите (L)+(R)+(A)+(ВВЕРХ)
    1. Включите консоль
    1. Если вы вошли в режим восстановления, обновите консоль.
1. Ваша консоль, скорее всего, превратилась в брик. Вы можете обратиться за поддержкой на канал [Nintendo Homebrew в Discord](https://discord.gg/MWxPgEp) (англ.), [группу 3DS_CFW вконтакте](http://vk.com/3ds_cfw) (рус.)

## Черный экран при загрузке SysNAND после установки b9s
<a name="ts_sys_b9s" />

1. Убедитесь, что у вас установлен рабочий загрузчик
    1. Проверьте, есть ли в корне SD-карты файл `boot.firm`.
1. Попробуйте сбросить настройки Luma3DS
    1. Удалите файл `/luma/config.bin` с SD-карты
    1. Выберите нужные настройки при запуске
1. Попробуйте запустить GodMode9
    1. Для устройства с Luma3DS, зажмите (START) при включении
1. Попробуйте очистить данные меню Home
    1. Чтобы очистить данные меню Home перейдите в папку `/Nintendo 3DS/(32 Character ID)/(32 Character ID)/extdata/00000000/`на SD-карте и удалите папку, соответствующую вашему региону
        + EUR регион: Удалите `00000098`
        + JPN регион: Удалите `00000082`
        + USA регион: Удалите `0000008f`
        + CHN регион: Удалите `000000A1`
        + KOR регион: Удалите `000000A9`
        + TWN регион: Удалите `000000B1`
1. Попробуйте включить устройство без каких-либо картриджей (включая флеш-картриджи)
1. Если вы понижали прошивку через Gateway, то убедитесь, что у вас установлена самая последняя версия Luma3DS (не ниже 6.2.3)
1. Если версия вашего NAND между 3.0.0 и 4.5.0, проделайте следующие действия:
	+ Убедитесь, что используете самую свежую версию Luma 3DS (6.6, или выше)
	+ Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/00000056) и переименуйте его в `native.firm`
	+ Скачайте [этот файл](http://nus.cdn.c.shop.nintendowifi.net/ccs/download/0004013800000002/cetk)
	+ Скопируйте `native.firm` и `cetk` в папку `/luma/` на SD-карте
	+ Если у вас Luma3DS версии 7.1 или ниже, переименуйте `native.firm` в `firmware.bin`
	+ После обновления прошивки удалите оба этих файла
1. Попробуйте выполнить [CTRTransfer](ctrtransfer)
1. Вы можете обратиться за поддержкой на канал [Nintendo Homebrew в Discord](https://discord.gg/MWxPgEp) (англ.), или [группу 3DS_CFW вконтакте](http://vk.com/3ds_cfw) (рус.).

## Не запускается ни один пейлоадер. Сразу запускается консоль
<a name="payloaders_fault" />

{% capture notice-10 %}

+ Убедитесь, что зажали кнопку, соответствующую пейлоадеру до включения приставки.
+ Убедитесь, что на карте памяти лежит пейлоадер, соответствующий типу установленного взлома - .firm для b9s и .bin для a9lh
+ Для luma3ds ниже версии 7, следует в начале имени пейлоадера писать кнопку, отвечающую за его вызов. Например, переименовав decrypt9.bin в x_decrypt9.bin, вы сможете запустить Decrypt9WIP, зажав (X) при включении консоли
+ Если вы уверены, что все у вас правильно, а пейлоадер все равно не запускается, сделайте резервную копию всех файлов на SD-карте и отформатируйте ее, а замет верните все файлы обратно и попробуйте еще раз
+ Попробуйте другую карту памяти
{% endcapture %}

<div class="notice--info">{{ notice-10 | markdownify }}</div>

## Игры часто зависают с ошибкой

Если у вас приставка линейки New, убедитесь, что в настройках Luma3DS отключен разгон: 

1. Выключите приставку
1. Включите консоль с зажатым (SELECT)
1. Отключите разгон:
	* Установите значение поля **New 3DS CPU** в положение **Off**
	
Если не помогло, попробуйте Legacy-ветку Luma3DS

1. Скачайте [Luma3DS 7.1 Legacy](files/boot.firm)
1. Поместите скачанный файл в корень карты памяти с заменой
1. Вставьте SD-карту в приставку и перезагрузите её
1. Устройство загрузится в меню настройки Luma3DS
  + Если после включения экран остаётся чёрным, то перейдите к разделу [проблемы и их решения](troubleshooting#черный-экран-при-загрузке-sysnand-после-установки-b9s)
1. Нажимая (A) выберите следующие пункты:    
  + **"Enable game patching"**
  + **"Show NAND or user string in System Settings"**
1. Если у вас **New 3DS**, вы *также* можете включить следующие опции:
  + **"New 3DS CPU" выбрать значение "Clock+L2(x)"**
    + Это увеличит частоту кадров в множестве игр, но может отразиться на стабильности других
    + Если какие-либо игры работают некорректно, отключите эту опцию
	
    ![]({{ base_path }}/images/screenshots/luma-settings.png)
	{: .text-center}
    {: .notice--info}

## После обновления Luma3DS через Luma3DS Updater и теперь приставка не включается. Загорается синий диод и тухнет
<a name="lumaupdater" />

Вы установили Luma3DS на не поддерживаемый boot. 
{: .notice--warning}

Сперва попробуем определить boot какой версии прошит в приставку.
{: .notice--info}

### Способ I - CTRNAND

Если прошивка выполнялась по этому гайду , то в CTRNAND приставки должны были быть скопированы файлы прошивки. Следовательно, вынув КП из приставки и запустив 3DS, вы сможете запустить Luma и увидеть её версию, из чего легко сделать вывод о том, какой загрузчик стоит в системе.
{: .notice--info}

1. Отключите 3DS
1. Достаньте КП из приставки
1. Загрузите приставку с зажатой кнопкой (SELECT)
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s)
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s), если вы не знаете какая именно у вас стоит сейчас

    ![]({{ base_path }}/images/screenshots/luma.png)
	{: .text-center}
    {: .notice--info}

### Способ II - Перебор

Этот метод для тех, кто по каким-то причинам не стал устанавливать Luma3DS в CTRNAND, либо для тех, кто обновился до b9s 1.0 в момент его выхода и обновил Luma3DS через Luma3DS Updater
{: .notice--info}

1. Выключаем консоль
1. Вставляем SD-карту из приставки в компьютер
1. Качаем [Luma3DS 7.0.5](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.0.5)
1. Копируем `arm9loaderhax.bin` из архива `Luma3DSv7.0.5.7z` в корень карты памяти с заменой
1. Возвращаем карту памяти в консоль
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас a9lh - [перейдите на b9s актуальной версии](a9lh-to-b9s). 
  + Если не сработало, двигаемся дальше
1. Качаем [Luma3DS 7.1](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1) 
1. Копируем `boot.firm` из архива `Luma3DSv7.1.7z` в корень карты памяти с заменой 
1. Возвращаем карту памяти в консоль 
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас b9s 1.0 и нужно обновить его до актуальной версии по инструкции (updating-b9s)
  + Если не сработало, двигаемся дальше
1. Качаем [свежую версию Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest)
1. Копируем `boot.firm` из `7z-архива` Luma3DS в корень SD-карты с заменой 
1. Возвращаем SD-карту в консоль 
1. Пробуем запустить приставку. 
1. Если сработало и приставка запустилась, то у вас b9s или выше и самая последняя версия Luma3DS. Можете [обновить b9s до актуальной версии](updating-b9s), если вы не знаете какая именно у вас стоит сейчас
  + Если ничего не помогло, попробуйте выполнить [CTRTransfer](ctrtransfer)

## Голубой экран при загрузке (bootrom error)
<a name="ts_sys_blue" />

1. У вас брик
	+ Если вы делали хардмод, попробуйте его отпаять полностью
1. Для восстановления вам понадобится [хардмод](https://gbatemp.net/threads/414498/) (англ.) или ремонт / замена устройства

