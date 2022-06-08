{% capture notice-10 %}
**Universal Updater** - программа для обновления кастомной прошивки. Запустите его чтобы проверить наличие новой версии Luma3DS. Найдите на верхнем экране Luma3DS, выделите её курсором и 
нажмите {% include inc/btn.txt btn="A" %}, выберите 'boot.firm'. После окончания закачки перезагрузите консоль. Версия Luma3DS бдет автоматически помещена и в CTRNAND єто нужно только для того, чтобы приставка могла загружаться без SD-карты.<br><br>**Обновление Luma 3DS - это не тоже самое что обновление системы (System Update). В данный момент у вас самая свежая версия Luma3DS и обновлять её не нужно.**
{% endcapture %}

<div class="notice--info">{{ notice-10 | markdownify }}</div>

{% capture notice-10 %}
По умолчанию будет запускаться Luma3DS CFW SysNAND, установленная на SD-карту.    
Для запуска конфигуратора Luma3DS включите консоль с зажатой кнопкой {% include inc/btn.txt btn="SELECT" %}.    
<br>
Для запуска Luma3DS chainloader удерживайте {% include inc/btn.txt btn="START" %} при загрузке системы (обратите внимание, что Luma3DS chainloader меню отображается только если существует более одного приложения).
<br><br>
Нажатие {% include inc/btn.txt btn="L" %} + {% include inc/btn.txt btn="DOWN" %} + {% include inc/btn.txt btn="SELECT" %} в запущенной системе открывает меню Rosalina, встроенное в Luma3DS.         
{% endcapture %}

<div class="notice--info">{{ notice-10 | markdownify }}</div>

{% capture notice-6 %}   
Если вы хотите заменить вашу SD-карту на более ёмкую, [отформатируйте](https://customfw.xyz/format_sd) новую SD-карту в FAT32 и скопируйте на неё содержимое SD-карты приставки.     

Если размер новой SD-карты превышает 32Гб, используйте для форматирования [guiformat](http://www.ridgecrop.demon.co.uk/index.htm?guiformat.htm) для Windows, [gparted](http://gparted.org/download.php) для Linux, или [Disk Utility](https://support.apple.com/en-gb/guide/disk-utility/format-a-disk-for-windows-computers-dskutl1010/mac) для Mac.    
{% endcapture %}

<div class="notice--info">{{ notice-6 | markdownify }}</div>

Для использования [NTR CFW](https://github.com/44670/BootNTR/){:target="_blank"}, установите [BootNTR Selector](https://gbatemp.net/threads/432911/){:target="_blank"}. Если вы не знаете что это, - не устанавливайте. 
{: .notice--info}

Чтобы узнать, как сменить регион своей консоли, обратитесь к разделу [Смена региона](region-changing){:target="_blank"}.
{: .notice--success}

Для получения информации по использованию различных функций GodMode9 обратитесь к разделу [Использование GodMode9](godmode9-usage){:target="_blank"}.
{: .notice--success}

Для справки об использовании различных функций Luma3DS обратитесь к её [вики](https://github.com/AuroraWright/Luma3DS/wiki/Options-and-usage){:target="_blank"} (англ.).
{: .notice--success}

Различные инструкции, не имеющие прямого отношения ко взлому, однако помогающие лучше изучить возможности 3DS на кастомной прошивке и эффективнее ей пользоваться находятся [здесь](addons){:target="_blank"}.
{: .notice--success}