FROM ubuntu:20.04

RUN apt-get update && apt-get install -y nginx 

COPY ./web /var/www/html/

CMD ["nginx", "-g", "daemon off;"]

