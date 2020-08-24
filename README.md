# docker-intro
Docker introductory presentation

## Introduction
- [ ] Why do you need docker?
    - [ ] Web server
    - [ ] Database
    - [ ] Messaging
    - [ ] Orchestration
    - [ ] Compatibility with underlying OS
    - [ ] Compatibility with services and libraries that were dependent on OS
    - [ ] New developers need to setup their environments (same OS, same versions of each component, etc)
    - [ ] Different Dev/Test/Prod environments
- [ ] Virtualization vs. Containers
￼

## Virtualization AND Docker containers 
￼
- [ ] Containers vs. Image
    - [ ] Image —> Package or template like a VM, that’s used to create one or more containers
    - [ ] Containers —> Running instances of images
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
