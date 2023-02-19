# api_final_yatube

### Описание:

Финальная часть учебного проекта социальной сети, в которой есть возможность публиковать записи, комментировать их и подписываться/отписываться от авторов.

### Технологии:

Python 3.7, Django 2.2, DRF, JWT

### Как запустить проект:

Клонируй репозиторий и перейди в него в командной строке:

```git clone https://github.com/zamir041/api_final_yatube```

``` cd api_final_yatube```

Cоздай и активируй виртуальное окружение:

```python -m venv venv```

* Если у тебя Linux/macOS

    ```source venv/bin/activate```

* Если у тебя windows

    ```source env/scripts/activate```

```python -m pip install --upgrade pip```

Установи зависимости из файла requirements.txt:

```pip install -r requirements.txt```

Выполни миграции:

```python manage.py migrate```

Запусти проект:

```python manage.py runserver```

Создаем суперпользователя:

```python manage.py createsuperuser```

### Примеры запросов

```
GET  http://127.0.0.1:8000/api/v1/posts/
```
Результат:
```json
[
    {
        "id": 1,
        "author": "newbor",
        "text": "Hey",
        "pub_date": "2022-08-08T18:41:19.125087Z",
        "image": null,
        "group": null
    },
    {
        "id": 2,
        "author": "newbor",
        "text": "Тестовый пост",
        "pub_date": "2022-08-09T13:23:43.516385Z",
        "image": null,
        "group": null
    }
]
```
```
POST  http://127.0.0.1:8000/api/v1/follow/
```
Данные запроса: 
```json
{
  "following": "leo"
}
```
Результат: 
```json
{
    "id": 1,
    "following": "leo",
    "user": "newbor"
}
```

По адресу `http://127.0.0.1:8000/redoc/` будет доступна документация для API **Yatube**
____
## Авторы

- Команда Яндекс.Практикума
- Мустафаев Замир