# NBN-1
Doubts 
fc
ASM team


Microservices enablement KT sessions

we are managing tnd spaces micro services and 60+  microservices we are using in EKS clusters

jenkins 68 use for build activities and deployment 
jenkins 12 use for autoTDmatations related to infrastructure like health checks, patching of servers

we have two different kafka
1. TND kafka and
2. jigsaw kafka (remedy kafka)
   

7 environments running in NON PROD 
(system test)
(system integration testing)
Sit1
sit3
rsvt
st2
st
psvt
dev4

All the above environment has x-stack enabler. This x stack enabler job is starting up the entire cluster daily triggers and start up the env like it will start up the zookeeper 
instances and auto scaling group.



jenkis 68

Task 1
Heppening in Jenkins 68:
As this is the lower env non prod goes down at 11pm AST and comes up 8am AST
1-> 6:00am AST scales up the EKS cluster worker nodes(15) pipeline
2-> 6:30am AST kafka will start -->one pipeline to bring up the X- Stack enabler of kafka cluster  
3-> 7:00am AST scale up the pods of microservices to get the replicate count 1
4-> 7:15am AST internal health check
5-> 8:00am AST external health check report

Task 2 jenkins 68
Provisioners debugging

task 3
Health checks

task 4 
changing github token in jenkins



jenkins 12 ( patching work)

CSA MS ec2 patching ( pipeline update ami pipeline)



Tools:
ORGE---> FOR AWS cost cutting
Plutora---> we need to raise ECR'S using plutora, when we do somthing on enviromnents like RSVT, SIT1 AND SIT3 which are managed by MR teams that time we need to raise ECR'S 





