# Week 2 — Distributed Tracing

## Required Homework

Completed all required homework without any problems. Most of it done while attending live class. I don't really have anything to add here.

### Something else

While doing homework I have noticed that my frontend-react wouldn't start after docker compose up. I went to Docker containers, right clicked on frontend, clicked on View logs. It was showing this error:

![Frontend problem 2](https://user-images.githubusercontent.com/124433076/222892907-0fa8dbff-4e24-450d-a1bb-f0c44480edf3.png)

I had no idea why or how to fix it. I tried to google my problem, but it wasn't much use. I still couldn't understand what was the problem. So I decided to try and solve it myself. I have restarted GitPod. And this time I noticed:

![Frontend problem](https://user-images.githubusercontent.com/124433076/222893605-2aa289e4-6071-4162-bdde-1b950fc87e77.png)

That gave me an idea that it must be something to do with starting GitPod. But I still wasn't sure where to look. First I looked in frontend-react-js folder and it's content. I couldn't spot any faults. I was looking at all codes I could find. Checked backend-flask folder. Docker-compose.yml. Only then I checked gitpod.yml (not sure why I didn't think to check it first). I couldn't see any mistakes but I was pretty sure now that it's something wrong here. So I compared with Andrew's code. It made me laugh when I spotted my error.

![Mistake](https://user-images.githubusercontent.com/124433076/222894052-1c6f7fbd-aced-4c37-85dd-dd1c1dab94a7.png)

| was missing.


## Homework Challenges 
