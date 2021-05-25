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

# Kafdrop

Kafdrop is a web UI for viewing Kafka topics and browsing consumer groups

```
git clone https://github.com/obsidiandynamics/kafdrop && cd kafdrop
```

```
helm install --set kafka.brokerConnect=kafka-kafka-0.kafka:9094,kafka-kafka-1.kafka:9094,kafka-kafka-2.kafka:9094 --set image.tag=3.27.0 --set server.servlet.contextPath="/" --set jvm.opts="-Xms128M -Xmx256M" kafdrop chart -n kafka
```

```
helm uninstall kafdrop chart -n kafka
```
