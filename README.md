# TaskiStack

TaskiStack — это веб-приложение на Django, контейнеризованное с помощью Docker и включающее REST API для управления задачами.

## 📆 Стек технологий

* Python / Django
* Django REST Framework
* Docker / Docker Compose
* SQLite (по умолчанию, можно заменить на PostgreSQL)
* GitHub Actions (CI/CD)

## 🚀 Быстрый старт

### 1. Клонировать репозиторий

```bash
git clone https://github.com/ShiroyashaSG/TaskiStack.git
cd TaskiStack
```

### 2. Создать `.env` файл

Пример .env:
```
POSTGRES_USER=django_user
POSTGRES_PASSWORD=mysecretpassword
POSTGRES_DB=django
DB_HOST=db
DB_PORT=5432
```

### 3. Собрать и запустить контейнеры

```bash
docker-compose up --build
```

Проект будет доступен по адресу [http://localhost:8000](http://localhost:8000)

### 4. Применить миграции и создать суперпользователя

```bash
docker-compose exec backend python manage.py migrate
docker-compose exec backend python manage.py createsuperuser
```

## 📊 Тесты

Для запуска тестов:

```bash
docker-compose exec backend python manage.py test
```

## ⚙️ CI/CD

Настроен GitHub Actions workflow (`.github/workflows/main.yml`) для автоматической сборки и тестирования проекта при каждом push.

## 📋 Лицензия

Проект распространяется по лицензии MIT.
