# docker
## hub.docker.com to list all the images from docker hub.
Learning Docker

**First comands:**

docker run hello-world
docker run -it ubuntu bash
docker ps (images that are running)
docker ps -a (show all images of containers, running or not, and some details)
docker rm <container name or ID> (to remove container, not downloaded image)
docker images (to see de images tha are downloaded)
docker rmi <image name> (delete images it was downloaded)
docker rmi -f <image name> (not recommended, the option -f force stop/delete container and remove image)
docker pull <image name> (just download image from docker hub)
docker run -d <image name> Run container in background and print container ID
docker exec <container name> <command> (to execute a command inside of container)
docker exec -it <container name> bash (open a bash inside of container)
docker volume ls (list all avaliable volumes.)

**Running the webserver nginx**
docker run -d -p 8080:80 -name webserver nginx (-p: port 8080 is from your phisical host/pc and 80 is the port of container. The option -name just give a personalized name to your container)

**Creating a personalizated image from docker hub original (your own image)**
docker commit <container name> <new image name>  (container name = your container that are in you pc and are personalizated)

**How to create and volume disk and map inside your container (use option -v)**
docker run -itd -p 8080:80 -v /usr/share/nginx/html --name webserver nginx
