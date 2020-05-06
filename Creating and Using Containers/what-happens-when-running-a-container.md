# What happens when running a container 

1. Looks for that image locally in image cache, doesn't find anything 
2. Then looks in remote image repository (defaults to Docker Hub)
3. Dowloads the latest version (nginx:latest by default)
4. Creates new container based on that image and prepares to start
5. Gives it a virtual IP on a private network inside docker engine 
6. Opens up port 80 on host and forwards to port 80 in container 
7. Starts container by using the CMD in the image Dockerfile