from bryandollery/maven-repo as build

run git clone https://github.com/Rawan005/level2-project.git&& \
    cd /root/level2-project/person-service  && \
    mvn clean package -DskipTests

from adoptopenjdk/openjdk11:alpine

copy --from=build /root/level2-project/person-service/target/person-service-1.0.0.jar /

cmd ["java", "-jar", "person-service-1.0.0.jar"]

