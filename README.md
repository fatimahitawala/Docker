# Docker
Understanding of Docker Architecture
### WHAT IS Docker
Docker is a Containerized tool, to automate the application deployment for them to run in any environment or any OS effeciently. It packages all its dependencies, libraries along with the code.
In the architecture there is docker-client, docker host, and docker registry. Docker client uses rest API methods to talk to docker deamon. Docker deamon do heavy lifting of building, running and distributing of your containers. Another docker clinet is docker compose, which will let you develop multiple containers.

### Multistage and distorless images

##### Advantages of using multistage images to reduce docker image size from GB to MB.
In dockerfile we can  make use of multistage, on first stage we can add heavy image like ubuntu, or any ther image with all  required packages, then in next build we can use base image and add lightweight images like python run-time, go-lang etc which will utlizise its parents image and finally only child image will be our final image. Hence we can take advantage of multistage images.
##### Distorless images
These images are light weight images, which will not contain the libraies, packages, instead only include run-time or sometimes not even that, hence its secure and reduce vuln as its not expose to machine.

##### Docker Volumnes
###### Bind mounts/Host volumne,
container and host os are binded, whatever file we have in cotainer, backup will be there on host system, as containers are ephimeral (once down and there wont be data persistence) so bind volume comes in handy



