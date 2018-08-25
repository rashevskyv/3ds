---
title: Завершение установки #
lang: ru
permalink:  finalizing-setup_ocs.html
author_profile: true
---

{% include toc title="Разделы" %}

## Описание шагов

Файл `boot.firm` - это то, что boot9strap запускает после загрузки из NAND, и этот файл может быть любым arm9-приложением. Этот файл может быть заменён когда угодно, однако Luma3DS позволяет запускать другие arm9 приложения в FIRM формате, используя свой загрузчик.

Мы используем Luma3DS от [AuroraWright](https://github.com/AuroraWright/){:target="_blank"}, чтобы запускать пропатченный SysNAND напрямую, поэтому необходимость в каком-либо виде EmuNAND полностью пропадает, что значительно упрощает использование взломанной 3DS и экономит место на SD-карте.

В процессе мы установим и настроим следующие программы:    

+  **FBI** *(установщик приложений и игр в формате CIA)*
+  **Anemone3DS** *(установка пользовательских тем)*
+  **Checkpoint** *(резервное копирование и восстановление сохранений для игр 3DS и DS)*
+  **GodMode9** *(многофункциональная утилита для работы с NAND и картриджами)*
+  **Homerew Launcher Loader** *(запускает Homebrew Launcher в качестве обычного приложения благодаря магии Rosalina)*
+  **ftpd** *(просто ftp-клиент для простого доступа к карте памяти без разбора приставки)*
+  **Luma3DS Updater** *(удобное обновление CFW)*

## Инструкция

### Часть I - Обновление системы
{% include /inc/if_emunand.txt %}
{% include /inc/sys_update.txt %}

### Часть II - Запуск OCS

Убедитесь, что на устройстве включена беспроводная связь и есть стабильное подключение к интернету. OCS интернет требуется для работы.
{: .notice--warning}

{% include /inc/hbl.txt content="OCS" %}

### Часть III - OCS

Если вы испытываете трудности с запуском OCS, или любые другие, связанные с работоспособностью этой программы - воспользуйтесь [ручным методом установки программ](finalizing-setup_old){:target="_blank"}
{: .notice--warning}

1. Нажмите {% include inc/btn.txt btn="A" %}, для начала работы программы
1. Дождитесь окончания загрузки и установки
1. Нажмите {% include inc/btn.txt btn="START" %} по запросу для выхода из программы 
1. Нажмите {% include inc/btn.txt btn="HOME" %} для выхода из HBL

### Часть IV - CTRNAND Luma3DS и очистка SD-карты 

{% include /inc/ctrnand_luma_cleansd.txt %}

### Часть V - Создание резервной копии (бекап) SysNAND

{% include /inc/sysnand_backup.txt %}

### Часть VI - Дополнительные материалы

{% include /inc/finalize_addons.txt %}

___

{% include /inc/finalize_footer.txt %}