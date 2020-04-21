# Starting a Nginx Web Server

#### Running an Nginx container 

docker container run --publish 80:80 nginx

 1. Downloaded image 'nginx' from Docker Hub
 2. Started a new container from that image
 3. Opened port 80 on the host IP
 4. Routes that traffic to the container IP, port 80 

#### Running Container in the background
docker container run --publish 80:80 --detach nginx => to run in the background => returns unique container ID. 

#### See all running container
To see all containers running =>  docker container ls (running containers) && docker container ls -a (all containers that have been started) 

#### Stopping a Container 
Top stop container => docker container stop ${Container ID}

#### run vs start 
"docker container run" always start a new container 
"dokcer container start" starts an existing container

#### Naming a container
docker container run --publish 80:80 --detach --name webhost nginx => To give the name "webhost" to container
--detach => run container in the background 

#### Output a Container Logs 
to output the logs of a container by name => docker container logs webhost 

#### Remove a container 
docker container rm DockerID 