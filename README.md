# Приложение для Благотворительного фонда поддержки котиков QRKot.

### Фонд собирает пожертвования на различные целевые проекты: на медицинское обслуживание нуждающихся хвостатых,
### на обустройство кошачьей колонии в подвале, на корм оставшимся без попечения кошкам — на любые цели,
### связанные с поддержкой кошачьей популяции.

# Как запустить проект

Клонировать репозиторий и перейти в него в командной строке:

git clone git@github.com:SolovyevAlexey/cat_charity_fund.git

Cоздать и активировать виртуальное окружение:

python -m venv venv
 . venv/Scripts/activate

Обновить версию pip и установить зависимости из requirements.txt:

python -m pip install --upgrade pip
pip install -r requirements.txt

# Для применения миграций введите следующие команды:

alembic revision --autogenerate -m "First migration"

alembic upgrade head

# Для запуска приложения введите комманду:

uvicorn app.main:app --reload

## Для работоспособности приложения следует указать следующие настройки env файла:

APP_TITLE

APP_DESCRIPTION

DATABASE_URL

SECRET

FIRST_SUPERUSER_EMAIL

FIRST_SUPERUSER_PASSWORD