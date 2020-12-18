# **docker-template** 

<br>

## **About**
You can create lemp environment on your docker-container.

## **Inside Package**
 * web nginx:latest
 * app php:7.3-fpm
 * db  mysql:5.7
 * phpmyadmin (Option1)
 * node node:lts (Option2)

## **How to use**

1. clone the repository & run docker-compose up

```
git clone https://github.com/siwai0208/docker-template-laravel
docker-compose up
```

2. confirm container status by docker-ompose ps
```
docker-compose ps
Name                        Command               State                 Ports              
----------------------------------------------------------------------------------------------------
docker-template_app_1     docker-php-entrypoint php-fpm    Up      9000/tcp                         
docker-template_mysql_1   docker-entrypoint.sh mysqld      Up      0.0.0.0:3306->3306/tcp, 33060/tcp
docker-template_web_1     /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8000->80/tcp    
```

### **Option1: use phpmyadmin**:
 
 1. uncomment "phpmyadmin" section (line 37-49) in docker-compose.yml file
 2. restart docker-compose
 3. you can access phpmyadmin via your-host-ipaddres:8080

### **Option2: use npm for scss->css compile**

 1. uncomment "node" section (line 52-56) in docker-compose.yml file
 2. restart docker-compose
 3. docker-compose run node npm install
 4. docker-compose run node npm run dev

## **RUN Laravel Application**

 - [Laravel8を用いたECサンプルアプリ](https://github.com/siwai0208/food-app)