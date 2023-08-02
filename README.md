# Picus

Picus - социальная сеть, гибрид Instagram и бывшего Twitter, создана на базе фреймворка [Django](https://www.djangoproject.com/).

## Оглавление
- [Введение](#Введение)
- [Особенности](#Особенности)
- [Установка](#installation)
- [Использование](#Использование)

## Введение
Picus - веб-приложение, социальная сеть, позволяющая пользователям регистрировать аккаунты, размещать посты, включающие текст и графические изображения, подписываться на других пользователей, таким образом формируя собственную ленту, а также ставить лайки постам и оставлять комментарии под ними.

## Особенности
Реализованные функции:
- Аутентификация пользователей и управление профилями, личный аккаунт пользователя;
- Размещение постов, содержащих текст и/или графические изображения;
- Лайки под постами;
- Подписка на других пользователей с возможностью видеть их размещенные посты;
- Лента, состоящая из постов пользователей, на которых осуществлена подписка.

## Установка
Для локального запуска Picus необходимы:
- Python 3.x
- менеджер пакетов pip

Для установки Picus выполните следующие шаги:

1. Клонируйте репозиторий:
```
git clone https://github.com/konevyar/picus.git
```

2. Перейдите в каталог проекта:
```
cd picus
```

3. Создайте виртуальную среду:
```
python -m venv .venv
```

4. Активируйте виртуальную среду:
```
source .venv/bin/activate
```

5. Установите необходимые зависимости:
```
pip install -r requirements.txt
```

6. Сгенерируйте секретный ключ Django:
```
python -c 'from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())'
```

7. Создайте в корневой директории проекта файл .env со следующим содержимым:
```
SECRET_KEY=вставьте ваш секретный ключ
DEBUG=True
```

8. Настройте базу данных:
```
python manage.py makemigrations
```

```
python manage.py migrate
```
   
9. Запустите сервер разработки:
```
python manage.py runserver
```

10. Получите доступ к Picus в веб-браузере по адресу `http://localhost:8000`.

## Использование
После доступа к Picus перед вами откроется с предложением войти в аккаунт или создать его. После логина или создания аккаунта вы попадете в личный аккаунт пользователя.

Зарегистрированные пользователи могут создавать посты, подписываться на других пользователей и отписываться от них, ставить лайки.