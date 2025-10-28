## Практическое задание № 6

## Использование ORM (GORM). Модели, миграции и связи между таблицами.

Студент группы *ЭФМО-02-25 Пягай Даниил Игоревич*

## Описание

**Цели:**

1.	Понять, что такое ORM и чем удобен GORM.
2.	Научиться описывать модели Go-структурами и автоматически создавать таблицы (миграции через AutoMigrate).
3.	Освоить базовые связи: 1:N и M:N + выборки с Preload.
4.	Написать короткий REST (2–3 ручки) для проверки результата.


## Открываем postgres и создаём базу данных (Linux)

![create_db](img/create_db.JPG)

## Инициализация проекта

```bash
mkdir pz6-db && cd pz6-db
go mod init example.com/pz6-gorm
go get gorm.io/gorm gorm.io/driver/postgres github.com/go-chi/chi/v5
```

## Создаём структуру файлов

![structure](img/structure.JPG)

### Содержимое postgres.go
![postgres.go](img/postgres.go.JPG)

### Содержимое models.go
![models.go](img/model.go.JPG)

### Содержимое main.go
![main.go](img/main.go.JPG)

### Содержимое router.go
![main.go](img/router.go.JPG)

## Содержимое handlers.go
![handlers.go](img/handlers.go(1).JPG)
![handlers.go](img/handlers.go(2).JPG)
![handlers.go](img/handlers.go(3).JPG)
![handlers.go](img/handlers.go(4).JPG)

# Запуск и проверка
![export](img/export_post.JPG)
![go.run](img/go_run.JPG)

# Проверяем
## здоровье
![health](img/health.JPG)
## создаём пользователя
![user](img/create_user.JPG)
## создаём заметку с тегами
![notes](img/create_notes.JPG)
## получаем заметку с автором и тегами
![notes](img/create_notes_1.JPG)
