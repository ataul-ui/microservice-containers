



# microservice-containers
This repository contains the code for a event-based microservice project. The "consumer" and "pulisher" containers comunicate with each other with the rabbitmq message broker container. 



## Requirements
Make sure you have docker installed.





## How to build the microservice project in you local system

First you'll need to create a docker network:
```bash
docker run -d --rm --net rabbits --hostname rabbit-1 --name rabbit-1 rabbitmq:3.8 
```

Then you'll need to start up the "publisher"
```bash
docker pull ataulhaq234/publisher-rabbit:v1.0

docker build . -t ataulhaq234/publisher-rabbit:v1.0
docker run -it --rm --net rabbits -e RABBIT_HOST=rabbit-1 -e RABBIT_PORT=5672 -e RABBIT_USERNAME=guest -e RABBIT_PASSWORD=guest ataulhaq234/publisher-rabbit:v1.0
```

And the "consumer"
```bash
docker pull ataulhaq234/consumer-rabbit:v1.0

docker build . -t ataulhaq234/consumer-rabbit:v1.0
docker run -it --rm --net rabbits -e RABBIT_HOST=rabbit-1 -e RABBIT_PORT=5672 -e RABBIT_USERNAME=guest -e RABBIT_PASSWORD=guest ataulhaq234/consumer-rabbit:v1.0
```


## How to test the microservice project
Type any word in the publisher terminal and press enter, and it should appear in the consumer terminal

