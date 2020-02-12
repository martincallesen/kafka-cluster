# Description
Projects is enable you to start up a kafka cluster via ansible scripts. There is provided a vagrant enviroment that will
have docker-compose available and docker-compose file from confluent will be used to boot up the kafka cluster.

# Requirements
You must have virtualbox and vagrant installed at your machine. 
Then the machine must at least have 16 gb memory available.

# How to use project
In the root of the project issue command: 
* vagrant up

Then you will be able to access the control center in the kafka cluster on localhost:9021
* Open a browser and navigate to http://localhost:9021/clusters

If virtualbox for some reason has been stopped the kafka cluster needs to be booted up againg. So issue command:
* vagrant provision

