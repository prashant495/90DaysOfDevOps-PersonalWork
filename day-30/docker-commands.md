| Command            | Purpose                        |
| ------------------ | ------------------------------ |
| `docker --version` | Check Docker version           |
| `docker info`      | Show Docker system information |
| `docker help`      | Show Docker help               |
| `docker login`     | Login to Docker Hub            |
| `docker logout`    | Logout from Docker Hub         |

| Command                                   | Purpose                         |
| ----------------------------------------- | ------------------------------- |
| `docker images`                           | List local Docker images        |
| `docker pull nginx`                       | Download an image               |
| `docker build -t myapp:1.0 .`             | Build an image                  |
| `docker rmi nginx`                        | Remove an image                 |
| `docker image inspect nginx`              | Show detailed image information |
| `docker image history nginx`              | Show image layers               |
| `docker tag myapp:1.0 username/myapp:1.0` | Tag an image                    |
| `docker push username/myapp:1.0`          | Push image to Docker Hub        |


| Command                          | Purpose                         |
| -------------------------------- | ------------------------------- |
| `docker run nginx`               | Create and start a container    |
| `docker run -d nginx`            | Run container in background     |
| `docker run -d --name web nginx` | Run with a custom name          |
| `docker run -d -p 8080:80 nginx` | Map host port to container port |
| `docker ps`                      | List running containers         |
| `docker ps -a`                   | List all containers             |
| `docker stop web`                | Stop a container                |
| `docker start web`               | Start a stopped container       |
| `docker restart web`             | Restart a container             |
| `docker rm web`                  | Remove a container              |
| `docker kill web`                | Forcefully stop a container     |

| Command              | Purpose                                 |
| -------------------- | --------------------------------------- |
| `docker logs web`    | View container logs                     |
| `docker logs -f web` | Follow live logs                        |
| `docker inspect web` | Detailed container information          |
| `docker stats`       | Show CPU/memory usage                   |
| `docker top web`     | Show processes running inside container |
| `docker port web`    | Show port mappings                      |

# Images
docker pull nginx
docker pull ubuntu
docker pull alpine
docker images
docker image ls
docker image inspect nginx
docker rmi alpine

# Image layers
docker image history nginx
docker history nginx
docker image history --no-trunc nginx

# Container lifecycle
docker create --name my-nginx nginx
docker start my-nginx
docker pause my-nginx
docker unpause my-nginx
docker stop my-nginx
docker restart my-nginx
docker kill my-nginx
docker rm my-nginx

# Running containers
docker run -d --name web-server -p 8080:80 nginx
docker ps
docker ps -a
docker logs web-server
docker logs -f web-server
docker exec -it web-server /bin/bash
docker exec web-server ls
docker exec web-server nginx -v
docker inspect web-server
docker port web-server

# Cleanup
docker stop $(docker ps -q)
docker rm $(docker ps -aq)
docker container prune
docker image prune
docker image prune -a
docker system df
docker system df -v
