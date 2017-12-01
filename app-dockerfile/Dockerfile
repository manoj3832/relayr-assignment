## Using Official JAVA8 base image which is apline based.

## we have created my assignment .jar file from my assignment code and a config.yml for this 
## assignment service. 

# This DOckerfile will use my assignment service jar and config.yml file to build Hello Word ! Service as docker.


FROM java:8-alpine

# Copying jar file to docker path in assignment_service.jar

ADD assignment_service.jar /usr/local/assignment_service.jar 

# Copying config.yml file to docker path in assignment_config.yml

ADD assignment_config.yml /usr/local/assignment_config.yml

# Copying service startup script to docker entrypoint

ADD assignment_start.sh /usr/local/assignment_start.sh

# Defining Working Directory when docker will be start
WORKDIR /usr/local

ENTRYPOINT ["sh","assignment_start.sh"]
CMD ["server", "config.yml"]

