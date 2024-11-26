## Модель БД

Модель базы данных сделана на основе варианта из курса "Фронтэнд-разработка" - фитнесс зал.  
![](src/img.png)

## Сущности

Главная сущность, вокруг которой работаеть весь сайт, - пользователь. Все остальные, так или иначе, с ним связаны.

## API Endpoints
### Authentication Endpoints (Djoser)
- POST /auth/token/login/ - Получить токен
![](src/token.jpg)
- POST /auth/users/ - Зарегистрировать пользователя
![](src/auth.jpeg)
- POST /auth/token/logout/ - Выйти (удалить токен)  


### Account
- GET /account/ - Информация о пользователе
![](src/account-info.jpg)
- GET /account/workots - Список тренировок, которые завершил пользователь


# Workouts
- GET /workouts/ - Список всех тренировок
    Доп. параметры:
    - trainer_id: фильтрация по тренеру
    - type: фильтрация по типу тренировки
- GET /workouts/id/ - Подробности по отдельной тренировке
![](src/workout_info.jpg)
- POST /workouts/create/ - Создание тренировки
![](src/workout-create.jpg)


### User Workout Tracking
- POST /workouts/workout_id/start/ - Логгирование начала тренировки
![](src/workout_start.jpg)
- POST /workouts/workout_id/complete/ - Логгирование окончания тренировки
![](src/workout_complete.jpg)


### Blogs
- GET /blogs/ - Все посты в блоге
    Доп. параметры:
    - category: фильтрация по категории
    - author_id: фильтрация по автору
![](src/blog-list.jpg)
- GET /blogs/id/ - Подробности по отдельному посту
![](src/blog-info.jpg)
- POST /blogs/create/ - Создать новый пост
![](src/blog-create.jpg)
- PUT /blogs/<id>/manage/ - Обновить пост (только автор)
- DELETE /blogs/<id>/manage/ - Удалить пост (только автор)


### Trainers
- GET /trainers/ - Список всех тренеров
- GET /trainers/id/ - Подробности по отдельному тренеру
![](src/trainer-info.jpg)
- POST /trainers/create/ - Создать профиль тренера
