---
title: "Использование SoundHax для запуска Hombrew Launcher"
permalink: /homebrew-launcher-soundhax.html
author_profile: true
---
{% include toc title="Разделы" %}

SoundHax - одна из многочисленных точек входа. Он совместим с версиями прошивки от 9.0.0 до 11.3.0 включительно в регионах EUR, JPN, KOR и USA.

Убедитесь, что на устройстве включена беспроводная связь и есть стабильное подключение к интернету. OCS интернет требуется для работы.
{: .notice--warning}

{% capture notice-1 %}

Заметьте, что обновление на картридже позволяет обновить только базовые функции консоли, такие как Системные настройки, меню Home, и т. п. Приложение Звук Nintendo 3DS и сетевые функции, такие как Передача данных, Интернет-браузер, Площадь StreetPass Mii или eShop с картриджа не обновляются.
<br><br>
Помните, что обновление картриджем с версии, содержащей старое приложение Звук Nintendo 3DS *(<7.0.0 для Old 3DS регионов EUR, JPN, KOR, и USA)*, сделает невозможной работу [Soundhax](homebrew-launcher-soundhax){:target="_blank"}! Вам понадобится [альтернативный метод](homebrew-launcher-alternatives){:target="_blank"} запуска Homebrew Launcher!
{% endcapture %}

<div class="notice--warning">{{ notice-1 | markdownify }}</div>

## Что понадобится

{% include /inc/files/ocs.txt %}
* Последняя версия [SoundHax](http://soundhax.com/){:target="_blank"} *(для вашего устройства и региона)*
* [otherapp payload](https://smealum.github.io/3ds/#otherapp){:target="_blank"} *(для вашей версии ПО и региона приставки; если версия вашего браузера меньше, чем -7, попробуйте использовать otherapp для версии -7)*

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Скопируйте Soundhax `.m4a` в корень вашей SD-карты
1. Скопируйте otherapp payload в корень вашей SD-карты и переименуйте его в `otherapp.bin`
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

1. Консоль должна загрузиться в OCS

___

Следующий шаг: [Установка boot9strap (Homebrew Launcher)](installing-boot9strap-homebrew-launcher)
{: .notice--success}

