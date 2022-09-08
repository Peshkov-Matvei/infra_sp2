# Проект API_YAMDB
### Описание
API проект для получения информации, выполненное в ходе подготовки к командной работе.
### Технологии
- Python
- Django
- Docker
- docker-compose
### Шаблон  env-файла
```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```
### Команды для запуска приложения
- Склонируйте репозитрий 
```
git clone https://github.com/Peshkov-Matvei/infra_sp2.git
```
- Войдите в папку infra/
- соберите образ docker-compoce
```
docker-compose up -d --build
```
- Запустите миграции
```
docker-compose exec web python manage.py migrate
```
- Запустите статику
```
docker-compose exec web python manage.py collectstatic --no-input
```
- Создайте суперюзера
```
docker-compose exec web python manage.py createsuperuser
```
