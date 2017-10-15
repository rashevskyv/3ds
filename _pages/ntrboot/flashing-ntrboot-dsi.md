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

  + [Acekard 2i](http://www.nds-card.com/ProShow.asp?ProID=160), **купить**: [![]({{"http://flags.fmcdn.net/data/flags/h20/ru.png" | absolute_url }})](https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_fleshka_acekard_2i_dlya_nintendo_ds_544116629) : <= 1.4.4
  + [R4i Gold 3DS RTS](http://www.nds-card.com/ProShow.asp?ProID=149), **купить**: [![]({{"http://flags.fmcdn.net/data/flags/h20/ru.png" | absolute_url }})](https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_r4i_gold_dlya_nintendo_ds_dsi_3ds_2ds_604415936) : <= 1.4.5
  + R4i Gold 3DS "Starter" : <= 1.4.5
  + [R4i-sdhc](http://R4i-sdhc.com), **купить**: [![]({{"http://flags.fmcdn.net/data/flags/h20/ua.png" | absolute_url }})](https://vk.com/market-125012133?section=album_3&w=product-125012133_1058176) : <= 1.4.5
  + [R4isdhc](http://R4isdhc.com) : <= 1.4.5
  + R4i Ultra : <= 1.4.1
  + Infinity 3 R4i : <= 1.4.5

{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>

Обратите внимание, что в некоторых редких случаях процесс прошивки может **брикнуть** поддельный флешкартридж и навсегда сделать его нерабочим. Это маловероятно, но тем не менее поддерживаются только оригинальные флешкартриджи из списка. Чтобы уменьшить вероятность получения поддельного картриджа, рекомендуется использовать проверенный сайт для покупки флешкартриджа (например [NDS Card](http://www.nds-card.com/))
{: .notice--danger}

## Что понадобится

* Флешкартридж, совместимый с ntrboot
* Две консоли 
  + **Исходная DSi**: Nintendo DSi, совместимая с вашим флешкартриджем
  + **Целевая 3DS**: консоль семейства 3DS с официальной прошивкой
* Свежая версия [ak2i_ntrcardhax_flasher](https://github.com/d3m3vilurr/ak2i_ntrcardhax_flasher/releases/latest) *(`dsi`-версия; стандартная версия не подходит)*

## Инструкция

### Часть I - Подготовительные работы

1. Выключите **исходную DSi**
1. Вставьте SD-карту флешкартриджа в компьютер
1. Скопируйте `ak2i_ntrcardhax_flasher_dsi.nds` на SD-карту флешкартриджа
1. Вставьте SD-карту флешкартриджа обратно во флешкартридж
1. Вставьте ваш DS / DSi флешкартридж, совместимый с ntrboot, в **исходную DSi**

### Часть II - Прошивка ntrboot

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
{: .notice--success}