# brytforst_mail-yandex-Termux
Всем привет севодня мы будем подабрывать народи к емейлам через брутфорст и термукса.

# !!!ВНИМАНИЕ!!!
### Автор данной статьи не несет отвествености за любите последствие от ёё протчение. Все материалы в исключительно образовательных целях!


#### Брутфорс - метод взлома различных учетных записей, путем подбора логина и пароля. В линуксе есть огромное количество брутфорсов, но сегодня мы разберем один и разберем его в термукс.
#### Hydra - взломщик входа в сеть.

Установка :

pkg install hydra

Чтобы получить справку, прописываем :

hydra -h

Теперь давайте попробуем провести перебор по айпи, допустим у меня в локальной сети находится как-то сервер:

hydra -V -L login -P pass ssh://192.168.1.20  

---

#### Как мы видим, мы произвели атаку по p 192.168.1.20 нацеленную на ssh.

---

### Сейчас попробую подробнее разобрать эту команду :

##### hydra - означает что запускаем гидру

##### "-V" - означает что будут перебраны все комбинации логинов и паролей из файлов 

##### "-L" - Файл с логинами

##### "-P" - Файл с паролями 

#### Тут всё работает алгоритмом, всё это выучить нельзя, можно только понимать, ведь всё здесь цепляется одно за другое. 

---

### Теперь давайте рассмотрим атаку уже на какой-нибудь сайт :

##### $hydra -V -S -L login -P pass smtp://smtp.mail.ru

##### Ключ -S  - это SSL шифрование

### Этой командой мы провели перебор, в маил. Скажу вам так - этот способ до сих пор рабочий. И один раз меня выручил. 
### В конце хочу оставить вам ключи из справки, и в следующей части мы разберем уже брутфорс социальных сетей)

##### -R - восстановить ранее прерванную сессию Hydra;
##### -S - использовать SSL для подключения;
##### -l - использовать логин;
##### -L - выбирать логины из файла со списком;
##### -p - использовать пароль;
##### -P - использовать пароль из файла со списком;
##### -M - взять список целей из файла;
##### -x - генератор паролей;
##### -u - по умолчанию hydra проверяет все пароли для первого логина, эта опция позволяет проверить один пароль для всех логинов;
##### -f - выйти, если правильный логин/пароль найден;
##### -o - сохранить результат в файл;
##### -t - количество потоков для программы;
##### -w - время между запросами в секундах;
##### -v - подробный вывод;
##### -V - выводить тестируемые логины и пароли.

А але есть один минус у mail.ru шифрований smtp а у Яндекса тоже вроди и ето плохо бо еслы би било https или http то было б все хорошо ну вроді были би некороторие слабких мечта а може и не били
Ну надеюсь вы разобрались итак Пака УДАЧИ!!!
