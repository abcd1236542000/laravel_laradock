# Laradock
## 初始
### 複製laradock .env
```
cp -p ./laradock/.env.example ./laradock/.env

```
## 切換 PHP 版本
### 路徑 ./laradock/.env 
```
8.0 - 7.4 - 7.3 - 7.2 - 7.1 - 7.0 - 5.6
PHP_VERSION=7.3
```
## 定義container名稱
### 路徑 ./laradock/.env 
```
COMPOSE_PROJECT_NAME=laradock
```

---

## 安裝

### 安裝+開啟
```
docker-compose --env-file=laradock/.env up -d nginx mysql phpmyadmin redis
```
### 開啟
```
docker-compose --env-file=laradock/.env start nginx mysql phpmyadmin redis
```
### 關閉
```
docker-compose --env-file=laradock/.env stop
```

### 卸載+關閉
```
docker-compose --env-file=laradock/.env down -v --rmi all
```
---


# Laravel
## 初始

### 連入container
```
docker-compose --env-file=laradock/.env exec workspace bash
cd /var/www
```
### 複製 .env
```
cp -p .env.example .env

```
---

## 安裝
### 安裝套件
```
composer install
```
### generate key
```
php artisan key:generate
```
---
## 開始
```
http://localhost
```

