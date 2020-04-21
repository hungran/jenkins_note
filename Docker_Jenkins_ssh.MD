### Dockerize OpenSSH server base centos
- define ssh server to become remote-host service [dockerfile](./Dockerfile)
- modified Dockercompose.yml as below, add centos service for remote-host:
note: publish port 2222 map to 22

      version: '3'
      services:
        jenkins:
          container_name: jenkins
          image: jenkins/jenkins
          ports:
            - "8080:8080"
          volumes:
            - $PWD/jenkins_home:/var/jenkins_home
          networks:
            - net
      remote_host:
        container_name: remote-host
        iamge: remote-host
        build:
          context: centos7
        port: 
          - 2222:22
        networks:
          - net
      networks:
        net:
