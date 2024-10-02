# To create and run a Docker container using a Docker image, follow these steps:

## 1. Find or Pull a Docker Image

You can either use a Docker image that you already have on your machine or pull one from Docker Hub (Docker's public repository of images).

To search for an image :-

docker search (image-name)

Example :-  docker search nginx

To pull an image from Docker Hub :-

docker pull (image-name)

Example :-  docker pull nginx

This will download the latest nginx image to your local machine.

## 2. Create and Run a Container from the Image

Use the docker run command to create and start a container from the pulled image.

docker run -d --name (container-name) -p (host-port):(container-port) (image-name)

Example  :-  docker run -d --name my-nginx-container -p 8080:80 nginx

In this example :-

-d runs the container in detached mode (in the background).

--name gives your container a name (e.g., my-nginx-container).

-p 8080:80 maps port 8080 on your local machine to port 80 inside the container.

nginx is the name of the image you are running.

You can now access the service running in the container by visiting http://localhost:8080 in your web browser. or PUBLIC-IP

3. List Running Containers
You can check if the container is running by listing all active containers:

bash
Copy code
docker ps
4. Stop a Container
To stop a running container:

bash
Copy code
docker stop <container-name>
Example:
bash
Copy code
docker stop my-nginx-container
5. Remove a Container
Once the container is stopped, you can remove it if necessary:

bash
Copy code
docker rm <container-name>
Example:
bash
Copy code
docker rm my-nginx-container
This will delete the container, but the Docker image will still be available on your machine, allowing you to create new containers from it later.

6. (Optional) Remove the Docker Image
To remove the image (if you no longer need it):

bash
Copy code
docker rmi <image-name>
Example:
bash
Copy code
docker rmi nginx
This will delete the Docker image from your system.


















