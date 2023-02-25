# Week 1 — App Containerization

## Required Homework

Completed all required homework. Below I explain about some issues I faced.

### Docker-compose file

Up to this point all tasks went smoothly and worked just fine. I have created a Docker-compose file. But when tried to docker compose up, it didn't work as expected (I can't remember what was the error because I wasn't documenting my actions due to lack of time. But I think I'll try to do from now on). I start from beginning, went through all the steps again. And when came round to creating docker-compose file, I noticed that first time I saved the file in backend-flash folder. I moved it to frontend-react folder using CLI commands and deleted from backend-flash folder. And that solved the problem. Docker compose up worked.

### DynamoDB

I also experienced a problem while testing DynamoDB. It wasn't finding DynamoDB. I checked the code and everything looked good. I went through instructions again and watched video. Then I noticed that when I entered AWS command in terminal it showed an error. I couldn't understand why. Because previous week I have installed AWS CLI and it worked fine. So I closed the terminal and quit GitPod. I was suspecting that it wasn't running the code on start. This time instead of just opening GitPod site I went through GitHub account and pressed GitPod button. And it worked. I am still not sure what was the problem and how I solved it though. Was it my mistake or glitch with GitPod. I will keep an eye on it next time I use it and try different ways to see if it happens again so I can understand the problem.

##  Homework challenge

### Run the dockerfile CMD as an external script

NOTE. I am also learning how to take screenshots, document here, Markdown syntax to quote code, text and insert images.

I don't have any experience with this so first I had to go on internet and find out how to do that. I found some information. Not sure how it will work, but here it goes. Steps I took:
#### Create shell script.

```
#!/bin/sh
echo "Hello, World!"
```

![Created shell script](https://user-images.githubusercontent.com/124433076/221354088-877c77b9-a5c8-46d1-a1fb-4b5f1b1df825.png)

#### Create Dockerfile 

Used example code:
```
FROM <your_base_image>

COPY start.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/start.sh

ENTRYPOINT ["/usr/local/bin/start.sh"]
```
And this is how edited code looked like:

![Created Dockerfile](https://user-images.githubusercontent.com/124433076/221354617-e4317563-9de8-414a-80c8-ee0e78a5853b.png)

#### Build Docker image. 

Here I faced a problem. It showed an error 

>"unable to prepare context: unable to evaluate symlinks in Dockerfile path: lstat /workspace/aws-bootcamp-cruddur-2023/Dockerfile: no such file or directory". 

I wasn't sure what it's all about but guessed I might be in wrong directory. After few failed attempts:

![Failing to build docker image](https://user-images.githubusercontent.com/124433076/221355740-12b4d98a-0878-4588-afad-e93db00e19ca.png)

I finally managed to get to the right directory and build Docker image:

![Docker image built](https://user-images.githubusercontent.com/124433076/221355819-6818346f-4b5e-4814-b60a-b5433bc5ea29.png)

#### Run container. 

I believe I have successfully completed the task.

![Run container](https://user-images.githubusercontent.com/124433076/221355962-0d036ccf-bb00-4de2-a2b1-6b77ebee1a64.png)

#### Test

I decided to make changes to the shell script and go through the process again. I was surprised by how fast and easy it was to do that. Here is updated text:

![Updates shell script](https://user-images.githubusercontent.com/124433076/221356329-2dfe9c93-23e0-4584-91dc-e42d812cffa8.png)

### Push and tag an image to DockerHub

#### Opened free-tier DockerHub account and logged in to Docker CLI

Using command 
`docker login`

#### Tag image

Next I wanted to tag image. But I had no idea how to do that. First I found that I need to know if I already have an image or I need to create one.

To check for any Docker images I ran command

`docker images` 

![Docker images](https://user-images.githubusercontent.com/124433076/221358116-75fca7fa-3d78-4df8-9bfe-baa8cbeb141d.png)

Once I knew I have an image and it's details I was able to tag an image with command:

`docker tag <image_name> <dockerhub_username>/<repository_name>:<tag>`

#### Push tagged image to DockerHub

Next I pushed tagged image to DockerHub using command:

`docker push <dockerhub_username>/<repository_name>:<tag>`

Here is successfully pushed image

![Push image to dockerHub](https://user-images.githubusercontent.com/124433076/221358670-00a0d81a-3db6-445b-a1a6-b776454c0fbf.png)

## ***Mission accomplished***


