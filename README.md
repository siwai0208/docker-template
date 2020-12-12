# docker-template-laravel

<br>

## About ##

<br>

You can create plane laravel8 environment on your docker-container.

<br>

## Inside Package ##

<br>

 * web nginx:latest
 * app php:7.3-fpm
 * db  mysql:5.7
 * phpmyadmin (Option1)
 * node node:lts (Option2)

<br>

## How to use ##

<br>

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
 7. you can access laravel8-home via your-host-ipaddres:8000

<br>

 ### Option1: use phpmyadmin ###
 
<br>

 1. uncomment "phpmyadmin" section (line 37-49) in docker-compose.yml file
 2. restart docker-compose
 3. you can access phpmyadmin via your-host-ipaddres:8080

<br>

 ### Option2: use npm for scss->css compile ###

<br>

 1. uncomment "node" section (line 52-56) in docker-compose.yml file
 2. restart docker-compose
 3. docker-compose run node npm install
 4. docker-compose run node npm run dev

<br>
