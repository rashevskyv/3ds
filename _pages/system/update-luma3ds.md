---
title: Обновление Luma3DS
permalink: /update-luma3ds.html
---
{% include toc title="Разделы" %}

## Последняя версия Luma3DS: {% include /vars/luma_version.txt %}

## Что понадобится

* Установленный и рабочий [b9s](updating-b9s){:target="_blank"} последней версии (*если уже делали, то повторно делать не нужно*)
* Установленный и рабочий [FBI](fbi){:target="_blank"}
* Свежая версия {% include /inc/luma_adress.txt %}
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
	+ Если Luma3DS 8 и выше, то b9s 1.2 или выше - обновите Luma3DS по инструкции ниже
	
Если вы обновили Luma3DS через Luma3DS Updater и теперь приставка не включается. Загорается синий диод и тухнет, обратитесь к [этой части руководства](troubleshooting#3ds-не-включается-после-обновления-через-luma3ds-updater---загорается-синий-диод-и-тухнет){:target="_blank"}.
{: .notice--warning}
	
## Часть I - Обновление Luma3DS и приложений

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `cias` в корне SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` {% include /inc/luma_adress.txt %} в корень SD-карты
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте `cleanmaster.gm9` в папку `/gm9/scripts/` на SD-карте
1. Верните SD-карту в приставку 
1. Включите консоль
  + Если после включения экран остаётся чёрным, то перейдите к разделу [проблемы и их решения](troubleshooting#черный-экран-при-загрузке-sysnand-после-установки-b9s){:target="_blank"}   

## Часть II - Настройка Luma3DS

{% include /inc/luma_setup.txt %}

## Часть III - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

## Часть IV - Обновление системы

{% include /inc/sys_update.txt %}

___

{% include /inc/finalize_footer.md %}