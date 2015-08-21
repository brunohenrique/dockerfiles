FROM ubuntu:14.04

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.0.list

RUN rm -rf /var/lib/apt/lists/*
RUN apt-get update && apt-get install -y mongodb-org

RUN mkdir -p /data/db

EXPOSE 27017

ENTRYPOINT ["/usr/bin/mongod"]
