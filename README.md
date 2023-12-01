# Laravel with Docker

![DockerVersion Support](https://img.shields.io/badge/docker-23%2B-brightgreen.svg?style=flat-square) ![Composer Version Support](https://img.shields.io/badge/docker%20compose-2.17%2B-brightgreen.svg?style=flat-square)

Files for quick Laravel configuration with  Docker Compose, customizable for different version levels

-----

### Instalation

1. Clone this repository
```sh
git clone https://github.com/willavelar/laravel-with-docker.git
```

2. Clone the Laravel repository
```sh
git clone https://github.com/laravel/laravel.git app-laravel
```

3. Copy the files from this project to laravel
```sh
cp -rf laravel-with-docker/* app-laravel/
```
```sh
cd app-laravel/
```

4. Create the .env file
```sh
cp .env.example .env
```


5. Add the following lines at the end of .gitignore

```dosgitignore
/.docker
```

6. Create .env file in laravel project
```sh
cp .env.example .env
```

7. Update the .env file environment variables
```dosini
APP_NAME="Webapp name"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```

8. Upload project containers
```sh
docker-compose up -d
```


9. Access the container
```sh
docker-compose exec app bash
```


10. Install project dependencies
```sh
composer install
```


11. Generate the Laravel project key
```sh
php artisan key:generate
```


Acessar o projeto
[http://localhost:8989](http://localhost:8989)
