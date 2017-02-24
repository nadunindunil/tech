---
layout: post
title: Docker
description: Introduction to Docker
img: docker.png
---

At the beginning when people host applications they used separate servers for each application. But using a whole machine for just one application was a waste of machine’s resources. Also the cost people spent on the server was considered as a waste, because single application could use at most a half of a machine resource.

![delete gh-pages branch](https://qph.ec.quoracdn.net/main-qimg-5381f9e1731eb4a2b78c591f6fb4e575?convert_to_webp=true)

Then the virtual machines were introduced. In this scenario one machine could be separated into many virtual machines and use them as separate machines. VM method could reduce the cost and increase the efficiency but there were some drawbacks.

Even though Virtual Machines are a success than using separate servers, resources consumed by the OS was too high. Then people found out that an application required only secure and isolated environment with minimum operating system services.

Then what is the perfect solution for this scenario and what is docker?

So, the question of **what is docker** can be answered as follows,

*Docker is considered as the world's leading software containerization platform.*

**What is a Container?**
<blockquote>
container is an object for holding or transporting something.
The meaning of the container can be considered as a large metal box of a standard design and size used for the transport of goods by road, rail, sea, or air.
</blockquote>

When it comes to Docker the same properties of containers in real-life applies to Docker Containers. Docker container wraps up your application, environment and all the things you need to run the application. Then you can host your application anywhere you want without worrying about the dependencies.

Containers are considered as light weight and resource efficient than VMs.


![delete gh-pages branch](https://qph.ec.quoracdn.net/main-qimg-f7e5896d1238d0172f188ae20dfc1a61?convert_to_webp=true)

Containers, however, use shared operating systems, means they are much more efficient than hypervisors in system resource terms. Instead of virtualizing hardware, containers rest on top of a single Linux instance.
A container is considered as light weight because it does not include a full operating system inside and runs on top of the host OS. Containers are considered as isolated user spaces that include minimum OS services required for your application. In addition to that, containers can provide security to your server using namespaces and capability kernel security services.

Before the introduction of Docker, your code would run in your laptop and you'd think you got it working as you expected, but then something is different on the server, not the right files or configuration or something else, and it would not work. Then you can waste the rest of your day analyzing what was the mistake you made. But if you use the Docker, it can save the day from guarantying your applications functionality in any server. If it worked in your local container it would work in your server container as it worked in your local. what you have to do is just deploy your docker image in a docker container service.

As the conclusion, Docker is the newest trend in server virtualization and it’s becoming a famous technology in industry since the qualities it has such as ***light weight,resource efficiency*** and last but not least ***guarantying functionality of your application in any server as it worked in your laptop.***
Hope this article helped for you to have a brief idea about what docker is and why we need to use docker. In my next article we will discuss about docker containers in details.

references - [This is the best explanation we've heard for why Docker has become such a hot startup](http://www.businessinsider.com/docker-why-it-took-off-2015-3)

[What is Docker and why is it so darn popular ZDNet](http://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/)
