# docker-intro
Docker introductory presentation

## Introduction
- [ ] Why do you need docker?
    - Let's consider you're working on a team with three other engineers. The goal is to create a web application. You decided on the frameworks, database, and orchestration tools to use. Each of you would like to contribute to the code base on all three items. 
    Each piece of the project may rely on different OS', libraries, and services. It becomes a mess to manage, especially when: 
        - New developers need to setup their environments to match the current project
        - Creating development, testing, and production environments
        - OS upgrades for each application installed

- [ ] Virtualization vs. Containers
￼   - Virtualization is a simulated computer, often with it's own BIOS/EFI and simulated (often configurable) hardware.
        - Applications layer and own kernel (does not use host kernel) 
        - Any OS can be run on any other OS
        - GUI based VMs
    - Containers will run guest applications on the same OS kernel as the host.
        - Easy to update
        - Minimal maintaince
        - Size of images is smaller
        - Speed of start-up is much faster
        - Restarting takes it to it's inital state

## Virtualization AND Docker containers 
￼
- [ ] Containers vs. Image
    -  Containers run the instances of the images that you create
    -  Images are the package or template, similar to a VM, that's used to create one or several containers

- [ ] Community vs. Enterprise Edition
- [ ] Commands
    - [ ] Docker ps -a
    - [ ] Docker run <name>
        - [ ] This is considered attached mode
    - [ ] Docker run -d <name>
        - [ ] This is considered in the detach mode (background)
        - [ ] You can attach back to the container later with
            - [ ] Docker attach <characters of container>
    - [ ] Docker run -it <name>
        - [ ] I is the STDIN (interactive mode_ 
        - [ ] T is for terminal
    - [ ] Docker pull <name> (Only pull the image, don’t run the container)
    - [ ] Docker stop <name>
    - [ ] Docker rm <name> 
    - [ ] Docker images
    - [ ] Docker rmi <name>
    - [ ] Docker exec <container name> cat /etc/hosts
    - [ ] Networking
        - [ ] Docker run -p 80:5000 <Name> 
            - [ ] Mapping port 80 of localhost to 5000 of docker container
    - [ ] Volume
￼
  
## Troubleshooting
- [ ] Troubleshoot
    - [ ] Docker inspect <name>
    - [ ] Docker logs <name> 
  
## Envirnoment Variables
- [ ] Environment variables
    - [ ] Docker run -e HELLO_NAME=Stevan <name>
  
## Security
- [ ] Security
    - [ ] Anchore
- [ ]

## Commands
docker build -t mydocker .
docker run --rm mydocker https://httpbin.org/get
docker-compose run app -I https://httpbin.org/get 
   
