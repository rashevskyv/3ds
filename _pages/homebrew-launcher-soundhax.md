---
title: Использование SoundHax для запуска Homebrew Launcher
permalink: /homebrew-launcher-soundhax.html
author_profile: true
---
{% include toc title="Разделы" %}

SoundHax - одна из многочисленных точек входа. Он совместим с версиями прошивки от 9.0.0 до 11.3.0 включительно в регионах EUR, JPN, KOR и USA.

<!-- Убедитесь, что на устройстве включена беспроводная связь и есть стабильное подключение к интернету. OCS интернет требуется для работы.
 -->{: .notice--warning}

{% capture notice-1 %}

Заметьте, что обновление на картридже позволяет обновить только базовые функции консоли, такие как Системные настройки, меню Home, и т. п. Приложение Звук Nintendo 3DS и сетевые функции, такие как Передача данных, Интернет-браузер, Площадь StreetPass Mii или eShop с картриджа не обновляются.
<br><br>
Помните, что обновление картриджем с версии, содержащей старое приложение Звук Nintendo 3DS *(<3.0.0 для Old 3DS регионов EUR, JPN, KOR, и USA)*, сделает невозможной работу [Soundhax](homebrew-launcher-soundhax){:target="_blank"}! Вам понадобится [альтернативный метод](homebrew-launcher-alternatives){:target="_blank"} запуска Homebrew Launcher, либо установка boot9strap. 
{% endcapture %}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!
{: .notice--info}

<div class="notice--warning">{{ notice-1 | markdownify }}</div>

## Что понадобится

<!-- {% include /inc/files/ocs.txt %} -->
* [Homebrew Menu v2.0.0](https://github.com/fincs/new-hbmenu/releases/latest){:target="_blank"}
* Последняя версия [SoundHax](http://soundhax.com/){:target="_blank"} *(для вашего устройства? версии ПО и региона)*
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest){:target="_blank"}
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest){:target="_blank"} *(стандартный boot9strap; не `devkit` файл, не `ntr` файл)*
* Свежая версия [safehax](https://github.com/TiniVi/safehax/releases/latest){:target="_blank"} *(`.3dsx` файл)*
* Свежая версия [udsploit](https://github.com/smealum/udsploit/releases/latest){:target="_blank"}
* Свежая версия {% include /inc/luma_adress.txt %}
* [otherapp payload](https://smealum.github.io/3ds/#otherapp){:target="_blank"} *(для вашей версии ПО и региона приставки; если версия вашего браузера меньше, чем -7, попробуйте использовать otherapp для версии -7)*

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
<!-- 1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты -->
1. Создайте папку `3ds` в корне SD-карты, если таковой нет
1. Создайте папку `luma` в корне SD-карты 
1. Скопируйте `boot.3dsx` в корень SD-карты
1. Скопируйте Soundhax `.m4a` в корень вашей SD-карты
1. Скопируйте otherapp payload в корень вашей SD-карты и переименуйте его в `otherapp.bin`
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` boot9strap в папку `/boot9strap/` в корне SD-карты
1. Скопируйте `safehax.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `udsploit.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `SafeB9SInstaller.bin` из `.zip-архива` SafeB9SInstaller в корень SD-карты и переименуйте `SafeB9SInstaller.bin` в `safehaxpayload.bin`

    ![]({{ "/images/screenshots/boot9strap-hb-file-layout.png" | absolute_url }})
    {: .notice--info}
	
1. Вставьте SD-карту обратно в консоль
1. Включите консоль
1. Запустите приложение Звук Nintendo 3DS (Nintendo 3DS Sound)

    ![]({{ "/images/screenshots/soundhax-welcome.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Если вы никогда не запускали Звук Nintendo 3DS (Nintendo 3DS Sound) ранее и видите советы по использованию приложения, пролистайте все сообщения птички, затем закройте приложение и снова запустите его
  + В этой ситуации, при запуске Soundhax сразу, без закрытия, птичка будет появляться при каждом запуске приложения, до тех пор, пока вы не выполните этот пункт
1. Перейдите в `/SDCARD`, затем начните воспроизведение "<3 nedwill 2016"
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова

    ![]({{ "/images/screenshots/soundhax-launch.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Консоль должна загрузиться в Homebrew Launcher

___

## [Установка boot9strap (Homebrew Launcher)](installing-boot9strap-homebrew-launcher)
{: .notice--success}