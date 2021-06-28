# Docker

## Docker

Check available Images

```text
sudo docker images
```

Check the running containers

```text
sudo docker ps
```

Run the image

```text
sudo docker run -it jasonchaffee/kali-linux
```

Commit the Container

```text
sudo docker commit CONTAINER_ID NEW_IMAGE_NAME
```

Mount the Directory

```text
docker run -d -it --name mounttest --mount type=bind,source="/home/ohhboy/",target=/app jasonchaffee/kali-linux
```

Run kali

```text
docker run -d -it jasonchaffee/kali-linux
```



