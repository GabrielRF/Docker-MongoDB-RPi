# MongoDB docker conteiner for RaspberryPi

##### Dockerfile originally written by: https://github.com/matteoredaelli/docker-mongodb-rpi

===

##### This image was tested on a RaspberryPi3 as MongoDB oficial image didn't work.

===

## Docker build

##### The image should be ready at hub.docker. Build it only if you aren't getting it from hub.docker.

```
git clone https://github.com/GabrielRF/Docker-MongoDB-RPi/ 
cd Docker-MongoDB-RPi/
docker build -t gabrielrf/docker-mongodb-rpi .
```

## Docker installation

```
curl -ssl https://get.docker.com | sh
```

## Docker run

```
docker run -d -v /usr/local/bin/mongo:/data/db -p 27017:27017 --name mongodb gabrielrf/docker-mongodb-rpi
```
`-d`: Run as a daemon

`-v`: Mount a volume - host:container

`-p`: Ports - host:container


## Known issues

If you are getting any error after stoping the container, check if `mongod.lock` existis. If it does, remove it.

```
rm /usr/local/bin/mongo/mongod.lock
```
