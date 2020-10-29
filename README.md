# laravel-docker-template

sudo docker-compose up

docker-compose exec app composer create-project --prefer-dist "laravel/laravel=6.*"

docker-compose exec app bash

cd laravel

vim .env
 DB_HOST=mysql
 DB_DATABASE=
 DB_USERNAME=
 DB_PASSWORD=
 
php artisan migrate

docker-compose run node npm install

docker-compose run node npm run dev
