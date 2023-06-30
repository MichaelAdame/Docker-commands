
---

**Manage containers**



A set of Docker commands that describes how to create and manage Docker containers. 

How to start a new container from an image, assign it a name, map a port, start the container in the background, assign a hostname, and add a DNS entry. 

Each command is followed by an example using the "nginx" image.



Show a list of running containers:

`docker ps`

This command lists all the running containers on your system. 

It displays information such as the container ID, image, status, and names of the running containers.

Show a list of all containers:

`docker ps -a`

By using the -a flag, this command shows a list of all containers on your system, including both running and stopped containers. 

It provides information about the container ID, image, status, and names of all containers.

Delete a container:

`docker rm CONTAINER`

`docker rm web`

This command removes a specified container. By providing the container's ID or name to the docker rm command, you can delete a container. 

In the example provided, the container named "web" is being removed.

Delete a running container:

`docker rm -f CONTAINER`

`docker rm -f web`

Using the -f flag with the docker rm command, this command forces the removal of a running container. 

It sends a termination signal to the running container and then removes it. 

Be cautious when using this flag, as data loss may occur if the container's state is not properly handled.

Delete stopped containers:

`docker container prune`

Running the docker container prune command removes all stopped containers, freeing up space. 

It is a convenient way to clean up and remove containers that are no longer needed.

Stop a running container:

`docker stop CONTAINER`

`docker stop web`

This command stops a running container. 

By providing the container's ID or name to the docker stop command, you can gracefully stop the execution of the container.

Start a stopped container:

`docker start CONTAINER`

`docker start web`

With the docker start command, you can start a previously stopped container by providing the container's ID or name. 

When you start a container, it resumes from its previous state.

Copy a file from a container to the host:

`docker cp CONTAINER:SOURCE TARGET`

`docker cp web:/index.html index.html`

By running the docker cp command, you can copy files or directories from a container to the host machine. 

In the provided example, the /index.html file from the "web" container is being copied to the current directory on the host.

Copy a file from the host to a container:

`docker cp TARGET CONTAINER:SOURCE`

`docker cp index.html web:/index.html`

This command allows you to copy files or directories from the host machine to a container. 

In the given example, the index.html file from the host is being copied to the root directory (/) of the "web" container.

Start a shell inside a running container:

`docker exec -it CONTAINER EXECUTABLE`

`docker exec -it web bash`

By using the docker exec command with the -it flags, you can start an interactive shell inside a running container. 

In the provided example, bash is the default shell being executed in the "web" container. 

This allows you to enter commands and interact with the container's environment.

Rename a container:

`docker rename OLD_NAME NEW_NAME`

`docker rename 096 web`

This command renames a container with a new name. 

By providing the current name (OLD_NAME) and the desired new name (NEW_NAME) to the docker rename command, you can change the name of a container. 

In the example provided, the container with the ID "096" is being renamed to "web".

Create an image out of a container:

`docker commit CONTAINER`

`docker commit web`

Running the docker commit command, you can create a new image out of a container's current state. 

This allows you to capture changes made within a container and create a reusable image. In the given example, an image is being created from the "web" container.

Please note that the commands above assume you have Docker installed and properly configured.

---