# MYSQL Container aufsetzten 

Pull MYSQL Image 

> sudo docker pull mysql/mysql-server:latest

Lister aller Docker Images. 

> sudo docker images

Erstellen des Containers. 

> sudo docker run --name=mysql_docker -d mysql/mysql-server:latest

überprüfen ob der Container läuft. 

> docker ps

Installation MySQL client package. 

> apt-get install mysql-client

Dann öffne das LOG File des MYSQL Containers um das generierte Root Passwort zu finden. 

> sudo docker logs mysql_docker

Scrolle bis zu diser Linie [Entrypoint] GENERATED ROOT PASSWORD: , dort ist das generierte Root Passwort 

Als nöchstes gehen wir in das Bash des MYSQL Containers. 

> sudo docker exec -it mysql_docker bash

![grafik](https://user-images.githubusercontent.com/89446428/178361030-d779633b-2c07-4e40-8ac6-79f75bb41eae.png)

## Danach ist alles Bergab gegangen... 

### Konfiguration MySQL Container

erstelle ein Directory auf der Host Maschine 

> sudo mkdir -p /root/docker/mysql_docker/conf.d

Erstelle ein eigenes MYSQL File. 

Zum überürfen des Files: 

> sudo docker inspect mysql_docker

Volumen Directory erstellen. 

> sudo mkdir -p /LB2/mysql-data

Neustart des Containers und Mountain des Volumen 

docker run \
--detach \
--name=mysql_docker \
--env="MYSQL_ROOT_PASSWORD=my_password" \
--publish 6603:3306 \
--volume=/root/docker/mysql_docker/conf.d:/etc/mysql/conf.d \
--volume=/storage/docker/mysql-data:/var/lib/mysql \
mysql

Überprüfen ob die änderungen angenommen wurden. 

> sudo docker inspect mysql_docker

To start the MySQL container run:

> sudo docker start mysql_docker

Stop the MySQL container, use the command:

> sudo docker stop mysql_docker

To restart the MySQL container run:

> sudo docker restart mysql_docker

Dann löschen des Containers: 

> sudo docker rm mysql_docker

