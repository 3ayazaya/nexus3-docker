# Nexus3 - хранилище артефактов, репозиториев и тд

## Сборка проекта

> Для удобства я буду использовать [Task](https://taskfile.dev/installation/)

Заполняем файл с переменными `.env`

Собираем Docker-образ, скачиваем зависимости и заливаем в container registry

> Если заливать на регистри не нужно - комментируем строки в Taskfile.yaml, которые содержат `docker push`

```bash
task build
```
## Запуск среды для разработки

```bash
task run-dev
```

## Запуск для продакшн

> Изменены точки монтирования и порты

```bash
task run-prod
```

или

 ```bash
source .env
docker-compose -f docker-compose.yaml -d
```