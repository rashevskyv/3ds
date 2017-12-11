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
Хорошо заранее продумайте что и как вы будете делать, поскольку прошивка без дополнительных технических средств возможна только при стечении определенных обстоятельств: версия прошивки больше, чем 9.0.0 с браузером версии выше, чем -7 (говорят, что otherapp от -0 до -7 взаимозаменяем, но это требует тщательной проверки), обновленная **НЕ через картридж**. Только в таком случае будет работать [Soundhax](homebrew-launcher-soundhax){:target="_blank"}. 
<br><br>
Например, имея на руках консоль с версией ПО 11.3.0-35 вы просто используете [Soundhax](homebrew-launcher-soundhax){:target="_blank"}.
<br><br>
С другой стороны - приставка с прошивкой 1.0.0-0. Очевидно, что браузера на ней нет и обновление картриджем не позволит использовать ни [Soundhax](homebrew-launcher-soundhax){:target="_blank"}, ни [browserhax](installing-boot9strap-browser){:target="_blank"}, ни [2xrsa](installing-boot9strap-2xrsa){:target="_blank"}. Остаются следующие возможности:
+ Использование [MSET](installing-boot9strap-mset){:target="_blank"}, для чего понадобится флеш-картридж от Nintendo DS и картридж для Nintendo 3DS, содержащий обновление системного ПО до версии, поддерживающей MSET (4.0.0-4.5.0, 6.0.0-6.3.0); 
+ Использование [HBL через альтернативную точку входа](homebrew-launcher-alternatives){:target="_blank"}, для чего необходимо будет так же обновиться с помощью картриджа до прошивки, необходимой для запуска выбранного эксплойта.
Помните, что для использования [альтернативной точки входа в HBL](homebrew-launcher-alternatives){:target="_blank"} вам в большинстве случаев понадобится вторая уже прошитая приставка (либо устройство [Powersaves](https://amzn.to/2fb3VY7){:target="_blank"}) для записи кода эксплойта в картридж с игрой, который тоже, ясное дело, должен у вас быть (допускается использование sky3ds). 
<br><br>
Например, вы остановили свой выбор на oothax. Для его работы следует обновить приставку до версии ПО от 9.0.0 до 11.3 с помощью картриджа и следовать инструкции на сайте эксплойта. В определенный момент вам понадобится вторая приставка, или Powersave для записи эксплойта прямо в картридж. С другой стороны freakyhax или Ninjhax 2 не потребуют ничего, кроме самих картриджей, либо sky3ds, эмулирующий картриджи с указанными играми.
+ Использование [Hardmode](making-hardmod){:target="_blank"} или [ntrboot](ntrboot){:target="_blank"}, что требует определенных навыков работы с паяльником, или [совместимый с ntrboot картридж](ntrboot#Список-совместимых-картриджей){:target="_blank"} соответственно.        
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
      <td style="text-align: center;" colspan="2"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)"><img src="/images/hardmode.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/cart_update.png"></a> до 4.0-4.5 или 6.0-6.3</td>
      <td style="text-align: center;" rowspan="10">
		<a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)">
			<img src="/images/ntrhax.png">
		</a>
		<br><br>
		<a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)">
			<img src="/images/hardmode.png">
		</a>
	  </td>
	</tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" colspan="2">2.1.0</td>
      <td style="text-align: center;"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)"><img src="/images/hardmode.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/cart_update.png"></a> до 4.0-4.5 или 6.0-6.3</td>
      <td style="text-align: center;"><a href="installing-boot9strap-2xrsa">Установка boot9strap (2xrsa)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">2.2.0</td>
      <td style="text-align: center; font-weight: bold;"	>3.1.0</td>
      <td style="text-align: center;" colspan="2"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)"><img src="/images/hardmode.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/cart_update.png"></a> до 4.0-4.5 или 6.0-6.3</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">4.0.0</td>
      <td style="text-align: center; font-weight: bold;">4.5.0</td>
      <td style="text-align: center;"><a href="installing-boot9strap-mset">Установка boot9strap (MSET)</a></td>
      <td style="text-align: center;"><a href="installing-boot9strap-browser">Установка boot9strap (Browser)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">5.0.0</td>
      <td style="text-align: center; font-weight: bold;">5.1.0</td>
      <td style="text-align: center;"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)"><img src="/images/hardmode.png"></a>, или <a href="cart-update" title="Обновление прошивки с помощью картриджа с игрой"><img src="/images/cart_update.png"></a> до 6.0-6.3</td>
      <td style="text-align: center;"><a href="installing-boot9strap-browser">Установка boot9strap (Browser)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">6.0.0</td>
      <td style="text-align: center; font-weight: bold;">6.3.0</td>
      <td style="text-align: center;"><a href="installing-boot9strap-mset">Установка boot9strap (MSET)</a></td>
      <td style="text-align: center;"><a href="installing-boot9strap-browser">Установка boot9strap (Browser)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">7.0.0</td>
      <td style="text-align: center; font-weight: bold;">8.1.0</td>
      <td style="text-align: center;"><a href="ntrboot" title="Установка ntrboothax (необходим совместимый флеш-картридж)"><img src="/images/ntrhax.png"></a><a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)"><img src="/images/hardmode.png"></a></td>
      <td style="text-align: center;"><a href="installing-boot9strap-browser">Установка boot9strap (Browser)</a></td>
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
	<img src="/images/ntrhax.png" > - установка ntrboothax (необходим совместимый флеш-картридж)
</a>
<br>
<a href="making-hardmod" title="Установка через hardmode (необходимы навыки работы с паяльником)">
	<img src="/images/hardmode.png"> - установка через hardmode (необходимы навыки работы с паяльником)
</a>

{% endcapture %}
		
<div class="notice--info">{{ notice-7 | markdownify }}</div>


