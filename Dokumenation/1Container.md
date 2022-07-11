# Apache Webserver aufsetzten 

Zuerst muss man Docker Compose installieren 

> sudo apt-get install docker-compose

Danach erstellen wir einen Ordner. 

> mkdir LB2

Dort drin erstellen wir dann ein Dockerfile und index.html. 

> nano Dockerfile

Und wir fügen folgenden Input ein:

FROM ubuntu/apache2
COPY index.html /var/www/html/
EXPOSE 8080

Hier definieren wir das image, welches wir installieren möchten.

Nun erstellen wir noch das index.html file:

> nano index.html

Dort fügen wir unseren Code ein. 

Die Codierung läuft nach HTML 

Jetzt builden wir unser Image

> docker build -t LB2-webserver .

> docker images

Nun lassen wir das image laufen mit Docker run. 

> docker run --name LB2-webserver -d --hostname LB2-webserver -p 8080:80 LB2-webserver

Jetzt kann über die IP und den Port auf die Webseite zugegriffen werden. 

  ![grafik](https://user-images.githubusercontent.com/89446428/178357882-db21da7f-7fa2-4db4-a252-096d23e83761.png)
  
  Man könnte Hier auch eine ganze Website kopieren z.B. 20min, jedoch haben wir uns wegen Zeitmangel für einen eifnachen Text entschieden. 
  
  ![grafik](https://user-images.githubusercontent.com/89446428/178358092-c6ca9fe8-879e-4bd2-b6ee-b8ea4d94cf8a.png)


