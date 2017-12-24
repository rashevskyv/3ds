---
title: "ntrboot"
lang: ru
permalink: ntrboot.html
author_profile: true
---
{% include toc title="Разделы" %}

## Общая информация

Если вы уже прошили ntrboot на ваш флешкартридж, вы можете перейти к странице [Установка boot9strap (ntrboot)](installing-boot9strap-ntrboot){:target="_blank"} для получения инструкций об установке b9s в приставку.
{: .notice--success}

Для установки boot9strap при помощи ntrboot требуется совместимый NDS / DSi флешкартридж, на который можно прошить ntrboot. Имейте ввиду, что некоторые производители картриджей продают их уже с прошитым ntrboot. 

Несмотря на то, что сам ntrboot работает вне зависимости от версии системного ПО приставки, ntrboot flasher (программа, с помощью которой идет установка ntrboot на картридж) работает на определенной версии прошивки, которая зависит от типа картриджа, на который происходит установка. Это означает, что некоторые картриджи можно прошить лишь на определенной версии системного ПО, если у вас не прошитая консоль. В случае с прошитой приставкой версия прошивки системы значения не имеет. 

Имейте в виду, что картриджи с так называемой "Time Bomb" (немалая часть DSTT-клонов по истечению определенной даты на системных часах приставки перестают работать) так же не смогут запускать `.*nds-файлы` после срабатывания "бомбы". Один из способов это обойти - перевести часы на несколько лет назад. 

Картриджи могут отличаться цветом корпуса, поэтому внимательно смотрите на наклейку. Обращайте внимание на сайт, указанный на наклейке. Рынок переполнен клонами китайских клонов, поэтому не удивляйтесь, если картридж, который должен работать - не работает. Возможно у вас клон, либо в картридже установлен чип, который в данный момент не поддерживается.

Важно понимать, что у флешкартриджа своя SD-карта, а у приставки своя и консоль не имеет никакого доступа к SD-карте картриджа, то есть ничего не может с неё читать и ничего не может на неё записывать. Так же у каждого картриджа есть своё собственное ядро, которое необходимо скачать с сайта, указанного на корпусе картриджа, или найти где-нибудь ещё. Ядро нужно записывать в корень SD-карты картриджа. Перед тем, как шить во флешкартридж ntrboot, закиньте на SD-карту картриджа ядро и убедитесь, что картридж работает и запускает игры и программы в формате `.nds` и только после этого приступайте к прошивке. 

Файлы для ntrboot и любые другие файлы нужно скидывать на SD-карту **приставки**, если не указано иное!

## Список совместимых картриджей

<table><colgroup> <col style="width: 20%;" span="1" /> <col style="width: 12%;" span="1" /> <col style="width: 8%;" span="1" /> <col style="width: 8%;" span="1" /> <col style="width: 8%;" span="1" /> <col style="width: 44%;" span="1" /> </colgroup>
<thead>
<tr>
<th style="text-align: center; font-weight: bold;">Картридж</th>
<th style="text-align: center; font-weight: bold;">Внешний вид</th>
<th style="text-align: center; font-weight: bold;">Версия 3DS</th>
<th style="text-align: center; font-weight: bold;">Версия DSi</th>
<th style="text-align: center; font-weight: bold;">Версия NDS</th>
<th style="text-align: center; font-weight: bold;">Примечания</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">Acekard 2i</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=160" target="blank">$20.99</a><br /><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_fleshka_acekard_2i_dlya_nintendo_ds_544116629" target="blank"><img src="/images/ru.png" /><br />₽1500</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/acekard.png"><img src="/images/flashcarts/acekard_small.png" /></a>&nbsp;<a href="/images/flashcarts/acekard2.png"><img src="/images/flashcarts/acekard2_small.png" /></a></td>
<td style="text-align: center;"><em>&le;4.3.0</em></td>
<td style="text-align: center;"><em>&le;1.4.4</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Может запускать DS-игры на взломаной приставке даже с установленным ntrboot и не требует удаления последнего.</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="https://gbatemp.net/threads/review-ace3ds-x.487871/" target="blank">Ace3DS X</a><br /><br />Цена:<br /><a href="http://3ds-flashcard.com/home/65-ace3ds-x-supports-3dsds-mode.html" target="blank">$41</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/ace3dsx.png"><img src="/images/flashcarts/ace3dsx_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;"><em>Не требует перепрошивки. Для смены режима работы используйте переключатель.</em></td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;">DSTT<br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=157" target="blank">$9.99</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/dstt.png"><img src="/images/flashcarts/dstt_small.png" /></a>&nbsp;<a href="/images/flashcarts/dstt2.png"><img src="/images/flashcarts/dstt2_small.png" /></a></td>
<td style="text-align: center;"><em>?</em></td>
<td style="text-align: center;"><em>?</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Только модели с определенными <a href="https://gist.github.com/Hikari-chin/6b48f1bb8dd15136403c15c39fafdb42" target="blank">чипами памяти</a> совместимы с ntrboot</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4ids.cn/r4ids-e.htm" target="blank">R4i Gold 3DS Plus</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=575" target="blank">$19</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4igold3ds+.png"><img src="/images/flashcarts/r4igold3ds+_small.png" /></a></td>
<td style="text-align: center;"><em>&le;4.3.0</em></td>
<td style="text-align: center;"><em>&le;1.4.4</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;"><em>Не требует перепрошивки. Для смены режима работы используйте переключатель.</em></td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://r4ids.cn/" target="blank">R4i Gold 3DS RTS</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=149" target="blank">$19.99</a><br /><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/fleshkartridzh_r4i_gold_dlya_nintendo_ds_dsi_3ds_2ds_604415936" target="blank"><img src="/images/ru.png" /><br />₽1500</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4i_gold_rts.png"><img src="/images/flashcarts/r4i_gold_rts_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">&nbsp;</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/aboute.asp" target="blank">R4i-SDHC.com 3DS RTS</a><br />с установленным b9s<br />и магнитом<br /><br />Цена:<br /><a href="https://vk.com/market-125012133?section=album_3&amp;w=product-125012133_1058176" target="blank"><img src="/images/ua.png" align="bottom" /><br />₴500</a><br /><a href="https://vk.com/market-125012133?section=album_3&amp;w=product-125012133_1058176" target="blank"><img src="/images/ru.png" /><br />₽1400</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_rts.png"><img src="/images/flashcarts/r4i-sdhc_rts_small.png" /></a><br /><strong>+ b9s</strong></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Картридж продается с предустановленным ntrboot<br /><br />"<strong>Timebomb</strong>":<br /><strong>1.87</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/aboute.asp" target="blank">R4i-SDHC.com 3DS RTS</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=146" target="blank">$13.99</a><br /><a href="https://vk.com/market-125012133?section=album_3&amp;w=product-125012133_1122131" target="blank"><img src="/images/ua.png" align="bottom" /><br />₴400</a><br /><a href="https://vk.com/market-125012133?section=album_3&amp;w=product-125012133_1122131" target="blank"><img src="/images/ru.png" /><br />₽1200</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_rts.png"><img src="/images/flashcarts/r4i-sdhc_rts_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">"<strong>Timebomb</strong>":<br /><strong>1.87</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4i-sdhc.com/B9SSector.asp" target="blank">R4i-SDHC.com 3DS B9S</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=574" target="blank">$15.99</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4i-sdhc_b9s.png"><img src="/images/flashcarts/r4i-sdhc_b9s_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Картридж продается с предустановленным ntrboot<br /><br />"<strong>Timebomb</strong>":<br /><strong>1.87</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Dual-Core 20XX</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-dc.png"><img src="/images/flashcarts/r4isdhc-dc_small.png" /></a></td>
<td style="text-align: center;"><em>&le;4.3.0</em></td>
<td style="text-align: center;"><em>&le;1.4.4</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Все картриджи r4i SDHC 20XX одинаковые<br /><br />"<strong>Timebomb</strong>":<br /><strong>3.9b</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4isdhc.com" target="blank">R4iSDHC.com Gold Pro RTS 20XX</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=490" target="blank">$9.99</a><br /><a href="https://www.avito.ru/moskva/igry_pristavki_i_programmy/r4i_ntrboot_kartridzh_1111381830" target="blank"><img src="/images/ru.png" /><br />₽1200</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-gp.png"><img src="/images/flashcarts/r4isdhc-gp_small.png" /></a>&nbsp;<a href="/images/flashcarts/r4isdhc-gp2.png"><img src="/images/flashcarts/r4isdhc-gp2_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Все картриджи r4i SDHC 20XX одинаковые<br /><br />"<strong>Timebomb</strong>":<br /><strong>3.9b</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://r4isdhc.com" target="blank">R4iSDHC.com RTS LITE 20XX</a><br /><br />Цена:<br /><a href="http://www.nds-card.com/ProShow.asp?ProID=450" target="blank">$13.99</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/r4isdhc-lite.png"><img src="/images/flashcarts/r4isdhc-lite_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Все картриджи r4i SDHC 20XX одинаковые<br /><br />"<strong>Timebomb</strong>":<br /><strong>3.9b</strong>: 3.09.19</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4infinity.com/" target="blank">Infinity 3 R4i</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/infinity.png"><img src="/images/flashcarts/infinity_small.png" /></a></td>
<td style="text-align: center;"><em>&le;{% include /vars/sys_version.txt %}</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">&nbsp;</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;">R4 3D Revolution</td>
<td style="text-align: center;"><a href="/images/flashcarts/3d_rev.png"><img src="/images/flashcarts/3d_rev_small.png" /></a></td>
<td style="text-align: center;"><em>?</em></td>
<td style="text-align: center;"><em>?</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">Аппаратный клон R4i Gold 3DS RTS ревизии HW A6</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;"><a href="http://www.r4ids.cn/" target="blank">R4 iGold 3DS Deluxe "Starter"</a></td>
<td style="text-align: center;"><a href="/images/flashcarts/starter.png"><img src="/images/flashcarts/starter_small.png" /></a>&nbsp;<a href="/images/flashcarts/starter_b.png"><img src="/images/flashcarts/starter_b_small.png" /></a></td>
<td style="text-align: center;"><em>4.1.0 - 4.5.0</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">&nbsp;</td>
</tr>
<tr>
<td style="text-align: center; font-weight: bold;">R4i Ultra</td>
<td style="text-align: center;"><a href="/images/flashcarts/ultra.png"><img src="/images/flashcarts/ultra_small.png" /></a></td>
<td style="text-align: center;"><em>&le;4.3.0</em></td>
<td style="text-align: center;"><em>&le;1.4.5</em></td>
<td style="text-align: center;"><em>Все</em></td>
<td style="text-align: center;">&nbsp;</td>
</tr>
</tbody>
</table>
  
Убедитесь, что ваш картридж корректно запускается. Убедитесь в наличии ядра или прошивки на SD-карте вашего флешкартриджа. За подробностями обратитесь к инструкции картриджа.
  
Обратите внимание, что конкретные методы могут иметь дополнительные сведения о совместимости.

Этот эксплойт, вне зависимости от метода прошивки, требует наличия небольшого магнита, если целевая консоль имеет складную конструкцию (любая консоль семейства 3DS кроме old 2DS с переключателем режима ожидания). Это необходимо, потому что эксплойт требует ввести консоль в режим ожидания, сохранив при этом доступ к кнопкам.

Чтобы проверить работоспособность магнита, приложите его к кнопкам {% include inc/btn.txt btn="A" %}{% include inc/btn.txt btn="B" %}{% include inc/btn.txt btn="X" %}{% include inc/btn.txt btn="Y" %} или рядом с ними, когда консоль включена. Проверьте, включает ли он режим ожидания. Если это так, то оба экрана будут выключаться, пока магнит находится на этом месте.
{: .notice--info}

Обратите внимание, что флешкартридж не сможет использоваться для своих стандартных функций, пока на нем установлен эксплойт ntrboot (кроме Acekard 2i, который сохраняет функционал, *но только на консолях 3DS с кастомной прошивкой*). Картридж даже не будет отображаться в меню приставки. В конце инструкций по прошивке ntrboot есть дополнительные шаги, чтобы по окончанию удалить его с флешкартриджа.

Обратите внимание, что в некоторых редких случаях процесс прошивки может **брикнуть** поддельный флешкартридж и навсегда сделать его нерабочим. Это маловероятно, но тем не менее поддерживаются только оригинальные флешкартриджи из списка. Чтобы уменьшить вероятность получения поддельного картриджа, рекомендуется использовать проверенный сайт для покупки флешкартриджа (например [NDS Card](http://www.nds-card.com/){:target="_blank"})
{: .notice--danger}

___

## Прошивка ntrboot (на не прошитой 3DS)

[Этот метод](flashing-ntrboot-3ds-single-system) не требует ничего кроме одной не прошитой консоли 3DS и совместимого флешкартриджа. Суть метода в запуске флешера формата `*.nds` через флешкартридж. Поэтому в первую очередь необходимо, чтобы флешкартридж виделся и запускался на вашей 3DS. Некоторые флешкартриджи не могут быть запущены на непрошитой приставке с системным ПО, выше определенной версии. 

Этот метод не совершенен и иногда с его помощью не прошиваются картриджи, которые прошиваются без проблем [этим методом](https://3ds.customfw.xyz/ntrboot#прошивка-ntrboot-с-привлечением-прошитой-3ds){:target="_blank"}.

## Прошивка ntrboot (с привлечением прошитой 3DS)

[Этот метод](flashing-ntrboot-3ds-multi-system) требует временный доступ ко второй консоли семейства 3DS с установленной кастомной прошивкой и b9s (если у вас a9lh, то вы не сможете запустить инсталлер, [переходите на boot9strap](a9lh-to-b9s){:target="_blank"}). Метод не требует, чтобы выбранный картридж был совместим с какой-либо определенной прошивкой. 

## Прошивка ntrboot (NDS)

[Этот метод](flashing-ntrboot-nds) требует временного доступа к Nintendo DS или Nintendo DS Lite, совместимой с вашим флешкартриджем. Суть метода в запуске флешера формата `*.nds` через флешкартридж. Поэтому в первую очередь необходимо, чтобы флешкартридж виделся и запускался на вашей 3DS. Некоторые флешкартриджи не могут быть запущены на непрошитой приставке с системным ПО, выше определенной версии. 

Этот метод не совершенен и иногда с его помощью не прошиваются картриджи, которые прошиваются без проблем [этим методом](https://3ds.customfw.xyz/ntrboot#прошивка-ntrboot-с-привлечением-прошитой-3ds){:target="_blank"}.

## Прошивка ntrboot (DSi)

[Этот метод](flashing-ntrboot-dsi) требует временного доступа к Nintendo DSi, совместимой с вашим флешкартриджем. Суть метода в запуске флешера формата `*.nds` через флешкартридж. Поэтому в первую очередь необходимо, чтобы флешкартридж виделся и запускался на вашей 3DS. Некоторые флешкартриджи не могут быть запущены на непрошитой приставке с системным ПО, выше определенной версии.

Этот метод не совершенен и иногда с его помощью не прошиваются картриджи, которые прошиваются без проблем [этим методом](https://3ds.customfw.xyz/ntrboot#прошивка-ntrboot-с-привлечением-прошитой-3ds){:target="_blank"}.

## Картридж с уже прошитым ntrboot 

Имея на руках такой картридж, можно сразу переходить к [установке boot9strap](installing-boot9strap-ntrboot) в приставку, минуя установку ntrboot на картридж. 

Так же одним из вариантов может быть покупка подходящего картриджа по указанным ссылкам с просьбой к продавцу о прошивке ntrboot. В большинстве случаев продавец идет на встречу и прошивает загрузчик в картридж. Если вы купили картридж с уже прошитым ntrboot, можно сразу переходить к [установке boot9strap](installing-boot9strap-ntrboot).