---
title: Начнем
permalink: /get-started.html
author_profile: true
---

Эта страница содержит инструкции по установке boot9strap на *не взломанную* 3DS или 2DS. Если у вас уже установлен arm9loaderhax, и вы хотите обновиться до boot9strap, следуйте инструкциям в разделе [обновление до boot9strap](a9lh-to-b9s){:target="_blank"}.

Прежде чем начать, рекомендуется проверить свою SD-карту на ошибки с помощью [H2testw (Windows)](h2testw-windows){:target="_blank"}, [F3 (Linux)](f3-linux){:target="_blank"}, или [F3X (Mac)](f3x-mac){:target="_blank"}!

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!

Если на приставке нет важных для вас данных, то я крайне рекомендую произвести форматирование [приставки](clean_sd#i-Форматирование-приставки) и [SD-карты](clean_sd#ii-Форматирование-sd-карты) перед началом взлома. **Помните, что форматирование уничтожит все ваши данные на приставке и SD-карте. Делайте его только в том случае, если на приставке и карте нет ничего важного!**
{: .notice--warning}

___

Столбцы "С" и "По" обозначают границы диапазона. Это означает, к примеру, что диапазон "с 9.0.0 по 9.2.0" включает в себя 9.0.0, 9.1.0 и 9.2.0.

Последнее число вашей версии системы (после дефиса) относится к версии браузера. Если версия оканчивается на -0, значит, у вас отсутствует браузер, любое другое число говорит о том, что браузер установлен. В настоящее время все New 3DS и New 2DS имеют браузер!

Например, если у вас версия прошивки "5.0.0-**0**E", необходимо выбрать ячейку на пересечении колонки "Без браузера" и ряда "С 5.0.0 по 5.1.0" так как версия системы находится в этом диапазоне и в системе не установлен браузер.

Версия программного обеспечения вашего устройства отображается в правом нижнем углу верхнего экрана в приложении Системные настройки (System settings).
{: .notice--success}

![]({{ "/images/screenshots/system-version.png" | absolute_url }}){:target="_blank"}
{: .text-center}
{: .notice--info}

#### Таблица версий

Для всех консолей, любой версии прошивки можно использовать [NTRBootHax](ntrboot){:target="_blank"} или [Steelminer](steelminer){:target="_blank"}, даже если они не указаны в таблице! Для первого понадобится совместимый флеш-картридж, но этот метод наиболее простой, для второго - обновиться до последней версии системного ПО и этот метод комплексный и более сложный. <br><br>**Вы можете прошить любую приставку с любой изначальной версией системного ПО, обновив её до {% include /vars/sys_version.txt %} через Системные настройки, а затем воспользовавшись методом [Steelminer](steelminer){:target="_blank"}. Этот метод не требует дополнительных вложений**
{: .notice--warning}

<table>
  <colgroup>
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 38%;">
    <col span="1" style="width: 38%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;">С</th>
      <th style="text-align: center; font-weight: bold;">По</th>
      <th style="text-align: center; font-weight: bold;">Браузера нет</th>
      <th style="text-align: center; font-weight: bold;">Браузер есть</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">1.0.0</td>
	  <td style="text-align: center; font-weight: bold;">2.0.0</td>
      <td style="text-align: center;" colspan="2"><a href="ntrboot">ntrboothax</a> или <a href="steelminer">Steelminer</a></td>
	</tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" colspan="2">2.1.0</td>
      <td style="text-align: center;"><a href="ntrboot">ntrboothax</a> или <a href="steelminer">Steelminer</a></td>
      <td style="text-align: center;"><a href="installing-boot9strap-2xrsa">Установка boot9strap (2xrsa)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">2.2.0</td>
      <td style="text-align: center; font-weight: bold;">2.2.0</td>
      <td style="text-align: center;" colspan="2"><a href="ntrboot">ntrboothax</a> или <a href="steelminer">Steelminer</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">3.0.0</td>
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
      <td style="text-align: center;" colspan="2"><a href="steelminer">Steelminer</a><br><b>(не требует вложения денег)</b></td>
    </tr>
</tbody>
</table>