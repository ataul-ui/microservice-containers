All the containers stuff for the cloud native project can be done in this,

the codespaces pull request stuff can be done on this

since this part will be entirely containers, 

so yeah delete the other container stuff from the cloud native project

and also link this repo in the cloud native readme to give examples of containers
that can be uploaded to azure container registry, hmmm maybe use github actions?
idk





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




also give credits to marcelus demprey provide a link to his git repo I took the code from