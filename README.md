# Custom Nginx Docker Image

A simple Docker project that creates a custom Nginx image based on the official Nginx Docker image. The container serves a custom static web page.

## Features

- Based on the official `nginx:latest` image
- Serves a custom `index.html`
- Includes static assets (images)
- Easy to build and run with Docker

## Project Structure

```
.
├── Dockerfile
├── README.md
├── index.html
└── photo.jpg
```

## Prerequisites

- Docker installed

## Build the Image

```bash
docker build -t mynginx .
```

## Run the Container

```bash
docker run -d -p 8080:80 --name mynginx-container mynginx
```

## Access the Website

Open your browser and visit:

```
http://localhost:8080
```

## Dockerfile

This project uses the official Nginx image as its base:

```dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/
COPY photo.jpg /usr/share/nginx/html/
```
Note: An alternative project structure is to place website  files in a dedicated website/ directory and copy them using:
```dockerfile
FROM nginx:latest
COPY website/ /usr/share/nginx/html/
```
## Docker Image

The Docker image is available on Docker Hub:

https://hub.docker.com/bacharidocker/mynginx


## Author

Hossein Bachi
