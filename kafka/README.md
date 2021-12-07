#### Zookeeper start
bin/zookeeper-server-start.sh config/zookeeper.properties

#### Start
 bin/kafka-server-start.sh config/server.properties

#### Create Topic
bin/kafka-topics.sh --create --topic \<topic_name\> --bootstrap-server localhost:9092 --partitions \<count\> --replication-factor \<count\>