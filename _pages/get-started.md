---
title: Начнем
permalink: /get-started.html
author_profile: true
---

{% include toc title="Разделы" %}

Прежде чем начать, рекомендуется [проверить свою SD-карту на подлинность](https://customfw.xyz/test_sd){:target="_blank"}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!

Если на приставке нет важных для вас данных, то я крайне рекомендую произвести форматирование [приставки](clean_sd#i-Форматирование-приставки) и [SD-карты](clean_sd#ii-Форматирование-sd-карты) перед началом взлома. **Помните, что форматирование уничтожит все ваши данные на приставке и SD-карте. Делайте его только в том случае, если на приставке и карте нет ничего важного!**
{: .notice--warning}

___

Столбцы "**С**" и "**По**" обозначают границы диапазона. Это означает, к примеру, что диапазон "**с 9.0.0 по 9.2.0**" включает в себя 9.0.0, 9.1.0 и 9.2.0.

Версия программного обеспечения вашего устройства отображается в правом нижнем углу верхнего экрана в приложении Системные настройки (System settings).
{: .notice--success}

![]({{ "/images/screenshots/system-version.png" | absolute_url }}){:target="_blank"}
{: .text-center}
{: .notice--info}

### Таблица версий

Для всех консолей, любой версии прошивки можно использовать [NTRBootHax](ntrboot){:target="_blank"}, даже если они не указаны в таблице! Для первого понадобится совместимый флеш-картридж, но этот метод наиболее простой, для второго - обновиться до последней версии системного ПО. <br><br>**Вы можете прошить любую приставку с любой изначальной версией системного ПО, обновив её до {% include /vars/sys_version.txt %} через Системные настройки, а затем воспользовавшись методом [Steelminer](steelminer){:target="_blank"}. Этот метод не требует дополнительных вложений**
{: .notice--warning}

<table>
  <colgroup>
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 5%;">
    <col span="1" style="width: 38%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;">С</th>
      <th style="text-align: center; font-weight: bold;">По</th>
      <th style="text-align: center; font-weight: bold;">Способ прошивки</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">1.0.0</td>
	  <td style="text-align: center; font-weight: bold;">2.0.0</td>
      <td style="text-align: center;"><a href="ntrboot">ntrboothax</a> или <a href="steelminer">Steelminer</a></td>
	</tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">2.1.0</td>
      <td style="text-align: center; font-weight: bold;">8.1.0</td>
      <td style="text-align: center;"><a href="installing-boot9strap-soundhax">Установка boot9strap (Soundhax)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">9.0.0</td>
      <td style="text-align: center; font-weight: bold;">11.3.0</td>
      <td style="text-align: center;"><a href="homebrew-launcher-soundhax">Homebrew Launcher (Soundhax)</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">11.4.0</td>
      <td style="text-align: center; font-weight: bold;">{% include /vars/sys_version.txt %}</td>
      <td style="text-align: center;"><a href="browserhax">Homebrew Launcher (Browserhax)</a><br><b>(не требует вложения денег)</b></td>
    </tr>
    <!--<tr>
      <td style="text-align: center; font-weight: bold;" colspan="2">{% include /vars/sys_version.txt %}</td>
      <td style="text-align: center;"><a href="steelminer">Steelminer</a><br><b>(не требует вложения денег)</b></td>
    </tr>-->
</tbody>
</table>