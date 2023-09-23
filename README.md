

This is the helper reposityory for the kube cloud project, if you wanna run the container do pull my for dockerhub as well as the rabbitmq container






Hi this is the repo that contains the consumer and publisher containers,
that are used in the microservices project. I have deployed them on dockerhub


use go routines to do something with threads and send the thread data to consumer,
after a certain time period. 


include this code in publisher.go file:
```go
package main

import (
	"fmt"
	"os"
	"syscall"
	"time"
)

func main() {
	// Get the process ID (PID)
	pid := os.Getpid()
	fmt.Printf("Publisher's process ID (PID) is %d\n", pid)
	time.Sleep(time.Second * 2)

	// Get the thread ID (TID)
	tid := syscall.Gettid()
	fmt.Printf("Publisher's thread ID (TID): %d\n", tid)
}
```
cool I learned how to do this, now just need to understand http in go

^^ make it run every 5 mins or something, include if statements when possible
use time.sleep!!!!!     this tutorial uses it:
https://www.youtube.com/watch?v=LGVRPFZr548&ab_channel=AnthonyGG 

link to go playground: https://go.dev/play/ 

https://www.youtube.com/watch?v=LGVRPFZr548&ab_channel=AnthonyGG 


to access images go to this dockerhub link: https://hub.docker.com/r/ataulhaq234/publisher-rabbit

or use this command

```bash
docker pull ataulhaq234/publisher-rabbit
```


I can write a go command that collects current thread info and sends it to consumer container. Go is basically like C in that I can use the multiplexing stuff I learned undergrad.



^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


This way all i need to have in this container is the go applications

look at this video: https://www.youtube.com/watch?v=ZBhm9X9BgcA&list=LL&index=1&t=742s&ab_channel=HoussemDellai 



ALSO DON'T DO RABBITMQ CLUSTER, JUST DO REGULAR APPLICATION USING KUBERNETES, 
MY JOB IS TO TRANSLATE THE KUBE YAML FILES INTO TERRAFORM CODES AND STUFF




ACTUALLY JUST BASICALLY COPY WHAT MARCELUS DOES IN THIS TUTORIAL:
https://www.youtube.com/watch?v=_lpDfMkxccc&t=1s&ab_channel=ThatDevOpsGuy 

I DO NEED TO DEPLOY TO DOCKER REGISTRY TO SHOW TO EMPLOYERS THAT I CARE ABOUT PRIVACY, AND BESIDE
I NEED MORE PRACTICE WIHT GOLANG ANYWAY

NO NEED TO DEPLOY TO AZURE DOCKER REGISTRY, CAN JUST DEPLOY TO DOCKERHUB USING
DEPLOYMENT.YAML FILE, THEN ON THE TERRAFORM PROJECT I CAN JUST CALL THE CONTAINERS
FROM DOCKERHUB








explain how to upload to azure container registry using the azure cli, aka follow this tutorial:
https://www.youtube.com/watch?v=jAWLQFi4USk&list=LL&index=1&ab_channel=AdamMarczak-AzureforEveryone 

just cd to the correct folder and type the az command to build and upload the image
