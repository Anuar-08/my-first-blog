# Copilot Instructions for AI Agents

## Обзор архитектуры
- Проект основан на Django (см. `manage.py`, папки `blog/`, `mysite/`).
- Основные компоненты:
  - `blog/`: приложение с моделями, представлениями и миграциями.
  - `mysite/`: глобальные настройки, маршрутизация, запуск через WSGI/ASGI.
- База данных: SQLite (`db.sqlite3`).
- Виртуальное окружение: `anuvenv/` (используйте `Scripts/activate` для активации).

## Ключевые файлы и директории
- `manage.py`: точка входа для команд Django.
- `requirements.txt`: зависимости Python (Django, djangorestframework и др.).
- `blog/models.py`: определяет структуру данных.
- `blog/views.py`: реализует обработку HTTP-запросов.
- `mysite/settings.py`: конфигурация проекта.
- `mysite/urls.py`: маршрутизация URL.

## Рабочие процессы
- **Запуск сервера**: `python manage.py runserver`
- **Миграции**: `python manage.py makemigrations` и `python manage.py migrate`
- **Тесты**: `python manage.py test blog`
- **Создание суперпользователя**: `python manage.py createsuperuser`

## Конвенции и паттерны
- Модели размещаются в `blog/models.py`, миграции — в `blog/migrations/`.
- Представления (views) реализуются в `blog/views.py`.
- URL-маршруты определяются в `mysite/urls.py` и могут быть расширены в приложениях.
- Используйте DRF (`rest_framework`) для API, если требуется.
- Все команды выполняются через `manage.py`.
- Для новых приложений используйте `python manage.py startapp <имя>`.

## Интеграции и зависимости
- Django REST Framework (`rest_framework`) установлен для API.
- Все зависимости фиксируются в `requirements.txt`.
- Виртуальное окружение обязательно для разработки.

## Примеры паттернов
- Пример модели: `blog/models.py`
- Пример миграции: `blog/migrations/0001_initial.py`
- Пример view: `blog/views.py`
- Пример маршрута: `mysite/urls.py`

## Рекомендации для AI-агентов
- Всегда проверяйте структуру приложения перед изменениями.
- Следуйте существующим паттернам размещения кода.
- Для новых функций создавайте миграции и тесты.
- Не изменяйте файлы виртуального окружения (`anuvenv/`).

---

Если какие-либо разделы требуют уточнения или дополнения, пожалуйста, сообщите для доработки.