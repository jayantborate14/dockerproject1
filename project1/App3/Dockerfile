FROM ubuntu:latest 
LABEL Name="app3image"
RUN apt update -y && apt install -y apache2 wget unzip 
RUN mkdir -p /tmp/app3
RUN wget https://templatemo.com/download/templatemo_589_lugx_gaming -O /tmp/app3/file.zip
RUN unzip file.zip && cp templatemo_589_lugx_gaming/ /var/www/html/
WORKDIR /tmp/app3
EXPOSE 80
CMD ["apachectl" ,"-D" ,"FOREGROUND" ]
