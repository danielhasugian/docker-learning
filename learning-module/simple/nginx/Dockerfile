FROM ubuntu
RUN apt-get -y update && apt-get -y install nginx
COPY index.html /var/www/html
EXPOSE 80
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
