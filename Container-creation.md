
---

**Run a container**

A set of Docker commands that can be used to create and manage Docker containers.

How to start a new container from an image, assign it a name, map a port, map all ports, start the container in the background, assign a hostname, and add a DNS entry.

Each command is followed by an example using the "nginx" image.

Collection of commands to create and manage Docker containers for applications.

---

Start a new container from an image:

`docker run IMAGE`

`docker run nginx`

This command starts a new container based on the specified Docker image.

In this case, it starts an instance of the "nginx" image.

The Docker engine will pull the image from the Docker registry if it's not already available locally.

---

Assign it a name:

`docker run --name CONTAINER IMAGE`

`docker run --name web nginx`

By using the --name flag, this command assigns a specific name, in this case, "web," to the container being created.

Typically, Docker automatically assigns a random name to the container if it is not explicitly specified.

---

Map a port:

`docker run -p HOSTPORT:CONTAINERPORT`

`docker run -p 8080:80 nginx`

With the -p flag, this command maps the specified host port (HOSTPORT) to the corresponding container port (CONTAINERPORT).

In the given example, port 8080 of the host is mapped to port 80 of the container.

This allows access to services running inside the container through the specified port on the host machine.

---

Map all ports:

`docker run -P IMAGE`

`docker run -P nginx`

Using the -P flag, this command automatically maps all the exposed ports defined in the Docker image to ephemeral ports on the host machine.

This allows accessing the container's services through dynamically assigned ports on the host.

---

Start the container in the background:

`docker run -d IMAGE`

`docker run -d nginx`

By specifying the -d flag, this command runs the container in detached mode, meaning it runs in the background without attaching the container's terminal to the current terminal session.

This allows you to continue using the current terminal for other tasks while the container runs in the background.

---

Assign a hostname:

`docker run --hostname HOSTNAME IMAGE`

`docker run --hostname srv nginx`

This command sets the hostname of the container to the specified value.

The container can be accessed using its hostname from within the network environment.

In the example provided, the hostname "srv" is assigned to the container.

---

Add a DNS entry:

`docker run --add-host HOSTNAME:IP IMAGE`

`docker run --add-host srv:IP nginx`

The --add-host flag allows adding an entry to the container's /etc/hosts file.

It maps the specified hostname to the specified IP address.

This can be useful to define custom host-to-IP mappings within the container.

In the given example, the hostname "srv" is mapped to the IP address "IP".

---

Please make sure to replace IMAGE, HOSTPORT, CONTAINERPORT, CONTAINER, and IP with actual values as per your requirements.

---
