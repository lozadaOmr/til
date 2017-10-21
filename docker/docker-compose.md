# Docker Compose

## Redis

Connection should be `redis:6379`. For some reason I was baffled when trying it as
localhost:6379 -- even tried exposing port 6379 to check if Redis container is working

docker-compose.yml
```
services:
  redis
    image: redis

  app
    envinronment
      ...
      REDIS_HOST: redis
      REDIS_PORT: 6379
  
```
