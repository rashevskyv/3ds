---
title: "Запуск и установка FBI"
permalink: /fbi.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

{% include /inc/olx_vk.txt %}
{: .notice--info}

* Установленный и рабочий [b9s](updating-b9s) последней версии (*если уже делали, то повторно делать не нужно*)
* Свежая версия [FBI](https://github.com/Steveice10/FBI/releases/latest) *(`.cia-файл`и `.3dsx-файл`)*

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Скопируйте `boot.3dsx` в корень SD-карты
1. Скопируйте `FBI.3dsx` в папку `/3ds/` на SD-карте
1. Скопируйте `FBI.cia` в папку `/cias/` в корне SD-карты
1. Вставьте SD-карту обратно в консоль

### Часть II - Обновление системы

{% include /inc/sys_update.txt %}

### Часть III - Запуск Homebrew Launcher

{% include /inc/hbl.txt content="Homebrew Launcher" %}

### Часть IV - Установка CIA

1. Выберите в списке Homebrew FBI и запустите его
1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs" и нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Нажмите {% include inc/btn.txt btn="HOME" %}, затем закройте приложение Загружаемая игра (Download Play)

Чтобы обновить FBI, воспользуйтесь пунктом "Update" в его меню. В случае, если FBI у вас установлен с помощью инъекции в приложение "Информация о здоровье и безопасности" (Health & Safety), то при обновлении его иконка дублируется. Для того, чтобы этого избежать, восстановите приложение ["Информация о здоровье и безопасности"](https://3ds.customfw.xyz/godmode9-usage#восстановление-приложения-информация-о-здоровье-и-безопасности)
{: .notice--info}