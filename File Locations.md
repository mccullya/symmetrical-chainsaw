

### Service Files
Fedora:
###### Base service Files
* /usr/lib/systemd/system/confluent-control-center.service  
* /usr/lib/systemd/system/confluent-kafka-connect.service 
* /usr/lib/systemd/system/confluent-kafka-rest.service  
* /usr/lib/systemd/system/confluent-ksqldb.service  
* /usr/lib/systemd/system/confluent-schema-registry.service  
* /usr/lib/systemd/system/confluent-server.service  
* /usr/lib/systemd/system/confluent-zookeeper.service  
###### Override services Files
* /etc/systemd/system/confluent-control-center.service.d/override.conf
* /etc/systemd/system/confluent-kafka-connect.service.d/override.conf
* /etc/systemd/system/confluent-kafka-rest.service.d/override.conf
* /etc/systemd/system/confluent-ksqldb.service.d/override.conf
* /etc/systemd/system/confluent-schema-registry.service.d/override.conf
* /etc/systemd/system/confluent-server.service.d/override.conf
* /etc/systemd/system/confluent-zookeeper.service.d/override.conf

Self-Signed Certificates
in `/var/ssl/private`:
```
kafka_broker.chain  
kafka_broker.crt  
kafka_broker.key  
kafka_broker.keystore.jks  
kafka_broker.truststore.jks
```



confluenttruststorepass

Config Files:
```
/opt/confluent/etc/kafka/client.properties  
/opt/confluent/etc/kafka/connect-distributed.properties  
/opt/confluent/etc/kafka/server.properties  
/opt/confluent/etc/kafka/zookeeper.properties  
/opt/confluent/etc/kafka/zookeeper-tls-client.properties
/opt/confluent/etc/confluent-control-center/control-center-production.properties
/opt/confluent/etc/kafka-rest/kafka-rest.properties4
/opt/confluent/etc/ksqldb/ksql-server.properties
/opt/confluent/etc/schema-registry/schema-registry.properties
```


Log Dir:
/var/log/kafka


Log4j Config:
/opt/confluent/confluent-7.2.2/etc/kafka/log4j.properties


systemctl restart confluent-control-center.service  
systemctl restart confluent-kafka-connect.service 
systemctl restart confluent-kafka-rest.service  
systemctl restart confluent-ksqldb.service  
systemctl restart confluent-schema-registry.service  
systemctl restart confluent-server.service  
systemctl restart confluent-zookeeper.service  