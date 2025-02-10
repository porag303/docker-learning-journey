## Run an NGINX Docker Container

`docker run -d --name first-container -p 8090:80 nginx`

### The command is used to run an NGINX container in Docker. Here's the breakdown of the components:

`docker run`: This command instructs the Docker Engine to run the container from a specific image.

`-d`: This flag stands for "detached mode." It means that the container will run in the background.

`--name first-container`: This assigns a custom name (first-container) to the container for easier reference later.

`-p 8090:80`: This flag maps a port on the local machine to a port inside the container.

  - ``8090``: This is the port on the local machine (host) that want to access.</li>

  - ``80``: This is the port inside the container where the NGINX web server will be running. Nginx default HTTP port.

>By mapping the host's port 8090 to the container's port 80, we can access the NGINX server by visiting http://localhost:8090 on the browser.

`nginx`: This specifies the image want to use to create the container. Docker will pull the official NGINX image from Docker Hub if it’s not already available on the local machine.

__Accessing the Web Server: Open a browser and go to http://localhost:8090 to see the NGINX default page__

## Stopping the Container:

`docker stop first-container`

## Removing the Container:

`docker rm first-container`
