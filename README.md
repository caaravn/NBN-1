Tool's
GIT HUB
JENKINS
EKS

EC2
MONGO DB
KAFKA AND ZOOKEEPER



CSA----->Customer service assurance 
In our micro service we do not have any UI we are purely backend service and are writen in java version 11

Applications we work on1. Microservices
2. TND( test and diagones)
3. Flexicache
4. TYK (It is a api gateway)
5. 


Microservices enablement KT sessions

We are managing tnd spaces micro services and 80+  microservices we are using in EKS clusters

jenkins 68 use for build activities and deployment (micro service)
jenkins 12 use for automatations related to infrastructure like health checks, patching of servers (for tyk)


We have two different kafka clusters (To communicate between microservices we are using kafka)
1. TND kafka 
2. Jigsaw kafka (remedy kafka)

   

Zookeeper ----> Inside zookeeper server kafka brokers are running


2 environments running in PROD
PROD
PSUP  
   

We maintain 7 environments running in NON PROD 
(System test)
(System integration testing)

MR team will work on this four envts and should be up and running before 8am
Sit1
Sit3
Rsvt
Psvt
St2


Lower env Developers(operations) will work on this two Env and testing happens. 
St
Dev4


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
Note:-- Patching refers to the process of updating software and systems to fix  vulnerabilities, improve functionality and ensure stability. This
        practice is critical for maintaing the security and reliability of applications and infrastructure. 


Tools:
ORGE---> FOR AWS cost cutting
Plutora---> we need to raise ECR'S using plutora, when we do somthing on enviromnents like RSVT, SIT1 AND SIT3 which are managed by MR teams that time we need to raise ECR'S 


# NBN-1
Doubts 
fc
ASM team


