FROM java:8-jre
WORKDIR usr/src
ENV MONGO_DATABASE=UserServiceDB
ENV MONGO_URL=mongodb://mongocontainer:27018/UserServiceDB
ADD ./target/docker-user-service.jar /usr/src/docker-user-service.jar
EXPOSE 8080
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongocontainer:27017/UserServiceDB","-jar","/usr/src/docker-user-service.jar"]