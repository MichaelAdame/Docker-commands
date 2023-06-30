grouped by category:

**Docker Images**

- `docker images` - List all images on your machine
- `docker pull <image>` - Pull an image from a registry
- `docker build -t <image> .` - Build an image from a Dockerfile
- `docker tag <source_image> <target_image>` - Assign a new name to an image
- `docker rmi <image>` - Remove an image from your machine

**Docker Containers**

- `docker ps` - List all running containers
- `docker ps -a` - List all containers (running and stopped)
- `docker run -d -p <host_port>:<container_port> --name <name> <image>` - Run a container from an image in detached mode with a name and a port mapping
- `docker start <name|id>` - Start a stopped container
- `docker stop <name|id>` - Stop a running container
- `docker restart <name|id>` - Restart a container
- `docker rm <name|id>` - Remove a container from your machine
- `docker exec -it <name|id> <command>` - Execute a command inside a running container
- `docker logs <name|id>` - View the logs of a container

**Docker Volumes**

- `docker volume ls` - List all volumes on your machine
- `docker volume create <name>` - Create a volume with a name
- `docker volume inspect <name>` - View the details of a volume
- `docker volume rm <name>` - Remove a volume from your machine

**Docker Networks**

- `docker network ls` - List all networks on your machine
- `docker network create --driver <driver> <name>` - Create a network with a name and a driver
- `docker network inspect <name>` - View the details of a network
- `docker network rm <name>` - Remove a network from your machine

**Docker Compose**

- `docker-compose up` - Build and run containers defined in a docker-compose.yml file
- `docker-compose up -d` - Run containers in detached mode
- `docker-compose down` - Stop and remove containers and networks created by up
- `docker-compose ps` - List containers managed by compose
- `docker-compose logs` - View the logs of containers

