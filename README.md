# QRkot_spreadseets

О проекте
```
Проект QRKot предназначен для сбора пожертвований
для благотворительного фонла на помощь котикам. Также
предусмотрена возможность сформировать отчёт по закрытым
проектам.
API и краткая докуентация для возможности интеграции с другими приложениями
доступны по адресу: http://127.0.0.1:8000/docs
```


**Как развернуть**

Клонировать репозиторий и перейти в него в командной строке:

```
git clone 
```

```
cd cat_charity_fund
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

* Если у вас Linux/macOS

    ```
    source venv/bin/activate
    ```

* Если у вас windows

    ```
    source venv/scripts/activate
    ```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Применить миграции:

```
alembic upgrade head
```

Запустить проект на локальном сервере:

```
uvicorn app.main:app --reload
```

Сформировать отчёт по закрытым проектам:

```
POST: http://127.0.0.1:8000/google/
```


Использованные технологии:
* Фреймворк [FastApi](https://fastapi.tiangolo.com/)
* Библиотека для работы с базой данных [SqlAlchemy](https://www.sqlalchemy.org/)
* Библиотека для работы с миграциями [Alembic](https://alembic.sqlalchemy.org/en/latest/)
* ASGI web server [Uvicorn](https://www.uvicorn.org/)
* Библиотека [Aiogoogle](https://pypi.org/project/aiogoogle/)

Переменные окружения можно взять из файла .env.example

**Автор:** [Алексей Данилов](https://github.com/AlexeyDanilov/)

Проект доступен [по ссылке](https://github.com/AlexeyDanilov/cat_charity_fund)
