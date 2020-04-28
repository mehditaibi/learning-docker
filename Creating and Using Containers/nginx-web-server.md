# Starting a Nginx Web Server

## Running an Nginx container 

docker container run --publish 80:80 nginx

 1. Downloaded image 'nginx' from Docker Hub
 2. Started a new container from that image
 3. Opened port 80 on the host IP
 4. Routes that traffic to the container IP, port 80 
