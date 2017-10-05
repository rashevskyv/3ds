---
title: "Прошивка ntrboot (DSi)"
lang: ru
permalink: flashing-ntrboot-dsi.html
author_profile: true
---
{% include toc title="Разделы" %}
Прежде чем продолжить, убедитесь что вы прочитали всю информацию на странице [ntrboot](ntrboot)

Этот метод требует временного доступа к Nintendo DSi, совместимой с вашим флешкартриджем.

{% capture notice-1 %}   
Обратите внимание, что на новых версиях прошивки DSi заблокирован доступ к некоторым флешкартриджам. Поэтому они не смогут запустить `.nds` файл для прошивки эксплойта на новых версиях. Эксплойт ntrboot совместим ТОЛЬКО со следующими флешкартриджами **(даже не спрашивайте про другие; совместимы только два конкретно этих типа картриджей)**:

  + [Acekard 2i](http://www.nds-card.com/ProShow.asp?ProID=160) (HW-44, HW-81), жители РФ могут купить [здесь](https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_fleshka_acekard_2i_dlya_nintendo_ds_544116629)
  + [R4i Gold 3DS RTS](http://www.nds-card.com/ProShow.asp?ProID=149) (A5/A6/A7), жители РФ могут купить [здесь](https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_r4i_gold_dlya_nintendo_ds_dsi_3ds_2ds_604415936)
  + [R4i Ultra](http://r4ultra.com)
  + [R4i Gold 3DS Starter](http://r4ids.cn)
  + [R4 3D Revolution](http://r4idsn.com)
  + [Infinity 3 R4i](http://r4infinity.com)
  + DSTT ([лишь некоторые из них!](https://gist.github.com/Hikari-chin/6b48f1bb8dd15136403c15c39fafdb42))

{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>

Обратите внимание, что в некоторых редких случаях процесс прошивки может **брикнуть** поддельный флешкартридж и навсегда сделать его нерабочим. Это маловероятно, но тем не менее поддерживаются только оригинальные флешкартриджи из списка. Чтобы уменьшить вероятность получения поддельного картриджа, рекомендуется использовать проверенный сайт для покупки флешкартриджа (например [NDS Card](http://www.nds-card.com/))
{: .notice--danger}

#### Что понадобится

* Флешкартридж, совместимый с ntrboot
* Две консоли 
	+ **Исходная DSi**: Nintendo DSi, совместимая с вашим флешкартриджем
	+ **Целевая 3DS**: консоль семейства 3DS с официальной прошивкой* Флешкартридж, совместимый с ntrboot
* Свежая версия [ak2i_ntrcardhax_flasher](https://github.com/d3m3vilurr/ak2i_ntrcardhax_flasher/releases/latest) *(`dsi`-версия; стандартная версия не подходит)*

#### Инструкция

##### Часть I - Подготовительные работы

1. Выключите *целевую* консоль
1. Вставьте SD-карту флешкартриджа в компьютер
1. Скопируйте `ak2i_ntrcardhax_flasher_dsi.nds` на SD-карту флешкартриджа
1. Вставьте SD-карту флешкартриджа обратно во флешкартридж
1. Вставьте в консоль ваш DS / DSi флешкартридж, совместимый с ntrboot, в *целевую* консоль

##### Часть II - Прошивка ntrboot

1. Запустите `ak2i_ntrcardhax_flasher_dsi.nds` на **исходной DSi**, используя флешкартридж
1. Нажмите (A), чтобы продолжить
1. Используйте (ВВЕРХ) и (ВНИЗ) чтобы выбрать ваш флешкартридж
1. Нажмите (A), чтобы продолжить
1. Нажмите (A), чтобы выбрать "inject ntrboothax"
1. Нажмите (A), чтобы выбрать "RETAIL"
1. Нажмите (A), чтобы продолжить
1. Выберите "EXIT"

___

Следующий шаг: [Установка boot9strap (ntrboot)](installing-boot9strap-ntrboot)
{: .notice--succeess}