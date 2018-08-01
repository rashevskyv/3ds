---
title: Переход с A9LH на boot9strap #
lang: ru
permalink: a9lh-to-b9s.html
author_profile: true
---
{% include toc title="Разделы" %}

Эта страница предназначена для пользователей arm9loaderhax, чтобы обновить их устройства до boot9strap.

Все **новые** релизы Luma3DS будут только в формате `.firm`, который будет совместим только с boot9strap и sighax. Это означает, что для того, чтобы продолжать получать последние обновления Luma3DS, вы должны использовать эту страницу для обновления установки.

Если в Luma3DS вы используете PIN-код, то при работе SafeB9SInstaller вы получите ошибку "OTP Crypto Fail". Для решения этой проблемы временно откажитесь от использования PIN-кода (вы сможете включить его обратно после обновления). Если вы не помните, или не знаете свой PIN, сбросьте его используя [mkey generator](https://mkey.salthax.org/){:target="_blank"}
{: .notice--warning}

Имейте ввиду, что ф9др совместим с пейлоадерами **только** в формате `.bin`. После перехода на b9s заработают `.firm`, но до этого момента будьте внимательны и следите за тем, что и в каком формате скачиваете и устанавливаете на карту! Если вы не видите расширения файлов на карте, то вы не выполнили [эту](file-extensions-windows) часть инструкции. 
{: .notice--warning}

## Что понадобится

Обратите внимание, что `secret_sector.bin` необходим для отката эксплойта arm9loaderhax только для приставок ревизии New. **Если у вас не New 3DS/2DS, вам не нужен `secret_sector.bin`**.
{: .notice--info}

<!-- {% include /inc/files/ocs.txt %} -->
* [Homebrew Menu v2.0.0](https://github.com/fincs/new-hbmenu/releases/latest){:target="_blank"}
* Свежая версия {% include /inc/luma_adress.txt %}
* Свежая версия [Luma3DS Updater](https://github.com/KunoichiZ/lumaupdate/releases/latest){:target="_blank"}
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest){:target="_blank"}
{% include /inc/files/bootstrap_standart.txt %}
* <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - **Только для пользователей New 3DS:** [`secret_sector.bin`](magnet:?xt=urn:btih:15a3c97acf17d67af98ae8657cc66820cc58f655&dn=secret_sector.bin&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl% 3A2710%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce){:target="_blank"}
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"}
* [`cleanmaster.gm9`]({{ "/gm9_scripts/cleanmaster.gm9" | absolute_url }}){:target="_blank"}

## Инструкция

### Часть I - Определение версии загрузчика 

Сначала нужно убедиться, что у вас действительно a9lh. 

1. Отключите 3DS
1. Загрузите приставку с зажатой кнопкой {% include inc/btn.txt btn="SELECT" %}
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s){:target="_blank"}
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s){:target="_blank"}, если вы не знаете какая именно у вас стоит сейчас

    ![]({{ "/images/screenshots/luma.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

### Часть II - Подготовительные работы

Для всех шагов в этой части перезаписывайте любые существующие файлы на SD-карте.
{: .notice--info}

1. Выключите консоль
1. Вставьте SD-карту в компьютер
<!-- 1. Скопируйте `boot.3dsx` (OCS) в корень вашей SD-карты -->
1. Скопируйте `boot.3dsx` (Homebrew Menu 2.0.0) в корень SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` свежей версии Luma3DS в корень SD-карты
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` boot9strap в папку `/boot9strap/` в корне SD-карты
1. **Только для пользователей New 3DS:** Скопируйте `secret_sector.bin` в папку `/boot9strap/` на SD-карте
1. Скопируйте `SafeB9SInstaller.bin` из `.zip-архива` SafeB9SInstaller в папку `/luma/payloads/` на SD-карте
1. Переименуйте `SafeB9SInstaller.bin` в папке `/luma/payloads/` на SD-карте в `start_SafeB9SInstaller.bin`
1. Удалите все существующие `.bin` приложения в папке `/luma/payloads/` на SD-карте, так как они не будут совместимы с boot9strap совместимыми версиями Luma3DS
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` GodMode9 в корень SD-карты
1. Скопируйте `cleanmaster.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `lumaupdater.cia` в папку `/cias` на SD-карте

    ![]({{ "/images/screenshots/updating-to-b9s-file-layout.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль

### Часть III - Запуск SafeB9SInstaller

Некоторые версии Luma3DS будут напрямую запускать любое приложение, начинающееся со `start_`. Если вместо меню chainloader запускается SafeB9SInstaller, просто следуйте инструкции.

{% include /inc/safeb9sinstaller.txt %}
  
### Часть IV - Установка boot9strap

{% include /inc/install_b9s.txt %}

### Часть V - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
  
Для обновления всего ПО до актуальных версий следует перейти к странице [Завершение установки](finalizing-setup)
___

{% include /inc/finalize_footer.txt %}