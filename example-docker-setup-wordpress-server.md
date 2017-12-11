### Wordpress Dev Environment with Docker

#### Step 1: Search an image
```
docker search wordpress nginx
```

#### Step 2: Pull an image
```
docker pull tlongren/docker-wordpress-nginx-ssh
```
#### Step 3: Create a container
```
docker run -d -ti tlongren/docker-wordpress-nginx-ssh bash
```
- Get container name
```
docker ps -l
```
- Start some services in "background" docker.
- "admiring_dubinsky" is the name of Container of my server, change it for your server.

```
docker exec -ti admiring_dubinsky bash -c "service mysql start"
```
```
docker exec -ti admiring_dubinsky bash -c "service nginx start"
```

#### Step 4: Test

- Get container IP:
```
  docker inspect <containr-ID> | grep IP
```
- Is nginx running ?
```
  telnet <container-IP> 80
```
#### Step 5: Port forward for external access to container.
@TODO
##### With CentOS

##### With Ubuntu