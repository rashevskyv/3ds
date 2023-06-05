---
title: Установка boot9strap (Soundhax)
permalink: /installing-boot9strap-soundhax.html
---

{% include toc title="Содержание" %}

## Обязательно к прочтению

Soundhax (в сочетании с pre9otherapp) совместим с версиями прошивки от 2.1.0 до 8.1.0 в регионах EUR, JPN, KOR и USA.

{% capture notice-1 %}
Заметьте, что обновление на картридже позволяет обновить только базовые функции консоли, такие как Системные настройки, меню HOME, и т. п. приложение Звук Nintendo 3DS и сетевые функции, такие как Передача данных, Интернет-браузер, Площадь StreetPass Mii или eShop с картриджа не обновляются.

Это означает, что обновление картриджем с версии, содержащей старое приложение Звук Nintendo 3DS *(<3.0.0)*, до версии с новым приложением Звук Nintendo 3DS сделает невозможной работу [Soundhax](homebrew-launcher-(soundhax))! Используйте [альтернативный метод](installing-boot9strap-mset) входа в Homebrew Launcher!
<br>
{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>

Убедитесь, что на приставке включён "**Беспроводной режим**"! Интернет при этом подключать не обязательно.
{: .notice--warning}

## Что понадобится

* Свежая версия {% include /inc/files/3dssdfiles.txt %}

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
{% include /inc/soundhax.md %}
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть II - Запуск SafeB9SInstaller

1. Вставьте SD-карту обратно в консоль
1. Включите консоль
1. Запустите приложение **Звук Nintendo 3DS** (Nintendo 3DS Sound)

    ![]({{ "/images/screenshots/soundhax-welcome.png" | absolute_url }})
    {: .text-center}
    {: .notice--info}
    
1. Если вы никогда не запускали Звук Nintendo 3DS (Nintendo 3DS Sound) ранее и видите советы по использованию приложения, пролистайте все сообщения птички, затем закройте приложение и снова запустите его
  + Если запустить Soundhax не закрыв приложение, то птичка будет появляться при каждом запуске программы, до тех пор, пока вы не выполните этот пункт
1. Перейдите в `/SDCARD`, затем начните воспроизведение "<3 nedwill 2016"
  + Может потребоваться несколько попыток
  + При зависании отключите питание консоли, зажав кнопку питания, и попробуйте снова

    ![]({{ "/images/screenshots/soundhax-launch.png" | absolute_url }})
	{: .text-center}
	{: .notice--info}

1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть III - Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}