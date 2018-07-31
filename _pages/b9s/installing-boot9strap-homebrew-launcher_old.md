---
title: "Установка boot9strap  (Homebrew Launcher) вручную" #
lang: ru
permalink: installing-boot9strap-homebrew-launcher_old.html
author_profile: true
---
{% include toc title="Разделы" %}

{% include /inc/emunand_note.txt %}

Убедитесь, что на устройстве включена беспроводная связь и есть стабильное подключение к интернету. safehax требует интернет для работы.

## Что понадобится

* Свежая версия {% include /inc/luma_adress.txt %}
* Свежая версия [Homebrew Launcher](https://github.com/fincs/new-hbmenu/releases){:target="_blank"}
* Свежая версия [safehax](https://github.com/TiniVi/safehax/releases/latest){:target="_blank"}
* Свежая версия [udsploit](https://github.com/smealum/udsploit/releases/latest){:target="_blank"}
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest){:target="_blank"}
{% include /inc/files/bootstrap_standart.txt %}

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` в корень вашей SD-карты с заменой
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` boot9strap в папку `/boot9strap/` в корне SD-карты
1. Создайте папку `3ds` в корне SD-карты
1. Скопируйте `safehax.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `udsploit.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `SafeB9SInstaller.bin` из `.zip-архива` SafeB9SInstaller в корень SD-карты и переименуйте `SafeB9SInstaller.bin` в `safehaxpayload.bin`

    ![]({{ "/images/screenshots/boot9strap-hb-file-layout.png" | absolute_url }}){:target="_blank"}
    {: .notice--info}
	{: .text-center}

1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть II - Запуск Homebrew Launcher

1. Запустите приложение Звук Nintendo 3DS (Nintendo 3DS Sound)

    ![]({{ "/images/screenshots/soundhax-welcome.png" | absolute_url }}){:target="_blank"}
    {: .notice--info}
	{: .text-center}

1. Если вы никогда не запускали Звук Nintendo 3DS (Nintendo 3DS Sound) ранее и видите советы по использованию приложения, пролистайте все сообщения птички, затем закройте приложение и снова запустите его
  + Если запустить Soundhax не закрыв приложение, то птичка будет появляться при каждом запуске программы, до тех пор, пока вы не выполните этот пункт
1. Перейдите в `/SDCARD`, затем начните воспроизведение "<3 nedwill 2016"
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
  + Если вы видите красный экран, убедитесь что вы скопировали _содержимое_ папки `starter` в корень вашей SD-карты

    ![]({{ "/images/screenshots/soundhax-launch.png" | absolute_url }}){:target="_blank"}
    {: .notice--info}
	{: .text-center}

1. Консоль должна загрузиться в Homebrew Launcher

    ![]({{ "/images/screenshots/homebrew-launcher.png" | absolute_url }}){:target="_blank"}
    {: .notice--info}
	{: .text-center}
	
### Часть III - Запуск и применение эксплойтов

1. Выберите **udsploit** в списке Homebrew
  + Вам может потребоваться пролистать список ВНИЗ, чтобы увидеть нужный пункт
1. После завершения нажмите {% include inc/btn.txt btn="START" %} для выхода из **udsploit**
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
1. Выберите **safehax** в списке Homebrew
  + Вам может потребоваться пролистать список ВНИЗ, чтобы увидеть нужный пункт
  + Если появляется ошибка "PM INIT FAILED", убедитесь, что используете **safehax** со включенным WiFi
  + Если "PM INIT FAILED" *всё ещё* появляется, попробуйте использовать [safehax версии r19](https://github.com/TiniVi/safehax/releases/tag/r19){:target="_blank"}
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова
1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть IV - Установка boot9strap

{% include /inc/install_b9s.txt %}

### Часть V - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
		+ Если появляется ошибка, просто переходите к следующей странице

___

## [Завершение установки](finalizing-setup_old)
{: .notice--success}