# Basic Docker Commands

#### Install Docker
`sudo yum install -y docker`
#### Start Docker
`sudo service docker start`
#### Add user to the Docker group
`sudo usermod -a -G docker "<user>"`

| Command                     | Purpose                                         | Example                                           |
| --------------------------- | ----------------------------------------------- | ------------------------------------------------- |
| `docker --version`          | Check Docker version                            | `docker --version`                                |
| `docker info`               | Display Docker system information               | `docker info`                                     |
| `docker help`               | Display Docker help                             | `docker help`                                     |
| `docker images`             | List downloaded Docker images                   | `docker images`                                   |
| `docker ps`                 | List running containers                         | `docker ps`                                       |
| `docker ps -a`              | List all containers                             | `docker ps -a`                                    |
| `docker pull`               | Download an image from Docker Hub               | `docker pull nginx`                               |
| `docker run`                | Create and start a container                    | `docker run nginx`                                |
| `docker run -d`             | Run a container in the background               | `docker run -d nginx`                             |
| `docker run -it`            | Run a container interactively                   | `docker run -it ubuntu bash`                      |
| `docker run --name`         | Create a named container                        | `docker run --name mycontainer nginx`             |
| `docker run -p`             | Map container ports to host ports               | `docker run -p 8080:80 nginx`                     |
| `docker run -v`             | Mount a volume or directory                     | `docker run -v mydata:/data nginx`                |
| `docker start`              | Start a stopped container                       | `docker start mycontainer`                        |
| `docker stop`               | Stop a running container                        | `docker stop mycontainer`                         |
| `docker restart`            | Restart a container                             | `docker restart mycontainer`                      |
| `docker pause`              | Pause a running container                       | `docker pause mycontainer`                        |
| `docker unpause`            | Resume a paused container                       | `docker unpause mycontainer`                      |
| `docker kill`               | Forcefully stop a container                     | `docker kill mycontainer`                         |
| `docker rm`                 | Remove a stopped container                      | `docker rm mycontainer`                           |
| `docker rm -f`              | Forcefully remove a container                   | `docker rm -f mycontainer`                        |
| `docker rmi`                | Remove a Docker image                           | `docker rmi nginx`                                |
| `docker exec`               | Execute a command inside a running container    | `docker exec mycontainer ls`                      |
| `docker exec -it`           | Open an interactive shell inside a container    | `docker exec -it mycontainer sh`                  |
| `docker logs`               | View container logs                             | `docker logs mycontainer`                         |
| `docker logs -f`            | Follow container logs in real time              | `docker logs -f mycontainer`                      |
| `docker inspect`            | Display detailed container information          | `docker inspect mycontainer`                      |
| `docker stats`              | Monitor container resource usage                | `docker stats`                                    |
| `docker top`                | Display running processes inside a container    | `docker top mycontainer`                          |
| `docker cp`                 | Copy files between host and container           | `docker cp file.txt mycontainer:/tmp/`            |
| `docker rename`             | Rename a container                              | `docker rename oldname newname`                   |
| `docker build`              | Build an image from a Dockerfile                | `docker build -t myapp .`                         |
| `docker tag`                | Tag a Docker image                              | `docker tag myapp myapp:v1`                       |
| `docker history`            | Display image history                           | `docker history nginx`                            |
| `docker image prune`        | Remove unused dangling images                   | `docker image prune`                              |
| `docker container prune`    | Remove stopped containers                       | `docker container prune`                          |
| `docker system prune`       | Remove unused Docker resources                  | `docker system prune`                             |
| `docker system df`          | Show Docker disk usage                          | `docker system df`                                |
| `docker volume ls`          | List Docker volumes                             | `docker volume ls`                                |
| `docker volume create`      | Create a Docker volume                          | `docker volume create myvolume`                   |
| `docker volume inspect`     | Display volume details                          | `docker volume inspect myvolume`                  |
| `docker volume rm`          | Remove a Docker volume                          | `docker volume rm myvolume`                       |
| `docker network ls`         | List Docker networks                            | `docker network ls`                               |
| `docker network create`     | Create a Docker network                         | `docker network create mynetwork`                 |
| `docker network inspect`    | Display network details                         | `docker network inspect mynetwork`                |
| `docker network connect`    | Connect a container to a network                | `docker network connect mynetwork mycontainer`    |
| `docker network disconnect` | Disconnect a container from a network           | `docker network disconnect mynetwork mycontainer` |
| `docker network rm`         | Remove a Docker network                         | `docker network rm mynetwork`                     |
| `docker compose up`         | Create and start services                       | `docker compose up`                               |
| `docker compose up -d`      | Start services in the background                | `docker compose up -d`                            |
| `docker compose down`       | Stop and remove Compose containers and networks | `docker compose down`                             |
| `docker compose ps`         | List Compose service containers                 | `docker compose ps`                               |
| `docker compose logs`       | View Compose service logs                       | `docker compose logs`                             |
| `docker compose build`      | Build Compose service images                    | `docker compose build`                            |
| `docker compose restart`    | Restart Compose services                        | `docker compose restart`                          |
| `docker login`              | Log in to a Docker registry                     | `docker login`                                    |
| `docker logout`             | Log out of a Docker registry                    | `docker logout`                                   |
| `docker push`               | Upload an image to a registry                   | `docker push username/myapp:v1`                   |
| `docker search`             | Search Docker Hub for images                    | `docker search nginx`                             |

Note: Commands such as `docker rm`, `docker rmi`, `docker system prune`, and `docker volume rm` can delete containers, images, or data. Use them carefully.

