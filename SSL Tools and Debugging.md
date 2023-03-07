- keytool -printcert -file kafka.pem
```
Owner: CN=kafka.cp01.oso.sh
Issuer: CN=cp01.oso.sh Intermediate Authority
Serial number: a53eccf0e870caad2303dc16141e8bb93902fa3

...

#4: ObjectId: 2.5.29.17 Criticality=false
SubjectAlternativeName [
  DNSName: kafka.cp01.oso.sh
  DNSName: kafka1.cp01.oso.sh
]
```
- openssl x509 -in kafka.pem -noout -text
```
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            0a:53:ec:cf:0e:87:0c:aa:d2:30:3d:c1:61:41:e8:bb:93:90:2f:a3
        Signature Algorithm: sha256WithRSAEncryption
        Issuer: CN = cp01.oso.sh Intermediate Authority
        Validity
            Not Before: Nov  4 09:51:06 2022 GMT
            Not After : Dec  4 09:51:36 2022 GMT
        Subject: CN = kafka.cp01.oso.sh
        Subject Public Key Info:
...
    X509v3 Subject Alternative Name: 
        DNS:kafka.cp01.oso.sh, DNS:kafka1.cp01.oso.sh
```


keytool -printcert -file /var/ssl/private/kafka_broker.crt

keytool -printcert -file /var/ssl/private/zookeeper.crt

zookeeper.key

keytool -list -storepass confluentkeystorestorepass -v -keystore /var/ssl/private/kafka_broker.keystore.jks

keytool -list -storepass confluenttruststorepass -v -keystore /var/ssl/private/kafka_broker.truststore.jks


keytool -list -storepass  confluentkeystorestorepass -v -keystore /var/ssl/private/zookeeper.keystore.jks