---
title: "Snippets - Docker"
last_modified_at: 2020-09-19T22:17:49
categories:
  - Blog
tags:
  - Snippets
  - Docker
toc: true
toc_sticky: true
toc_label: "Dans cette page..."
---


Some Docker commands snippets


# Commands about docker-compose.yml file

## build
```
docker-compose -f docker-compose.yml build MY_CONTAINER_NAME
```

## Build without cache
```
docker-compose -f docker-compose.yml build --no-cache MY_CONTAINER_NAME
```

## Run container in the background and leave them running
```
docker-compose -f docker-compose.yml up -d MY_CONTAINER_NAME
```

## Start existing container
```
docker-compose -f docker-compose.yml start MY_CONTAINER_NAME
```

## Stop container
```
docker-compose -f docker-compose.yml stop MY_CONTAINER_NAME
```

## Stop and remove existing container, network
```
docker-compose -f docker-compose.yml down MY_CONTAINER_NAME
```

## Stop and remove existing container and volumes
```
docker-compose -f docker-compose.yml down -v MY_CONTAINER_NAME
```

## Get log container
Change tail value as you need.
```
docker-compose -f docker-compose.yml logs --tail=100 -f MY_CONTAINER_NAME
```

## Get Status container
```
docker-compose -f docker-compose.yml ps
```

## Remove all unused docker objects
```
docker system prune
```

## Remove all unsed docker images
"f" force removing
```
docker prune -af
```

## Some example on how to interact with a docker-compose.yml container

Run bash command line
```
docker-compose -f docker-compose.yml exec MY_CONTAINER_NAME /bin/bash
```

Run psql command line
```
docker-compose -f docker-compose.yml exec MY_CONTAINER_NAME psql -U PG_USERNAME
```