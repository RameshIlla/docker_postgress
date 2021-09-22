## Docker Postgress
Setup Postgres DB on a docker contaner and run the .sql file provided during startup
# How to start
Install Docker  

Either clone the repo of download as zip 
<pre>
In a terminal window, navigate to the folder where this repo is downloaded and run the below command to build the docker image  
	
	docker build -t postgres_image -f ./Dockerfile .  # Make sure the dot is included  

Now run the below command to run create the container and run the startup command provided in the Dockerfile
	
	docker run -d --name postgres_container -p 5432:5432 postgres_image

In case you want to remove images you can run this command:
    docker stop postgres_container #First stop the container
    docker  rm postgres_container #Then Remove the container
    docker image rm 'postgres_image' #Finally delete the image
</pre>