FROM brunohenrique/java

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

RUN apt-get update && apt-get install -y wget

WORKDIR /opt

ENV SPARK_VERSION 1.4.1
ENV HADOOP_VERSION 2.6

RUN wget http://d3kbcqa49mib13.cloudfront.net/spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz

RUN tar xvf spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz
