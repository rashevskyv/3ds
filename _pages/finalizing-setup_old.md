---
title: "Завершение установки вручную" #
lang: ru
permalink:  finalizing-setup_old.html
author_profile: true
---

{% include toc title="Разделы" %}

## Описание шагов

Файл `boot.firm` - это то, что boot9strap запускает после загрузки из NAND, и этот файл может быть любым arm9-приложением. Этот файл может быть заменён когда угодно, однако Luma3DS позволяет запускать другие arm9 приложения в FIRM формате, используя свой загрузчик.

Мы используем Luma3DS от [AuroraWright](https://github.com/AuroraWright/){:target="_blank"}, чтобы запускать пропатченный SysNAND напрямую, поэтому необходимость в каком-либо виде EmuNAND полностью пропадает, что значительно упрощает использование взломанной 3DS и экономит место на SD-карте.

В процессе мы установим и настроим следующие программы:    

+  **FBI** *(установщик приложений и игр в формате CIA)*
+  **Themely** *(установка пользовательских тем)*
+  **Checkpoint** *(резервное копирование и восстановление сохранений для игр 3DS и DS)*
+  **Luma3DS Updater** *(удобное обновление CFW)*
+  **GodMode9** *(многофункциональная утилита для работы с NAND и картриджами)*
+  **freeshop** *(open source клон eShop, облегчающий поиск игр)*
+  **Homerew Launcher Loader** *(запускает Homebrew Launcher в качестве обычного приложения благодаря магии Rosalina)*
+  **DSP1** *(простенькая утилита для дампа бинарного компонента звукового процессора 3DS, что необходимо для радя хомбрю, используюзщих звук)*

## Что понадобится

* The Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip){:target="_blank"}
* Свежая версия [Checkpoint](https://github.com/BernardoGiordano/Checkpoint/releases/latest){:target="_blank"} *(`.cia`-файл)*
* Свежая версия [DSP1](https://github.com/zoogie/DSP1/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [FBI](https://github.com/Steveice10/FBI/releases/latest){:target="_blank"} *(`.cia-файл` и `.3dsx-файл`)*
* Свежая версия [freeshop](https://notabug.org/arc13/freeShop/releases){:target="_blank"} *(`.cia` файл)*
* Свежая версия [hblauncher_loader](https://github.com/yellows8/hblauncher_loader/releases/latest){:target="_blank"}
* Свежая версия [Luma3DS Update](https://github.com/KunoichiZ/lumaupdate/releases/latest){:target="_blank"} *(`.cia` файл)*
* Свежая версия [Themely](https://github.com/ErmanSayin/Themely/releases/latest){:target="_blank"} *(`.cia`-файл)*
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest){:target="_blank"} *(`.zip`-архив)*
* [`setup_ctrnand_luma3ds.gm9`]({{ "/gm9_scripts/setup_ctrnand_luma3ds.gm9" | absolute_url }}){:target="_blank"}
* [`cleanup_sd_card.gm9`]({{ "/gm9_scripts/cleanup_sd_card.gm9" | absolute_url }}){:target="_blank"}

## Инструкция

### Часть I - Подготовительные работы

1. Отключите приставку
1. Вставьте SD-карту в компьютер
1. Скопируйте boot.3dsx из архива `starter.zip` в корень SD-карты
1. Создайте папку `3ds` в корне SD-карты, если таковой нет
1. Скопируйте `FBI.3dsx` в папку `/3ds/` на SD-карте
1. Создайте папку `cias` в корне SD-карты, если таковой нет
1. Скопируйте `Checkpoint.cia` в папку `/cias/` на SD-карты
1. Скопируйте `DSP1.cia` в папку `/cias/` на SD-карты
1. Скопируйте `FBI.cia` в папку `/cias/` на SD-карты
1. Скопируйте `freeshop.cia` в папку `/cias/` на SD-карты
1. Скопируйте `hblauncher_loader.cia` из `.zip` архива hblauncher_loader в папку `/cias/` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Скопируйте `Themely.cia` в папку `/cias/` на SD-карты

    ![]({{ "/images/screenshots/cias-file-layout.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Создайте папку `payloads` в папке `luma` на SD-карте, если таковой нет
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `setup_ctrnand_luma3ds.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `cleanup_sd_card.gm9` в папку `/gm9/scripts/` на SD-карте

    ![]({{ "/images/screenshots/finalizing-setup-file-layout.png" | absolute_url }}){:target="_blank"}
	{: .text-center}
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Включите приставку

### Часть II - Обновление системы
{% include /inc/if_emunand.txt %}
{% include /inc/sys_update.txt %}

### Часть III - Запуск HBL

{% include /inc/hbl.txt content="Homebrew Launcher" %}

### Часть IV - Установка CIA

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs" и нажмите {% include inc/btn.txt btn="A" %} для подтверждения
1. Нажмите {% include inc/btn.txt btn="HOME" %} для возврата в меню Home

### Часть V - DSP Dump

1. Запустите приложение DSP1
1. После завершения работы программы, нажмите {% include inc/btn.txt btn="B" %}, чтобы автоматически удалить программу из меню Home

### Часть VI - CTRNAND Luma3DS

{% include /inc/ctrnand_luma.txt %}

### Часть VII - Создание резервной копии (бекап) SysNAND

{% include /inc/sysnand_backup.txt %}

### Часть VIII - Очистка SD-карты

1. Нажмите кнопку {% include inc/btn.txt btn="HOME" %} для вызова меню
1. Выберите "Scripts..."
1. Выберите "cleanup_sd_card"
1. При появлении запроса, нажмите {% include inc/btn.txt btn="A" %} для продолжения
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Нажмите {% include inc/btn.txt btn="START" %} для перезагрузки

После работы скрипта корень SD-карты будет выглядеть следующим образом: 

![]({{ base_path }}/images/screenshots/final-file-layout.png){:target="_blank"}
{: .text-center}

### Часть IX - Дополнительные материалы

{% include /inc/finalize_addons.txt %}

___

{% include /inc/finalize_footer.txt %}