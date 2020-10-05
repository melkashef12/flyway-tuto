## Postgres Docker

```
docker run --rm --name postgres-sandbox -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v $HOME/Devel/docker/volumes/postgres:/var/lib/postgresql/data postgres
```

## Flyway 

### Run migrations

```
mvn clean flyway:migrate -Dflyway.configFile=myFlywayConfig.properties
```

### Check migrations
```
mvn flyway:info -Dflyway.configFile=myFlywayConfig.properties
```
