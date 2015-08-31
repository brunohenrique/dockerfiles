FROM ubuntu:14.04

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

RUN apt-get update && apt-get install -y wget software-properties-common

RUN apt-add-repository ppa:webupd8team/java
RUN apt-get update && apt-get upgrade -y
RUN echo debconf shared/accepted-oracle-license-v1-1 select true | sudo debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | sudo debconf-set-selections
RUN apt-get install -y oracle-java7-installer

WORKDIR /opt

ENV SPARK_VERSION 1.4.1
ENV HADOOP_VERSION 2.6

RUN wget http://d3kbcqa49mib13.cloudfront.net/spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz

RUN tar xvf spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz
