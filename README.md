# Dockerizing-a-Node.js-web-app

The goal of this example is to show you how to get a Node.js  application into a Docker container. The guide is intended for development, and not for a production deployment. The guide assumes you have a basic understanding of how a Node.js application is structured. We will create a simple web application in Node.js, then we will build a Docker image for that application, and lastly we will instantiate a container from that image.

### Building the Docker image
I have already developed the Dockerfile and Node.js app and it is available in my GitHub Repository

```sh
docker build -t <your username>/node-web-app> .
```

```sh
# docker images ls
jeenajoy5/nodejs       latest                                     642564ee0a03   3 minutes ago       59.5MB
```

Now run the container from the Image created:

```sh
docker container run --name nodejs -p 80:3000 -d <your username>/node-web-app>
```

```sh
# docker container ls
CONTAINER ID   IMAGE                COMMAND             CREATED         STATUS         PORTS                                   NAMES
f36394a7538a   jeenajoy5/nodejs  "node nodeapp.js"   3 minutes ago   Up 3 minutes   0.0.0.0:80->3000/tcp, :::80->3000/tcp   nodejs
```
