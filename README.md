# Пульт охраны банка

Это внутренний репозиторий для сотрудников банка «Сияние». Если вы попали в этот репозиторий случайно, то вы не сможете его запустить, т.к. у вас нет доступа к БД, но можете свободно использовать код вёрстки или посмотреть как реализованы запросы к БД.

Пульт охраны — это сайт, который можно подключить к удалённой базе данных с визитами и карточками пропуска сотрудников нашего банка.

### Как установить

Запросите доступ к БД у менеджера вашего банка. Для доступа вам понадобятся хост, порт, имя базы, имя пользователя и пароль. Они находятся в переменных окружения.

### Переменные окружения

Пример файла .env(его можно создать в корне проекта):

```
DEBUG=True
DATABASE_HOST=192.168.0.1
DATABASE_PORT=5432
DATABASE_NAME=databasename
DATABASE_USER=user
DATABASE_PASSWORD=pAsSwOrD
SECRET_KEY=replace_me
ALLOWED_HOSTS = 127.0.0.1
```

Python3 должен быть уже установлен. 
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```

Далее запустите проект:

```
python manage.py runserver
```

 В браузере перейдите по [адресу](http://127.0.0.1:8000/)
 
 Либо можно указать другой порт, например:

 ```
python manage.py runserver 0.0.0.0:9000
 ```

### Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/).