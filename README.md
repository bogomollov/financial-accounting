# Установка

Запуск Docker Compose
```sh
./vendor/bin/sail up
```

Вход в контейнер Laravel
```sh
docker exec -it laravel-financial bash
```

Установка зависимостей NPM и Composer 
```sh
npm i
composer i
```

Запуск миграцию таблиц БД
```sh
php artisan migrate
```

Запуск Vite
```sh
npm run dev
```

Открытие сайта происходит через APP_URL, указанная в .env
