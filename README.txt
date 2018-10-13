Sat 10/13/2018 03:16 PM

This repository contains the code for a simple Spring Cloud Config
server.

The server exposes standard end points at port 8888.

The configuration data is housed in a git backend and the uri is
specified in the src\main\resources\application.yml.

There are three environment configuration files -
appointmentservice.yml appointmentservice-dev.yml and
appointmentservice-prod.yml. The files have to be named with the
application name and the searchPath name specifies sub folder in the
repository.

Hitting the end point http://localhost:8888/appointmentservice/default
shows the properties from the appointmentservice.yml

http://localhost:8888/appointmentservice/dev gets the properties from
appointmentservice-dev.yml
http://localhost:8888/appointmentservice/prod gets the properties from
appointmentservice-prod.yml

The desired environment is specified in the application.yml of the
client application as the spring.profiles.active value.


To run this:

Clone the repository or download a zip archive to your local environment and then run 

mvn spring-boot:run

Should start up a local microservice at localhost:8888 and you are open for business.
