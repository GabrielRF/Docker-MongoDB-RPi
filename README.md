# MongoDB docker conteiner for RaspberryPi

##### Dockerfile originally written by: https://github.com/matteoredaelli/docker-mongodb-rpi

===

##### This image was tested on a RaspberryPi3 as MongoDB oficial image didn't work.

===

## Docker installation

```
curl -ssl https://get.docker.com | sh
```

## Docker run

```
docker run -v /usr/local/bin/thumbot/mongo:/data/db -p 27017:27017 --name mongodb GabrielRF/Docker-MongoDB-RPi
```

`-v`: Mount a volume - host:container

`-p`: Ports - host:container
