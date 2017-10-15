---
title: "Обновление boot9strap"
permalink: updating-b9s.html
author_profile: true
---
{% include toc title="Разделы" %}

<h3>Самая свежая версия b9s - 1.3 от 06.09.2017</h3>

Эта страница предназначена для пользователей boot9strap, чтобы они могли обновить установленный boot9strap до последней версии. Если у вас a9lh - перейдите на [b9s](a9lh-to-b9s). Если вы еще не прошили приставку, вернитесь в [начало гайда](/) и прошейте. 

## Что понадобится

* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z-архив`)*
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(стандартный boot9strap; не `devkit-файл`, не `ntr-файл` и не `devkit-ntr-файл`)*
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest)
* Свежая версия [Luma3DS Updater](https://github.com/KunoichiZ/lumaupdate/releases/latest)
* Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
* [`setup_ctrnand_luma3ds.gm9`]({{ "/gm9_scripts/setup_ctrnand_luma3ds.gm9" | absolute_url }})
* [`cleanup_sd_card.gm9`]({{ "/gm9_scripts/cleanup_sd_card.gm9" | absolute_url }})

## Инструкция

### Часть I - Определение версии загрузчика 

Сначала нужно определить каким методом приставка взломана. 

1. Отключите 3DS
1. Загрузите приставку с зажатой кнопкой (SELECT)
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s)
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s), если вы не знаете какая именно у вас стоит сейчас

    ![]({{ base_path }}/images/screenshots/luma.png)
	{: .text-center}
    {: .notice--info}

### Часть II - Подготовительные работы

Для всех шагов в этой части перезаписывайте любые существующие файлы на SD-карте.
{: .notice--info}

{% capture notice-10 %}
**Не копируйте** в этой части boot.firm от Luma3DS 8, если у вас b9s 1.0! Если вы сделали это следуйте следующим рекомендациям: 
<br><br>
[Cкачайте Luma3DS 7.1](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1), и скопируйте boot.firm из архива с прошивкой на SD-карту, согласившись на замену. 
Обновление Luma3DS до актуальной версии будет произведено в следующей части. 
Если у вас b9s 1.2, то вреда от копирования не будет.
{% endcapture %}

<div class="notice--danger">{{ notice-10 | markdownify }}</div>

1. Перейдите в Системные настройки (System Settings), Управление данными (Data Managment), Nintendo 3DS, Программы (Software) и удалите Luma3DS Updater
1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. **Помните, что ещё не следует копировать boot.firm от Luma 8.0, мы сделаем это в следующей части**
1. Скопируйте _содержимое_ архива `starter.zip` в корень SD-карты **целевой 3DS**
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `setup_ctrnand_luma3ds.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `SafeB9SInstaller.firm` из `.zip-архива` SafeB9SInstaller в папку `/luma/payloads/` на SD-карте
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. Создайте папку `cias` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Вставьте SD-карту обратно в консоль

### Часть III - Обновление системы

{% include /inc/sys_update.txt %}

### Часть IV - Установка boot9strap

1. Включите приставку, удерживая кнопку (START), чтобы запустить меню Luma3DS chainloader
1. Запустите SafeB9SInstaller, нажав кнопку (A)
1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки
1. Выключите консоль, нажатием любой кнопки, **игнорируя ошибку**
  + Обратите внимание, что ошибка `Unsupported launcher (argc = 0)` будет появляться до тех пор, пока вы до конца не выполните инструкцию из этой страницы

### Часть V - Обновление Luma3DS

1. Вставьте SD-карту в компьютер
1. Удалите файл `boot.firm` из корня SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Вставьте SD-карту обратно в консоль

### Часть VI - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

### Часть VII - Установка Luma3DS Updater

{% include /inc/luma_updater.txt %}

### Часть VIII - CTRNAND Luma3DS

{% include /inc/ctrnand_luma.txt %}

### Часть IX - Очистка SD-карты

Помните, что скрипт, используемый ниже, удалит папки `/boot9strap/` и `/cias/` с SD-карты!
{: .notice--danger}

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "cleanup_sd_card"
1. При появлении запроса, нажмите (A) для продолжения
1. Нажмите (A), чтобы продолжить
1. Нажмите (START) для перезагрузки

После работы скрипта корень SD-карты будет выглядеть следующим образом: 

![]({{ base_path }}/images/screenshots/final-file-layout.png)
{: .text-center}

___

{% include /inc/finalize_footer.txt %}