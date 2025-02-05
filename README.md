1.Download latest apache kafka from https://kafka.apache.org/quickstart

2.unzip the folder and store in any drive .

3.follow the below commnads. 

----------------------->Commands for running apache kafka on local machine<-----------------------

bin\windows\zookeeper-server-start.bat config\zookeeper.properties                                                       ------>to start zookeeper

bin\windows\kafka-server-start.bat config\server.properties                                                              ------>to start kafka server

bin\windows\kafka-topics.bat--to check kafka topics                                                                       ------>to check topics

bin\windows\kafka-topics.bat --create --topic user-topic --bootstrap-server localhost:9092                                ------>to create topics

bin\windows\kafka-console-producer.bat --topic user-topic --bootstrap-server localhost:9092                                ------>to create producer

>hi
>This is producer       ----->inputs given from cmd   
  
bin\windows\kafka-console-consumer.bat --topic user-topic --from-beginning --bootstrap-server localhost:9092     ---->    to create consumer
hi                     ------->expected output from cmd 
this is producer


4.Use postman request  as   "http://localhost:8080/location/update"

5.after end user project completed run below command in new cmd prompt to view response from postmen request  

bin\windows\kafka-console-consumer.bat --topic location-update-topic --from-beginning --bootstrap-server localhost:9092  
