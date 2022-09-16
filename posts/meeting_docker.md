---
title: Just a little Docker should not give you harm, right?
publish_date: 2021-06-16
---

Struggling around to get through your first day with Docker? It really kinda is frustrating. Add a few more tools that you just met and that's how you start burning out. To cool it down a bit, I will list a few hints I wish someone gave me when embarking a Full-Stack role including some minor DevOps tasks that keeps you going.

TL;DR

Docker plays the role similar to node and npm combined. Instead of code libraries, it makes flexible management of servers that are going to run the code that you will be developing throughout your career, potentially. You can browse documentation of run commands here. It brings server virtualization to a whole new level.

Docker Hub traffic

Talking about analogies let me do the same to Dockerfile. Similar to what package.json's role is, the Dockerfile also tells dependencies-like of your server with additional functionalities. Instead of solely telling what kind of dependencies you need it can also perform additional Linux commands, copy/move files, run scripts.

Since you now know a bit what Docker does, lets break down other keywords which make up a delicious lasagna when we first hear about them. Keywords list goes like, hub, images, containers, clusters, compose and so on.

Hub is the registry where people publish their images. An entire directory which becomes available by default on your terminal. So whenever you would try to run a server, for example docker run node it will grab a public image which uses node as its name: https://hub.docker.com/_/node (you can also host your own private registry).

Images are the entire definition of the container/vps starting from its OS to any kind of services it tells the to run, at which port and/or which port it should be exposed. Once you run a server from an image, that specific image will be saved/cached on the host or your own machine for further use/or same server recreation.

Containers, since we reached this section I will make the final analogy. Considering the others above we will keep comparing it with Javascript eco-system. Given the convenience of reusing the logic of a large codebase, developers split repeated logics and port them as npm packages. Same approach is now possible with Docker, providing Linux services or backend operations in isolated environments serving a huge app's backend. Besides the security benefits it brings on server management it also makes use of its resources more efficiently by load balancing them.

Clusters as the name suggests it is a group of some resources. In Docker it is a logical set of containers. Based on how they're designed, for example they can communicate internally without applying any security measures, reverse proxying specific containers services to the public e.g. HTTP (80) and HTTPS (443).

Compose is the engine which constructs a container or multiple in an automated fashion. It can be extended using additional configuration management software named Ansible. Docker-compose turns infrastructure-as-a-code to a sane job.

Now you have a better picture of what is going on the Docker end you can get back to your code and do the best you can 🚀