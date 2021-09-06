# docker-php-practice
PHPをDockerで立ち上げる

## PHPのバージョンを指定する場合
docker-compose.ymlのimageを`php:<version>-apache`に変更する
```
例) バージョン7.2を使用する場合

version: "3.9"

services:
  php:
    image: php:7.2-apache ← ここ
    ports:
      - "8000:80"
    volumes:
      - ./src:/var/www/html
```


## ローカルサーバーの起動
```
docker-compose up -d
```
```
open http://localhost:8000/
```
