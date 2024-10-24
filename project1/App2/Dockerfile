FROM ubuntu:latest 
LABEL Name="app2image"
RUN apt update -y && apt install -y apache2 wget unzip 
RUN mkdir -p /tmp/app2
RUN wget https://templatemo.com/download/templatemo_590_topic_listing -O /tmp/app2/file.zip
RUN unzip file.zip && cp templatemo_590_topic_listing/ /var/www/html/
WORKDIR /tmp/app2
EXPOSE 80
CMD ["apachectl" ,"-D" ,"FOREGROUND" ]
