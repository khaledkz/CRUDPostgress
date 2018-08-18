# CRUDPostgress

 

## docker:

we can use docker to manage the server it can help for developers and sysadmins to build, ship, and run distributed applications,

1-create 

```
docker-compose.yml
```
it contain 

,,,
version: '3.1'
services:
  db:
    image: postgres
    ports:
        - "5432:5432"
    environment:
        POSTGRES_USER: cyf
        POSTGRES_PASSWORD: password
        POSTGRES_DB: legodi
    restart: always
,,,
