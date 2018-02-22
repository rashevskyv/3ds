---
title: "Обновление Luma3DS"
permalink: /update-luma3ds.html
author_profile: true
---
{% include toc title="Разделы" %}

## Последняя версия Luma3DS: {% include /vars/luma_version.txt %}

## Что понадобится

* Установленный и рабочий [b9s](updating-b9s){:target="_blank"} последней версии (*если уже делали, то повторно делать не нужно*)
* Установленный и рабочий [FBI](fbi){:target="_blank"}
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest){:target="_blank"} *(`.7z`-архив)*
* Свежая версия [Luma3ds Updater](https://github.com/KunoichiZ/lumaupdate/releases/latest){:target="_blank"} (`lumaupdater.cia`)
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"}
* [`cleanmaster.gm9`]({{ "/gm9_scripts/cleanmaster.gm9" | absolute_url }}){:target="_blank"}

## Определение типа и версии взлома 

Определить какая версия взлома стоит на вашей приставке достаточно просто: 

1. Выключите приставку
1. Зажмите кнопку {% include inc/btn.txt btn="SELECT" %} и, удерживая её, включите консоль
1. Запустится меню конфигурации Luma3DS

    ![]({{ base_path }}/images/screenshots/luma.png){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Обратите внимание на версию Luma3DS и перейдите по ссылке, соответствующей вашей версии:
	+ Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - [перейдите на b9s актуальной версии](a9lh-to-b9s){:target="_blank"}
	+ Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s){:target="_blank"}
	+ Если Luma3DS 8 и выше, то b9s 1.2 или выше (можете [обновить b9s до актуальной версии](updating-b9s){:target="_blank"}, если вы не знаете какая именно у вас стоит сейчас) - обновите Luma3DS по инструкции ниже, одним из удобных для вас способов
	
Если вы обновили Luma3DS через Luma3DS Updater и теперь приставка не включается. Загорается синий диод и тухнет, обратитесь к [этой части руководства](troubleshooting#3ds-не-включается-после-обновления-через-luma3ds-updater---загорается-синий-диод-и-тухнет){:target="_blank"}.
{: .notice--warning}
	
## Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `cias` в корне SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте `cleanmaster.gm9` в папку `/gm9/scripts/` на SD-карте
1. Верните SD-карту в приставку 
1. Включите консоль

## Часть II - Установка Luma3DS Updater

{% include /inc/luma_updater.txt %}

## Часть III - Обновление Luma3DS удобным для вас способом

### Способ I - Luma3ds Updater

1. Запустите lumaupdater из меню Home
1. Выберите "Install stable version" и нажмите {% include inc/btn.txt btn="A" %}
1. Нажмите {% include inc/btn.txt btn="A" %} + {% include inc/btn.txt btn="X" %} для установки Luma3DS на SD-карту и в CTRNAND
1. При появлении надписи "Update complite", нажмите {% include inc/btn.txt btn="START" %} для перезагрузки

### Способ II - Обновление Luma3ds вручную
  
1. Вставьте SD-карту из приставки в ПК
1. Скопируйте `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты, **соглашаясь на перезапись файлов**
1. Вставьте SD-карту в приставку
1. Включите 3DS
  + Если после включения экран остаётся чёрным, то перейдите к разделу [проблемы и их решения](troubleshooting#черный-экран-при-загрузке-sysnand-после-установки-b9s){:target="_blank"}   

## Часть IV - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

## Часть V - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

___

{% include /inc/finalize_footer.txt %}