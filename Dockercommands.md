# Below are some basic docker commands

## 1. Managing Containers

1. This command lists all the currently running containers
  __docker ps__
2. If you want to see all containers, including those that are not currently running, you can use this command
     __docker ps -a__
3. If you want to check its status, you can use the __docker inspect <container_name_or_id>__ command
4. You can start a stopped container using the docker start command __docker start <your_container_name>__
5. Stop a Running Container __docker stop <container_name_or_id>__
6. Restart a Container
     - Restarts a running or stopped container __docker restart <container_name_or_id>__
7. Remove a Container
     - Removes a stopped container __docker rm <container_name_or_id>__
8. View Logs of a Container
     - Shows the logs of a running or stopped container __docker logs <container_name_or_id>__
9. Execute a Command Inside a Running Container
     - Opens an interactive terminal inside a running container __docker exec -it <container_name_or_id> <command>__
## 2. Managing Images
1. List Docker Images
   - Shows a list of all locally available Docker images __docker images__
2. Pull an Image from Docker Hub
    - Downloads an image from Docker Hub __docker pull <image_name>:<tag>__
3. Remove an Image
     - Removes a Docker image. If the image is in use by a container __docker rmi <image_name_or_id>__
4. Build an Image from a Dockerfile
     - Builds a Docker image using a Dockerfile __docker build -t <image_name>:<tag> /path/to/dockerfile__
5. Tag an Image
    - Tags an existing image with a new name __docker tag <source_image> <target_image>__
6. Push an Image to Docker Hub
    - Uploads a local image to Docker Hub __docker push <image_name>:<tag>__

## 3. Below are commands will help to remove a application from docker container.
Here I have used coco annotator removal process. When you want to remove the other application the steps are remain same.

1. Navigate to the application folder
         __cd /path/to/coco-annotator__
2. Stop and Remove Docker Containers
    __docker-compose down__
3. Remove Docker Images
    __docker-compose rm__
4. Delete the Coco Annotator Directory
    __rm -rf /path/to/coco-annotator__
5. Optional: Remove Docker Network and Volumes
    __docker network prune__
    __docker volume prune__
## 4. Managing Volume
1. List out the volumes
     - docker volume ls
2.  To list all volumes that are using the local driver
     - docker volume ls -f driver=local










       
 



   
