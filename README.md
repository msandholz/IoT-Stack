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

5. Run Docker Compose: `docker-compose up -d` 

6. Check 


7. End Docker
   - IoT-Stack beenden: `docker-compose down`
   - Volumes löschen: `docker volume prune`
   - Images löschen: `docker image prune`
   - Netzwerke löschen: `docker network prune`

8. SSH to running Docker Container
   - Get IP Adress of Container: `sudo docker inspect -f "{{ .NetworkSettings.IPAddress }}" container_name`
   - Check communication: `ping –c 3 172.17.0.2`
   - SSH to Docker Container: `ssh root@172.17.0.2`

====



8. Config ⏵ mosquitto.conf
```
allow_anonymous true
listener 1883 192.168.1.202
```

9. InfluxDB : https://docs.influxdata.com/influxdb/v1.8/introduction/get-started/
10. 
