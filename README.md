# docker-template-laravel

## About ##
You can create plane laravel-8 site on your docker-container.

## Inside Package ##
 * WEB nginx:latest
 * APP php:7.3-fpm
 * DB  mysql:5.7
 * phpmyadmin (Option1)
 * NODE node:lts (Option2)

## How to use ##
 1. clone the repository
 2. docker-compose up
 3. docker-compose exec app composer create-project --prefer-dist laravel/laravel
 4. docker-compose exec app bash
 5. cd laravel and revice .env file
    DB_HOST=mysql
    DB_DATABASE=laravel
    DB_USERNAME=root
    DB_PASSWORD=password
 6. php artisan migrate

 ### Option1: use phpmyadmin ###
 1. delete the commentout(#) phpmyadmin section on your docker-compose.yml
 2. docker-compose run node npm run dev
 3. docker-compose run node npm install

 ### Option2: use npm for ###
 1. delete comment out 
 2. docker-compose run node npm install
 3. docker-compose run node npm run dev
