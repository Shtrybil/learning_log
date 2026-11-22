# Learning Log

Веб-приложение на Django для ведения личного журнала обучения.

## Возможности

- Регистрация и авторизация пользователей.
- Создание и просмотр тем обучения.
- Добавление записей к темам.
- Редактирование и удаление собственных записей.
- Административная панель Django.

## Используемые технологии

- Python 3.12
- Django 6.1.1
- SQLite
- Bootstrap 4
- Gunicorn
- WhiteNoise
- Docker и Docker Compose

## Локальный запуск

1. Клонировать репозиторий:

   ```bash
   git clone https://github.com/Shtrybil/learning_log.git
   cd learning_log
   ```

2. Создать виртуальное окружение:

   ```bash
   python -m venv ll_env
   ```

3. Активировать виртуальное окружение в Windows:

   ```powershell
   .\ll_env\Scripts\Activate.ps1
   ```

4. Установить зависимости:

   ```bash
   pip install -r requirements.txt
   ```

5. Выполнить миграции:

   ```bash
   python manage.py migrate
   ```

6. Запустить сервер:

   ```bash
   python manage.py runserver
   ```

Приложение будет доступно по адресу http://127.0.0.1:8000/.

## Запуск через Docker Compose

Для запуска через Docker Compose необходимо создать файл `.env` с настройками окружения, затем выполнить:

```bash
docker compose up -d --build
```

Проверить состояние контейнера:

```bash
docker compose ps
```

## Структура проекта

- `learning_log/` — настройки и конфигурация Django.
- `learning_logs/` — приложение с темами и записями.
- `users/` — приложение для регистрации и авторизации пользователей.
- `Dockerfile` — инструкция для сборки Docker-образа.
- `compose.yaml` — конфигурация Docker Compose.
- `requirements.txt` — зависимости проекта.