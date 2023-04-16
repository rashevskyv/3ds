---
title: Установка boot9strap (BannerBomb3)
permalink: /bannerbomb3.html
---

{% include toc title="Содержание" %}

Если у вас не работает кнопка одна из кнопок: {% include inc/btn.txt btn="L" %}, {% include inc/btn.txt btn="R" %}, {% include inc/btn.txt btn="UP" %} или {% include inc/btn.txt btn="A" %}, то воспользуйтесь [другим методом](fredtool) для продолжения взлома.
{: .notice--danger}

Этот метод не подходит для консолей тайваньского региона (TWN). Если у вас такая, воспользуйтесь [другим методом](https://3ds.hacks.guide/bannerbomb3-fredtool-(twn)) взлома
{: .notice--warning}

### Часть I - Подготовительная работа

1. Откройте [Bannerbomb3 Injector](3dstools.nhnarwhal.com/#/bb3gen) на вашем ПК
1. Нажмите на кнопку "**Choose File**" ("Обзор") и выберите `movable.sed`, его мы получали ранее
1. Нажмите на кнопку "**Build and Download**"
    * Вам предложат сохранить на ПК архив `DSIWARE_EXPLOIT.zip`, содержащий файлы `F00D43D5.bin` и `bb3.bin`
1. Отключите консоль
1. Вставьте SD-карту приставки в ПК 
1. Скопируйте _содержимое_ `.zip-архива` {% include /inc/files/3dssdfiles.txt %} в корень вашей SD-карты
1. Скопируйте `bb3.bin` из архива `DSIWARE_EXPLOIT.zip` в корень вашей карты памяти
1. Перейдите в папку `Nintendo 3DS > ID0 > ID1 > Nintendo DSiWare`
    * ID0 должен совпадать с тем, который мы использовали выше, при получении `movable.sed`
    * Если папки `Nintendo DSiWare` нет, создайте её
    * Если в папке `Nintendo DSiWare` есть файлы, переместите их на ПК 
1. Скопируйте файл `F00D43D5.bin`, находящийся в архиве `DSIWARE_EXPLOIT.zip`, в папку `Nintendo DSiWare`

### Часть II - BannerBomb3

1. Верните SD-карту обратно в консоль
1. Включите приставку 
1. Перейдите в "**Системные настройки**" (System Settings) -> "**Управление данными**" (Data Management) -> "**DSiWare**"
1. Выберите "**Карта SD**" (SD Card), загрузится **BB3 multihax**
1. Нажмите "**Install unSAFE_MODE**"
    * После установки хака, приставка выключится 

### Часть III - unSAFE_MODE

1. Если приставка всё ещё включена, выключите её 
    * Удерживайте кнопку {% include inc/btn.txt btn="POWER" %} при необходимости 
1. Зажмите и удерживайте следующие кнопки: {% include inc/btn.txt btn="L" %} + {% include inc/btn.txt btn="R" %} + {% include inc/btn.txt btn="UP" %} + {% include inc/btn.txt btn="A" %}, а затем, не отпуская указанные кнопки, включите приставку. Не отпускайте кнопки, покуда не включится экран
{% spoiler Наглядная демонстрация %}
{% include youtube.html id="Wja1_HWXBGA"%}
{: .text-center}
{: .notice--info}
{% endspoiler %}

{:start="3"}
1. Нажмите "**OK**", чтобы начать поиск точки доступа 
1. Согласитесь с условиями пользования и нажмите **ОК**
1. Поиск завершится с ошибкой `003-1099`. Так и задумано, нажмите **ОК**
1. На запрос "**Выполнить Интернет-настройки**" (Would you like to configure Internet settings?), нажмите "**Выполнить**"
1. В появившемся меню выберите **Связь 1** (Connection 1) -> **Изменить настройки** (Change Settings) -> перейдите на следующую страницу (стрелка в правой части экрана) -> **Настройки прокси** (Proxy Settings) -> **Подробнее** (Detailed Setup)
1. Когда верхний экран окрасится в <span style="color: grey">серый</span> и на нём появится сообщение **B9S install SUCCESS**, нажмите любую кнопку

___

## **Следующий шаг:** [Завершение установки](finalizing-setup)
{: .notice--success}

<script>
	localStorage.setItem('usm', 1);
</script>