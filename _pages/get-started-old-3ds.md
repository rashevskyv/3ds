---
title: "Начнем (Old 3DS и Old 2DS)"
permalink: /get-started-old-3ds.html
author_profile: true
---

{% include toc title="Разделы" %}

Столбцы "С" и "По" обозначают границы диапазона. Это означает, к примеру, что диапазон "с 9.0.0 по 9.2.0" включает в себя 9.0.0, 9.1.0 и 9.2.0.
<br><br>
Последнее число вашей версии системы (после дефиса) относится к версии браузера. Если версия оканчивается на -0, значит, у вас отсутствует браузер, любое другое число говорит о том, что браузер установлен.
<br><br>
Например, если у вас версия прошивки "5.0.0-**0**E", необходимо выбрать ячейку на пересечении колонки "Без браузера" и ряда "С 5.0.0 по 5.1.0" так как версия системы находится в этом диапазоне и в системе не установлен браузер.

{% include /inc/cartrige_update.txt %}

{% capture notice-1 %}
Хорошо заранее продумайте что и как вы будете делать, поскольку прошивка без дополнительных технических средств возможна только при стечении определенных обстоятельств: версия прошивки больше, чем 4.0.0. Только в таком случае будет работать [Soundhax](installing-boot9strap-soundhax){:target="_blank"}. 
<br><br>
Например, имея на руках консоль с версией ПО 11.3.0-35 вы просто используете [Soundhax](homebrew-launcher-soundhax){:target="_blank"}.
{% endcapture %}

<div class="notice--warning">{{ notice-1 | markdownify }}</div>

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


