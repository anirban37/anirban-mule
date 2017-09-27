[![](https://images.microbadger.com/badges/image/anir37/anirban-mule.svg)](https://microbadger.com/images/anir37/anirban-mule "Get your own image badge on microbadger.com")   [![](https://images.microbadger.com/badges/version/anir37/anirban-mule.svg)](https://microbadger.com/images/anir37/anirban-mule "Get your own version badge on microbadger.com")
# anirban-mule
It contains the configuration to run Mule runtime and Mule application on Docker container

![94a0a117494a8e9f1332f1b6e54f61d8](https://user-images.githubusercontent.com/1582548/30781889-3b15342e-a145-11e7-99a6-f574388789e4.jpeg)

### Steps to use the service ###

* Pull the image using docker [`docker pull anir37/anirban-mule`](https://hub.docker.com/r/anir37/anirban-mule/) 
* Once the image is pulled successfully use docker `docker run -p 9082:9082 -t -i anirban-mule`.
* The sample application `TestApplication.zip` will be added and deployed to the Mule runtime which runs on http port `9082`.
* To access and test the deployed test application, use the url :- `http://<your ip>:9082/testApplication`
* Please note the here `<your ip>` is the `docker-machine` ip if you are running docker in Windows; if running on Unix, where docker is intalled locally, you can use `http://localhost:9082/testApplication` or the ip address of the system.
* You can also use the command `docker ps` command to get the container id and then use  `docker inspect <container id> | grep IPAddress` to get the ip address to test the sample application.

:smiley: Thats it! You are ready with your **Mule EE runtime** in Docker container :+1:
* Not that: If you have an enterprise licence key, you can put **your own licence key** in the Licence folder and uncomment the Dockerfile code that will install your licence file with the mule runtime (go through the detailed [instruction](https://github.com/anirban37/anirban-mule/blob/master/Licence/Read%20Me.txt)).

If you **don't have a licence key**, then leave it as it is, the runtime will be created with **Trial licence for 30 days**.
