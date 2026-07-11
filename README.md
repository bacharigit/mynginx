# Dockerized Nginx Static Website

This project demonstrates how to create a custom Docker image using **Debian Stable Slim** and **Nginx** to serve a static HTML website.

## Project Structure

```text
.
├── Dockerfile
├── index.html
├── image1.png
└── README.md
```

## Dockerfile Overview

* Uses `debian:stable-slim` as the base image.
* Installs the Nginx web server.
* Copies the website files into Nginx's document root (`/var/www/html`).
* Exposes port **80**.
* Runs Nginx in the foreground.

## Build the Docker Image

```bash
docker build -t mynginx  .
```

## Run the Container

```bash
docker run -d -p 8080:80 --name my-nginx-container my-nginx-image
```

> **Note:** Replace `my-nginx-container` with any container name you prefer.

## Verify the Container

List running containers:

```bash
docker ps
```

View the container logs:

```bash
docker logs my-nginx-container
```

## Access the Website

Open your browser and visit:

```text
http://localhost:8080
```

You should see the custom `index.html` page served by Nginx.

## Stop and Remove the Container

```bash
docker stop my-nginx-container
docker rm my-nginx-container
```

## Technologies Used

* Docker
* Debian Stable Slim
* Nginx
* HTML

## What I Learned

Through this project, I practiced:

* Building a custom Docker image from a Debian base image.
* Installing software using `apt`.
* Copying application files into a Docker image.
* Exposing container ports.
* Running a web server inside a Docker container.
* Serving a static website with Nginx.


```
## Docker Image

The Docker image is available on Docker Hub:
https://hub.docker.com/r/bacharidocker/mynginx

## Author

Hossein Bachari




