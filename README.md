# DB Lowcode Core

Универсальная low-code платформа для работы с legacy базами данных.

## Стек
- **Backend:** Python 3.12, FastAPI, SQLAlchemy 2.0
- **Frontend:** Vue 3, TypeScript, AG Grid
- **Meta DB:** PostgreSQL 16
- **Инфраструктура:** Docker, Docker Compose, GitHub Actions

## Быстрый старт
```bash
cp .env.example .env
# заполни .env своими значениями
docker compose up --build -d
```

## Сервисы
- Frontend: http://localhost:5173
- Backend API: http://localhost:8000
- Swagger docs: http://localhost:8000/docs
