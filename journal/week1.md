# Week 1 — App Containerization

## Required Homework

Completed all required homework. Below I explain about some issues I faced.

### Docker-compose file

Up to this point all tasks went smoothly and worked just fine. I have created a Docker-compose file. But when tried to docker compose up, it didn't work as expected (I can't remember what was the error because I wasn't documenting my actions due to lack of time. But I think I'll try to do from now on). I start from beginning, went through all the steps again. And when came round to creating docker-compose file, I noticed that first time I saved the file in backend-flash folder. I moved it to frontend-react folder using CLI commands and deleted from backend-flash folder. And that solved the problem. Docker compose up worked.

### DynamoDB

I also experienced a problem while testing DynamoDB. It wasn't finding DynamoDB. I checked the code and everything looked good. I went through instructions again and watched video. Then I noticed that when I entered AWS command in terminal it showed an error. I couldn't understand why. Because previous week I have installed AWS CLI and it worked fine. So I closed the terminal and quit GitPod. I was suspecting that it wasn't running the code on start. This time instead of just opening GitPod site I went through GitHub account and pressed GitPod button. And it worked. I am still not sure what was the problem and how I solved it though. Was it my mistake or glitch with GitPod. I will keep an eye on it next time I use it and try different ways to see if it happens again so I can understand the problem.

##  Homework challenge

### Run the dockerfile CMD as an external script

I don't have any experience with this so first I had to go on internet and find out how to do that. I found some information. Not sure how it will work, but here it goes. Steps I took:
1. Create shell script. No problems.
2. Created Dockerfile. It is saved in Homework challenges folder.
