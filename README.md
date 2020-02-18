# person-api

steps i did to build app on my locam machine:

JARFILE=person-0.0.1-SNAPSHOT.jar

clone git repo

./mvnw compile

./mvnw package

./mvnw clean install -P dockerBuild,dockerRelease

sudo docker build . --build-arg JARFILE=person-0.0.1-SNAPSHOT.jar

sudo docker run $image made from above cmd
