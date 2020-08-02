FROM ubuntu

RUN apt-get update && apt-get install wget -y \
	&& apt-get install software-properties-common -y \
	&& apt-get install openjdk-8-jdk -y \
	&& apt-get install -y curl \
	&& apt-get install -y net-tools \
	&& apt-get install -y nginx \
	&& apt-get install screen -y 

RUN adduser admin
RUN adduser nginx

RUN usermod -aG sudo admin

RUN echo "nginx ALL=(ALL) NOPASSWD: /usr/sbin/service nginx start|restart|stop" >> /etc/sudoers


#RUN rm /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/conf.d/ 

CMD ["nginx", "-g", "daemon off;"]
#RUN curl 0.0.0.0:8080
