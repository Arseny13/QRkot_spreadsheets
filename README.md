# отчёт в Google Sheets для QRKot

<h4>Автор:</h4>

**Изимов Арсений**  - студент Яндекс.Практикума Когорта 16+
https://github.com/Arseny13



<h2>Задание</h2>
Продолжение проекта https://github.com/Arseny13/cat_charity_fund

Добавьте в приложение QRKot возможность формирования отчёта в гугл-таблице. В таблице должны быть закрытые проекты, отсортированные по скорости сбора средств — от тех, что закрылись быстрее всего, до тех, что долго собирали нужную сумму.


<h2>Как использовать</h2>

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Arseny13/QRkot_spreadsheets.git
cd QRkot_spreadsheets
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
python -m pip install --upgrade pip
pip install -r requirements.txt
```
Заполнить файл .env по аналогу .env.example

Установить alembic и выполнить миграции

```
alembic init --template async alembic 
alembic revision --autogenerate -m "Add table reservation"
alembic upgrade head
```

Запустить приложение 

```
uvicorn app.main:app --reload
```

<h2>Используемые технологии</h2>

- Python 3.9
- FastAPI v.0.78.0
- SQLite
- SQLAlchemy
- Alembic
- Google API