#base image
FROM alpine:latest
#image labels
LABEL org.opencontainers.image.authors="jberkowitz89@gmail.com"
LABEL org.opencontainers.image.source=https://github.com/jduncan-rva/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
LABEL org.opencontainers.image.server_type="edge_server"
# Updating apk - apk is the alpine package keeper (package manager)
RUN apk update
# adding the nginx package to our container. nginx is an open source web serving software.
RUN apk add nginx
#copying our config and web content file to the container
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
#exposing port 80 for listening
EXPOSE 80
#CMD command - still a little unclear here
CMD ["nginx", "-g", "daemon off;"]
