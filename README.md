# Laradock
## 初始
### 複製laradock .env
```
cp -p ./laradock/.env.example ./laradock/.env

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
