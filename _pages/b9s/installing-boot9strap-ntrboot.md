---
title: "Установка boot9strap (ntrboot)"
lang: ru
permalink: installing-boot9strap-ntrboot.html
author_profile: true
---

{% include toc title="Разделы" %}

Для использования [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme){:target="_blank"}-ссылок в этом руководстве необходим torrent-клиент, например [Deluge](http://dev.deluge-torrent.org/wiki/Download){:target="_blank"}.
{: .notice--success}

## Что понадобится

* Магнит для ввода консоли в режим ожидания (если используется консоль складной конструкции)
* Флешкартридж с прошитым ntrboot
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest){:target="_blank"}
{% include /inc/files/bootstrap_standart.txt %}
* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest){:target="_blank"} *(`.7z-архив`)*
{% include /inc/files/ocs.txt %}

## Инструкция

### Часть I - Подготовительные работы

1. Выключите консоль
1. Вставьте SD-карту из **приставки** в компьютер
1. Скопируйте `boot.3dsx` (OCS) в корень SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Скопируйте `SafeB9SInstaller.firm` из архива с SafeB9SInstaller в папку `/luma/payloads/`, если таковой нет - создайте её
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты

    ![]({{ "/images/screenshots/boot9strap-ntrboot-file-layout.png" | absolute_url }}){:target="_blank"}
    {: .notice--info}
	{: .text-center}

1. Вставьте SD-карту обратно в консоль
1. Включите консоль

### Часть II - ntrboot

1. Используйте магнит, чтобы найти место на консоли, где срабатывает датчик режима ожидания
  + Этот шаг не требуется выполнять для консоли old 2DS (которая имеет переключатель режима ожидания)
1. **Выключите консоль**
1. Вставьте ваш флешкартридж в консоль
1. Поместите магнит на место, где срабатывает датчик режима ожидания
  + На консоли old 2DS вместо этого включите переключатель режима ожидания
1. На несколько секунд зажмите кнопки {% include inc/btn.txt btn="POWER"%} + {% include inc/btn.txt btn="START" %} + {% include inc/btn.txt btn="SELECT" %} + {% include inc/btn.txt btn="X" %}, затем отпустите все, кроме {% include inc/btn.txt btn="START"%}
  + Может потребоваться несколько попыток
  + Убедитесь, что приставка **выключена**!!!
1. Если эксплойт сработал, запустится меню настройки Luma3DS

### Часть III - Настройка Luma3DS

{% include /inc/luma_setup.txt %}
  + **Вам нужно нажать и удерживать {% include inc/btn.txt btn="START"%}** до тех пор, пока не появится luma chainloader
1. Не отпускайте кнопку {% include inc/btn.txt btn="START"%}, пока не появится SafeB9SInstaller
  + Иногда бывает, что кнопку {% include inc/btn.txt btn="START"%} нужно отпустить на полсекунды и зажать снова, до появления SafeB9SInstaller

### Часть IV - Установка boot9strap

1. Дождитесь окончания всех проверок безопасности
1. Введите комбинацию клавиш, указанную на экране и нажмите {% include inc/btn.txt btn="A"%}
1. Уберите магнит от устройства, можете так же вытащить картридж из приставки
  + На old 2DS выйдите из режима сна переключателем
1. При появлении запроса нажмите {% include inc/btn.txt btn="A"%} для загрузки в Luma3DS

___


Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}

___

Это дополнительный раздел, который позволяет вернуть флешкартридж в исходное состояние (чтобы использовать флешкартридж для его стандартных функций).

Обратите внимание, что Acekard 2i сохраняет возможность запускать `.nds` файлы, пока на нем установлен эксплойт ntrboot. Это относится только к случаю, когда Acekard 2i используется на 3DS с установленной кастомной прошивкой! Пока эксплойт ntrboot установлен на Acekard 2i, флешкартридж не может запускать `.nds` файлы на не прошитых консолях NDS, NDSL, DSi, или 3DS.

Не приступайте к этой части, пока вы не выполнили остальные инструкции на этой странице.

## Удаление ntrboot

#### Что понадобится

{% include /inc/files/ntrboot_flasher_firm.txt %}
* Резервная копия прошивки, соответствующая вашему флешкартриджу 
  + Обратите внимание, что если вы следовали инструкции [Прошивка ntrboot (с привлечением прошитой 3DS)](https://3ds.customfw.xyz/flashing-ntrboot-3ds-multi-system), резервная копия уже существует в нужном месте, и скачивать ее не требуется
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
      <td style="text-align: center; font-weight: bold;" rowspan="2"><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">Acekard 2i</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">$20.99</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_fleshka_acekard_2i_dlya_nintendo_ds_544116629" target="blank"><img src="/images/ru.png"><br>₽1500</a></td>
      <td style="text-align: center;"> HW 81</td>
      <td style="text-align: center;" rowspan="2"><a href="/images/flashcarts/acekard.png"><img src="/images/flashcarts/acekard_small.png"></a>&nbsp;<a href="/images/flashcarts/acekard2.png"><img src="/images/flashcarts/acekard2_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:948e6865b57fa2fc469d68df500f774a6d5887a4&dn=Acekard_2i_%28HW_81%29-Flashrom.zip&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">Acekard_2i_(HW_81)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center;">HW 44</td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:d12b46b1bfadc6b03ff260ab90dcb136d890fd39&dn=Acekard_2i_%28HW_44%29-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">Acekard_2i_(HW_44)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.ace3ds.com/" target="blank">Ace3DS X</a><br><br>Цена:<br><a href="http://3ds-flashcard.com/home/65-ace3ds-x-supports-3dsds-mode.html" target="blank">$41</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/ace3dsx.png"><img src="/images/flashcarts/ace3dsx_small.png"></a></td>
      <td style="text-align: center;"><i>Не требует перепрошивки. Для смены режима работы используйте переключатель.</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">DSTT<br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=157" target="blank">$9.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/dstt.png"><img src="/images/flashcarts/dstt_small.png"></a>&nbsp;<a href="/images/flashcarts/dstt2.png"><img src="/images/flashcarts/dstt2_small.png"></a></td>
      <td style="text-align: center;"><i>Отсутствует</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4ids.cn/r4ids-e.htm" target="blank">R4i Gold 3DS Plus</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=575" target="blank">$19</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4igold3ds+.png"><img src="/images/flashcarts/r4igold3ds+_small.png"></a></td>
      <td style="text-align: center;"><i>Не требует перепрошивки. Для смены режима работы используйте переключатель.</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;" rowspan="3"><a href="http://r4ids.cn/" target="blank">R4i Gold 3DS RTS</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=149" target="blank">$19.99</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_r4i_gold_dlya_nintendo_ds_dsi_3ds_2ds_604415936" target="blank"><img src="/images/ru.png"><br>₽1500</a></td>
      <td style="text-align: center;">HW A5</td>
      <td style="text-align: center;" rowspan="3"><a href="/images/flashcarts/r4i_gold_rts.png"><img src="/images/flashcarts/r4i_gold_rts_small.png"></a></td>
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
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/aboute.asp" target="blank">R4i-SDHC.com 3DS RTS</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=146" target="blank">$13.99</a><br><a href="https://vk.com/market-125012133?section=album_3&w=product-125012133_1122131" target="blank"><img src="/images/ua.png" align="bottom"><br>₴400</a><br><a href="https://vk.com/market-125012133?section=album_3&w=product-125012133_1122131" target="blank"><img src="/images/ru.png"><br>₽1200</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_rts.png"><img src="/images/flashcarts/r4i-sdhc_rts_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:26BDE6B3F2A43AB819006AB2700EDC90A100D644&dn=R4i-SDHC_3DS_RTS-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i-SDHC_3DS_RTS-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/aboute.asp" target="blank">R4i-SDHC.com 3DS RTS<br>с установленным b9s<br>и магнитом</a><br><br>Цена:<br><a href="https://vk.com/market-125012133?section=album_3&w=product-125012133_1058176" target="blank"><img src="/images/ua.png" align="bottom"><br>₴500</a><br><a href="https://vk.com/market-125012133?section=album_3&w=product-125012133_1058176" target="blank"><img src="/images/ru.png"><br>₽1400</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_rts.png"><img src="/images/flashcarts/r4i-sdhc_rts_small.png"></a><br><b>+ b9s</b></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:26BDE6B3F2A43AB819006AB2700EDC90A100D644&dn=R4i-SDHC_3DS_RTS-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i-SDHC_3DS_RTS-Flashrom.zip</a></i><br>Картридж продается с предустановленным ntrboot</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/B9SSector.asp" target="blank">R4i-SDHC.com 3DS B9S</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=574" target="blank">$15.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_b9s.png"><img src="/images/flashcarts/r4i-sdhc_b9s_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:39ef29b9520db11cafd28399e2d79ee52c7a98e6&dn=R4i-SDHC_B9S-Flashrom.zip&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce" target="blank">R4i-SDHC_B9S-Flashrom.zip</a></i><br>Картридж продается с предустановленным ntrboot</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Dual-Core 20XX</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-dc.png"><img src="/images/flashcarts/r4isdhc-dc_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:D4D1AC33E221BCB5375081B81F95EDF8BAA71883&dn=R4iSDHC_Dual-Core_20XX-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">R4isdhc_com_-_Dual-Core_RTS.zip</a></i><br>Все картриджи r4i SDHC 20XX одинаковые</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Gold Pro RTS 20XX</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=490" target="blank">$9.99</a><br><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/r4i_ntrboot_kartridzh_1111381830" target="blank"><img src="/images/ru.png"><br>₽1200</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-gp.png"><img src="/images/flashcarts/r4isdhc-gp_small.png"></a>&nbsp;<a href="/images/flashcarts/r4isdhc-gp2.png"><img src="/images/flashcarts/r4isdhc-gp2_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:9E122B8E93C0D2724123A703D71383580E958B17&dn=R4iSDHC_GOLD_Pro_20XX-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce" target="blank">R4iSDHC_GOLD_Pro_20XX-Flashrom.zip</a></i><br>Все картриджи r4i SDHC 20XX одинаковые</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://r4isdhc.com" target="blank">R4iSDHC.com RTS LITE 20XX</a><br><br>Цена:<br><a href="http://www.nds-card.com/ProShow.asp?ProID=450" target="blank">$13.99</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-lite.png"><img src="/images/flashcarts/r4isdhc-lite_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:9ab860002df831d0af054248b60e6fb9fbaa92b2&dn=R4iSDHC_RTS_LITE_20XX-Flashrom.zip&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce" target="blank">R4iSDHC_GOLD_Pro_20XX-Flashrom.zip</a></i><br>Все картриджи r4i SDHC 20XX одинаковые</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4infinity.com/" target="blank">Infinity 3 R4i</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/infinity.png"><img src="/images/flashcarts/infinity_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:e69774d8a950879e93b18a5c1ccd36ab305b4acd&dn=R4i_Gold_3DS_%28HW_A5%29-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A5)-Flashrom.zip</a></i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">R4 3D Revolution</td>
      <td style="text-align: center;">HW A6</td>
      <td style="text-align: center;"><a href="/images/flashcarts/3d_rev.png"><img src="/images/flashcarts/3d_rev_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:ed75f8b81b78dad0d98cea59e38f3f61a80d981d&dn=R4i_Gold_3DS_%28HW_A6%29-Flashrom.zip&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce" target="blank">R4i_Gold_3DS_(HW_A6)-Flashrom.zip</a></i><br>Аппаратный клон R4i Gold 3DS RTS ревизии HW A6</td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;"><a href="http://www.r4ids.cn/" target="blank">R4i Gold 3DS Deluxe "Starter"</a></td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/starter.png"><img src="/images/flashcarts/starter_small.png"></a>&nbsp;<a href="/images/flashcarts/starter_b.png"><img src="/images/flashcarts/starter_b_small.png"></a></td>
      <td style="text-align: center;"><i>Отсутствует</i></td>
    </tr>
    <tr>
      <td style="text-align: center; font-weight: bold;">R4i Ultra</td>
      <td style="text-align: center;">-</td>
      <td style="text-align: center;"><a href="/images/flashcarts/ultra.png"><img src="/images/flashcarts/ultra_small.png"></a></td>
      <td style="text-align: center;"><i><i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для работы с ней."></i> - <a href="magnet:?xt=urn:btih:614e9951a6c26145e68de34ed8c23a44bf190728&dn=R4i_Ultra-Flashrom.zip&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce" target="blank">R4i_Ultra-Flashrom.zip</a></i></td>
    </tr>
	</tbody>
</table>
   
#### Инструкции

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `ntrboot` в корне SD-карты
1. Скопируйте `backup.bin` из `.zip-архива` с резервной копией прошивки вашего картриджа в папку `/ntrboot/` в корне SD-карты
1. Создайте папку `payloads` внутри папки `luma` на SD-карте 
1. Скопируйте `ntrboot_flasher.firm` из `.zip-архива` ntrboot_flasher в папку `/luma/payloads/` на SD-карте
1. Вставьте SD-карту обратно в консоль
1. Вставьте в консоль ваш DS / DSi флешкартридж, совместимый с ntrboot
1. Удерживайте кнопку {% include inc/btn.txt btn="START" %} во время загрузки приставки, чтобы запустить luma chainloader
1. Запустите ntrboot_flasher
1. Прочтите предупреждение на красном экране
1. Нажмите {% include inc/btn.txt btn="A" %}, чтобы продолжить
1. Выберите ваш флешкартридж
	+ Если вашего флешкартриджа нет в списке на верхнем экране, прочтите информацию о каждой из опций на нижнем экране, возможно вы найдете свой картридж в описании
1. Выберите "Restore Flash"
1. Нажмите {% include inc/btn.txt btn="A" %} чтобы продолжить
1. Дождитесь окончания процесса
1. Нажмите {% include inc/btn.txt btn="A" %} для возврата в главное меню
1. Нажмите {% include inc/btn.txt btn="B" %} чтобы выключить консоль

___

Следующий шаг: [Завершение установки](finalizing-setup)
{: .notice--success}