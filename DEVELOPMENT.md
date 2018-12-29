# Laravel Classify System API

## Install Lighthouse & Graphql Playground Package

1. Install

    ```
    composer require nuwave/lighthouse mll-lab/laravel-graphql-playground
    ```

2. Publish views & configuration file

    ```
    # lighthouse
    php artisan vendor:publish --provider="Nuwave\Lighthouse\Providers\LighthouseServiceProvider"

    # playground
    php artisan vendor:publish --provider="MLL\GraphQLPlayground\GraphQLPlaygroundServiceProvider"
    ```

3. Configure database in .env

    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=classify_system
    DB_USERNAME=ravuthz
    DB_PASSWORD=123123
    ```

4. Run migration to generate tables

    ```
    php artisan migrate:fresh
    ```

5. Go to tinker can seed some faker users

    ```
    php artisan tinker

    factory('App\User', 10)->create();
    ```

6. Start laravel serve

    ```
    php artisan serve
    ```

7. Now we test GraphQL with playgroud
   http://127.0.0.1:8000/graphql-playground

    ```
    {
        user(id: 1) {
            id
            name
            email
        }
    }
    ```
