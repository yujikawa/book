FROM centos
RUN yum -y --enablerepo=extras install epel-release
RUN yum install -y wget git git-core java-1.8.0-openjdk epel-release python3-pip gcc python3-devel libevent-devel which vim
RUN wget -O /tmp/kafka_2.12-2.4.0.tgz http://ftp.jaist.ac.jp/pub/apache/kafka/2.4.0/kafka_2.12-2.4.0.tgz && \
  tar -xzf /tmp/kafka_2.12-2.4.0.tgz -C /opt && mv /opt/kafka_2.12-2.4.0 /opt/kafka
COPY start.sh /opt/start.sh
# nohup /opt/kafka/bin/zookeeper-server-start.sh /opt/kafka/config/zookeeper.properties &
# nohup /opt/kafka/bin/kafka-server-start.sh /opt/kafka/config/server.properties &
# /opt/kafka/bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic sample-topic
# /opt/kafka/bin/kafka-topics.sh --list --zookeeper localhost:2181 sample-topic
# /opt/kafka/bin/kafka-topics.sh --describe --zookeeper localhost:2181 --topic sample-topic
# /opt/kafka/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic sample-topic
# /opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:2181 --topic sample-topic --from-beginning