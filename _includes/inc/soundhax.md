1. Выберите версию **SoundHax**, соответствующую версии вашего устройства (OLD или NEW), ПО и региона и поместите скачанный `.m4a`-файл в корень вашей SD-карты
    * Версию прошивки можно посмотреть в настройках приставки. Она будет написана справа внизу на верхнем экране.
    * Если по нажатию на кнопку "**Скачать M4A**" вам просто откроется окно с видеофайлом, нажмите "**Ctrl+S**", чтобы сохранить его
   
    <link href="files/payload/soundhax.css" rel="stylesheet" type="text/css" media="all" />
    <div class="downloads">
        <div class="btn-group region">
            <span>Регион консоли:</span>
            <button class="group selected" id="eur">EUR</button>
            <button class="group" id="usa">USA</button>
            <button class="group" id="jpn">JPN</button>
            <button class="group" id="kor">KOR</button>
        </div>
        <div class="btn-group console">
            <span>Ревизия консоли:</span>
            <button class="group" id="n3ds">NEW</button>
            <button class="group" id="o3ds">OLD</button>
        </div>
        <div class="btn-group firmware">
            <span>Версия системного ПО:</span>
            <button class="group" id="v2.1and2.2">2.1.0 - 2.2.0</button>
            <button class="group" id="v3.xand4.x">3.0.0 - 4.5.0</button>
            <button class="group" id="post5.0">5.0.0 - 11.3.0</button>
        </div>
        <button id="download" class="round group" href="poop">Скачать M4A</button>
    </div>
    <script src="assets/js/jquery-3.1.1.min.js"></script>
    <script src="assets/js/scripts.js"></script>