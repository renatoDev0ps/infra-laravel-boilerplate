## How to run this services

### 1 . Modify .env with your configurations, set database name, your credencials for database.
### 2 . Run this command to up the services
```
$ docker-compose up -d --build
```
### 3 . Check if services are running with this command
```
$ docker ps -a
```
### 4 . Into the container laravel, run this command to access
```
$ docker exec -it laravel bash
```
### 5 . Now, install laravel latest go to the laravel blog in https://laravel.com/docs/7.x/installation
```
$ composer create-project --prefer-dist laravel/laravel blog
```
### 6 . Go into blog folder and change all archives to workdir in /var/www
```
$ mv * .* ../
```
### 7 . Now exit and delete blog folder
```
$ cd ../ && rm -rf blog
```
### 8 . Edit database.php and set database's configs in this path: 
```
$ vim config/database.php
```
### 9 . Now Connect laravel to postgresql database
```
$ php artisan migrate
```
