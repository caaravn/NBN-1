# NBN-1
Doubts 
fc


Microservices enablement KT sessions

we are managing tnd spaces micro services and 60+  microservices we are using in EKS clusters

we have jenkins 68 use for build activities and deployment 
and jenkins 12 use for autoTDmatations related to infrastructure like health checks, patching of servers

we have two different kafka 1. TND kafka and 2. jigsaw kafka
Kafka is used for messaging purposes 


7 environments running in non prod
(system test)
(system integration testing)

Sit1
sit3
st2
st
psvt
rsvt
dev4


Automated scheduled pipelines



Task 1
Heppening in Jenkins 68:
As this is the lower env non prod goes down at 11pm AST and comes up 8am AST
1-> 6am scales up the EKS cluster worker nodes(14) pipeline
2-> one pipeline to bring up the X- Stack enabler of kafka cluster  -> 6:30 am kafka will start
3-> Scaleup of pods of micrservices to get the replicate count 1  -> 7:00 am scale up the pods
4-> 7:15 internal health check
5-> 8:00 external health check report


Task 2 jenkins 68
Provisioners debugging
