-------------------------------------------
Папки "nginx" и "postgres" для создания соотв. контейнеров.
Папка "survey" - само приложение.
-------------------------------------------
Запуск контейнера:

$ docker-compose up

С указанием запускаемого файла:

$ docker-compose -f ./docker-compose.yml up

Для перестроения (при изменений):

$ docker-compose up --build

В фоне:

$ docker-compose up -d


После запуска контейнера, перейти по http://127.0.0.1:8888/,
где будет документация по api.


-- доп информация --
-------------------------------------------
Доступ по "localhost" или "127.0.0.1", порт "8888".
Вод на Сайт: http://127.0.0.1:8888/  (или http://localhost:8888/)
Первая станица тех.задание, докуметация по API и вход в API.

API:  http://127.0.0.1:8888/api/v1/surveys/
API-Admin: http://127.0.0.1:8888/api/v1/api-admin/
Login API-Admin: http://127.0.0.1:8888/api/v1/api-auth/login/

Админ Django: http://127.0.0.1:8888/admin/

Доступ к админеру БД порт "9000":
http://127.0.0.1:9000/ или http://localhost:9000/
--------------------------------------------
-------------------------------------------
Доступ к БД из локалки:  192.168.0.244:5432
Для просмотра адреса:
$ docker network ls
$ docker network inspect <NETWORK_ID>
-------------------------------------------
Остановка контейнера:

$ docker-compose down


Удаляет контейнеры, сеть, но оставляет тома.
Для полной очистки можно их удалить:

$ docker volume ls
$ docker volume rm <VOLUME_NAME>
