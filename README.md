We are currently on the "Main Branch"

## Provide a command that will create a docker network.

```
docker network create EH-network
```

## Provide a command that will run a mysql:latest docker image with the name of db with a root password=my-secret-password.

```
docker run --name db -e MYSQL_ROOT_PASSWORD=my-secret-password -d mysql:latest
```

## Provide a command that will run the docker image:
#### phpmyadmin/phpmyadmin on the network previously created mapping a port of your choice to port 80 of the container

```
docker run --name my-phpmyadmin -d --network EH-network -p 8080:80 phpmyadmin/phpmyadmin
```