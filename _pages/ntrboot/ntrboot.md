---
title: "ntrboot"
lang: ru
permalink: ntrboot.html
author_profile: true
---
{% include toc title="Разделы" %}

## Общая информация

Если вы уже прошили ntrboot на ваш флешкартридж, вы можете перейти к странице [Установка boot9strap (ntrboot)](installing-boot9strap-ntrboot) для получения инструкций о том, как его использовать.
{: .notice--success}

Для установки boot9strap при помощи ntrboot требуется совместимый DS / DSi флешкартридж, на который можно прошить ntrboot.

{% capture notice-1 %}   
Эксплойт ntrboot совместим ТОЛЬКО со следующими флешкартриджами **(даже не спрашивайте про другие; совместимы только конкретно эти типы картриджей)**:

{% include /inc/ntrboot.txt %}
   
  ![]({{ "/images/screenshots/ntrboot-flashcarts.png" | absolute_url }})
  {: .text-center}
  {: .notice--info}

{% endcapture %}
<div class="notice--warning">{{ notice-1 | markdownify }}</div>
  
Обратите внимание, что конкретные методы могут иметь дополнительные сведения о совместимости.

Этот эксплойт, вне зависимости от метода прошивки, требует наличия небольшого магнита, если целевая консоль имеет складную конструкцию (любая консоль семейства 3DS кроме old 2DS с переключателем режима ожидания). Это необходимо, потому что эксплойт требует ввести консоль в режим ожидания, сохранив при этом доступ к кнопкам.

Чтобы проверить работоспособность магнита, приложите его к кнопкам (A)(B)(X)(Y) или рядом с ними, когда консоль включена. Проверьте, включает ли он режим ожидания. Если это так, то оба экрана будут выключаться, пока магнит находится на этом месте.
{: .notice--info}

Обратите внимание, что флешкартридж не сможет использоваться для своих стандартных функций, пока на нем установлен эксплойт ntrboot (кроме Acekard 2i, который сохраняет функционал, *но только на консолях 3DS с кастомной прошивкой*). В конце инструкций по прошивке ntrboot есть дополнительные шаги, чтобы по окончанию удалить его с флешкартриджа.

Обратите внимание, что в некоторых редких случаях процесс прошивки может **брикнуть** поддельный флешкартридж и навсегда сделать его нерабочим. Это маловероятно, но тем не менее поддерживаются только оригинальные флешкартриджи из списка. Чтобы уменьшить вероятность получения поддельного картриджа, рекомендуется использовать проверенный сайт для покупки флешкартриджа (например [NDS Card](http://www.nds-card.com/))
{: .notice--danger}

___

## Прошивка ntrboot (на не прошитой 3DS)

{% capture notice-2 %}   
[Этот метод](flashing-ntrboot-3ds-single-system) не требует ничего кроме вашей обычной не прошитой 3DS.

Обратите внимание, что на более поздних версиях 3DS заблокирован доступ к некоторым флешкартриджам, а некоторые из них на 3DS никогда не работали. Поэтому они не смогут запустить `.nds-файл` для прошивки эксплойта на новых версиях. 

Флешкартриджи, совместимые с ntrboot, способные запускать `.nds-файлы` на 3DS (с указанием версии прошивки):

{% include /inc/ntrboot_fw.txt %}

{% endcapture %}
<div class="notice--success">{{ notice-2 | markdownify }}</div>

## Прошивка ntrboot (несколько консолей 3DS)

[Этот метод](flashing-ntrboot-3ds-multi-system) требует временный доступ ко второй консоли семейства 3DS с установленным boot9strap или arm9loaderhax.
{: .notice--success}

## Прошивка ntrboot (NDS)

[Этот метод](flashing-ntrboot-nds) требует временного доступа к Nintendo DS или Nintendo DS Lite, совместимых с вашим флешкартриджем.
{: .notice--success}

## Прошивка ntrboot (DSi)

[Этот метод](flashing-ntrboot-dsi) требует временного доступа к Nintendo DSi, совместимой с вашим флешкартриджем.
{: .notice--success}

## Картридж с уже прошитым ntrboot 
{% capture notice-2 %}   

В данный момент на рынке только один картридж, идущий с уже зашитым ntrboot - [R4i-B9S от R4i-sdhc.com](http://R4i-sdhc.com). Имея на руках такой картридж, можно сразу переходить к [установке boot9strap](installing-boot9strap-ntrboot) в приставку, минуя установку ntrboot на картридж. 
<br><br>
Так же одним из вариантов может быть покупка подходящего картриджа по указанным ссылкам с просьбой к продавцу о прошивке ntrboot. В большинстве случаев продавец идет на встречу и прошивает загрузчик в картридж. Если вы купили картридж с уже прошитым ntrboot, можно сразу переходить к [установке boot9strap](installing-boot9strap-ntrboot).
{% endcapture %}
<div class="notice--success">{{ notice-2 | markdownify }}</div>