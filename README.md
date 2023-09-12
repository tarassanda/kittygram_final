## Описание проекта:

Проект kittygram- это сервис для просмотра изображений и достижений различных котиков. С помощью kittygram можно запрашивать данные о котиках, их год рождения, цвет, достижения и само фото питомца. kittygram - это учебный проект курса "backend-python" от Яндекс-Практикума.


### Как запустить проект:

1.  Клонировать репозиторий и перейти в него в командной строке:
    
    -   git clone git@github.com:tarassanda/kittygram_final.git
    -   cd kittygram_final
2.  Cоздать и активировать виртуальное окружение:
    
    -   python3 -m venv venv
    -   source venv/bin/activate

для windows систем: - python -m venv venv - source/Scripts/activate

3.  Обновить pip:
    -   python3 -m pip install --upgrade pip

для windows систем: - python -m pip install --upgrade pip

4.  Установить docker в вашу операционную систему.

5.  Из папки cоздать образы и запустить сеть контейнеров:
    -   docker compose build
    -   docker compose up

6.  выполнить сборку статики и миграций:
    -   docker compose exec backend python manage.py collectstatic
    -   docker compose exec backend cp -r /app/collected_static/. /backend_static/static/ 
    -   docker exec taski_backend_container python manage.py migrate


### Основные доступные эндпоинты:

1.  https://taras-kittygram.sytes.net :
    -   Главная страница проекта 
2.  https://taras-kittygram.sytes.net/signin :
    -   Регистрация и вход

3.  https://taras-kittygram.sytes.net/cats/(some_id) :
    -   Информация о котике

4.  https://taras-kittygram.sytes.net/admin/ :
    -   Страница администрирования проекта

5.  https://taras-kittygram.sytes.net/api/ :
    -   Информация об api

