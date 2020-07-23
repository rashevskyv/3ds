---
title: Использование SoundHax для запуска Homebrew Launcher
permalink: /homebrew-launcher-soundhax.html
author_profile: true
---
{% include toc title="Разделы" %}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!
{: .notice--info}

{% capture notice-1 %}
Заметьте, что обновление на картридже позволяет обновить только базовые функции консоли, такие как Системные настройки, меню Home, и т. п. Приложение Звук Nintendo 3DS и сетевые функции, такие как Передача данных, Интернет-браузер, Площадь StreetPass Mii или eShop с картриджа не обновляются.
<br><br>
Помните, что обновление картриджем с версии, содержащей старое приложение Звук Nintendo 3DS *(<3.0.0 для Old 3DS регионов EUR, JPN, KOR, и USA)*, сделает невозможной работу [Soundhax](homebrew-launcher-soundhax){:target="_blank"}! Вам понадобится [альтернативный метод](homebrew-launcher-alternatives){:target="_blank"} запуска Homebrew Launcher, либо установка boot9strap. 
{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>

Убедитесь, что на приставке включён "**Беспроводной режим**"! Интернет при этом подключать не обязательно.
{: .notice--warning}

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
{% include /inc/soundhax.md %}
{% include /inc/payload.txt payload_name="otherapp.bin" %}
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
1. Вставьте SD-карту обратно в консоль
1. Включите консоль
1. Запустите приложение **Звук Nintendo 3DS** (Nintendo 3DS Sound)

    ![]({{ "/images/screenshots/soundhax-welcome.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Если вы никогда не запускали **Звук Nintendo 3DS** (Nintendo 3DS Sound) ранее и видите советы по использованию приложения, пролистайте все сообщения птички, затем закройте приложение и снова запустите его
  + В этой ситуации, при запуске Soundhax сразу, без закрытия, птичка будет появляться при каждом запуске приложения, до тех пор, пока вы не выполните этот пункт
1. Перейдите в `/SDCARD`, затем начните воспроизведение "<3 nedwill 2016"
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова

    ![]({{ "/images/screenshots/soundhax-launch.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Консоль должна загрузиться в Homebrew Launcher

___

## **Следующий шаг:** [Установка boot9strap (Homebrew Launcher)](installing-boot9strap-homebrew-launcher)
{: .notice--success}