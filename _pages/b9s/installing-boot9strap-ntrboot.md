---
title: "Установка boot9strap (ntrboot)"
lang: ru
permalink: installing-boot9strap-ntrboot.html
author_profile: true
---

{% include toc title="Разделы" %}

Для использования [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme)-ссылок в этом руководстве необходим torrent-клиент, например [Deluge](http://dev.deluge-torrent.org/wiki/Download).
{: .notice--success}

## Что понадобится

* Магнит для ввода консоли в режим ожидания (если используется консоль складной конструкции)
* Флешкартридж с прошитым ntrboot
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(стандартный boot9strap; не `devkit-файл`, не `ntr-файл`)*
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z-архив`)*
* Свежая версия [OCS](https://github.com/Pirater12/ocs/releases/latest)

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту из приставки в компьютер
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Скопируйте `SafeB9SInstaller.firm` в корень SD-карты и переименуйте его в `boot.firm`
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты

    ![]({{ "/images/screenshots/boot9strap-ntrboot-file-layout.png" | absolute_url }})
    {: .notice--info}

1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть II - ntrboot

1. Используйте магнит, чтобы найти место на консоли, где срабатывает датчик режима ожидания
  + Этот шаг не требуется выполнять для консоли old 2DS (которая имеет переключатель режима ожидания)
1. Выключите консоль
1. Вставьте ваш флешкартридж в консоль
1. Поместите магнит на место, где срабатывает датчик режима ожидания
  + На консоли old 2DS вместо этого включите переключатель режима ожидания
1. На несколько секунд зажмите кнопки (Power) + (START) + (SELECT) + (X), затем отпустите
  + Может потребоваться несколько попыток
1. Если эксплойт сработал, запустится SafeB9SInstaller

### Часть III - Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. Уберите магнит от устройства
  + На old 2DS выйдите из режима сна переключателем
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения принудительно выключите консоль, удерживая кнопку питания
  + Ваша консоль будет загружаться только в SafeB9SInstaller до выполнения следующей части

### Часть IV - Настройка Luma3DS

1. Достаньте SD-карту из приставки и вставьте ее в компьютер
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты с заменой
1. Вставьте SD-карту в приставку и включите её
{% include /inc/luma_setup.txt %}
  + Если появляется ошибка, просто переходите к следующей странице

___


{% capture notice-6 %}   

Следующий шаг: [Завершение установки](finalizing-setup)

{% endcapture %}

<div class="notice--success">{{ notice-6 | markdownify }}</div>

___

Это дополнительный раздел, который позволяет вернуть флешкартридж в исходное состояние (чтобы использовать флешкартридж для его стандартных функций).

Обратите внимание, что Acekard 2i сохраняет возможность запускать `.nds` файлы, пока на нем установлен эксплойт ntrboot. Это относится только к случаю, когда Acekard 2i используется на 3DS с установленной кастомной прошивкой! Пока эксплойт ntrboot установлен на Acekard 2i, флешкартридж не может запускать `.nds` файлы на не прошитых консолях NDS, NDSL, DSi, или 3DS.

Не приступайте к этой части, пока вы не выполнили остальные инструкции на этой странице.

### Часть V - Удаление ntrboot

#### Что понадобится

{% include /inc/files/ntrboot_flasher_firm.txt %}
	+ **ТОЛЬКО для R4i-SDHC.com b9s**: <i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - [b9s-flasher-v1.0.zip](magnet:?xt=urn:btih:CE7DB5641C9B469B484F226928C0CEDF0A1634AA&dn=b9s-flasher-v1.0.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce)
* Резервная копия прошивки, соответствующая вашему флешкартриджу 
  + Обратите внимание, что если вы следовали инструкции "Прошивка ntrboot (Две консоли 3DS)", резервная копия уже существует в нужном месте, и скачивать ее не требуется
  + Если вы не знаете HW revision вашего флешкартриджа, просто попробуйте их все. Только правильная версия позволит запустить флешкартридж из меню HOME, но прошивка неправильной версии не испортит картридж:
   
<table>
  <colgroup>
    <col span="1" style="width: 27%;">
    <col span="1" style="width: 11%;">
    <col span="1" style="width: 12%;">
    <col span="1" style="width: 50%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center; font-weight: bold;">Флешкартридж</th>
      <th style="text-align: center; font-weight: bold;">HW revision</th>
      <th style="text-align: center; font-weight: bold;">Внешний вид</th>
      <th style="text-align: center; font-weight: bold;">Прошивка для восстановления</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; font-weight: bold;">DSTT<br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=157" target="blank">$9.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/dstt.png"><img src="/images/flashcarts/dstt.png"></a>&nbsp;<a href="/images/flashcarts/dstt2.png"><img src="/images/flashcarts/dstt2.png"></a></td>
      <td style="text-align: center;"><i>Отсутствует</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" rowspan="3"><a href="http://r4ids.cn/" target="blank">R4i Gold 3DS RTS</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=149" target="blank">$19.99</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_r4i_gold_dlya_nintendo_ds_dsi_3ds_2ds_604415936" target="blank">₽1500</a></td>
      <td style="text-align: center;">HW A5</td>
      <td style="text-align: center;" rowspan="3"><a href="/images/flashcarts/r4i_gold_rts.png"><img src="/images/flashcarts/r4i_gold_rts.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:e69774d8a950879e93b18a5c1ccd36ab305b4acd&dn=R4i_Gold_3DS_%28HW_A5%29-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A5)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center;">HW A6</td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:ed75f8b81b78dad0d98cea59e38f3f61a80d981d&dn=R4i_Gold_3DS_%28HW_A6%29-Flashrom.zip&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A6)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center;">HW A7</td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:fd1bc5c522988379ee931db45f82b223241ae729&dn=R4i_Gold_3DS_%28HW_A7%29-Flashrom.zip&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A7)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" rowspan="2"><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">Acekard 2i</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">$20.99</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_fleshka_acekard_2i_dlya_nintendo_ds_544116629" target="blank">₽1500</a></td>
      <td style="text-align: center;"> HW 81</td>
      <td style="text-align: center;" rowspan="2"><a href="/images/flashcarts/acekard.png"><img src="/images/flashcarts/acekard.png"></a>&nbsp;<a href="/images/flashcarts/acekard2.png"><img src="/images/flashcarts/acekard2.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:948e6865b57fa2fc469d68df500f774a6d5887a4&dn=Acekard_2i_%28HW_81%29-Flashrom.zip&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">Acekard_2i_(HW_81)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center;">HW 44</td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:d12b46b1bfadc6b03ff260ab90dcb136d890fd39&dn=Acekard_2i_%28HW_44%29-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">Acekard_2i_(HW_44)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/aboute.asp" target="blank">R4i-SDHC.com 3DS RTS</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=146" target="blank">$13.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_rts.png"><img src="/images/flashcarts/r4i-sdhc_rts.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:26BDE6B3F2A43AB819006AB2700EDC90A100D644&dn=R4i-SDHC_3DS_RTS-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i-SDHC_3DS_RTS-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/B9SSector.asp" target="blank">R4i-SDHC.com 3DS B9S</a><br><br>Цена:<br><a href="https://vk.com/market-125012133?section=album_3&w=product-125012133_1058176" target="blank">₴600</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_b9s.png"><img src="/images/flashcarts/r4i-sdhc_b9s.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="/files/b9s-flasher-v1.0.zip" target="blank">b9s-flasher-v1.0.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Dual-Core 20XX</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-dc.png"><img src="/images/flashcarts/r4isdhc-dc.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:D4D1AC33E221BCB5375081B81F95EDF8BAA71883&dn=R4iSDHC_Dual-Core_20XX-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">R4isdhc_com_-_Dual-Core_RTS.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Gold Pro RTS 20XX</a><br><br>Цена:<br><a href="https://vk.com/market-125012133?w=product-125012133_1122131%2Fquery" target="blank">$9.99</a><br><a href="https://vk.com/market-125012133?w=product-125012133_1122131%2Fquery" target="blank">₴600</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/r4i_ntrboot_kartridzh_1111381830" target="blank">₽1200</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-gp.png"><img src="/images/flashcarts/r4isdhc-gp.png"></a>&nbsp;<a href="/images/flashcarts/r4isdhc-gp2.png"><img src="/images/flashcarts/r4isdhc-gp2.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:9E122B8E93C0D2724123A703D71383580E958B17&dn=R4iSDHC_GOLD_Pro_20XX-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">R4iSDHC_GOLD_Pro_20XX-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://r4isdhc.com" target="blank">R4iSDHC.com RTS LITE 20XX</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=450" target="blank">$13.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-lite.png"><img src="/images/flashcarts/r4isdhc-lite.png"></a></td>
      <td style="text-align: center;"><i>Отсутствует</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4infinity.com/" target="blank">Infinity 3 R4i</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/infinity.png"><img src="/images/flashcarts/infinity.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:e69774d8a950879e93b18a5c1ccd36ab305b4acd&dn=R4i_Gold_3DS_%28HW_A5%29-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A5)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">R4 3D Revolution</td>
      <td style="text-align: center;">HW A6</td>
      <td style="text-align: center;"><a href="/images/flashcarts/3d_rev.png"><img src="/images/flashcarts/3d_rev.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:ed75f8b81b78dad0d98cea59e38f3f61a80d981d&dn=R4i_Gold_3DS_%28HW_A6%29-Flashrom.zip&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A6)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4ids.cn/" target="blank">Gold 3DS Deluxe "Starter"</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/starter.png"><img src="/images/flashcarts/starter.png"></a>&nbsp;<a href="/images/flashcarts/starter_b.png"><img src="/images/flashcarts/starter_b.png"></a></td>
      <td style="text-align: center;"><i>Отсутствует</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">R4i Ultra</td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/ultra.png"><img src="/images/flashcarts/ultra.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:614e9951a6c26145e68de34ed8c23a44bf190728&dn=R4i_Ultra-Flashrom.zip&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce" target="blank">R4i_Ultra-Flashrom.zip</a></i></td>
    </tr>
	</tbody>
</table>
   
#### Инструкции

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `ntrboot` в корне SD-карты
1. Скопируйте `backup.bin` из `.zip-архива` с резервной копией прошивки вашего картриджа в папку `/ntrboot/` в корне SD-карты
	+ Пользователи R4i-SDHC.com b9s копируют `r4i-sdhc.bin` из архива `b9s-flasher-v1.0.zip` в папку `/ntrboot/` в корне SD-карты
1. Создайте папку `payloads` внутри папки `luma` на SD-карте 
1. Скопируйте `ntrboot_flasher.firm` из `.zip-архива` ntrboot_flasher в папку `/luma/payloads/` на SD-карте
	+ Пользователи R4i-SDHC.com b9s копируют `r4i-sdhc.firm` из архива `b9s-flasher-v1.0.zip` в папку `/luma/payloads/` в корне SD-карты
1. Вставьте SD-карту обратно в консоль
1. Вставьте в консоль ваш DS / DSi флешкартридж, совместимый с ntrboot
1. Удерживайте кнопку (START) во время загрузки приставки, чтобы запустить luma chainloader
1. Запустите ntrboot_flasher
	+ Пользователи R4i-SDHC.com b9s запускают r4i-sdhc
1. Прочтите предупреждение на красном экране
1. Нажмите (A), чтобы продолжить
1. Выберите ваш флешкартридж
	+ Если вашего флешкартриджа нет в списке на верхнем экране, прочтите информацию о каждой из опций на нижнем экране, возможно вы найдете свой картридж в описании
1. Выберите "Restore Flash"
	+ Пользователи R4i-SDHC.com: выберите Restore Red Flash
1. Нажмите (A) чтобы продолжить
1. Дождитесь окончания процесса
1. Нажмите (A) для возврата в главное меню
1. Нажмите (B) чтобы выключить консоль