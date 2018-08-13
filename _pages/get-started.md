---
title: Начнем
permalink: /get-started.html
author_profile: true
---

Эта страница содержит инструкции по установке boot9strap на *не взломанную* 3DS или 2DS. Если у вас уже установлен arm9loaderhax, и вы хотите обновиться до boot9strap, следуйте инструкциям в разделе [Обновление до boot9strap](a9lh-to-b9s){:target="_blank"}.

Прежде чем начать, рекомендуется проверить свою SD-карту на ошибки с помощью [H2testw (Windows)](h2testw-windows){:target="_blank"}, [F3 (Linux)](f3-linux){:target="_blank"}, или [F3X (Mac)](f3x-mac){:target="_blank"}!

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!

Если на приставке нет важных для вас данных, то я крайне рекомендую произвести форматирование [приставки](clean_sd#i-Форматирование-приставки) и [SD-карты](clean_sd#ii-Форматирование-sd-карты) перед началом взлома. **Помните, что форматирование уничтожит все ваши данные на приставке и SD-карте. Делайте его только в том случае, если на приставке и карте нет ничего важного!**
{: .notice--warning}

После выхода 11.8 появились опасения того, что Nintendo сможет отслеживать пользователей freeshop и прицельно их банить. Если ваша приставка на прошивке от 11.4 и отсутствие бана для вас весомо, воспользуйтесь методом прошивки [ntrboot](ntrboot){:target="_blank"}, а в настройках подключения пропишите первичный DNS `159.203.242.044`
{: .notice--warning}

___

Столбцы "С" и "По" обозначают границы диапазона. Это означает, к примеру, что диапазон "с 9.0.0 по 9.2.0" включает в себя 9.0.0, 9.1.0 и 9.2.0.

Последнее число вашей версии системы (после дефиса) относится к версии браузера. Если версия оканчивается на -0, значит, у вас отсутствует браузер, любое другое число говорит о том, что браузер установлен. В настоящее время все New 3DS и New 2DS имеют браузер!

Например, если у вас версия прошивки "5.0.0-**0**E", необходимо выбрать ячейку на пересечении колонки "Без браузера" и ряда "С 5.0.0 по 5.1.0" так как версия системы находится в этом диапазоне и в системе не установлен браузер.

Любую версию прошивки можно обновить на более высокую из этой же колонки [с помощью картриджа](cart-update){:target="_blank"} (или выполнив Обновление системы), и после этого продолжить выполнять инструкцию.

**Если вы не можете следовать инструкциям для конкретной версии из-за невыполненных предварительных условий, обратите внимание на столбец "Для всех версий". Эти методы работают вне зависимости от версии прошивки.**

Для всех консолей, любой версии прошивки можно использовать [Хардмод](making-hardmod){:target="_blank"} или [NTRBootHax](ntrboot){:target="_blank"}
{: .notice--warning}

Версия программного обеспечения вашего устройства отображается в правом нижнем углу верхнего экрана в приложении Системные настройки (System settings).
{: .notice--success}

![]({{ "/images/screenshots/system-version.png" | absolute_url }}){:target="_blank"}
{: .text-center}
{: .notice--info}

#### Таблица версий

<table>
  <colgroup>
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 38%;">
    <col span="1" style="width: 38%;">
    <col span="1" style="width: 10%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;">С</th>
      <th style="text-align: center; font-weight: bold;">По</th>
      <th style="text-align: center; font-weight: bold;">Браузера нет</th>
      <th style="text-align: center; font-weight: bold;">Браузер есть</th>
      <th style="text-align: center; font-weight: bold;">Для всех версий</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">1.0.0</td>
	  <td style="text-align: center; font-weight: bold;">2.0.0</td>
      <td style="text-align: center;" colspan="2"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/consoles/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmod (необходимы навыки работы с паяльником)"><img src="/images/consoles/hardmod.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/consoles/cart_update.png"></a> до 4.0-4.5</td>
      <td style="text-align: center;" rowspan="10">
		<a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)">
			<img src="/images/consoles/ntrhax.png">
		</a>
		<br><br>
		<a href="making-hardmod" title="Установка через hardmod (необходимы навыки работы с паяльником)">
			<img src="/images/consoles/hardmod.png">
		</a>
	  </td>
	</tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" colspan="2">2.1.0</td>
      <td style="text-align: center;"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/consoles/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmod (необходимы навыки работы с паяльником)"><img src="/images/consoles/hardmod.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/consoles/cart_update.png"></a> до 4.0-8.1</td>
      <td style="text-align: center;"><a href="installing-boot9strap-2xrsa">Установка boot9strap (2xrsa)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">2.2.0</td>
      <td style="text-align: center; font-weight: bold;"	>3.1.0</td>
      <td style="text-align: center;" colspan="2"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/consoles/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmod (необходимы навыки работы с паяльником)"><img src="/images/consoles/hardmod.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/consoles/cart_update.png"></a> до 4.0-8.1</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">4.0.0</td>
      <td style="text-align: center; font-weight: bold;">8.1.0</td>
      <td style="text-align: center;" colspan="2"><a href="installing-boot9strap-soundhax">Установка boot9strap (Soundhax)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">9.0.0</td>
      <td style="text-align: center; font-weight: bold;">11.3.0</td>
      <td style="text-align: center;"><a href="homebrew-launcher-alternatives">Альтернативный метод запуска HBL</a></td>
      <td style="text-align: center;"><a href="homebrew-launcher-soundhax">Homebrew Launcher (Soundhax)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">11.4.0</td>
      <td style="text-align: center; font-weight: bold;">{% include /vars/sys_version.txt %}</td>
      <td style="text-align: center;" colspan="2"><a href="installing-boot9strap-dsiware">Установка boot9strap (DSiWare)</a></td>
    </tr>
</tbody>
</table>
{% capture notice-7 %}

**Методы, подходящие для всех версий прошивки:**

<a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)">
	<img src="/images/consoles/ntrhax.png" > - установка ntrboothax (необходим совместимый флеш-картридж)
</a>
<br>
<a href="making-hardmod" title="Установка через hardmod (необходимы навыки работы с паяльником)">
	<img src="/images/consoles/hardmod.png"> - установка через hardmod (необходимы навыки работы с паяльником)
</a>

{% endcapture %}
		
<div class="notice--info">{{ notice-7 | markdownify }}</div>


