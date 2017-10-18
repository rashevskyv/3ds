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

* Свежая версия [ntrboot_flasher](https://github.com/kitling/ntrboot_flasher/releases/latest)
* Резервная копия прошивки, соответствующая вашему флешкартриджу 
  + Обратите внимание, что если вы следовали инструкции "Прошивка ntrboot (Две консоли 3DS)", резервная копия уже существует в нужном месте, и скачивать ее не требуется
  + Если вы не знаете HW revision вашего флешкартриджа, просто попробуйте их все. Только правильная версия позволит запустить флешкартридж из меню HOME, но прошивка неправильной версии не испортит картридж:
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`r4i-sdhc-flashrom`](magnet:?xt=urn:btih:8243F5EBDB0B22FF296556AAF9D3057EF52AE2AA&dn=r4i-sdhc-flashrom.zip&tr=udp%3a%2f%2fexplodie.org%3a6969%2fannounce&tr=http%3a%2f%2ftorrent.gresille.org%2fannounce&tr=udp%3a%2f%2fzer0day.ch%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.leechers-paradise.org%3a6969%2fannounce&tr=udp%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftorrent.gresille.org%3a80%2fannounce&tr=udp%3a%2f%2ftracker.filetracker.pl%3a8089%2fannounce&tr=udp%3a%2f%2ftracker.tiny-vps.com%3a6969%2fannounce&tr=http%3a%2f%2ftracker.tfile.me%2fannounce&tr=udp%3a%2f%2ftracker.yoshi210.com%3a6969%2fannounce&tr=http%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=http%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=http%3a%2f%2ftracker.baravik.org%3a6970%2fannounce&tr=http%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2f9.rarbg.com%3a2710%2fanno) *(подходит для картриджей семейства r4i-sdhc.com и r4isdhc.com)*
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`R4i_Gold_3DS_(HW_A7)-Flashrom.zip`](magnet:?xt=urn:btih:fd1bc5c522988379ee931db45f82b223241ae729&dn=R4i_Gold_3DS_%28HW_A7%29-Flashrom.zip&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce) *(Также подходит для **R4i Gold 3DS RTS**)*
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`R4i_Gold_3DS_(HW_A6)-Flashrom.zip`](magnet:?xt=urn:btih:ed75f8b81b78dad0d98cea59e38f3f61a80d981d&dn=R4i_Gold_3DS_%28HW_A6%29-Flashrom.zip&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce) *(Также подходит для **R4 3D Revolution**)*
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`R4i_Gold_3DS_(HW_A5)-Flashrom.zip`](magnet:?xt=urn:btih:e69774d8a950879e93b18a5c1ccd36ab305b4acd&dn=R4i_Gold_3DS_%28HW_A5%29-Flashrom.zip&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce) *(Также подходит для **Infinity 3 R4i**)*
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - `R4i_Gold_3DS_"Starter"-Flashrom.zip` -- *Отсутствует*
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Используйте торрент-клиент для загрузки файла."></i> - [`Acekard_2i_(HW_81)-Flashrom.zip`](magnet:?xt=urn:btih:948e6865b57fa2fc469d68df500f774a6d5887a4&dn=Acekard_2i_%28HW_81%29-Flashrom.zip&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce)
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`Acekard_2i_(HW_44)-Flashrom.zip`](magnet:?xt=urn:btih:d12b46b1bfadc6b03ff260ab90dcb136d890fd39&dn=Acekard_2i_%28HW_44%29-Flashrom.zip&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce)
  + <i class="fa fa-magnet" aria-hidden="true" title="Это magnet-ссылка. Воспользуйтесь торрент-клиентом, чтобы скачать этот файл."></i> - [`R4i_Ultra-Flashrom.zip`](magnet:?xt=urn:btih:614e9951a6c26145e68de34ed8c23a44bf190728&dn=R4i_Ultra-Flashrom.zip&tr=udp%3A%2F%2Ftracker.yoshi210.com%3A6969%2Fannounce&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.tfile.me%2Fannounce&tr=udp%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2F9.rarbg.com%3A2710%2Fannounce&tr=http%3A%2F%2Ftracker.aletorrenty.pl%3A2710%2Fannounce&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fexplodie.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker1.wasabii.com.tw%3A6969%2Fannounce&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce&tr=udp%3A%2F%2Ftorrent.gresille.org%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce&tr=http%3A%2F%2Ftracker.baravik.org%3A6970%2Fannounce&tr=http%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce&tr=http%3A%2F%2Fp4p.arenabg.com%3A1337%2Fannounce&tr=udp%3A%2F%2Ftracker.filetracker.pl%3A8089%2Fannounce&tr=udp%3A%2F%2Fzer0day.ch%3A1337%2Fannounce&tr=http%3A%2F%2Ftorrent.gresille.org%2Fannounce)

#### Инструкции

1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. Создайте папку `ntrboot` в корне SD-карты
1. Скопируйте `backup.bin` из `.zip-архива` с резервной копией прошивки вашего картриджа в папку `/ntrboot/` в корне SD-карты
1. Создайте папку `payloads` внутри папки `luma` на SD-карте 
1. Скопируйте `ntrboot_flasher.firm` из `.zip-архива` ntrboot_flasher в папку `/luma/payloads/` на SD-карте **исходной 3DS**
1. Вставьте SD-карту обратно в консоль
1. Вставьте в консоль ваш DS / DSi флешкартридж, совместимый с ntrboot
1. Запустите ntrboot_flasher, держа нажатой кнопку (START) во время загрузки
1. Прочтите предупреждение на красном экране
1. Нажмите (A), чтобы продолжить
1. Выберите ваш флешкартридж
	+ Если вашего флешкартриджа нет в списке на верхнем экране, прочтите информацию о каждой из опций на нижнем экране
1. Выберите "Restore Flash"
1. Нажмите (A) чтобы продолжить
1. Дождитесь окончания процесса
1. Нажмите (A) для возврата в главное меню
1. Выберите "Exit" чтобы выключить консоль