Steps to run kafka Locally:

Step1(Generating Random UUID): .\bin\windows\kafka-storage.bat random-uuid

Step2: .\bin\windows\kafka-storage.bat format -t randomuuid -c C:\kafka_2.13-4.0.0\config\server.properties

Server Starting: .\bin\windows\kafka-server-start.bat .\config\server.properties
 
Topic Creation: .\bin\windows\kafka-topics.bat --create --topic test1 --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1

Producer: .\bin\windows\kafka-console-producer.bat --bootstrap-server localhost:9092 --topic test 
Consumer: .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning

Second step: .\bin\windows\kafka-storage.bat format -t usX6ZWLnSt-afLfkkJy92Q -c .\config\server.properties --standalone
