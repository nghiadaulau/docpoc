First, to run docker-compose, you need to check if the networks have been created. If not, then do:
```shell
docker network create ${NETWORK_NAME}
```
***replace your network name***

To run the services:
```shell
docker compose up -f docker-compose-db up
```


To turn off the services:
```shell
docker compose up -f docker-compose-db down
```

Note: For services that use Docker, remember to use the service name in docker-compose instead of using localhost.
Example:
People often use:
```json
localhost:3306
```
When people call from another docker, the configuration:
```json
mysql:3306
```