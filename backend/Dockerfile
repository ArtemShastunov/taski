FROM python:3.12

WORKDIR /app

# Системные зависимости — до копирования кода
RUN pip install gunicorn==25.3.0

COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

COPY . .

# Запуск через Gunicorn
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]