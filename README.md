# api_yamdb
api_yamdb

Описание проекта:
```
Проект представляет из себя социальную сеть в которой можно оставлять отзывы на 
фильмы, книги и музыку и ставить оценки.
```

# Как запустить проект:
В папку infra положить .env файл со следующими параметрами:
```
DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД
```

Запустить командой:
```
docker-compose docker-compose up --build -d
```

Выполнить миграции, создать суперпользователя и собрать статику
```
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic
```

Технологии которые использовались:
```
- Python
- Django
- Django REST Framework
```

Автор:
```
Иван Голенко
```
