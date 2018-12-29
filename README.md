# Laravel Classify System API

## Setup

### Copy .env from .env.example if it doesn't exists

    ```
    cp .env.example .env
    ```

### Configure database in .env

    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=classify_system
    DB_USERNAME=ravuthz
    DB_PASSWORD=123123
    ```

### Install confiure with command line below

    ```
    composer install

    php artisan key:generate

    php artisan migrate
    ```

[DEVELOPMENT](DEVELOPMENT.md)
