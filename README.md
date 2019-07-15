# docker-mastery
Repository for Docker Mastery course at Udemy https://www.udemy.com/docker-mastery

## Docker Containers Commands
Replace [c_name] with container name

Commands | Description
---------|------------
docker container run -d -p 3306:3306 --name [c_name] -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql | Creates a new mysql container
docker container start [c_name] | Starts an existing container
docker container stop [c_name] | Stops a running container
docker container logs [c_name] | Open logs to find random generated password
docker container run -d --name [c_name] -p 8080:80 httpd | Creates a new apache container
docker container run -d --name [c_name] -p 80:80 nginx | Creates a new nginx container
docker container top [c_name] | Shows container processes
docker container inspect [c_name] | Returns json with info about a container
docker container stats --all [c_name] | Shows container statistics
docker container inspect --format '{{.NetworkSettings.IPAddress}}' [c_name] | Select a specific node from inspect json
docker container port [c_name] | Shows all available ports on the container
docker container run -d --name [c_name] --network [n_name] nginx:alpine | Creates a container specifying network by DNS
docker exec -it [c_name] bash | Execute a task in a running containers
docker container run --rm -it centos:7 bash | Creates a new container that will be deleted once is stopped

## Docker Image Commands
Replace [i_name] with image name or sha

Commands | Description
---------|------------
docker image history [i_name] | Show the history of an image
docker image inspect [i_name] | Display detailed information on one or more images
docker image tag s_image[:tag] t_image[:tag] | Create a tag t_image that refers to s_image
docker image push [i_name] | Push an image or a repository to a registry
docker image build -t customnginx . | Build an image from a Dockerfile

## Docker Networks Commands
Replace [n_name] with network name

Commands | Description
---------|------------
docker network ls | Lists all the networks
docker network inspect [n_name] | Shows info about a network in json format
dokcer network create [n_name] | Creates a new network
docker network connect [n_name] [c_name] | Adds a new network interface to the container 
docker network disconnect [n_name] [c_name] | Removes a network interface from the container
docker exec -it [c_name] ping [c2_name] | Tests connection between containers


## Docker Security Commands

Commands | Description
---------|------------
docker login | Log in to a Docker registry

## Notes
* latest tag not always means latest, it's the default tag.
* Showing user info:
```bash
 cat .docker/config.json
 ```