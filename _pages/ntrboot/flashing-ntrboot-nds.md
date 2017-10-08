---
title: "Прошивка ntrboot (NDS)"
lang: ru
permalink: flashing-ntrboot-nds.html
author_profile: true
---
{% include toc title="Разделы" %}
Прежде чем продолжить, убедитесь что вы прочитали всю информацию на странице [ntrboot](ntrboot)

Обратите внимание, что флешкартридж R4i Gold 3DS RTS не сможет использоваться для своих стандартных функций (например запуск файлов `.nds`), пока эксплойт ntrboot установлен на нем. Это не относится к Acekard 2i.

В конце инструкций по установке ntrboot boot9strap есть дополнительные шаги, чтобы по окончанию удалить эксплойт ntrboot с флешкартриджа.

{% capture notice-1 %}   
Этот метод требует временного доступа к Nintendo DS или Nintendo DS Lite, совместимой с вашим флешкартриджем. Обратите внимание, что этот метод *не* совместим с Nintendo DSi. Метод совместим ТОЛЬКО со следующими флешкартриджами **(даже не спрашивайте про другие; совместимы только два конкретно этих типа картриджей)**:

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

## Что понадобится

* Флешкартридж, совместимый с ntrboot
* Две консоли семейства 3DS:
	+ **Исходная NDS / NDSL**: Nintendo DS или Nintendo DS Lite, совместимая с вашим флешкартриджем
	+ **Целевая 3DS**: консоль семейства 3DS с официальной прошивкой
* Предыдущая версия [ak2i_ntrcardhax_flasher](https://github.com/d3m3vilurr/ak2i_ntrcardhax_flasher/releases/tag/v2.3) *(стандартная версия; `dsi-версия` не подходит)*

## Инструкция

### Часть I - Подготовительные работы

1. Выключите **исходную NDS / NDSL**
1. Вставьте SD-карту флешкартриджа в компьютер
1. Скопируйте `ak2i_ntrcardhax_flasher.nds` на SD-карту флешкартриджа
1. Вставьте SD-карту флешкартриджа обратно во флешкартридж
1. Вставьте ваш DS / DSi флешкартридж, совместимый с ntrboot, в **исходную NDS / NDSL**

### Часть II - Прошивка ntrboot

1. Запустите `ak2i_ntrcardhax_flasher.nds` на **исходной NDS / NDSL**, используя флешкартридж
1. Нажмите (A), чтобы продолжить
1. Используйте (ВВЕРХ) и (ВНИЗ) чтобы выбрать ваш флешкартридж
1. Нажмите (A), чтобы продолжить
1. Нажмите (X), чтобы выбрать "load flashrom"
1. Нажмите (A), чтобы продолжить
1. Извлеките флешкартридж из **исходной NDS / NDSL**
1. Извлеките SD-карту из флешкартриджа
1. Вставьте флешкартридж без SD-карты обратно в **исходную NDS / NDSL**
1. Нажмите (A), чтобы продолжить
1. Нажмите (A), чтобы выбрать "inject ntrboothax"
1. Нажмите (A), чтобы выбрать "RETAIL"
1. Извлеките флешкартридж из **исходной NDS / NDSL**

___

Следующий шаг: [Установка boot9strap (ntrboot)](installing-boot9strap-ntrboot)
{: .notice--success}