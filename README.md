# FizzBuzz

для добавления в топик чисел я использовал вот эти команды 


1. Создание топика numbers:
    ```bash
    docker exec -it kafka /opt/kafka/bin/kafka-topics.sh --create --topic numbers --partitions 1 --replication-factor 1 --bootstrap-server kafka:9093
    ```

2. Добавление чисел в топик:
    ```bash
    seq 1000000 | docker exec -i kafka /opt/kafka/bin/kafka-console-producer.sh --topic numbers --broker-list kafka:9093
    ```


Для масштабирования приложения можно использовать Kafka Streams или Apache Flink,
но это требует дополнительной конфигурации и архитектурных решений.
Подходящий выбор зависит от вашего контекста и требований.
