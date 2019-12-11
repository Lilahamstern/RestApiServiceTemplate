#Template rest api service written in go.

#WIP

Setup user and database for service

```sh
$ docker ps

$ docker exec -it container-id ./cockroach sql --insecure

$ CREATE DATABASE project;

$ CREATE USER project_admin WITH PASSWORD 'supersecret';

$ GRANT ALL ON DATABASE project TO project_admin;
```

Modify config.json so it fits your information

```json
{
  "service": {
    "release": false,
    "clean": true,
    "name": "Template",
    "version": "0.0.1",
    "port": "5050",
    "description": "A template service"
  },
  "database": {
    "port": "26257",
    "host": "database",
    "user": "project_admin",
    "password": "supersecret",
    "name": "project"
  }
}
```
