---
layout: post
title: "Get Ready to Program - Part 1"
date: 2014-11-23 17:14:00 -0800
comments: true
categories: Long Road
---

As a new programmer in each team, I found myself always spend a lot setting up new environment.

Recently, I am exploring a software environment platform and application distribution tool called Docker. (https://www.docker.com/)

I would like to spend some time to explore it. To make it useful to distribute my personal working environment.

Docker is much easy to setup and learn than I thought. 
https://www.docker.com/tryit/ is a great link to try out some basic commands.

To be able to use Docker on my mac, I have done only few steps.

1. Install boot2docker in mac (https://github.com/boot2docker/boot2docker). boot2docker is a lightweight linux software, which used to run Docker container. After downloaded boot2docker, just double click it. Then the boot2docker will setup environment variables for mac. So, before you run your docker command, do remember to run
```
boot2docker start
```

2. Then simply put
```
docker run hello-world
```
Congratulations. That's the hello world for your docker environment. 
What does `run` command do? Running an application inside a container.
Under the hood of this command. Docker checks if these is any `image` installed in your docker. Because this is nothing in mac yet, so Docker checks public image registry, if there is any image works as default. In this case, docker download hello-world image for mac.

3. The real run command
```
docker run ubuntu:14.04 /bin/echo 'Hello world'
```
This run command use the image ubuntu:14.04 to run as a container. Then use this container to run an application, in this case, this application is `/bin/echo 'Hello world'`, which is only print `Hello world` in your terminal.

That's the basic setups and basic usage for docker. It setup a clean environment and make it available to distribute, which is like the version control software. In the following parts, I will be exploring more potential usage to make docker works as a personal environment setup tool.