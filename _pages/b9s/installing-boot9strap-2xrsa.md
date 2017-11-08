---
title: "Установка boot9strap (2xrsa)" #
lang: ru
permalink: installing-boot9strap-2xrsa.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
{% include /inc/files/bootstrap_standart.txt %}
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z`-архив)*
{% include /inc/files/ocs.txt %}

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. Скопируйте `arm9.bin` и `arm11.bin` из `.zip-архива` SafeB9SInstaller в корень SD-карты

    ![]({{ "/images/screenshots/boot9strap-2xrsa-file-layout.png" | absolute_url }})
    {: .notice--info}
	{: .text-center}

1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть II - Запуск SafeB9SInstaller

1. Запустите браузер на консоли и перейдите по ссылке:
  + `http://2xrsa.3ds.guide`
  + Если вы забыли включить Wi-Fi на New 3DS, New 2DS или Old 2DS, это можно сделать, вытащив батарею и отключив зарядное устройство на несколько секунд, а затем снова включить консоль
  + Если появляется ошибка "This service is not available in your region", поменяйте регион в Системных настройках (System Settings) на соответствующий тому, который был установлен при 2.1.0 CTRTransfer
  + Если вы забыли отключить Родительский контроль до начала процесса CTRTransfer или не можете получить доступ к настройкам сети, консоль подключится автоматически к беспроводной сети с именем `attwifi` без пароля
  + При возникновении другой ошибки, обратитесь к разделу [проблемы и их решения](troubleshooting#не-работает-эксплойт-на-основе-браузера)
1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть III - Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите {% include inc/btn.txt btn="A" %} для перезагрузки

### Часть IV - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
  + Если появляется ошибка, просто переходите к следующей странице

___

Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}