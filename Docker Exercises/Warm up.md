
## Warm up  
#### This simple exercise is intended to warm you up or help you understand the basics of Docker.
<details>
<summary><b>How do you inspect a Docker image?</b></summary><br>
  
```bash
$ docker inspect <image_name>
```
  </details>

<details>
<summary><b>
How do you mount a volume in a Docker container?</b></summary><br>

```bash
$ docker run -v <host_path>:<container_path> <image_name>
```
</details>

<details>
<summary><b>
How do you execute a command in a running Docker container?</b></summary><br>

```bash
$ docker exec <container_name> <command>
```
</details>
<details>
<summary><b>
How do you copy files from a Docker container to the host system?</b></summary><br>

```bash
$ docker cp <container_name>:<container_path> <host_path>
```
</details>

<details>
<summary><b>
How do you connect a Docker container to a Docker network?</b></summary><br>

```bash
$ docker run --network <network_name> <image_name>
```
</details>


<details>
<summary><b>
How do you inspect a Docker network?</b></summary><br>

```bash
$ docker network inspect <network_name>
```
</details>

<details>
<summary><b>
How do you remove a Docker network?</b></summary><br>

```bash
$ docker network rm <network_name>

```
</details>
<details>
<summary><b>
How do you restart a stopped Docker container?</b></summary><br>

```bash
$ docker restart <container_name>

```
</details>
<details>
<summary><b>
List all images on your local machine</b></summary><br>

```bash
$ docker image ls
```
</details>

<details>
<summary><b>
Pull the latest version of the nginx image from the Docker Hub registry</b></summary><br>

```bash
$ docker pull nginx:latest
```
</details>

  <details>
<summary><b>
Launch a new container from the nginx image, mapping port 80 in the container to port 8080 on the host</b></summary><br>
    
```bash
$ docker run --name mynginx -p 8080:80 nginx
```
 </details>

<details>
<summary><b>
List running containers</b></summary><br>

```bash
$ docker ps
```
</details>

<details>
<summary><b>
Stop the container named mynginx </b></summary><br>
  
```bash
$ docker stop mynginx
  ```
  </details>
  
<details>
<summary><b>
Start the container named mynginx
  </b></summary>
  <br>

```bash
$ docker start mynginx

```
</details>

<details>
<summary><b>
Display detailed information about the nginx image
  </summary></b>
  <br>
    
```bash
$ docker inspect nginx
```
</details>
<details>
<summary><b>
Run the ls command in the container named mynginx
  </summary></b>
  <br>
    
```bash
$ docker exec mynginx ls
```
</details>

<details>
<summary><b>
List all containers, including stopped containers
  </summary></b>
  <br>
    
```bash
$ docker ps -a
```
</details>

<details>
<summary><b>
Remove the container named mynginx</summary></b>
 <br>
    
```bash
$ docker stop mynginx
$ docker rm mynginx
# or
$ docker rm -f mynginx
```
</details>
