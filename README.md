# ***Docker for Laravel***

Inspired by :

* <https://github.com/aschmelyun/docker-compose-laravel>
* <https://github.com/jguyomard/docker-laravel>

## Usage

Install [docker](https://docs.docker.com/engine/installation/) and [docker-compose](https://docs.docker.com/compose/install/) ;

1. Copy `docker-compose.yml` file to your project root path, and edit it according to your needs ;
2. From your project directory, start up your application by running:

```
docker-compose up --build 
```

4. If you want, you can run composer or artisan through docker. For instance:

```
docker-compose exec php composer install
docker-compose exec php php artisan migrate
docker-compose exec php $yourCommandHere
```

5.  In Addition, you can work inside the container:

```
docker-compose exec php ash
```

## Docker Images

These docker images are configured in `docker-compose.yml` file. You can comment or uncomment some services according to your project.

* `gbelot2003/docker-laravel*php*1:latest (this docker image extends `php:7.4-fpm-alpine` to add some PHP extensions)`;
* `gbelot2003/docker-laravel*site*1:latest (this docker image extends `nginx:latest` to add Laravel vhost)`;
* `mysql:5.7.29`;
* `postgres:9.6-alpine` ;
* `redis:latest` ;
* `Node:13.7`;

## Contributing

Contributions are welcome! Leave an issue on Github, or create a Pull Request.

## Licence

This work is under [MIT](https://github.com/jguyomard/docker-laravel/blob/master/LICENCE) licence.
