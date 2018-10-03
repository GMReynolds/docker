# docker
A repository containing the project files and notes for the docker projects I have worked on

## Main Concepts of docker
Used to develop deploy deploy and run applications with containers.

### Containerisation
* Flexible - able to deal with simple to complex applications.
* Lightweight - leverage and share the host.
* Interchangable - can deploy updates and upgrades on the fly.
* Portable - build locally , deply to the cloud and run anywhere.
* Scalable - can increase and automatically distribute container replicas.
* Stackable - you can stack services vertically and on the fly.

**Image** = an executable package that includes everything needed to run the application (The code, a runtime, libraries, environment variables, and configuration files).

**Container** = launched by running an image. A runtime instance of an image (what it becomes in memoruy when it is executed)

To List the running containers:

```
docker ps
```
