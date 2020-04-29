spring-boot-kafka-test

    spring boot application with kafka integration

Start Zookeeper:

    zookeeper-server-start.bat ..\..\config\zookeeper.properties

Start Kafka Server:

    kafka-server-start.bat ..\..\config\server.properties

Create Topic:

    kafka-topics.bat --create --topic myTopic -zookeeper localhost:2181 --replication-factor 1 --partitions 1

Produce Endpoint:

    http://localhost:8080/kafka/produce?message=Test1

Consumer Endpoint:

    http://localhost:8080/kafka/messages
        - list out messages consumed so far.
