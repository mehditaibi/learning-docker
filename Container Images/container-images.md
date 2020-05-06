# What is an image?

- App Binaries and dependencies
- Metadata about the image data and how to run the image
- Not a complete OS. No kernel, kernel modules (e.g. drivers)
- Small as one file (you app binary) like a goland static binary
- Big as a Ubuntu distro with apt, and Apache, PHP, and more installed

# Image Tagging and Pushing to to Docker Hub

## Tag an image

docker image tag ${image} ${tag}

## Push an imgage to Docker Hub

docker image push ${image}
(Need to login via docker login and make sure to to do docker logout if using a shared computer or host as the credentials are saved locally until we logout )
