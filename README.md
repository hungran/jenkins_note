### VŨ MẠNH HÙNG
### vmhung290791@gmail.com
[Nguồn](https://google.com)

## Jenkins's note

# Enviroment
---
- Ubuntu LTS 16.04 on AWS (from vagrant box)
    - Security Group: HTTP_8080 for jenkin web
- Docker CE & Docker-compose (latest): [Installation](https://docs.docker.com/engine/install/ubuntu/) 
- Jenkins container by Docker Hub: [Installation](https://hub.docker.com/_/jenkins/)
 
---
# Initial Setup

- Using [docker-compose](/share/docker-compose.yml) file for creating Jenkins container 
- Download recommend plugins

    <img src="/picture/initial-setup.jpg">

- Setup User
    
    <img src="/picture/setup-user.jpg">

- Create first hell-world job
    
    <img src="/picture/first-hello-world-job.JPG">

# Paramater in Jenkins's project

<img src="/picture/parameter.JPG">

- Build with Parameter (String & Boolean)

    <img src="/picture/build-with-parameter.JPG">

    <img src="/picture/build-with-parameter2.JPG">

## Docker + Jenkins + SSH
[Link](./Docker_Jenkins_ssh.md)