
## Warm up  
#### This simple exercise is intended to warm you up or help you understand the basics of Docker.
<details>
<summary><b>How do you inspect a Docker image?<b></summary>
```bash
$ docker inspect <image_name>

```
</details>

- How do you mount a volume in a Docker container?

```bash
$ docker run -v <host_path>:<container_path> <image_name>

```
- How do you execute a command in a running Docker container?

```bash
$ docker exec <container_name> <command>

```
- How do you copy files from a Docker container to the host system?

```bash
$ docker cp <container_name>:<container_path> <host_path>

```
- How do you connect a Docker container to a Docker network?

```bash
$ docker run --network <network_name> <image_name>


```
- How do you inspect a Docker network?

```bash
$ docker network inspect <network_name>

```
- How do you remove a Docker network?

```bash
$ docker network rm <network_name>

```
- How do you restart a stopped Docker container?

```bash
$ docker restart <container_name>

```
- List all images on your local machine
```bash
$ docker image ls

```
- Pull the latest version of the nginx image from the Docker Hub registry

```bash
$ docker pull nginx:latest

```
- Launch a new container from the nginx image, mapping port 80 in the container to port 8080 on the host
```bash
$ docker run --name mynginx -p 8080:80 nginx

```
- List running containers
```bash
$ docker ps

```
- Stop the container named mynginx 
```bash
$ docker stop mynginx
```
- Start the container named mynginx:

```bash
$ docker start mynginx

```

- Display detailed information about the nginx image
```bash
$ docker inspect nginx

```
- Run the ls command in the container named mynginx
```bash
$ docker exec mynginx ls
```
- List all containers, including stopped containers
```bash
$ docker ps -a
```
- Remove the container named mynginx:
```bash
$ docker stop mynginx
$ docker rm mynginx
```

```bash
$ docker rm -f mynginx
```