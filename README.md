![Deploy badge] (https://github.com/NikoKozeeev/kittygram_final/actions/workflows/main.yml/badge.svg)
# Проект Kittygram - Яндекс.Практикум
Социальная сеть для котоманов

## Ссылка на проект - Kittygram(https://infrasprintovna.sytes.net/)
## Ссылка Репозиторий - NikoKozeev(https://github.com/NikoKozeev/kittygram_final)

### Особенности
Создание аккаунта
Загрузка собственных котиков на платформу с изображениями
Просмотр чужих котиков

### Локальное развертывание
Чтобы развернуть приложение Kittygram локально, следуйте этим шагам:

1. Клонируйте репозиторий на вашем локальном компьютере:

   ```bash
   git clone git@github.com:NikoKozeev/kittygram_final.git
   cd kittygram
   py manage.py migrate
   python manage.py runserver

2. Установите зависимости для бэкенда и запустите сервер разработки:
   ```bash
   cd ../frontend
   npm install
   npm start
Откройте веб-браузер и перейдите по адресу http://127.0.0.1, чтобы взаимодействовать с локальной версией Kittygram.

### Удаленное развертывание
1. Подключитесь по SSH к удаленному серверу и перейдите в директорию проекта.
2. Чтобы развернуть Kittygram на удаленном сервере, выполните следующие шаги:
   Подготовьте окружение на удаленном сервере с необходимым программным обеспечением (Docker, Docker Compose и т.д.).
3. Выполните команду fork, на своём аккаунте github из этого репозитория 
## Ссылка Репозиторий - NikoKozeev(https://github.com/NikoKozeev/kittygram_final)
4. Клонируйте репозиторий на удаленном сервере:
   ```bash
   git clone https://github.com/ваше-имя/kittygram_final.git
   cd kittygram_final
5. Выполните скачивание и развертывание продакшн версии:
```bash
   docker-compose -f docker-compose.production.yml pull
   docker-compose -f docker-compose.production.yml up -d
```
установка миграций и сбор статики произойдет в автоматическом режиме.
6. Для успешного развертывания проекта необходимо в главной директории создать файл .env, где будут указаны следуюшие параметры:
- POSTGRES_DB
- POSTGRES_USER
- POSTGRES_PASSWORD
- DB_NAME
- DB_HOST
- DB_PORT
- DEBUG
- SECRET_KEY
- ALLOWED_HOSTS

7. Для создания пользователя с правами администратора необходимо в терминале выполнить команду:
```bash
   cd backend
   py manage.py createsuperuser
```
Или выполните команду:
   ```bash
git push
```

### Автор
Проект Kittygram был создан NikoKozeev(https://github.com/NikoKozeev/kittygram_final) Николай Козеев

### Используемые технологии
Проект использует ряд технологий, включая, но не ограничиваясь:
Python, Django, PostgreSQL, Django Rest Framework, Djoser
