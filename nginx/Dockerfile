FROM ubuntu:16.04

MAINTAINER Yogi

RUN apt-get update && apt-get install -y nginx \
	&& apt-get clean \
	&& rm -rf /tmp/* /var/tmp/* /var/lib/apt/lists/*  \
	&& echo "daemon off;" >> /etc/nginx/nginx.conf

ADD default /etc/nginx/sites-available/default

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    &&  ln -sf /dev/stderr /var/log/nginx/error.log

CMD ["nginx"]
