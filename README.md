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

copy files in folder specified as per -v argument when running docker container. The files are available in ```\first-spring-boot-app\db_data\ps-first-spring-boot-app\database\postgresql```. copy the above files in ```C:/volumes``` as per above command.

To populate execute following commands:

```
$ docker exec -it pg-docker psql -f create_tables.sql
$ docker exec -it pg-docker psql -f insert_data.sql
```

### in windows:

##### steps to install docker
- install Docker Desktop from hub.docker.com
- in taskbar, rightclick on docker icon and open settings.
- goto Daemon, enable exeperimental features.

NOTE: unless it is enabled, we cannot pull images form docker hub.

This should be done in Linux containers only!. swicth to Linux containers if the container is windows container.











