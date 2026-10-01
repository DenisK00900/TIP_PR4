# Практическое занятие №4
по дисциплине «Технологии индустриального программирования».

# Требования
- Go 1.22 или выше
- Git

# Структура проекта
```text
F:.
│   go.mod
│   go.sum
│   main.go
│
├───internal
│   └───task
│           handler.go
│           model.go
│           repo.go
│
└───pkg
    └───middleware
            cors.go
            logger.go
```

# Скачивание и запуск
```text
git clone https://github.com/DenisK00900/TIP_PR4.git
cd TIP_PR4
go run .
```

# Запросы
```text
curl -i http://localhost:8080/
curl -i http://localhost:8080/health

curl -i -X POST http://localhost:8080/api/tasks -H "Content-Type: application/json" -d "{\"title\":\"Выучить chi\"}" //Создание новой задачи

curl -i http://localhost:8080/api/tasks //Получение всех задачь

curl -i http://localhost:8080/api/tasks/1 //Получение задачи по индексу

curl -i -X PUT http://localhost:8080/api/tasks/1 -H "Content-Type: application/json" -d "{\"title\":\"Выучить chi глубже\",\"done\":true}" //Изменение задачи (индекс задачи + изменение названия и статуса)

curl -i -X DELETE http://localhost:8080/api/tasks/2 //Удаление задачи по индексу

```
(или другой порт, если он был изменён)
