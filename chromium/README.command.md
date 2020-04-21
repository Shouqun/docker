https://docs.docker.com/engine/reference/commandline

# Docker images

```bash
docker images
```


```bash
docker rmi -f xxx
```

# Run docker

```bash
docker run -it -v /Users/xxx/Code/Browser/docker/data:/data:delegated -p 8022:22/tcp -p 8080:80/tcp chromium-android:1.0
```

# Attach/detach to container

```bash
docker attach 81ce417dbda4
#Detach: Ctrl + P + Q
```

# Commit change

```bash
ocker commit b5f6441d9178 chromium-android:1.0
```

# Save docker images

```bash
docker save chromium-android:1.0 | gzip > chromium-android-1.0.tar.gz
```

# docker load image

```bash
docker load -i chromium-android-1.0.tar
```
