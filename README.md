## Flume Agent.

Mysql(Source) --> Flume --> Kafka(Sink).

###Configuration:

Download:

- https://mvnrepository.com/artifact/org.keedio.flume.flume-ng-sources/flume-ng-sql-source

- https://mvnrepository.com/artifact/org.apache.flume.flume-ng-sinks/flume-ng-kafka-sink/1.6.0-cdh5.7.0 .(This can vary depends on your kafka version, in my case I'm using kafka on Cloudera)

- Copy those Jars in ${FLUME_HOME}/lib/ 

- $ flume-ng agent -Xmx512m -f ${USER.HOME}/mysql-agent.conf -Dflume.root.logger=INFO,console -n agent 
