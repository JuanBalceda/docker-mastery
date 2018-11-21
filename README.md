# docker-mastery
Repository for Docker Mastery course at Udemy https://www.udemy.com/docker-mastery

## Docker Containers Commands
Replace [c_name] with container name

Commands | Description
---------|------------
docker container run -d -p 3306:3306 --name [c_name] -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql | Creates a new mysql container
docker container logs [c_name] | Open logs to find random generated password
docker container run -d --name [c_name] -p 8080:80 httpd | Creates a new apache container
docker container run -d --name [c_name] -p 80:80 nginx | Creates a new nginx container
docker container top [c_name] | Shows container processes
docker container inspect [c_name] | Returns json with info about a container
docker container stats --all [c_name] | Shows container statistics
docker container inspect --format '{{.NetworkSettings.IPAddress}}' [c_name] | Select a specific node from inspect json
docker container port proxy | Shows all available ports on the container


## Docker Networks Commands
Replace [n_name] with network name

Commands | Description
---------|------------
