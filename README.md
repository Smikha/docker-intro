# docker-intro
## Introduction
###### Why Docker?
Let's consider you're working on a team with three other engineers. The goal is to create a web application. You decided on the frameworks, database, and orchestration tools to use. Each of you would like to contribute to the code base on all three items. 

Each piece of the project may rely on different OS', libraries, and services. It becomes a mess to manage, especially when: 
- New developers need to setup their environments to match the current project
- Creating development, testing, and production environments
- OS upgrades that may affect each application differently
        
 ![No Docker Solution](../master/images/DockerIntro-NoDocker.png?raw=true)

## VMs and Contaianers
Containers will run guest applications on the same OS kernel as the host.
- Easy to update
- Minimal maintaince
- Size of images is smaller
- Speed of start-up is much faster
- Restarting takes it to it's inital state

Containers vs. Image
- Containers run the instances of the images that you create
- Images are the package or template, similar to a VM, that's used to create one or several containers

 ![Docker Solution](../master/images/DockerIntro-Container.png?raw=true)


Virtualization is a simulated computer, often with it's own BIOS/EFI and simulated (often configurable) hardware.
- Applications layer and own kernel (does not use host kernel) 
- Any OS can be run on any other OS
- GUI based VMs

 ![VM Docker Solution](../master/images/DockerIntro-VM.png?raw=true)
 
 

## Commands <sup>1</sup>

Show all containers (default shows just running)

        docker ps -a

Run a command in a new container (attached mode)
        
    docker run <name> 

    -# Run container in background and print container ID (detached mode)

    docker run -d <name>
    
    -# You can attach back to the container later with
    
    docker attach <characters of container>

    docker run -it <name>
    -# I Keep STDIN open even if not attached
    -# T Allocate a pseudo-TTY

Pull an image or a repository from a registry

    docker pull <name> 

Stop one or more running containers

    docker stop <name>

Remove one or more containers
    
    docker rm <name> 

Remove one or more images
   
    docker rmi <name>

Manage images
    
    docker images

Run a command in a running container

    docker exec <container name> cat /etc/hosts

Remove all unused containers, networks, images (both dangling and unreferenced), and optionally, volumes.

    docker system prune -af
    docker system prune --volumes 

Networking
- Mapping port 80 of localhost to 5000 of docker container

      docker run -p 80:5000 <Name>

Volume  
￼ 
    ![Volume](../master/images/DockerIntro-DockerDB.png?raw=true)

  
## Troubleshooting
Return low-level information on Docker objects
    Docker inspect <name>

Fetch the logs of a container
    Docker logs <name> 
  
## Envirnoment Variables
- [ ] Environment variables
    Docker run -e HELLO_NAME=Stevan <name>
  
## Security
- [ ] Security
    - [ ] Anchore

## Commands
    docker build -t mydocker .
    docker run --rm mydocker https://httpbin.org/get
    docker-compose run app -I https://httpbin.org/get 



## Future Topics
- Networking
- Volume Mapping
- Security
- Orchestration


<sup>1</sup> https://docs.docker.com/engine/reference/commandline/cli/
   
