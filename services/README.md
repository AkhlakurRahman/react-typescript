# React Typescript demo project

## Getting db setup

You will need Docker in order to install a containerized MySQL dev environment. After getting Docker run the following command from anywhere.

```sh
docker run \
  -p 0.0.0.0:7999:3306 \
  --name rtd-db \
  -e MYSQL_ROOT_PASSWORD=password \
  -e MYSQL_USER=rtd-dev \
  -e MYSQL_PASSWORD=password \
  -e MYSQL_DATABASE=rtd \
  -d mysql:5.7.20
```

This will create a Docker instance called `rtd-db`, running MySQL v5.7.20, with root password `password`. It also creates a database called `rtd` creates a user called `rtd-dev` with a password `password`, and assigns that user with full permissions onto `rtd` database.
