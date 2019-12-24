# How to debug if docker not start

## use docker log
```
docker logs -f [container ID]
```

## use docker cp

copy the whole folder structure from container to local file system
```
docker cp [container ID]:/. ./tmp
```

## comment out the CMD and ENTRYPOINT

comment out the startup commands, like CMD or ENTRYPOINT, build and then use sh command to start the container
```
docker run -it [image repository] /bin/sh
docker run -it [image repository] "//bin//sh"
```

