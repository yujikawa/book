FROM centos
RUN yum -y --enablerepo=extras install epel-release
RUN yum install -y wget git git-core java-1.8.0-openjdk epel-release python3-pip gcc python3-devel libevent-devel which
RUN wget http://ftp.jaist.ac.jp/pub/apache/spark/spark-2.4.4/spark-2.4.4-bin-hadoop2.7.tgz && \
 tar xvzf spark-2.4.4-bin-hadoop2.7.tgz && \
 rm spark-2.4.4-bin-hadoop2.7.tgz && \
 mv spark-2.4.4-bin-hadoop2.7 /usr/local && \
 ln -s /usr/local/spark-2.4.4-bin-hadoop2.7/ /usr/local/spark
ENV SPARK_HOME /usr/local/spark
ENV PATH ${SPARK_HOME}/bin:${PATH}
ENV PYSPARK_PYTHON=/usr/bin/python3
ENV PYSPARK_DRIVER_PYTHON=python3