# kafka
Kafka deployment based on strimzi-kafka-operator


Example Commands:
```
helm install --set kafka.kafka.storage.volumes.size=10Mi --set kafka.zookeeper.storage.size=10Mi kafka helm -n kafka
```
```
helm upgrade --set kafka.kafka.storage.volumes.size=10Mi --set kafka.zookeeper.storage.size=10Mi kafka helm -n kafka
```
```
helm uninstall kafka helm -n kafka
```
