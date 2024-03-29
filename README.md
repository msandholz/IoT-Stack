# IoT-Stack

## Tutorials

> https://www.youtube.com/watch?v=JdV4x925au0

> https://github.com/echtelerp/IoT-Stack-tutorial

> https://www.youtube.com/watch?v=zyJ1NwPSqsk

> https://www.youtube.com/watch?v=mzYdsPUI1TA

## Install

1. Install Docker: `curl -sSL get.docker.com | sh`

2. Setting Docker user rigths: `sudo usermod -aG docker pi`  

2. Install Docker Compose: 
   - `sudo apt-get install libffi-dev libssl-dev`  
   - `sudo apt-get install -y python3 python3-pip`
   - `sudo apt-get remove python-configparser`
   - `sudo pip3 install docker-compose`

3. Install GIT: `sudo apt-get install git`

4. Clone GIT Repository: `git clone https://github.com/msandholz/IoT-Stack.git`
   (`git clone https://github.com/echtelerp/IoT-Stack-tutorial.git`)

5. Run Docker Compose: `pi@RasPi-Server:~/IoT-Stack $ docker-compose up -d` 

6. Check 


7. End Docker
   - IoT-Stack beenden: `docker-compose down`
   - Volumes löschen: `docker volume prune`
   - Images auflisten: `docker image list`
   - Images löschen: `docker image rm --force <IMAGE ID>` 
   - Ungenutze Images löschen: `docker image prune`
   - Netzwerke löschen: `docker network prune`


8. SSH to running Docker Container
   - List docker containers: `docker ps`
   - List all running containers: `docker ps -a`
   - Start docker container: `docker start <CONTAINER ID>` 
   - Stop docker container: `docker stop <CONTAINER ID>`
   - Get into container path: `docker exec -it <CONTAINER ID> bash` 

   - Get IP Adress of Container: `sudo docker inspect -f "{{ .NetworkSettings.IPAddress }}" container_name`
   - Check communication: `ping –c 3 172.17.0.2`
   - SSH to Docker Container: `ssh root@172.17.0.2`

9. Configure Influxdb
   - For more information regarding influxdb follow the wiki: https://github.com/msandholz/IoT-Stack/wiki/InfluxDB
  
10. Use Mosquitto MQTT Broker
   - For more information regarding publish and subcribe MQTT messages follow the wiki: https://github.com/msandholz/IoT-Stack/wiki/Mosquitto-MQTT-Broker

11. Grafana
   - Reset Grafana Password:
     1. Get Container ID: `docker ps` 
     2. Reset PW: `docker exec -ti <Container ID> grafana-cli admin reset-admin-password <new password>`
