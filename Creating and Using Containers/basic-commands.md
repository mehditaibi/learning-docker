
# Basic Commands

## Running Container in the background
docker container run --publish 80:80 --detach nginx => to run in the background => returns unique container ID. 

## See all running container
To see all containers running =>  docker container ls (running containers) && docker container ls -a (all containers that have been started) 

## Stopping a Container 
docker container stop ${Container ID}

## run vs start 
"docker container run" always start a new container 
"dokcer container start" starts an existing container

## Naming a container
docker container run --publish 80:80 --detach --name webhost nginx => To give the name "webhost" to container
--detach => run container in the background 

## Output a Container Logs 
to output the logs of a container by name => docker container logs webhost 

## Remove a container 
docker container rm DockerID 

## Showing all running processes 

ps aux 

## Process list of a container 

docker container top 

## Details of a container config 

docker container inspect 

## Performance stats for all containers 

docker container stats 

# Getting a Shell inside a container 

## Starting a new container interactively 

docker container run -it (-t simulates a terminal like what SSH does,  -i keep session open to receive terminal input)

## Running additional commands in existing container 

docker container exec -it 

## Check the exposed port of a container 

docker container port ${containerIDorName} 

# Networking 

## Check the IP Address of a container 

docker container inspect --format '{{ .NetworkSettings.IPAddress }}' ${containerIDorName}

## Show all the network that have been created 

docker network ls 

## Check the default Docker virtual network (bridge, NAT'ed behind the Host IP)

docker network inspect bridge 

## Create a Docker network 

docker network create my_app_network 

## Assign a new container to a network 

docker container run -d --name new_nginx --network my_app_network nginx 

## Connect a container to a network 
docker network connect ${networkID} ${dockerID} 

## Disconnect a container of a network
docker network disconnect ${networkID} ${dockerID} 
