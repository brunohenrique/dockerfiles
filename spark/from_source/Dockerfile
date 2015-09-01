FROM brunohenrique/java

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

RUN apt-get update && apt-get install -y wget

WORKDIR /opt

ENV SPARK_VERSION 1.4.1
ENV HADOOP_VERSION 2.6
ENV MAVEN_VERSION 3.2.5

RUN wget http://d3kbcqa49mib13.cloudfront.net/spark-$SPARK_VERSION.tgz

RUN tar xvf spark-$SPARK_VERSION.tgz

RUN wget http://download.nextag.com/apache/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz
RUN tar -xzf apache-maven-$MAVEN_VERSION-bin.tar.gz
RUN ln -f -s apache-maven-$MAVEN_VERSION maven
ENV M2_HOME=/opt/maven
ENV PATH=${M2_HOME}/bin:${PATH}

WORKDIR /opt/spark-$SPARK_VERSION
ENV MAVEN_OPTS="-Xmx2g -XX:MaxPermSize=512M -XX:ReservedCodeCacheSize=512m"
RUN mvn -Pyarn -Phadoop-$HADOOP_VERSION -Dhadoop.version=$HADOOP_VERSION.0 -DskipTests clean package
