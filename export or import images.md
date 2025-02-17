### Enter into a Docker Container

`docker exec -it container_id bash`

- `docker exec`: Run a command in a running container
- `-it`: Interactive terminal mode
- `container_id`: The container's ID or name you want to interact with
- `bash`: Start a bash shell inside the container

### Copy Local Files to Docker Container

`docker cp . mynginx:/usr/share/nginx/html`

- `docker cp`: Command to copy files or directories between the host and container
- `.`: The source directory (all files in the current directory)
- `mynginx`: The container name or ID
- `/usr/share/nginx/html`: The destination directory in the container

### Commit Docker Container to Export as an Image

`docker commit container_name new_image_name`
- `container_name`: Name or ID of the container you want to commit
- `new_image_name`: The name you want to give the new image.

### Run a Docker Container

```
docker images
docker run -d -p 8090:80 image-name
```
### Save Docker Images as a Tarball Archive

`docker save image-name | gzip > image-name.tar.gz`

- `docker save`: Export the image to a tarball
- `gzip`: Compress the tarball to save space
- `image-name.tar.gz`: The output compressed file

### Check the Size of the Image Tarball

`du -sh image-name.tar.gz`

- `du`: Disk usage command
- `-sh`: Human-readable output with the total size

### Remove Docker Container

`docker rm -f container_id`

### Remove Docker Image

`docker rmi image_id`

### Loading a Docker Image

`docker load -i <image-name>.tar`

### Run an Imported Container

`docker run -d --name <imported-container-name> --restart=always -p 8090:80 <container-name>`

- `-d`: Runs the container in detached mode, allowing it to run in the background
- `--name <imported-container-name>`: Assigns a name to the container
- `--restart=always`: Ensures the container will restart automatically if it stops or if Docker itself restarts
- `-p 8090:80`: Maps port 8090 on your host machine to port 80 inside the container
- `<container-name>`: The name of the image or the repository are using to run the container

### Viewing Container Logs

`docker logs <container-id>`

#### Follow Logs in Real-Time

`docker logs -f <container-id>`

## Summary of Commands

| Command | Description |
| --- | --- |
| `docker exec -it container_id bash` | Enter Docker Container |
| `docker cp. mynginx:/usr/share/nginx/html` | Copy Files from Local to Docker Container |
| `docker commit container_name new_image_name` | Commit Docker Container to New Image |
| `docker run -d -p 8090:80 image-name` | Run Docker Container in Detached Mode |
| `docker save image-name` | Save Docker Image to a Tarball Archive |
| `du -sh image-name.tar.gz` | Check Size of Saved Image |
| `docker logs <container-id>` | Viewing Container Logs |
| `docker logs -f <container-id>` | Follow Logs in Real-Time |
| `cat /etc/os-release` | Check Operating System Inside Container |
