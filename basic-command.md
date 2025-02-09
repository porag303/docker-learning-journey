## Docker Basic Commands

### Check Active Containers

`docker ps`

>This command displays information about active containers, such as container ID, image name, command, creation time, status, ports, and container name.

### Check All Containers (Including Stopped)

`docker ps -a`

>This command shows a list of all containers, both running and stopped, along with their details such as container ID, image name, status, and more.

### Stop Container

`docker stop <container_id_or_name>`

>This command gracefully stops a running container by sending a SIGTERM signal, giving it a chance to shut down properly. If the container does not stop within a set time, it will be forcefully terminated with a SIGKILL signal.

### Remove Stopped Containers

`docker system prune`

>This command removes all stopped containers, unused networks, dangling images, and build cache, freeing up disk space. Be cautious as this will delete unused data.

### Remove Running Container

`docker rm -f <container_id_or_name>`

>This command removes a running container, forcing it to stop if necessary. It’s used when you need to delete a container that is currently running.

### Remove Images

`docker rmi <image_id>`

>This command removes a Docker image from the local system. If the image is in use by a container, it must be stopped or removed before you can delete the image.
