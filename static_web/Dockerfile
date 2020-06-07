# Version: 0.0.1
FROM ubuntu:18.04

LABEL maintainer="john@johnmaguiredeveloper.com"
LABEL version="1.0"
LABEL location="New York" type="Data Center" role="Web Server"


ENV REFRESHED_AT 2020-23-05

RUN apt-get update; apt-get install -y nginx
RUN echo 'Hi, I am in your container' \
      >/var/www/html/index.html

ENTRYPOINT ["/usr/sbin/nginx"]

CMD ["-h"]

HEALTHCHECK --interval=10s --timeout=1m --retries=5 CMD curl http://localhost || exit 1
EXPOSE 80
