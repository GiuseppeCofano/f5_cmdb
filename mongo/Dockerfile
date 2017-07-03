FROM centos
MAINTAINER g.cofano87@gmail.com

COPY mongodb.repo /etc/yum.repos.d/mongodb.repo
RUN yum -y install mongodb-org && \
	mkdir -p /data/db

WORKDIR /home/mongo

EXPOSE 27017

ENTRYPOINT ["/usr/bin/mongod"]
