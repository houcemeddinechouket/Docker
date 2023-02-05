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
  - The above command runs an Nginx container in privileged mode. The --privileged option gives the container full access to the host machine's resources, including access to all devices.
  </details>
  
  
  <details>
<summary><b>Running a Docker Container with a Read-Only File System</b></summary><br>
  
```bash
$ docker run --read-only nginx
```
  - The above command runs an Nginx container with a read-only file system. The --read-only option makes the container's file system read-only, preventing any changes to the file system from within the container.
  </details>
  
  <details>
<summary><b>Running a Docker Container with Resource Limits</b></summary><br>
  
```bash
$ docker run --memory 512m --cpus 2 nginx
```
  </details>
  
  <details>
<summary><b>Creating a Docker Image from a Container</b></summary><br>
  
```bash
$ docker run --name mycontainer alpine
$ docker commit mycontainer myimage
```
  - The above command creates an Alpine container with a name mycontainer and then creates an image myimage from the container. The docker commit command creates an image from a container's changes.
  </details>
  
   <details>
<summary><b>Running a Docker Container with Resource Limits</b></summary><br>
  
```bash
$ docker run --memory 512m --cpus 2 nginx
```
  </details>
  
   <details>
<summary><b>Running a Docker Container with a Custom Hostname
</b></summary><br>
  
```bash
$ docker run --hostname customhostname nginx

```
  </details>
  
   <details>
<summary><b>Inspecting the Logs of a Docker Container</b></summary><br>
  
```bash
$ docker run --name mycontainer alpine echo "Hello from Docker"
$ docker logs mycontainer

```
  </details>
  
  
  
  
