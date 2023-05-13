# Docker Cheat Sheet

## Container Management Commands

| Snippet Command | Description |
| --- | --- |
| `docker run` | to start a new Docker container |
| `docker start` | Start a stopped container |
| `docker stop` | Stop a running container |
| `docker restart` | Restart a running container |
| `docker rm` | Remove a stopped container |
| `docker ps` | List running containers |
| `docker exec` | Execute a command inside a running container |
| `docker logs` | Display the logs of a container |
| `docker stats` | Display real-time container resource usage |

## Usefull Commands

| Snippet Command | Description |
| --- | --- |
| `docker logs name/id of a container` | Give some Information about the container |
| `docker run -d -p6000:6379 --name redis-older` |container should run in detached mode, meaning it runs in the background and returns control to the terminal.-p 6000:6379 maps the host machine's port 6000 to the container's port 6379. This allows the host machine to access the Redis service running inside the container via port 6000.`--name redis-older` gives the container a name of "redis-older", which can be used to reference the container in other Docker commands and scripts. |
| `docker exec -it containerID /bin/bash` | docker exec command to start an interactive terminal session ("-it") inside a running Docker container.`/bin/bash` is the command to execute inside the container, in this case starting a Bash shell.Overall, this command is useful for debugging or administering a running Docker container, allowing the user to execute commands and interact with the container's environment without having to start a new container instance. NB. the container should be running in the background to use this command.  |
| `ls` | Assuming the above command is successful, make sure you are on the container's root mode eg. `root@edc4c8d4704e:/data# ls`, `cd  /`, then ls => `bin  boot  data  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var` We are now in Vertual file system of the container, Lets check =>`env`, Finally `exit`|
| `docker tag` | Tag an image |
| `docker rmi` | Remove an image |


## Image Management Commands

| Snippet Command | Description |
| --- | --- |
| `docker images` | List all images |
| `docker pull` | Download an image from a registry |
| `docker push` | Push an image to a registry |
| `docker build` | Build a Docker image from a Dockerfile |
| `docker tag` | Tag an image |
| `docker rmi` | Remove an image |


## Network Management Commands

| Snippet Command | Description |
| --- | --- |
| `docker network` | Manage Docker networks |
| `docker network create` | Create a Docker network |
| `docker network connect` | Connect a container to a Docker network |
| `docker network inspect` | Display detailed information about a Docker network |
## Volume Management Commands

| Snippet Command | Description |
| --- | --- |
| `docker volume` | Manage Docker volumes |
| `docker volume create` | Create a Docker volume |
| `docker volume ls` | List all volumes |
| `docker volume inspect` | Display detailed information about a Docker volume |

## Compose Commands

| Snippet Command | Description |
| --- | --- |
| `docker-compose` | Manage multi-container Docker applications |
| `docker-compose up` | Start Docker containers defined in a Docker Compose file |
| `docker-compose down` | Stop and remove Docker containers defined in a Docker Compose file |
| `docker-compose logs` | Display logs from Docker containers defined in a Docker Compose file |

