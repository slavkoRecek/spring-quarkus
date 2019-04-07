**This project demonstrates the power of spring and quarkus combined**

It is a simple spring-boot application that with a connection 
to postges database. It is prepared to run on GRALVM 
using querkus.
The boot time of the packaged application is < 0.002s.

How to use is.
To run it in dev mode run `./mvnw compile quarkus:dev`.

To package native executables run `docker run --rm --name builder -v <path to working dir>:/build diegocsilva/quarkus_builder mvn package -Pnative -Dnative-image.docker-build=false`
To package the executable into an image run `docker build -t spring-quarkus .`
To run the container use `docker run -i --rm -p 8080:8080 spring-quarkus`

Test it by sending: curl http://localhost:8080/hello  