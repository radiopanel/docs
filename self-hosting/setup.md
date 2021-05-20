# Setup

{% hint style="danger" %}
This is an alpha version and should not be used in production
{% endhint %}

### Setup your docker-compose

Create a file called `docker-compose.yml` in an empty folder with the following content

```yaml
version: "2.4"
services:
    api:
        image: radiopanel/radiopanel-api:0.0.1-alpha.1
        container_name: radiopanel-api
        volumes:
            - ./uploads:/home/node/uploads:delegated
        env_file:
            - .env
        depends_on:
            database:
                condition: service_healthy

    app:
        image: radiopanel/radiopanel-app:0.0.1-alpha.1
        container_name: radiopanel-app
        ports:
            - 3000:80
        env_file:
            - .env
        depends_on:
            - api

    database:
        image: postgres:12.3-alpine
        container_name: radiopanel-postgres
        environment:
            POSTGRES_DB: radiopanel
            POSTGRES_USER: localuser
            POSTGRES_PASSWORD: CHANGE_ME
            PGDATA: /data/db
        ports:
            - 5432:5432
        volumes:
            - ./data:/data/db
        healthcheck:
            test: ["CMD-SHELL", "pg_isready -U localuser -d radiopanel"]
            interval: 10s
            timeout: 5s
            retries: 5

    redis:
        image: redis:6.0.6-alpine
        container_name: redis
        ports:
            - 6379:6379
        command: ["redis-server", "--appendonly", "yes"]
        volumes:
            - redis-data:/data

volumes:
    redis-data:
```

### Create a env file

In the same folder create a `.env` file with the following content and change the needed variables:

```yaml
PORT=80
NODE_ENV=production

FRONTEND_BASEURL=http://localhost:3501
UPSTREAM=api

TYPEORM_CONNECTION=postgres
TYPEORM_HOST=database
TYPEORM_PORT=5432
TYPEORM_USERNAME=localuser
TYPEORM_PASSWORD=CHANGE_ME
TYPEORM_DATABASE=radiopanel
TYPEORM_LOGGING=false
TYPEORM_LOGGER=advanced-console
TYPEORM_SSL=false

MAIL_HOST=CHANGE_ME
MAIL_PORT=CHANGE_ME
MAIL_SECURE=CHANGE_ME
MAIL_USER=CHANGE_ME
MAIL_PASSWORD=CHANGE_ME

JWT_PRIVATE=CHANGE_ME

REDIS_HOST=redis
REDIS_PORT=6379
```

### Start radiopanel

Now use the command `docker-compose up` and visit http://localhost:3000 to continue installation

