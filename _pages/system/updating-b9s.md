---
title: Обновление boot9strap
permalink: updating-b9s.html
author_profile: true
---
{% include toc title="Разделы" %}

## Самая свежая версия b9s: {% include /vars/b9s_version.txt %}

Эта страница предназначена для пользователей boot9strap, чтобы они могли обновить установленный boot9strap до последней версии. Если у вас a9lh - перейдите на [b9s](a9lh-to-b9s){:target="_blank"}. Если вы еще не прошили приставку, вернитесь в [начало гайда](/){:target="_blank"} и прошейте. 

## Что понадобится

* Свежая версия {% include /inc/files/3dssdfiles.txt %}
* Свежая версия {% include /inc/luma_adress.txt %}

## Инструкция

### Часть I - Определение версии загрузчика 

Сначала нужно определить каким методом приставка взломана. 

1. Отключите 3DS
1. Загрузите приставку с зажатой кнопкой {% include inc/btn.txt btn="SELECT" %}
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из [этой инструкции](a9lh-to-b9s){:target="_blank"}, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s){:target="_blank"}
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s){:target="_blank"}, если вы не знаете какая именно у вас стоит сейчас

    ![]({{ base_path }}/images/screenshots/luma.png){:target="_blank"}
	{: .text-center}
    {: .notice--info}

### Часть II - Подготовительные работы

Для всех шагов в этой части перезаписывайте любые существующие файлы на SD-карте.
{: .notice--info}

1. Перейдите в Системные настройки (System Settings), Управление данными (Data Managment), Nintendo 3DS, Программы (Software) и удалите Luma3DS Updater
1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
1. Скопируйте имеющийся на карте памяти `boot.firm` на рабочий стол
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
1. Скопируйте `boot.firm` из рабочего стола обратно на карту памяти, согласившись на замену
1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть III - Обновление системы

{% capture notice-10 %}
Если приставка не запускается, то, вероятнее всего, вы забыли или проигнорировали копирование `boot.firm` на рабочий стол и обратно!
Если вы не сделали этого, следуйте следующим рекомендациям: 
<br><br>
[Cкачайте Luma3DS 7.1](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1){:target="_blank"}, и скопируйте boot.firm из архива с прошивкой на SD-карту, согласившись на замену. 
Обновление Luma3DS до актуальной версии будет произведено в следующей части. 
{% endcapture %}
<div class="notice--danger">{{ notice-10 | markdownify }}</div>

{% include /inc/sys_update.txt %}

### Часть IV - Запуск SafeB9SInstaller

{% include /inc/safeb9sinstaller.txt %}

### Часть V - Установка boot9strap

{% include /inc/install_b9s.txt %}

### Часть VI - Обновление Luma3DS

1. Отключите приставку
1. Вставьте SD-карту из **приставки** в компьютер
1. Удалите файл `boot.firm` из корня SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` со свежей версией Luma3DS в корень SD-карты
1. Вставьте SD-карту обратно в консоль
1. Включите приставку

### Часть VII - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

### Часть VIII - Установка Luma3DS Updater

{% include /inc/luma_updater.txt %}

### Часть IX - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

Для обновления всего ПО до актуальных версий следует перейти к странице [Завершение установки](finalizing-setup)

___

{% include /inc/finalize_footer.md %}