# kafka
Kafka deployment based on strimzi-kafka-operator


Example Command:

helm install --set kafka.kafka.storage.volumes.size=10Mi --set kafka.zookeeper.storage.size=10Mi kafka . -n kafka


 helm upgrade --set kafka.kafka.storage.volumes.size=10Mi --set kafka.zookeeper.storage.size=10Mi kafka . -n kafka


helm uninstall kafka . -n kafka