### Стэк проекта
* nginx 1.17
* php-fpm 7.4
* postgres 12

### План разворачивания dev-окружения через docker-compose
1. В docker/config/nginx создать default.conf;
2. В корне кодовой базы выполнить команду `docker-compose up -d --build`;
3. Перейти в контейнер php `docker-compose exec php-fpm sh`;
4. Выполнить комманды:
    1. `composer install`;
    2. `php bin/console assets:install`.