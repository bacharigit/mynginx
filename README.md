# My Custom Nginx Image

This image is built from the official `nginx` image and serves a custom web page.
docker pull bacharidocker/my-nginx:latest

## Build
```bash
docker build -t mynginx .
```

## Run

```bash
docker run -d -p 8080:80 mynginx:latest
```

Then open:

http://localhost:8080

## Author
Hossein Bachari
