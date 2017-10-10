---
title: "Начнем"
permalink: /get-started.html
author_profile: true
---

{% include toc title="Разделы" %}

Разные модели устройств и версии прошивок требуют различных действий для установки кастомной прошивки с boot9strap. Эта страница поможет вам понять, откуда именно следует начать.

Нажмите на изображение вашего устройства, чтобы перейти на соответствующую страницу. Цвет вашего устройства может отличаться от представленного на картинках, вам стоит обратить внимание на расположение кнопок и особенности каждого типа устройства, чтобы сделать правильный выбор.

Если вы уже взламывали вашу 3DS ранее и использовали кастомную прошивку на основе EmuNAND, следуйте инструкциям, находясь на SysNAND. В конце все ваши данные будут перенесены из EmuNAND в SysNAND с B9S.

Эта страница содержит инструкции по установке boot9strap на *не взломанную* 3DS или 2DS. Если у вас уже установлен arm9loaderhax, и вы хотите обновиться до boot9strap, следуйте инструкциям в разделе [Обновление до boot9strap](a9lh-to-b9s).
{: .notice--primary}

Прежде чем начать, рекомендуется проверить свою SD-карту на ошибки с помощью [H2testw (Windows)](h2testw-windows), [F3 (Linux)](f3-linux), или [F3X (Mac)](f3x-mac)!
{: .notice--warning}

Если вы пользователь Windows, то перед началом работ убедитесь, что в вашей системе включено отображение расширений файлов. Если вы не знаете как это сделать, следуйте этой инструкции: [Расширения файлов (Windows)](file-extensions-windows)!
{: .notice--info}

#### Таблица устройств

<table>
  <colgroup>
    <col span="1" style="width: 50%;">
    <col span="1" style="width: 50%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: center">New 3DS или New 2DS</th>
      <th style="text-align: center">Old 3DS или Old 2DS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center">
	    <a href="get-started-new-3ds">
	      <img src="{{ base_path }}/images/new3ds.png" style="padding: 0.5em;">
		</a> 
		<a href="get-started-new-3ds">
		  <img src="{{ base_path }}/images/new3dsxl.png" style="padding: 0.5em;">
		</a> 
		<a href="get-started-new-3ds">
		  <img src="{{ base_path }}/images/new2dsxl.png" style="padding: 0.5em;">
		</a>
	  </td>
      <td style="text-align: center">
	    <a href="get-started-old-3ds">
		  <img src="{{ base_path }}/images/old3ds.png" style="padding: 0.5em;">
		</a>
		<a href="get-started-old-3ds">
		  <img src="{{ base_path }}/images/old3dsxl.png" style="padding: 0.5em;">
		</a>
		<a href="get-started-old-3ds">
		  <img src="{{ base_path }}/images/2ds.png" style="padding: 0.5em;">
		</a>
	  </td>
    </tr>
  </tbody>
</table>