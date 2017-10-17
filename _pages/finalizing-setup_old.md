---
title: "Завершение установки" #
lang: ru
permalink:  finalizing-setup_old.html
author_profile: true
---

{% include toc title="Разделы" %}

## Описание шагов

Файл `boot.firm` - это то, что boot9strap запускает после загрузки из NAND, и этот файл может быть любым arm9-приложением. Этот файл может быть заменён когда угодно, однако Luma3DS позволяет запускать другие arm9 приложения в FIRM формате, используя свой загрузчик.

Мы используем Luma3DS от [AuroraWright](https://github.com/AuroraWright/), чтобы запускать пропатченный SysNAND напрямую, поэтому необходимость в каком-либо виде EmuNAND полностью пропадает, что значительно упрощает использование взломанной 3DS и экономит место на SD-карте.

В процессе мы установим и настроим следующие программы:    

+  **FBI** *(установщик приложений и игр в формате CIA)*
+  **Anemone3DS** *(установка пользовательских тем)*
+  **Checkpoint** *(резервное копирование и восстановление сохранений для игр 3DS и DS)*
+  **Luma3DS Updater** *(удобное обновление CFW)*
+  **GodMode9** *(многофункциональная утилита для работы с NAND и картриджами)*
+  **freeshop** *(open source клон eShop, облегчающий поиск игр)*
+  **Homerew Launcher Loader** *(запускает Homebrew Launcher в качестве обычного приложения благодаря магии Rosalina)*
+  **DSP1** *(простенькая утилита для дампа бинарного компонента звукового процессора 3DS, что необходимо для радя хомбрю, используюзщих звук)*

## Что понадобится

* Свежая версия [Anemone3DS](https://github.com/astronautlevel2/Anemone3DS/releases/latest) *(`.cia`-файл)*
* Свежая версия [Checkpoint](https://github.com/BernardoGiordano/Checkpoint/releases/latest) *(`.cia`-файл)*
* Свежая версия [hblauncher_loader](https://github.com/yellows8/hblauncher_loader/releases/latest)
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest) *(`.zip`-архив)*
* Свежая версия [DSP1](https://github.com/zoogie/DSP1/releases/latest) *(`.cia` файл)*
* Свежая версия [FBI](https://github.com/Steveice10/FBI/releases/latest) *(`.cia-файл`и `.3dsx-файл`)*
* Свежая версия [Luma3DS Update](https://github.com/KunoichiZ/lumaupdate/releases/latest) *(`.cia` файл)*
* Свежая версия [freeshop](https://notabug.org/arc13/freeShop/releases) *(`.cia` файл)*
* The Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
* [`setup_ctrnand_luma3ds.gm9`]({{ "/gm9_scripts/setup_ctrnand_luma3ds.gm9" | absolute_url }})
* [`cleanup_sd_card.gm9`]({{ "/gm9_scripts/cleanup_sd_card.gm9" | absolute_url }})

## Инструкция

### Часть I - Подготовительные работы

1. Отключите приставку
1. Вставьте SD-карту в компьютер
1. Скопируйте _содержимое_ архива `starter.zip` в корне SD-карты
1. Скопируйте `FBI.3dsx` в папку `/3ds/` на SD-карте
1. Создайте папку `cias` в корне SD-карты, если таковой нет
1. Скопируйте `hblauncher_loader.cia` из `.zip` архива hblauncher_loader в папку `/cias/` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Скопируйте `Anemone3DS.cia` в папку `/cias/` на SD-карты
1. Скопируйте `Checkpoint.cia` в папку `/cias/` на SD-карты
1. Скопируйте `freeshop.cia` в папку `/cias/` на SD-карты
1. Скопируйте `DSP1.cia` в папку `/cias/` на SD-карты
1. Скопируйте `FBI.cia` в папку `/cias/` на SD-карты

    ![]({{ "/images/screenshots/cias-file-layout.png" | absolute_url }})
	{: .text-center}
    {: .notice--info}

1. Создайте папку `payloads` в папке `luma` на SD-карте, если таковой нет
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `setup_ctrnand_luma3ds.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `cleanup_sd_card.gm9` в папку `/gm9/scripts/` на SD-карте

    ![]({{ "/images/screenshots/finalizing-setup-file-layout.png" | absolute_url }})
	{: .text-center}
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Включите приставку

### Часть II - Обновление системы

{% include /inc/sys_update.txt %}

### Часть III - Запуск OCS

{% include /inc/hbl.txt content="OCS" %}

### Часть IV - Установка CIA

1. Перейдите в `SD` -> `cias`
1. Выберите "\<current directory>"
1. Выберите "Install and delete all CIAs" и нажмите (A) для подтверждения
1. Нажмите (HOME), затем закройте приложение Загружаемая игра (Download Play)

### Часть V - DSP Dump

1. Запустите приложение DSP1
1. После завершения работы программы, нажмите (B), чтобы автоматически удалить программу из меню Home

### Часть VI - CTRNAND Luma3DS

{% include /inc/ctrnand_luma.txt %}

### Часть VII - Резервное копирование SysNAND

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "Backup SysNAND"
1. Нажмите (A) для подтверждения
	+ Этот процесс займет некоторое время
1. Нажмите (A), чтобы продолжить
1. Удерживая (R) нажмите (B) для того, чтобы извлечь SD-карту
1. Вставьте SD-карту в компьютер
1. Скопируйте `<YYMMDD>_<serialnumber>_sysnand_###.bin` из папки `/gm9/out/` на SD-карте в безопасное место на вашем компьютере
  + Сделайте несколько резервных копий в нескольких местах (например в облачном хранилище)
  + Эти бэкапы позволят восстановить консоль, если впоследствии что-то пойдёт не так
1. После копирования удалите `<YYMMDD>_<serialnumber>_sysnand_###.bin` из папки `/gm9/out/` на SD-карте
1. Вставьте SD-карту обратно в консоль

### Часть VIII - Очистка SD-карты

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "cleanup_sd_card"
1. При появлении запроса, нажмите (A) для продолжения
1. Нажмите (A), чтобы продолжить
1. Нажмите (START) для перезагрузки

После работы скрипта корень SD-карты будет выглядеть следующим образом: 

![]({{ base_path }}/images/screenshots/final-file-layout.png)
{: .text-center}

### Часть IX - Дополнительные материалы

Теперь ваша приставка прошита и вы можете пользоваться всеми благами кастомной прошивки

1. Можете [установить freeshop](freeshop) для скачивания игр бесплатно прямно на консоли
1. Можете украсить приставку [жетонами](badges) и [темами](themes)
1. Ознакомится с остальным [списком полезных инструкций](addons)

___

{% include /inc/finalize_footer.txt %}