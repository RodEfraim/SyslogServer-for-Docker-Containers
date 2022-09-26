# SyslogServer-for-Docker-Containers
A centralized syslog server to accompany any Docker containers.

Run the following command:

```
sudo docker-compose up -d
```

This docker command will spin up the syslogserver, container5 and container6 docker containers. Note that container5 and container6 are just dummy containers used to demonstrate that syslogserver can indeed store the logs from other docker microservices.

To see the centralized logs you can enter the syslogser by running the command below and navigativng to /var/log/docker

```
sudo docker exec -it syslogserver /bin/sh
```

Alternatively you can see the centralized logs in the syslogserver by running the following:

```
sudo docker exec -it syslogserver ls /var/log/docker
sudo docker exec -it syslogserver cat /var/log/docker/container5.log
sudo docker exec -it syslogserver cat /var/log/docker/container6.log 
```
