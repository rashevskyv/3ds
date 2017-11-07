---
title: "Установка boot9strap (MSET)" #
lang: ru
permalink: installing-boot9strap-mset.html
author_profile: true
---
{% include toc title="Разделы" %}

{% include /inc/emunand_note.txt %}

## Что понадобится

* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
{% include /inc/files/bootstrap_standart.txt %}
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z`-архив)*
{% include /inc/files/ocs.txt %}
* Любой флешкартридж для DS, работающий на вашей версии прошивки

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. Скопируйте `SafeB9SInstaller.dat` из `.zip-ахрива` SafeB9SInstaller в корень SD-карты

    ![]({{ "/images/screenshots/boot9strap-mset-file-layout.png" | absolute_url }})
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Скопируйте `SafeB9SInstaller.nds` из `.zip-ахрива` SafeB9SInstaller на ваш DS-флешкартридж
1. Включите консоль

### Часть II - Запуск SafeB9SInstaller

1. Запустите флешкартридж DS
1. Запустите `SafeB9SInstaller.nds`, используя флешкартридж
1. Выберите опцию, соответствующую версии прошивки
  + 4.X.X -> "4.x SafeB9SInstaller"
  + 6.X.X -> "6.x SafeB9SInstaller"
1. Перезагрузите консоль, зайдите в "Системные настройки" (System Settings), затем "Прочие настройки" (Other Settings), затем "Профиль" (Profile), затем "Профиль Nintendo DS" (Nintendo DS Profile)
1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть III - Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки

### Часть IV - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
  + Если появляется ошибка, просто переходите к следующей странице

___

Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}


