FROM brunohenrique/java

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

ENV SPARK_VERSION 1.6.0
ENV HADOOP_VERSION 2.6

RUN apt-get update && apt-get install -y python

WORKDIR /usr/local/

RUN wget http://d3kbcqa49mib13.cloudfront.net/spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz
RUN tar xvf spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION.tgz

RUN ln -s spark-$SPARK_VERSION-bin-hadoop$HADOOP_VERSION spark

ENV SPARK_HOME /usr/local/spark
ENV PATH $PATH:$SPARK_HOME/bin

WORKDIR $HOME
