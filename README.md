## Installation of KAFKA

Download kafka [here](https://kafka.apache.org/quickstart) and unzip using the file into your computer.

### Starting the Zookeeper service:

Run the below command in a powershell window to start the service. This action must be performed from the kafka folder. Keep the window open.

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties```

### Starting the Kafka service

Run the below command in a powershell window to start the service. This action must be performed from the kafka folder. Keep the window open.

```.\bin\windows\kafka-server-start.bat .\config\server.properties```

### Create topics:

The below command lets us to create topics for kafka. This action must be performed from the kafka folder.

```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic topic-name```

To list the available topics run the command below from the kafka folder:

```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```

### Run the producer:

Use the command below to run the kafka producer for a particular topic.

```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic topic-name```

This will return a '>' symbol on success which means the producer is ready.

### Run the Consumer:

Use the command below to run the kafka consumer for a particular topic.

```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic topic-name --from-beginning```

This command returns the messages the producer has produced from beginning.


