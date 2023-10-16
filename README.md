# FizzBuzz

для добавления в топик чисел я использовал вот эти команды 

docker exec -it kafka /opt/kafka/bin/kafka-topics.sh --create --topic numbers --partitions 1 --replication-factor 1 --bootstrap-server kafka:9093
seq 1000000 | docker exec -i kafka /opt/kafka/bin/kafka-console-producer.sh --topic numbers --broker-list kafka:9093
