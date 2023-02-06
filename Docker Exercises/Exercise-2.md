
<details><summary><b>Run a Jenkins container and name it "myjenkins"</b></summary><br>

  ```bash
  $ docker run --name myjenkins -d -p 8080:8080 -v jenkins_data:/var/jenkins_home jenkins/jenkins
  ```
</details>
<details><summary><b>List running containers</b></summary><br>

  ```bash
$ docker ps
```
</details>
<details><summary><b>Attach to the container</b></summary><br>

  ```bash
  $ docker attach myjenkins
```
</details>
<details><summary><b>Check container logs</b></summary><br>

  ```bash
  $ docker logs myjenkins
```
</details>
<details><summary><b>Execute a command inside the container</b></summary><br>

  ```bash

$ docker exec myjenkins ls
  ```
</details>
<details><summary><b>Inspect the container and access it via IP address in the browser</b></summary><br>

  ```bash
  $docker inspect myjenkins
```
</details>
<details><summary><b>Pause the container</b></summary><br>

  ```bash
docker pause myjenkins
  ```
</details>
<details><summary><b>Resume the container</b></summary><br>

  ```bash
  $docker unpause myjenkins
  ```
</details>
<details><summary><b>Display stats</b></summary><br>

  ```bash
$ docker stats myjenkins
  ```
</details>
<details><summary><b>Stop the container</b></summary><br>

 ```bash
$ docker stop myjenkins
  ```
</details>
<details><summary><b>Delete the container</b></summary><br>

  ```bash
$ docker rm myjenkins
  ```
</details>
<details><summary><b>Remove all stopped containers</b></summary><br>

```bash  
$ docker container prune
```
</details>
<details><summary><b>Push a Docker image to Amazon ECR repository</b></summary><br>

```bash
$ aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com
$ docker images
$ docker tag <image-id> <aws_account_id>.dkr.ecr.<region>.amazonaws.com/my-repository:<tag>
$ docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/my-repository:<tag>
```
</details>

<details><summary><b>Pull image from Amazon ECR</b></summary><br>

  ```bash
  $ docker pull <aws_account_id.dkr>.ecr.<region>.amazonaws.com/my-repository:<tag>
  ```
</details>


