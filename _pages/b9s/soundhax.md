---
title: Использование SoundHax для установки boot9strip
permalink:  soundhax.html
---
{% include toc title="Разделы" %}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!
{: .notice--info}

Убедитесь, что на приставке включён "**Беспроводной режим**"! Интернет при этом подключать не обязательно.
{: .notice--warning}

## Инструкция

1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
1. Выберите версию **SoundHax**, соответствующую версии вашего устройства (OLD или NEW), ПО и региона и поместите скачанный `.m4a`-файл в корень вашей SD-карты
    * Версию прошивки можно посмотреть в настройках приставки. Она будет написана справа внизу на верхнем экране.
    * Если по нажатию на кнопку "**Скачать M4A**" вам просто откроется окно с видеофайлом, нажмите "**Ctrl+S**", чтобы сохранить его

    <link href="files/payload/soundhax.css" rel="stylesheet" type="text/css" media="all" />
    <div class="downloads">
        <div class="btn-group region">
            <span>Регион консоли:</span>
            <button class="group selected" id="eur">EUR</button>
            <button class="group" id="usa">USA</button>
            <button class="group" id="jpn">JPN</button>
            <button class="group" id="kor">KOR</button>
        </div>
        <div class="btn-group console">
            <span>Ревизия консоли:</span>
            <button class="group" id="n3ds">NEW</button>
            <button class="group" id="o3ds">OLD</button>
        </div>
        <div class="btn-group firmware">
            <span>Версия системного ПО:</span>
            <button class="group" id="v2.1and2.2">2.1.0 - 2.2.0</button>
            <button class="group" id="v3.xand4.x">3.0.0 - 4.5.0</button>
            <button class="group" id="post5.0">5.0.0 - 11.3.0</button>
        </div>
        <button id="download" class="round group" href="poop">Скачать M4A</button>
    </div>
    <script src="assets/js/jquery-3.1.1.min.js"></script>
    <script src="assets/js/scripts.js"></script>

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

1. Консоль должна загрузиться в **SafeB9SInstaller**

## Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите {% include inc/btn.txt btn="A" %} для перезагрузки

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}