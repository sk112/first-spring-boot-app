# first-spring-boot-app

## SOP

### in linux:

create postgres docker container.

#### steps

```
$ docker pull postgres:latest

$docker run --rm --name pg-docker -d -p 5432:5432 -v C:/volumes:/var/lib/postgres/data -e POSTGRES_PASWORD=docker postgres

```

above commands will run postgres docker container.

To access docker container
```
$ docker exec -it pg-docker bin/bash
```

To populate data in postgres DB:

copy files in folder specified as per -v argument whwn running docker container. The files are available in /first-spring-app/



