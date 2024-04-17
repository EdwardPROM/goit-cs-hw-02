#Використання базового образу
FROM python:3.10-slim

ENV APP_DIR /application

#Завдання робочої директорії в контейнер
WORKDIR $APP_DIR

#Копіювання файлів з робочої директорії в контейнер і встановлення залежностей
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

#Копіювання всіх файлів з робочої директорії в контейнер
COPY . .

#Запуск сервера
EXPOSE 8000

CMD [ "python","main.py" ]