FROM ubuntu:latest 
LABEL Name="app1image"
RUN apt update -y && apt install -y apache2 wget unzip 
RUN mkdir -p /tmp/app1
RUN wget https://templatemo.com/download/templatemo_591_villa_agency -O /tmp/app1/file.zip
RUN unzip file.zip && cp templatemo_591_villa_agency/ /var/www/html/
WORKDIR /tmp/app1
EXPOSE 80
CMD ["apachectl" ,"-D" ,"FOREGROUND" ]
