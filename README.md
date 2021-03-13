# Hello docker

Hello. Now i'll tell you about docker. Let's go.

## Install docker

---
For install docker you'll dowload [docker descktop](https://www.docker.com/products/docker-desktop) if you use windows or linux or install [docker engine](https://docs.docker.com/engine/install/) with package installer.

---

## Run docker container

If you installed docker use this command:

`docker run -d -p 80:80 docker/getting-started`

---

## What's container

**Container** is a isolated process for all process in you machine or container is a very light virtual machine with only what you need torun your project installed.

---

## What's Docker image

Docker Image is a isolated filesystem that uses docker container.

---

## Sample application

To the get started with app you'll dowload it in the [git rep](https://github.com/docker/getting-started/tree/master/app). After thats exstract folder app and delete other files or folders. Now you have a source code task manager on js. All that's left to do run it.

First you'll create file with name "Dockerfile".

You'll paste this code to the Dockerfile.

```docker
FROM node:12-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"] 
```

Save this file

Create a docker image by this command.

`docker build -t TAG_NAME .`

This command build image image named TAG_NAME using code from this folder.
