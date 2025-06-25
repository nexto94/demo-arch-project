

Demo project showed major skills in system design and API integrations

name: Demo project

structure:
  README.md: >
    Главная витрина проекта. Здесь кратко описывается:
    - Что за система моделируется (контекст)
    - Используемые технологии (стек)
    - Архитектурные схемы (ссылки на PNG)
    - Компоненты: API, события, брокер, CI/CD
    - Как запустить проект локально

  docs/
    c4-context.png: Контекстная диаграмма (C4 Level 1)
    c4-container.png: Диаграмма контейнеров (C4 Level 2)
    deployment-diagram.png: Диаграмма развёртывания (инфраструктура)
    ARCHITECTURE.md: >
      Подробное архитектурное описание:
      - Описание компонентов
      - Сценарии взаимодействий
      - Обоснование решений (trade-off'ы)
      - Ссылки на API и события

  api/
    openapi.yaml: OpenAPI 3.0 спецификация API (Swagger)

  events/
    user_created.json: JSON-схема события user.created
    status_changed.json: JSON-схема события status.changed

  services/
    api_mock/
      app.py: Простой FastAPI-сервис, реализующий API
      requirements.txt: Зависимости Python (FastAPI + Uvicorn)

  docker/
    docker-compose.yml: >
      Контейнеризация проекта:
      - mock-сервис
      - nginx как API Gateway
      - Redis (или RabbitMQ) как брокер сообщений

  postman/
    api-tests.postman_collection.json: Коллекция Postman-тестов для API

  .github/workflows/
    ci.yml: GitHub Actions: линтинг, тесты, docker build
