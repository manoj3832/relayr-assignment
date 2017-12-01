# relayr-assignment
prerequisite : Latest docker and docker-compose

when we are talking about service discovery , I am using docker swarm(as service discovery tool) and assuming you have enabled docker-swarm on your host.
reference command : 
> $ docker swarm init 

As per Expectations mentioend , you would like to run "docker-compose up" command and want to see results on localhost(127.0.0.1). if yes , then it is not required to enable swarm here , Only docker-compose depends_on feature can work to discover services on same host in same network. 

You  can also run same docker-compose.yml file to start container in swarm (works as service discovery tool here) by using :
  > $ docker stack deploy -c docker-compose.yml <your stack name>
   
Note : again if  you are runnning in swarm stack , cureenty i am assuming that you are running all container on Manager(Leader) , you can change node constraint in same docker-compose if you want to run on workers or other managers.

## service and db discovery : 
to make double check , you can change "Hello world" text to new text in DB and just refresh browser. postgrsql query to update text is :
> update MESSAGE set MESSAGE_TEXT = 'ENTER NEW TEXT HERE';


IF you required application backend code as well then please confirm i can upload the same. i hope jar and config file should be suffiucent.

## Service bootstram time is 10 sec , please browse http://127.0.0.1:8080 after bootstrap time(10 sec).
