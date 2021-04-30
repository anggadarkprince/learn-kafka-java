## Learn Kafka with Java

### Start Zookeeper
`bin/zookeeper-server-start.sh config/zookeeper.properties`

### Start Kafka
`bin/kafka-server-start.sh config/server.properties`

### Create Topic
`bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092`

`bin/windows/kafka-topics.bat --create --topic learn-kafka-event --bootstrap-server localhost:9092 --replication-facto
r 1 --partitions 3`

### Describe Topic
`bin/kafka-topics.sh --describe --topic quickstart-events --bootstrap-server localhost:9092`

### Write Event (Publisher)
`bin/kafka-console-producer.sh --topic quickstart-events --bootstrap-server localhost:9092`

### Read Event (Consumer)
`bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092`