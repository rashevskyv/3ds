---
title: "Установка boot9strap (Инъекция в сохранения DSiWare)" #
lang: ru
permalink: installing-boot9strap-dsiware-save-injection.html
author_profile: true
---

{% include toc title="Разделы" %}

{% include /inc/dsiware.txt 

needed_list="* Купленная DSiWare игра из списка ниже (пиратская копия **не** будет работать) на **исходной 3DS**
	+ **Fieldrunners**
	+ **Legends of Exidia**
	+ **Guitar Rock Tour**  
	+ **The Legend of Zelda: Four Swords**  
* Свежая версия [3ds_dsiwarehax_installer](https://github.com/yellows8/3ds_dsiwarehax_installer/releases)"

part1="1. Скопируйте `public.sav` из папки `/dsiware/(8-ми значный ID)/` из `.zip-архива` 3ds_dsiwarehax_installer, в корень SD-карты **исходной 3DS**
  + **Fieldrunners USA Region**: `4b464445`
  + **Fieldrunners EUR Region**: `4b464456`
  + **Legends of Exidia USA Region**: `4b4c4545`
  + **Legends of Exidia EUR Region**: `4b4c4556`
  + **Legends of Exidia JPN Region**: `4b4c454a`
  + **Guitar Rock Tour EUR Region**: `4b475256`
  + **Guitar Rock Tour USA Region**: `4b475245`
  + **The Legend of Zelda: Four Swords EUR Region**: `4b513956`   
  + **The Legend of Zelda: Four Swords USA Region**: `4b513945`   "


part2="### Часть II - Установка сохранения

1. Включите **исходную 3DS** кнопкой питания, держа нажатой кнопку (START), чтобы запустить GodMode9
1. Перейдите в `[0:] SDCARD`
1. Нажмите (Y) на `public.sav`, чтобы скопировать его
1. Нажмите (B) для возврата в главное меню
1. Перейдите в `[2:] SYSNAND TWLN` -> `title` -> `00030004`
1. Перейдите в папку, соответствующую вашей игре и региону:
  + **Fieldrunners USA Region**: `4b464445`
  + **Fieldrunners EUR Region**: `4b464456`
  + **Legends of Exidia USA Region**: `4b4c4545`
  + **Legends of Exidia EUR Region**: `4b4c4556`
  + **Legends of Exidia JPN Region**: `4b4c454a`
  + **Guitar Rock Tour EUR Region**: `4b475254`
  + **Guitar Rock Tour USA Region**: `4b47521`    
  + **The Legend of Zelda: Four Swords EUR Region**: `4b51356`   
  + **The Legend of Zelda: Four Swords USA Region**: `4b51345`   
1. Перейдите в папку `data`
1. Нажмите (X) на существующем `public.sav`, чтобы удалить его
1. Введите указанную комбинацию кнопок чтобы разрешить запись в SysNAND (lvl1)
1. Нажмите (A), чтобы продолжить
1. Нажмите (B), если появится запрос, чтобы не восстанавливать запрет на запись в раздел
1. Нажмите (Y) чтобы вставить файл `public.sav`
1. Выберите 'Copy path(s)'
1. Нажмите (START) для того, чтобы перезагрузить **исходную 3DS**
1. Запустите DSiWare-игру на **исходной 3DS**
1. Проверьте, работает ли сохранение
  + **Fieldrunners**: коснитесь кнопки 'Scores' в главном меню
  + **Legends of Exidia**: после того, как нажмёте (A) или (START) и пропустите два игровых экрана, выберите первый слот сохранения и нажмите продолжить (continue)
  + **Guitar Rock Tour**: листайте ВНИЗ и перейдите в High-Scores -> Drums -> Easy    
  + **The Legend of Zelda: Four Swords**: Просто начните игру
  + Если игра завершается с ошибкой, касающейся `boot.nds`, или просто в белый экран, **значит эксплойт работает и все в порядке!**"

test="  + **Fieldrunners**: коснитесь кнопки 'Scores' в главном меню
  + **Legends of Exidia**: после того, как нажмёте (A) или (START) и пропустите два игровых экрана, выберите первый слот сохранения и нажмите продолжить (continue)
  + **Guitar Rock Tour**: листайте ВНИЗ и перейдите в High-Scores -> Drums -> Easy
  + **The Legend of Zelda: Four Swords**: просто начните игру"
  
%}