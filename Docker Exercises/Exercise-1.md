<details>
<summary><b>Running a Docker Container in the Background Using nginx Image</b></summary><br>
  
```bash
$ docker run -d nginx
```
  </details>
 
 <details>
<summary><b>Running a Docker Container with a Specific Name</b></summary><br>
  
```bash
$ docker run --name web-server nginx
```
  </details>
  
  <details>
<summary><b>Exposing a Port in a Docker Container to the Host Machine</b></summary><br>
  
```bash
$ docker run -p 8080:80 nginx
```
- The above command runs an Nginx container and maps the container's port 80 to the host's port 8080. 
This means that you can access the Nginx server running in the container at http://localhost:8080. 
The -p option maps the host port to the container port.
  </details>
  
  <details>
<summary><b>Specifying an Environment Variable in a Docker Container</b></summary><br>
  
```bash
$ docker run -e MESSAGE='Hello from Docker' alpine echo $MESSAGE
```
  - The above command runs an Alpine container and sets an environment variable MESSAGE to Hello from Docker. 
  The -e option sets an environment variable in the container. In the command, echo $MESSAGE prints the value of the environment variable.
  </details>
  
  <details>
<summary><b>Running a Docker Container with a Host Directory as a Data Volume</b></summary><br>
  
```bash
$ docker run -v $(pwd)/html:/usr/share/nginx/html nginx
```
  - The above command runs an Nginx container and mounts the current working directory ($(pwd)) as a data volume in the container at the path /usr/share/nginx/html. 
  This means that any changes made to the files in the data volume will persist even after the container is deleted. 
  The -v option mounts a host directory as a data volume in the container.
  </details>
  
  <details>
<summary><b>How do you inspect a Docker image?</b></summary><br>
  
```bash
$ docker inspect <image_name>
```
  </details>
  
  <details>
<summary><b>Running a Docker Container with a Custom Network and Specifying IP Address</b></summary><br>
  
```bash
$ docker network create mynetwork
$ docker run --net=mynetwork --ip=172.18.0.100 nginx
```

  </details>
  
  <details>
<summary><b>Copying Files from a Docker Container to the Host Machine</b></summary><br>
  
```bash
$ docker create --name mycontainer alpine
$ docker cp mycontainer:/etc/passwd .

```
  </details>
  
  <details>
<summary><b>Running a Docker Container in Privileged Mode</b></summary><br>
  
```bash
$ docker run --privileged nginx
```
  </details>
  
  
  <details>
<summary><b>How do you inspect a Docker image?</b></summary><br>
  
```bash
$ docker inspect <image_name>
```
  </details>
  
  <details>
<summary><b>How do you inspect a Docker image?</b></summary><br>
  
```bash
$ docker inspect <image_name>
```
  </details>
  
  <details>
<summary><b>How do you inspect a Docker image?</b></summary><br>
  
```bash
$ docker inspect <image_name>
```
  </details>
