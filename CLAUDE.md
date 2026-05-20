# Platform Core — правила для Claude Code

## Стек
- Backend: Python 3.12, FastAPI, SQLAlchemy 2.0, Pydantic v2
- Frontend: Vue 3, TypeScript, AG Grid
- Meta DB: PostgreSQL 16
- Контейнеризация: Docker, Docker Compose

## Архитектура
Трёхзвенная система:
- Frontend SPA (Vue 3)
- Backend API (FastAPI) с двумя движками: MetaEngine и QueryEngine
- Meta DB (PostgreSQL) — хранит конфигурацию
- Legacy DB — только чтение через SQLAlchemy introspection, структуру не менять

## Правила
- Все запросы к Legacy DB только через repositories/legacy_repo.py
- Никогда не делать ALTER/DROP/CREATE на Legacy DB
- Миграции только для Meta DB через Alembic
- Все секреты только через .env, никогда не хардкодить
- Покрытие тестами минимум 70%
- Типизация обязательна везде (Python type hints, TypeScript strict mode)
