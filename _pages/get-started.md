---
title: Начнем
permalink: get-started.html
---

Прежде чем начать, рекомендуется [проверить свою SD-карту на подлинность](https://customfw.xyz/test_sd){:target="_blank"}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows){:target="_blank"}!

Если на приставке нет важных для вас данных, то я крайне рекомендую произвести форматирование [приставки](clean_sd#i-форматирование-приставки) и [SD-карты](https://customfw.xyz/format_sd) перед началом взлома. **Помните, что форматирование уничтожит все ваши данные на приставке и SD-карте. Делайте его только в том случае, если на приставке и карте нет ничего важного!**
{: .notice--warning}

___


Версия программного обеспечения вашего устройства отображается в правом нижнем углу верхнего экрана в приложении **Системные настройки** (System settings).
{: .notice--success}

![]({{ "/images/screenshots/system-version.png" | absolute_url }}){:target="_blank"}
{: .text-center}
{: .notice--info}

### Таблица версий

Для всех консолей, любой версии прошивки можно использовать [NTRBootHax](ntrboot){:target="_blank"}, даже если они не указаны в таблице! Для этого понадобится совместимый флеш-картридж, но этот метод наиболее простой. <br><br>**Вы можете прошить любую приставку с любой изначальной версией системного ПО, обновив её до {% include /vars/sys_version.txt %} через Системные настройки, а затем воспользовавшись соответствующим методом из таблицы**
{: .notice--warning}

<table>
  <colgroup>
    <col style="width: 5%;" span="1" />
    <col style="width: 5%;" span="1" />
    <col style="width: 38%;" span="1" />
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;" rowspan="2">С</th>
      <th style="text-align: center; font-weight: bold;" rowspan="2">По</th>
    </tr>
    <tr>
      <th style="text-align: center; font-weight: bold;">Old 3DS</th>
      <th style="text-align: center; font-weight: bold;">New 3DS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">1.0.0</td>
      <td style="text-align: center; font-weight: bold;">11.3.0</td>
      <td style="text-align: center;" colspan="2"><a href="soundhax">Установка boot9strap с помощью Soundhax</a></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">11.4.0</td>
      <td style="text-align: center; font-weight: bold;">{% include /vars/sys_version.txt %}</td>
      <td style="text-align: center;" rowspan="2"><a href="safecerthax">Установка boot9strap (safecerthax)</a><br /></td>
      <td style="text-align: center;"><a href="browserhax">Установка boot9strap (через браузер)</a><br /></td>
    </tr>
  </tbody>
</table>