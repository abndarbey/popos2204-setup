# Useful docker commands for postgres

### Create DB container
```bash
docker run -d -p 5432:5432 --name postgres -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret postgres:14.2-alpine
```

### Create DB
```bash
docker exec -it postgres createdb --username=root --owner=root <dbname>
```

### Drop DB
```bash
docker exec -it postgres dropdb --username=root <dbname>
```

### Open DB shell
```bash
docker exec -it postgres psql -U root -d <dbname>
```

### Open remote DB shell
```bash
docker exec -it postgres psql -U root -h <dbhost> <dbname>
```

### Take pg_dump for remote db
This will save the file inside docker container
```bash
docker exec -it postgres pg_dump -h <dbhost> -U root -f <filename> <dbname>
```

### Copy file from docker container to local machine
```bash
sudo docker cp <containerID>:/<path>/<filename> ~/<path>/<filename>
```