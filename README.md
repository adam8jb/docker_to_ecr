

## To push image to ECR from github

Based on https://www.youtube.com/watch?v=D8ym8RP1yvo

Need to login to github





## Github actions to build & test then push to dockerhub

Based on github actions notes on Notes app








## To push image to ECR from local machine

AWS expects a separate repo for each image

Whatever your image is called, in the tag make sure the name is the same as the AWS repo name:
>docker tag flask_basic_app:latest 720603319039.dkr.ecr.eu-west-2.amazonaws.com/app:latest

Then push to the repo ('view push commands' in the ECR console will give you the exact code for this)
>docker push 720603319039.dkr.ecr.eu-west-2.amazonaws.com/app:latest

If 'docker push' is timing out you might be able to go to Docker Desktop -> Prefernces -> Docker Engine, and on the line after '"experimental": false,', add a line '"max-concurrent-uploads" : 1,'. [Source](https://www.kovarus.com/blog/docker-push-timeout-to-aws-elastic-container-registry/)




## To deploy in K8s from private cluster

[Based on this](https://www.youtube.com/watch?v=asIS4KIs40M)

Make (1) secret component which contains credentials to docker registry, and (2) use Secret with imagePullSecrets




















# docker_to_ecr
